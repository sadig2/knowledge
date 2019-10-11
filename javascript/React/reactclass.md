## we have three files react to work : 
1)html, where i have <div id="root">
2)index.js which imports name of the file 'App.js' and calls my class in App.js  <App/>
3) App.js where i put next code:

    import React, {Component} from 'react';
    import logo from './logo.svg';
    import './App.css';

    class CommondHandler extends React.Component{

    constructor(props){
        super(props);
        this.state= {firstname:'', lastname:''}
    }

    onchanged = (event)=>{
        this.setState({[event.target.name]:event.target.value});
    }



    handleSubmit = (event)=>{
        alert(`Hello ${this.state.firstname} ${this.state.lastname}`);
    }

    render(){
        return(

        <form onSubmit={this.handleSubmit}>
            <label>first name</label>
            <input type="text" name="firstname" onChange={this.onchanged}/>
            <label>last name</label>
            <input type="text" name="lastname" onChange={this.onchanged}/>
            <input type="submit" value="submit"/>
        </form>



        )
    }

    }



    class FSubmit extends React.Component{


    constructor(props){
        super(props);
        this.state= {text:''};
    }

    inputChanged= (event)=>{
        this.setState({text:event.target.value})
    }


    handleSubmit = (event)=>{
        alert(`you typed: ${this.state.text}`);
        event.preventDefault();
    }


    render(){
        return(
        <form onSubmit={this.handleSubmit}>
            <input type="text" onChange={this.inputChanged}
            value={this.state.text}/>
            <input type="submit" value="Press me"/>  
        </form>


        )






    }



    }





    class MyForm extends React.Component{

    handleSubmit(event){
        alert('form submit');
        event.preventDefault();
    }

    render(){
        return(
        <form onSubmit={this.handleSubmit}>
            <input type="text" value="Submit"></input>
        </form>
        )
    }

    }



    class App1 extends React.Component{

    buttonPressed = ()=>{
    alert("Button PRessed");
    }

    render(){
    return(
        <div>
        <button onClick={this.buttonPressed}>Press me </button>

        </div>
    )
    }

    }



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

    export default CommondHandler;

