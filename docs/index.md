# JS & React

## JavaScript

#### What is lexical scoping?

- Lexical scope is the ability for a functions scope to access variable from the parent scope
- Inner function has a access of variables of its outer function

#### What is the primitive data type?

- The predefined data types provided by JS
- The Primitive Data types in JavaScript include Number, String, Boolean, Undefined, Null and Symbol

#### What are Non-primitive data types?

- Objects and Array

#### What is hoisting?

- It is default behavior of JS where all the variable and function declarations are moved on top
- Var variables are hoisted with a default value of undefined, which it accessible before declarations
- Let,const variables are hoisted without a default initialization
- Variable initializations are not hoisted, only variable declarations are hoisted

#### What is the difference between var,let and const?

- _Var_ has function scope and _let_, _const_ has block scope
- _Var_ variables can be updated and re-declared within its scope
  - _Let_ variable can be updated but not re-declared
  - _Const_ variables can neither be updated or re-declared

#### What is implicit type Coercion?

- Implicit type coercion in js is the automatic conversion of value from one data type to another
- it happens when the operator is used on different data type
  - _String coercion_: it is when + operator used, it always convert number type into string type
    - it is when - operator used, it always convert string type into number type
  - _Boolean coercion_: it is when using logical,ternary operators,if statement and loop checks
  - _Logical coercion_: They always return one of the operands
  - _Equality coercion_: it is when using using `===` operator

#### Is JS a statically typed or a dynamically typed language?

- Js is dynamically typed language
- In a dynamically type language, the type of the variable is check during run-time
- in statically type language, the type of variable is checked during compile-time

#### What is currying?

- It is a process that allows you to transform a function with multiple arguments into a sequence of nesting function
- It is an advanced technique to transform a function of arguments n, to n function of one or fewer arguments
  ```js title="curry.js"
  const add = (a) => {
    return function (b) {
      return a + b;
    };
  };
  add(3)(4);
  ```

#### What are Closures?

- It is an ability of a functions to remember the variable and function that are declared in its outer scope

#### Where we need to use closure function?

- In event handlers, callback functions and more...

#### What are object prototypes?

- All JS objects inherit properties from prototype like date from Date, Array object from Array prototype

#### What is recursion?

- It is a technique to iterate over an operation by having a function call itself repeatedly unit it arrives at a result

#### What is the rest parameter and spread operator?

- _Rest parameter_: is used to take a n number of arguments and turns them into array
- _Spread operator_: takes an array or an object and spreads it

#### What are promises?

- Promises are used to handle asynchronous operations in JS
- Promise object has four states-
  - _Pending_: initial state
  - _Fulfilled_: async operation is completed
  - _Rejected_: async operation is failed
  - _Settled_: the promise has been either rejected or fulfilled
- Promise constructor which takes in a callback function with two parameter resolve and reject

#### What are generator functions?

- There are a special class of functions, introduced in the ES6 version
- Generator function are declared with `function*` keyword instead of normal function
- In Generate function, when called, they do not execute the code instead, they return a generator object
  - that generator object handles the execution
  - the object consists of method called next()
  - next() method executes the code until the nearest `yield` statement
  - next() method returns the `yield` value : {value: 'some-value', done: true}
  - `value` property represents the yielded value and `done` tells, if function code is finished or not

#### What is Object Destructuring?

- It is a new way to extract elements from an object of an array

```js
const obj = { id: 1, name: "yo" };
const { userId: id, userName: name } = obj;
const { id, name } = obj; // if we want same name as the property
```

#### What is event binding and event apply?

- _Event binding_ refers to telling the browser that a particular
  function should be called whenever some 'event' occurs
- _Event apply_ used to call a function in a different object with the given _this_ value,
  and the arguments are passed in the form of an array

#### What is call() function?

- With the _call()_ method, we can write a method that can be used on different object

```js
const person = {
  fullName: function () {
    return this.firstName + " " + this.lastName;
  },
};
const person1 = {
  firstName: "John",
  lastName: "Doe",
};

// This will return "John Doe":
person.fullName.call(person1);
```

#### What is event-bubbeling?

- It is a method of `event propagation` in the HTML DOM API
- When event is in element inside another element, and both elements have registered to handle to that event
- It is process that starts with the element that triggered the event
  and then bubbles up to containing elements in hierarchy

#### What are synthetic events?

- Thery are cross-browser around the browser's native events like stopPropagation() and preventDefault()

#### How reduce() work in JS?

- Reduce an array to a single value
- Does not change the original array

## React

#### What is constructor in react?

- It is a method used to initialize an object's state in class
- _Constructor_ in a react component is called before the component is mounted

#### What is Super in react?

- _Super():_ it is used to call the constructor of its parent class

#### What is memo in react?

- React memo is a higher-oder component that wraps around a component to memoize the rendered output
  and avoid unnecessary renderings
- Using memo will cause React to skip rendering a component if its props haven't changed

#### What are the lifecycle methods of React?

- After react v 16.3+
- `getDrivedStateFromProps`: invoked before render() and is invoked on every render
- `componentDidMount`: executed after first rendering
- `shoudComponentUpdate`: determines if the component will be update or not, by default it returns true
- `getSnapshotBeforeUpdate`: executed right before rendered output is committed to DOM
- `componentDidUpdate`: mostly it used to update the DOM in response to prop or state changes
- `componentWillUnmount`: it will be used to cancel any outgoing process

#### What is render props?

- Instead of implementing its own render logic, a child component calls render props as functions.

#### What is action synctax in redux?

- Actions are plain JS object that must have a type attribute
  to indicate the type of action performed
  - {type: GET_DATA, payload: {}}

#### How arrow function bind `this`?

- Arrow function do not bind their own `this`, instead they inherit from parent scope or lexical scope
- In regular function the this keyword represented the object that called the function
  which could be the window, the document, a button or whatever

#### What is shadow DOM?

- Lets us create custom component
- It creates scoped DOM Tree inside our element

#### Why in clearInterval() didn't works right after setInterval() in useEffect?

- To handle this we can use useEffect's cleanup function
  ```js
  return () => {
    clearInterval(intervalId);
  };
  ```

#### How to pass state in context API?

#### How to connect GraphQL to react?
