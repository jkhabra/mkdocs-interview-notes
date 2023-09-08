## Failed interview question
#### Write code to print 1-100 where every multiple of 3 should print "FIZZ",
  every multiple of 5 should print "BUZZ" and every multiple of 3 and 5 as "FIZZBUZZ"
  Ex: 1 2 FIZZ 4 BUZZ

### Trantor interview
#### What is REST APIs?
- Representational state transfer is software architecture that impose condition on how API should work
- REST API is way of accessing web service in a simple and flexible way without having nay processing
- REST technology is generally preferred to the more robust Simple Object Access Protocol (SOAP)
  technology because REST uses less bandwidth, simple and flexible making it more suitable for internet usage
- All communication done via REST apis uses only HTTP request
#### What is Patch method?
- It is used to modify capabilities
- PATCH req only needs to contain the changes to resource, not the complete resource
#### How react renders?
#### What is difference between library and framework
#### How to make a custom hooks?
  - event loop, custom hooks

#### What this code do?
const obj = { value: 42 };

function getValue() {
  return this.value;
}

const boundFunction = getValue.bind(obj);
const result = getValue.call(obj);

#### What does this bind mean?
- Function being called to have a different this value than the default one
- bind() function, that always runs with a specific `this` value

#### What is difference null and undefined?
- `Null` means an empty value and is also a primitive type
    - The variable with has assigned as null contains no value
- `Undefined` variable has been declared, but its value has not been assigned
#### How CORS work?
- Cross-Origin Resource Sharing (cors)
  - is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, port)
- When a browser sends a request to a server, it includes an Origin header
  - This header contains the origin of the request, which is the domain, protocol, and port
  - The server can then decide whether to allow or deny the request
  - If the request is allowed, the server includes the Access-Control-Allow-Origin header in the response
  - This header specifies the origin that is allowed to access the resources
#### How react renders?
- After render triggered, `React` calls components to figure out what to display on screen
- The JSX is somehow converted into actual HTML DOM elements displayed on the screen
#### What is difference between library and framework?
- A `framework` can reduce complexity for developer
- A `framework` can abstract away logic, behavior and even architectural patterns
- A `library` can help with complexity, but typically focuses on code reuse


#### what are web APIs with example?
