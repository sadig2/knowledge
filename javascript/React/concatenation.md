## to concatenate arguments in React  use backtick 

    var person = {name:"sadig", surname:"naibb"};

    var result = `Hello ${person.name} ${person.surname}`;

### ES6 class
        class Person {
    constructor(firstName, lastName) {
    
        this.firstName = firstName;
        this.lastName = lastName;
            }
            }


## React inheritance 

                class Employee extends Person {
        constructor(firstName, lastName, title, salary) {
        super(firstName, lastName);
        this.title= title;
        this.salary = salary;
        }
        }
