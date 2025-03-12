# Microservices Architecture MCQs

## 1. Which of the following is NOT a characteristic of a microservice?

- A) Independently deployable
- B) Modeled around a business domain
- C) Shares databases with other services
- D) Manageable complexity

**Answer: C) Shares databases with other services**

---

## 2. In the context of microservices, what does "Domain coupling" refer to?

- A) The unavoidable dependencies between microservices that should be minimized
- B) The coupling that occurs when two microservices depend on the same shared state
- C) Direct access to another microservice's database
- D) When a microservice acts as an intermediary between two other services

**Answer: A) The unavoidable dependencies between microservices that should be minimized**

---

## 3. Which design concept from Domain-Driven Design represents a collection of objects representing a business domain concept with a lifecycle?

- A) Bounded Context
- B) Ubiquitous Language
- C) Aggregate
- D) Domain Event

**Answer: C) Aggregate**

---

## 4. Which migration pattern involves gradually wrapping the existing monolithic application with microservices until it is completely replaced?

- A) Big Bang pattern
- B) Strangler Fig pattern
- C) Parallel Run pattern
- D) Feature Toggle pattern

**Answer: B) Strangler Fig pattern**

---

## 5. What is the primary challenge when migrating from intra-process communication to Inter-Process Communication (IPC)?

- A) Increased security risks
- B) Performance degradation
- C) Inability to handle errors
- D) Higher development costs

**Answer: B) Performance degradation**

---

## 6. When implementing microservices, which of the following communication approaches provides the weakest coupling?

- A) Synchronous HTTP request/response
- B) RPC calls
- C) Event-driven communication
- D) GraphQL queries

**Answer: C) Event-driven communication**

---

## 7. According to the material, which statement is TRUE regarding microservice boundaries?

- A) Microservices should have weak cohesion and strong coupling
- B) Code that changes together should be separated across microservices
- C) A microservice with many domain coupling dependencies likely has too many responsibilities
- D) Content coupling should be encouraged for better performance

**Answer: C) A microservice with many domain coupling dependencies likely has too many responsibilities**

---

## 8. Which type of coupling occurs when a microservice directly accesses another microservice's database?

- A) Domain coupling
- B) Pass-through coupling
- C) Common coupling
- D) Content coupling

**Answer: D) Content coupling**

---

## 9. What is the recommended way to manage relationships between aggregates in different microservices?

- A) Use foreign keys in a shared database
- B) Store IDs or REST API URIs
- C) Implement distributed transactions
- D) Create a central aggregation service

**Answer: B) Store IDs or REST API URIs**

---

## 10. In the context of Domain-Driven Design, what is a Bounded Context?

- A) A set of aggregates with an explicit responsibility
- B) The physical boundary of a microservice's database
- C) The network perimeter within which microservices can communicate
- D) A limit on the number of microservices in an application

**Answer: A) A set of aggregates with an explicit responsibility**

---

## 11. Which of the following is NOT mentioned as an advantage of microservices?

- A) Technology heterogeneity
- B) Robustness
- C) Simplified deployment
- D) Reduced resource consumption

**Answer: D) Reduced resource consumption**

---

## 12. When implementing inter-microservice communication, what does Postel's law (robustness principle) recommend?

- A) "Be conversational in what you do, be precise in what you accept from others"
- B) "Be conservative in what you do, be liberal in what you accept from others"
- C) "Be liberal in what you do, be conservative in what you accept from others"
- D) "Be precise in what you do, be ambiguous in what you accept from others"

**Answer: B) "Be conservative in what you do, be liberal in what you accept from others"**

---

## 13. Which of the following is the most appropriate solution for handling data consistency across multiple microservices?

- A) Using a single shared database
- B) Implementing distributed transactions
- C) Using sagas
- D) Disabling data consistency checks

**Answer: C) Using sagas**

---

## 14. Which pattern of coupling occurs when two or more microservices depend on the same shared state or resource?

- A) Domain coupling
- B) Pass-through coupling
- C) Common coupling
- D) Content coupling

**Answer: C) Common coupling**

---

## 15. In microservices architecture, what is the primary purpose of an API Gateway?

- A) To add business logic to requests
- B) To handle north-south traffic (e.g., from frontend to backend)
- C) To implement service discovery
- D) To manage database connections

**Answer: B) To handle north-south traffic (e.g., from frontend to backend)**

---

## 16. What best describes a Service Mesh in a microservices architecture?

- A) A single monolithic network service
- B) A database synchronization tool
- C) An entity handling east-west traffic (inter-microservice communication)
- D) A frontend component management system

**Answer: C) An entity handling east-west traffic (inter-microservice communication)**

---

## 17. Which approach to microservice communication is most useful when a client needs to aggregate data from multiple services with precise filtering?

- A) REST
- B) gRPC
- C) GraphQL
- D) SOAP

**Answer: C) GraphQL**

---

## 18. What does the slide material recommend regarding API versioning for microservices?

- A) Use only major versions (X.0.0)
- B) Follow MAJOR.MINOR.PATCH versioning to prevent breaks
- C) Avoid versioning altogether
- D) Create new services instead of versioning existing ones

**Answer: B) Follow MAJOR.MINOR.PATCH versioning to prevent breaks**

---

## 19. Which characteristic is TRUE about a distributed monolith?

- A) It consists of a single-process application
- B) It includes several services but is deployed as a cohesive unit
- C) It is the recommended evolution of a microservices architecture
- D) It has no dependencies between its components

**Answer: B) It includes several services but is deployed as a cohesive unit**

---

## 20. According to DDD principles, what best describes the purpose of Ubiquitous Language?

- A) A programming language all microservices must use
- B) Using the same vocabulary in code as that used by domain experts
- C) A centralized dictionary for technical terms
- D) A protocol for inter-service communication

**Answer: B) Using the same vocabulary in code as that used by domain experts**
