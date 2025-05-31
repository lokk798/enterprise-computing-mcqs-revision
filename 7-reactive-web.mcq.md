# Enterprise Reactive Web Applications - MCQ Assessment

## Question 1

What is the primary motivation behind using reactive programming in enterprise applications compared to traditional synchronous approaches?

- a) To reduce memory consumption in applications
- b) To handle asynchronous data streams efficiently while maintaining non-blocking I/O operations
- c) To simplify database query operations
- d) To eliminate the need for error handling mechanisms
- e) To reduce the number of lines of code in controllers

**Correct Answer: b**
**Explanation:** Reactive programming is primarily motivated by the need to handle asynchronous data streams efficiently using non-blocking I/O, which is essential for building scalable and responsive enterprise applications.

---

## Question 2

In the Reactive Streams API data flow, what happens immediately after a subscriber calls `request(n)` on a subscription?

- a) The subscription is automatically canceled
- b) The `onComplete()` method is invoked on the subscriber
- c) The `onNext()` method is invoked n times with data elements
- d) A new subscription object is created
- e) The publisher stops producing data

**Correct Answer: c**
**Explanation:** After `request(n)` is called, the publisher responds by invoking `onNext()` up to n times (depending on available data) to deliver the requested number of elements to the subscriber.

---

## Question 3

Which of the following best describes the relationship between `Mono` and `Optional` in Java?

- a) Mono is the asynchronous version of Optional, both can contain 0 or 1 element
- b) Mono can contain multiple elements while Optional contains only one
- c) Mono is synchronous while Optional is asynchronous
- d) They serve completely different purposes with no similarities
- e) Mono is used for database operations while Optional is for web requests

**Correct Answer: a**
**Explanation:** Mono is described in the lecture as "the reactive equivalent of the Optional type in Java 8+", both can contain 0 or 1 element, but Mono operates asynchronously.

---

## Question 4

What is the primary difference between the `map` and `flatMap` operators in Project Reactor?

- a) map is for filtering data while flatMap is for sorting
- b) map applies synchronous transformations while flatMap must return a Publisher (Mono/Flux)
- c) map works with Flux only while flatMap works with Mono only
- d) map is deprecated in favor of flatMap
- e) There is no functional difference between them

**Correct Answer: b**
**Explanation:** The `map` operator applies synchronous functions to transform data, while `flatMap` is the reactive version that must return a Publisher (Mono or Flux), allowing for asynchronous transformations.

---

## Question 5

In the context of back pressure, what happens when a subscriber cannot keep up with the data production rate of a publisher?

- a) The application crashes with an OutOfMemoryError
- b) The publisher automatically slows down its production rate
- c) The subscriber must implement strategies like buffering, ignoring data, or stopping
- d) The Reactive Streams API automatically handles this without application intervention
- e) All data is stored permanently in memory until processed

**Correct Answer: c**
**Explanation:** When a publisher cannot control data production, the application must implement strategies like buffering, ignoring data, or stopping. This is application-specific and not automatically handled by the Reactive Streams API.

---

## Question 6

Which annotation combination is required for a reactive MongoDB repository to function properly in Spring WebFlux?

- a) @Repository and @Async
- b) @EnableMongoRepositories in the main application class
- c) @ReactiveRepository and @Document
- d) @MongoTemplate and @Reactive
- e) @Component and @Database

**Correct Answer: b**
**Explanation:** The lecture shows that `@EnableMongoRepositories` must be added to the class annotated with `@SpringBootApplication` to enable reactive MongoDB repositories.

---

## Question 7

What is the correct return type for a Spring WebFlux controller method that handles finding a single entity that might not exist?

- a) `Flux<ResponseEntity<Entity>>`
- b) `Mono<Entity>`
- c) `Mono<ResponseEntity<Entity>>`
- d) `Optional<Entity>`
- e) `ResponseEntity<Mono<Entity>>`

**Correct Answer: c**
**Explanation:** For a single entity that might not exist, the correct return type is `Mono<ResponseEntity<Entity>>`, which allows returning either a 200 response with the entity or a 404 response using `defaultIfEmpty()`.

---

## Question 8

In functional endpoint programming with Spring WebFlux, what are the two essential components that must be implemented?

- a) Controller classes and Service layers
- b) Handler functions and Router functions
- c) Repository interfaces and Entity models
- d) Filter chains and Interceptors
- e) Configuration classes and Properties files

**Correct Answer: b**
**Explanation:** Functional endpoints require two main components: Handler functions (methods that receive ServerRequest and return Mono<ServerResponse>) and Router functions (that define the routing configuration).

---

## Question 9

Which of the following statements about the `concat` and `merge` operators is most accurate?

- a) Both operators produce identical results regardless of timing
- b) concat waits for the first publisher to complete before subscribing to the second, while merge subscribes to both simultaneously
- c) merge is synchronous while concat is asynchronous
- d) concat only works with Mono while merge only works with Flux
- e) They are deprecated operators in modern Reactor versions

**Correct Answer: b**
**Explanation:** The lecture explains that `concat` concatenates data sequentially (waiting for completion), while `merge` mixes data from publishers simultaneously, creating different output patterns based on timing.

---

## Question 10

What is the purpose of using `@ResponseStatus(HttpStatus.CREATED)` on a POST method in a reactive controller?

- a) To enable cross-origin requests
- b) To automatically return HTTP 201 status code for successful resource creation
- c) To enable asynchronous processing
- d) To validate request body content
- e) To configure response caching headers

**Correct Answer: b**
**Explanation:** The `@ResponseStatus(HttpStatus.CREATED)` annotation ensures that successful POST operations return HTTP 201 (Created) status code, which is the appropriate response for resource creation.

---

## Question 11

In Server-Sent Events (SSE) implementation, what must be specified in the `@GetMapping` annotation?

- a) `method = RequestMethod.GET`
- b) `headers = "Accept=text/event-stream"`
- c) `produces = MediaType.TEXT_EVENT_STREAM_VALUE`
- d) `consumes = MediaType.APPLICATION_JSON_VALUE`
- e) `path = "/events"`

**Correct Answer: c**
**Explanation:** For SSE endpoints, the `produces = MediaType.TEXT_EVENT_STREAM_VALUE` must be specified to indicate that the endpoint produces server-sent events.

---

## Question 12

What is the primary advantage of using `switchIfEmpty()` in reactive programming?

- a) It improves performance by reducing memory usage
- b) It provides a reactive equivalent to if-else conditional logic for handling empty publishers
- c) It automatically retries failed operations
- d) It enables parallel processing of data streams
- e) It converts Flux to Mono automatically

**Correct Answer: b**
**Explanation:** `switchIfEmpty()` provides a reactive way to handle empty publishers by switching to an alternative publisher, effectively serving as a reactive if-else mechanism.

---

## Question 13

Which operator would you use to transform a `Mono<Integer>` containing the value 3 into a `Flux<Integer>` containing [1, 2, 3]?

- a) `map`
- b) `flatMap`
- c) `flatMapMany`
- d) `concatMap`
- e) `switchMap`

**Correct Answer: c**
**Explanation:** `flatMapMany` is specifically designed to transform a Mono into a Flux, as shown in the example where `Mono.just(3).flatMapMany(i -> Flux.range(1, i))` creates a Flux from a Mono.

---

## Question 14

In functional endpoint routing, why is the order of route definitions important?

- a) For performance optimization
- b) To ensure proper HTTP method matching
- c) Because more specific routes can be overshadowed by general patterns if placed after them
- d) To maintain alphabetical organization
- e) To support RESTful URL conventions

**Correct Answer: c**
**Explanation:** The lecture specifically mentions that routes like `/infos/events` must come before `/infos/{id}` because otherwise "events" would be considered as an id parameter for the general route pattern.

---

## Question 15

What does the `zipWith` operator accomplish in reactive streams?

- a) It compresses data to reduce bandwidth usage
- b) It combines elements from two publishers using a transformation function
- c) It creates a backup copy of the data stream
- d) It sorts elements in ascending order
- e) It filters out duplicate elements

**Correct Answer: b**
**Explanation:** The `zipWith` operator combines corresponding elements from two publishers using a transformation function, as demonstrated in the PUT handler function example.

---

## Question 16

Which of the following represents a correct handler function signature in Spring WebFlux functional endpoints?

- a) `public ResponseEntity<String> handleRequest(HttpServletRequest request)`
- b) `public Mono<ServerResponse> handleRequest(ServerRequest request)`
- c) `public Flux<Object> handleRequest(WebRequest request)`
- d) `public String handleRequest(ServerHttpRequest request)`
- e) `public CompletableFuture<Response> handleRequest(Request request)`

**Correct Answer: b**
**Explanation:** Handler functions must receive a `ServerRequest` parameter and return a `Mono<ServerResponse>`, as specified in the lecture definition of handler functions.

---

## Question 17

What is the main difference between `delayElements()` and `interval()` in Flux operations?

- a) delayElements works only with numbers while interval works with any type
- b) delayElements adds delay between existing elements while interval creates new elements at timed intervals
- c) interval is deprecated in favor of delayElements
- d) delayElements is synchronous while interval is asynchronous
- e) They perform identical operations with different method names

**Correct Answer: b**
**Explanation:** `delayElements()` adds delays between existing elements in a stream, while `interval()` creates a new stream that produces sequential numbers at specified time intervals.

---

## Question 18

In the context of reactive repositories, what is the significance of extending `ReactiveMongoRepository<RecruiterInfo, String>`?

- a) It enables SQL database operations
- b) It provides reactive CRUD operations with RecruiterInfo as entity type and String as ID type
- c) It automatically creates database indexes
- d) It enables caching mechanisms
- e) It provides transaction management

**Correct Answer: b**
**Explanation:** Extending `ReactiveMongoRepository<RecruiterInfo, String>` provides reactive CRUD operations where RecruiterInfo is the entity type and String is the ID type, following Spring Data repository conventions.

---

## Question 19

Which of the following scenarios would benefit most from using `Flux.interval()` in a real-world application?

- a) Processing a batch of user registrations
- b) Implementing periodic health checks or heartbeat mechanisms
- c) Validating form input data
- d) Caching frequently accessed data
- e) Parsing CSV file contents

**Correct Answer: b**
**Explanation:** `Flux.interval()` creates elements at regular time intervals, making it ideal for periodic operations like health checks, heartbeats, or scheduled monitoring tasks.

---

## Question 20

What is the primary architectural benefit of using functional endpoints over annotated controllers in Spring WebFlux?

- a) Better performance due to reduced reflection usage
- b) Enhanced support for functional programming paradigms and immutable design patterns
- c) Simplified testing procedures
- d) Automatic API documentation generation
- e) Built-in security features

**Correct Answer: b**
**Explanation:** Functional endpoints embrace functional programming principles, promoting immutable design patterns (as shown in the PUT example using `new RecruiterInfo()` instead of setters) and functional composition of request handling logic.

---
