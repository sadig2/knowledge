## we have three files react to work : 
1)html, where i have <div id="root">
2)index.js which imports name of the file 'App.js' and calls my class in App.js  <App/>
3) App.js where i put next code:

        import React, {Component} from 'react';
import logo from './logo.svg';
import './App.css';

class App extends React.Component{

  constructor(props){
    super(props);
    this.state={user:"John"};
  }


  componentDidMount(){

    const arr = [1,2,3,4]

    const newarr = arr.map((num, ind) => <li key={ind}> Listen {num} </li> );

  }

  render(){
    const arr = [{brand:"Lenovo",model:"thinkpad"}, {brand:"apple",model:"macbook pro"}];

    const newarr = arr.map((value,index)=>  <tr key={index}><td>{value.brand}</td>
    <td>{value.model}</td></tr>    )

    return (<table>{newarr}</table>);
  }

}

export default App;