Fat Arrow Functions:

  (param1, param2, …, paramN) => { statements } 
  (param1, param2, …, paramN) => expression 
    // equivalent to: => { return expression; } - do not use {} only if simple expression

  singleParam => { statements }
  () => { statements } 
    //no parameters

Conditional statements:

  condition ? expr1 : expr2 
    //If condition is true -> return the value of expr1; else -> it return the value of expr2.


Destructuring:
  const { children, selectedMenu } = this.props;
    //Evaluates to:
      const children = this.props.children;
      const selectedMenu = this.props.selectedMenu;
  const { children, selectedMenu, ...restOfProps } = this.props;
    // ...restOfProps - assign the remaining part of props object key/value pair

Declaring class:

  export class ExampleClass extends Component {
    constructor(props) {
      super(props);
      this.state = {date: new Date()};
    }

    render() {
      return (
        <div>
          <h1>Hello, world!</h1>
          <h2>It is {this.state.date.toLocaleTimeString()}.</h2>
        </div>
      );
    }
  }

  //when importing from another file:

  import { ExampleClass } from "../../exampleFolder";

Imports and Exports:
  - Named exports (several per module) - Names must match exactly in exporting and importing files
  - Default exports (one per module in exporting module) - Default exports always go outside of brackets when importing.
