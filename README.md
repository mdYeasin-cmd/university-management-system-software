# University Management System Software

### Covered topics in Module 11

- What is SDLC?
  - Planning
  - Analyze
  - Design
  - Implementation
  - Testing & Integration
  - Maintenance
- Requirement Analysis of PH University Management
  - Description
  - Functional requirements
  - Non functional requirements (Performance, Security, Scalability, Useability, Maintainence ect.)
- Modeling Data for PH University Management
- Design Schema and ER Diagram
  - Embedding vs Referencing
    - Embedding
      - if data is fixed and less than 16MB
      - It create duplicate data so kill the storage
    - Referencing
      - if data is growing day by day and which will be more than 16MB
      - It get rid from data duplication and save our database storage
- How to make ER Digram for PH University Management
  - Draw.io
  - Lucidchart
- One to one ralation ship database collection
- Create API Endpoints for PH University Management
  - Design organized endpoints for user
- Rafactoring is a part of development
- Create user interface, model and validation
  - For give validation message we can user validation library
  - In mongoose we can write only define default, requried etc.
- Refactor user validation, student route, controller and service
- Refactor user controller and service
- Create user as Student
  - When we write two collection inside one controller we should use transaction and roleback.
- Setup basic global error handler
  - Error handler middleware takes 4 parameter (err, req, res, next)
  - In express app - inside next function if we pass any parameter that automatically take as an error
- Create not found route & sendResponse utility
  - app.use(wirteNotFoundMiddleware)
- Create index route
  - routes folder separate and index.ts file

### Covered topics in Module 12

- Higher Order Function
  - A function that takes a function, do some task and return a function
  - By using catchAsync() higher order function we can get rid from try-catch repetation
  - By using validateRequest() higher order fucntion we can make a middleware for validate user input.
- Sanitizaation middleware --> validateRequest() function help us for make sanitization middleware
- After express route we can pass only RequestHandler function, If we want to pass a normal funtion we must need to pass their higher order function which return RequestHandler function.
- We need to keep relation between ER Diagram and Requirements analysis
- Every common logic we should check on models middleware
- For compare two data we can use custom mapper
- .padString() --> It is a string operator. which ensure that a word contain minimum specified characters
- lean() --> By default, Mongoose queries return an instance of the Mongoose Document class. Documents are much heavier than vanilla JavaScript objects, because they have a lot of internal state for change tracking. Enabling the lean option tells Mongoose to skip instantiating a full Mongoose document and just give you the POJO. It makes querying 5x faster than regular querying.

### Covered topics in Module 13

- A flow of start coding -> For a software below three steps should be sync
  - Requirement Analysis
  - ER Diagram
  - Start Code
- Transaction & Rollback
  - 4 principles of transaction & rollback
    - A --> Atomicity
    - C --> Consistency
    - I --> Isolation
    - D --> Durability
  - With all properties it called ACID properties
  - For two or more database operation we should use transaction & rollback
  - Transaction steps
    - startSession()
    - startTransaction()
    - if all operation success --> commitTransaction()
    - else --> abortTransaction()
    - endSession()
- Primitive fields can be muted but we should not muted the non-primitive fields
- When we update a document, should not send all data to backend, it will use our network bandwidth. So, we should send only our necessary information.
- We can extends our JavaScipt given class --> Error class is a example of that.

### Covered topics in Module 14

- What is error handling?
- Types of errors
  - Operational error
  - Programmatical error
  - Unhandled Rejection (Asynchronous Code)
  - Uncaught Exception (Synchronous Code)
- Unhandled Rejection and Uncaught Exception can be occur inside application or out site of the application
- Different error comes with different pattern
  - Zod error pattern
  - Mongoose validation pattern
  - Mongoose cast error pattern
  - Mongoose duplicate error pattern
- We should not send error stack in production frontend.
- proccess.exit(1) --> For synchronous code
- server.close(() => process.exit(1)) --> For asynchronous code
- Global error handler can handle only application error.
- For handle Unhandled Rejection and Uncaught Exception we will use server.ts file
- Searching & Filtering
  - Request Object in Express
    - body: {}
    - params: {}
    - query: {}
  - For filter we will use exact match
  - For search term we will use partial match
  - For query in database method chaining is an important thing
  - Formula for pagination --> (page -1) \* limit
- Some job performance good in functional approach and some job performance good in class based approach
- We can made query builder for query in database using class
