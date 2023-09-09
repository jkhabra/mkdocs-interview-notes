## Node and Express
#### What is REPL?

- It stands for Read, Eval, Print and Loop
  which means evaluating code on to go

#### What is callback hell?

- It is nested callbacks stacks below one another forming a pyramid structure
- Every callback depends/wait for previous callback, there making a pyramid
- that affects the readability and maintainability of the code

#### What is an event loop?

- The event loop executes tasks from the event queue only when the call stack is empty
- Event loop is an endless loop, which waits for tasks, execute them and
  then sleeps unit it receives more tasks
- It allows us to use callback and promises

#### What is an Event Emitter?

- It is a class that holds all the objects that can emit events
- It is used to trigger an event `.on` is used to add a callback function that's going
  to be executed when the event is triggered

```js title="event-emiter.js"
const EventEmitter = require("events");
class MyEmitter extends EventEmitter {}
const myEmitter = new MyEmitter();
myEmitter.on("event", () => {
  console.log("an event occurred!");
});
myEmitter.emit("event");
```

#### What are node.js streams?

- They are instances of EventEmitter which can be used to work with streaming data
- They handling and manipulating streaming large files(videos,mp3,..) over network
- They use buffer as temporary storage

#### What are buffers?

- it is a temporary memory that is used by stream to hold on to some data unit consumed

#### What is middleware?

- It comes in between request and business logic
- Mainly used to capture logs and enable rate limit, routing,authentication,
  whatever not part of business logic
- These are third party middleware also like body-parser and can write custom ones

#### What is a Reactor pattern in Node.js?

- It is a pattern for nonblocking I/O operations
- this is used in any event-driven architecture
- It has two components
  - _Reactor_: Its job is to dispatch I/O event to appropriate handlers
  - _Handler_: Its job is to actually work on those events

#### What is a thread pool?

- The thread pool is handled by the `libuv` library
- Libuv is a multi-platform C library that provides support for asynchronous I/O-based operations
  such as file system, networking and concurrency

#### What does event driven programming mean?

- Event driven programming approach uses events to trigger various functions
  - Event can be anything such as typing a key or clicking button
  - A callback fun is already registered with the element and executes whenever event is triggered

#### What are first-class functions?

- Function is treated as a variable that can be assigned to any other variable or passed as an argument

## MongoDb (mongoose)

#### What is Mongoose?

- Mongoose is a JS object-oriented programming library

#### What is a Document in MongoDB?

- it is an ordered set of keys with associated values
- It is represented by a map, hash or dictionary

#### What is Collection in MongoDB?

- It is a group of documents
- Documents within collection can have different fields
- A collection is the equivalent of a table in relational database system
- A collection exists within single database

#### What are Databases?

- MongoDB groups collection into database
  - It can host several database, each grouping together collection
  - Some reserved database names: admin, local and config

#### What are some features of MongoDB?

- _Indexing_: Indexes are data structure that support the efficient execution of queries
- _Aggregation_: it provides an aggregation framework based on the concept of data processing pipelines
- _Special collection and index types_: it supports time-to-live (TTL) collections for data
  that should expire at a certain time
- _File storage_: it supports an easy-to-use protocol for storing large files and file metadata
- _Sharding_: it is the process of splitting data up across machines

#### How to add data?

- To insert a single document `insertOne` method is used
- For many documents `insertMany` method is used

#### What are the data types?

- the common data types in MongoDB are:
  - Null, Boolean, Number, String, Date, Regular expression, Array,Embedded document,
    Object ID, Binary Data, Code

#### How is Querying done?

- The find method is used to perform queries
- it returns a subset of documents in a collection,
  from no documents at all to the entire collection
- Which documents get returned is determined by the first argument to find

#### What is Indexing?

- Indexes are data structure that support the efficient execution of queries
- They contain copies of parts of the data in document to make queries more efficient
- Without indexes MongoDB has to search every row in database
  table to find the document that match each query

#### What is the SET Modifier?

- If the value of a field doesn't yet exist, `$set` sets the value
- It is useful for updating schemas or adding user-defined keys

#### What do you mean by Transactions?

- It is a logical unit of processing in a database that indicates one or more database operations
  - Which can be read or write operations
- It provides a useful feature to ensure consistency
- Mongo has two APIs to use transaction
  - Core API
  - Call-back API

#### What is a replica set?

- A replica set is group of mongo instances that host the same data set
- Its one node is primary, and another is secondary
- From primary to the secondary node all data replicates

#### What is the correct use-case for MongoDB?

- MongoDB is prefect for _Product Data Management_
- It enables product data and related information to managed
  and processed in a single, central system
- This allows for detailed Cost Analysis, Increased Productivity and Improved Collaboration
