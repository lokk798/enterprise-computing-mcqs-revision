# Enterprise Application Testing - MCQ

---

## Question 1

When using `@SpringBootTest` with `webEnvironment = WebEnvironment.RANDOM_PORT`, what are the advantages over using a fixed port? (Select all correct answers)

- a) It provides better security by obscuring the port number
- b) It allows multiple test instances to run simultaneously without port conflicts
- c) It automatically enables SSL/TLS encryption for test requests
- d) It makes tests more portable across different environments
- e) It enables automatic load balancing across multiple test servers

**Correct Answers: b, d**
**Explanation:** RANDOM_PORT prevents port conflicts in parallel testing environments and makes tests more portable since they don't depend on specific port availability. Security and SSL features are not automatically enabled by this setting.

---

## Question 2

Which annotations are appropriate for testing only the web layer of a Spring application? (Select all correct answers)

- a) @SpringBootTest
- b) @WebMvcTest
- c) @AutoConfigureMockMvc
- d) @DataJpaTest
- e) @JsonTest

**Correct Answers: b, c**
**Explanation:** @WebMvcTest creates a slice test for web layer components, while @AutoConfigureMockMvc (when used with @SpringBootTest) configures MockMvc without starting a web server. @DataJpaTest is for JPA layer testing, and @JsonTest is for JSON serialization testing.

---

## Question 3

When testing a controller that depends on a service, which approaches can be used to handle the service dependency? (Select all correct answers)

- a) Use @MockBean to create a mock of the service
- b) Use @Autowired to inject the real service
- c) Use Mockito's @Mock annotation with manual configuration
- d) Create a test configuration class with a mocked service bean
- e) Use @ComponentScan to load all application components

**Correct Answers: a, d**
**Explanation:** @MockBean integrates seamlessly with Spring context, and creating a test configuration with mocked beans is also valid. @Mock requires manual setup and doesn't integrate with Spring context automatically. Using real services defeats the purpose of unit testing.

---

## Question 4

What are valid ways to verify the behavior of mocked objects in Mockito? (Select all correct answers)

- a) verify(service).methodName() to check method invocation
- b) when(service.method()).thenReturn(value) to define behavior
- c) assertEquals(expected, actual) to validate return values
- d) verify(service, times(2)).methodName() to check invocation count
- e) doThrow(exception).when(service).methodName() to simulate exceptions

**Correct Answers: a, d**
**Explanation:** verify() methods check if and how many times methods were called on mock objects. when().thenReturn() defines behavior but doesn't verify it. assertEquals() validates actual vs expected but doesn't verify mock interactions. doThrow() sets up exception behavior but doesn't verify.

---

## Question 5

In Spring MockMvc testing, which methods can be used to perform assertions on HTTP responses? (Select all correct answers)

- a) andExpect(status().isOk())
- b) andExpect(content().string(containsString("text")))
- c) andExpect(jsonPath("$.field", is(value)))
- d) andDo(print())
- e) andExpect(header().string("Content-Type", "application/json"))

**Correct Answers: a, b, c, e**
**Explanation:** All except andDo(print()) are assertion methods. andDo(print()) is an action that prints the response but doesn't perform assertions - it's used for debugging purposes.

---

## Question 6

What are appropriate use cases for ETag headers in REST API testing? (Select all correct answers)

- a) Managing resource versions to detect concurrent modifications
- b) Implementing optimistic locking in PUT requests
- c) Authenticating API requests
- d) Caching responses on the client side
- e) Compressing response data

**Correct Answers: a, b**
**Explanation:** ETags are primarily used for resource versioning and optimistic locking to prevent lost updates. While ETags can be used for caching, that's not their primary testing purpose. They don't provide authentication or compression.

---

## Question 7

Which HTTP status codes are appropriate for different REST API error scenarios? (Select all correct answers)

- a) 409 (Conflict) when updating a resource with an outdated ETag
- b) 404 (Not Found) when requesting a non-existent resource
- c) 400 (Bad Request) when the request body is malformed
- d) 201 (Created) when a resource update fails
- e) 500 (Internal Server Error) when the database is unavailable

**Correct Answers: a, b, c, e**
**Explanation:** All are correct except d. 201 (Created) indicates successful resource creation, not a failure. The other status codes correctly represent their respective error scenarios.

---

## Question 8

When testing services in Spring, which approaches help achieve proper isolation? (Select all correct answers)

- a) Mock repository dependencies using @MockBean
- b) Use real database connections for all tests
- c) Create mock objects for external service dependencies
- d) Use @Transactional with rollback for database operations
- e) Hardcode all test data within service methods

**Correct Answers: a, c**
**Explanation:** Mocking dependencies (repositories, external services) isolates the service logic being tested. Using real databases or hardcoding data reduces isolation. @Transactional with rollback helps with data cleanup but doesn't provide isolation from database logic.

---

## Question 9

What are the benefits of using an in-memory database like H2 for testing? (Select all correct answers)

- a) Faster test execution compared to external databases
- b) No need for external database server setup
- c) Tests become more portable across environments
- d) Automatic generation of complex test data
- e) Better support for advanced database features than production databases

**Correct Answers: a, b, c**
**Explanation:** H2 provides speed, portability, and eliminates external dependencies. It doesn't automatically generate test data, and it typically supports fewer advanced features than production databases like PostgreSQL or Oracle.

---

## Question 10

In DBUnit testing, which dataset strategies are available for managing test data? (Select all correct answers)

- a) CLEAN_INSERT - deletes existing data then inserts dataset
- b) INSERT - adds dataset records to existing data
- c) UPDATE - modifies existing records with dataset values
- d) DELETE_ALL - removes all data without insertion
- e) MERGE - combines dataset with existing data using primary keys

**Correct Answers: a, b, c**
**Explanation:** CLEAN_INSERT, INSERT, and UPDATE are standard DBUnit strategies. DELETE_ALL and MERGE are not standard DBUnit dataset strategies, though similar functionality might be available through other means.

---

## Question 11

Which annotations are commonly used together for comprehensive integration testing? (Select all correct answers)

- a) @SpringBootTest and @AutoConfigureMockMvc
- b) @SpringBootTest and @ActiveProfiles("test")
- c) @ExtendWith(SpringExtension.class) and @SpringBootTest
- d) @WebMvcTest and @DataJpaTest
- e) @SpringBootTest and @TestPropertySource

**Correct Answers: a, b, c, e**
**Explanation:** These combinations work well for integration testing. @WebMvcTest and @DataJpaTest are both slice tests that focus on specific layers, not comprehensive integration testing.

---

## Question 12

What should be verified when testing a successful POST request that creates a new resource? (Select all correct answers)

- a) HTTP status code 201 (Created)
- b) Location header pointing to the new resource
- c) Response body contains the created resource with generated ID
- d) Request processing time under specific threshold
- e) ETag header for the newly created resource

**Correct Answers: a, b, c, e**
**Explanation:** Status code, Location header, response body, and ETag are all important aspects of a REST POST response. Processing time is a performance concern, not a functional requirement typically tested in unit/integration tests.

---

## Question 13

Which testing approaches help ensure SQL query correctness in repository tests? (Select all correct answers)

- a) Testing against a real database with actual SQL execution
- b) Using H2 in-memory database for SQL compatibility
- c) Mocking the DataSource to avoid database interaction
- d) Using DBUnit to provide controlled test datasets
- e) Writing integration tests that span multiple repository methods

**Correct Answers: a, b, d**
**Explanation:** Real databases and H2 both execute actual SQL, and DBUnit provides controlled data. Mocking DataSource prevents SQL execution, which doesn't verify query correctness. Integration tests help but don't specifically ensure SQL correctness.

---

## Question 14

What are characteristics of effective unit tests for controllers? (Select all correct answers)

- a) They test controller logic in isolation using mocked dependencies
- b) They verify HTTP request/response handling
- c) They include database operations to ensure data persistence
- d) They validate proper error handling and status codes
- e) They test business logic implementation details

**Correct Answers: a, b, d**
**Explanation:** Unit tests should isolate controllers, test HTTP handling, and validate error scenarios. Database operations belong in integration tests, and business logic details should be tested in service unit tests, not controller tests.

---

## Question 15

Which statements about Test-Driven Development (TDD) are correct? (Select all correct answers)

- a) Tests are written before the implementation code
- b) It helps ensure all code has corresponding tests
- c) It eliminates the need for integration testing
- d) It provides faster development once the practice is established
- e) It reduces fear of making changes to existing code

**Correct Answers: a, b, e**
**Explanation:** TDD involves writing tests first, ensures test coverage, and provides confidence for refactoring. It doesn't eliminate integration testing needs and initially may slow development until teams become proficient.

---

## Question 16

What are valid ways to configure test-specific database settings in Spring? (Select all correct answers)

- a) Using application-test.properties file
- b) Using @TestPropertySource annotation
- c) Using @ActiveProfiles("test") with profile-specific configurations
- d) Hardcoding database URLs in test classes
- e) Using @ConfigurationProperties with test-specific values

**Correct Answers: a, b, c**
**Explanation:** Spring provides multiple configuration mechanisms for tests. Hardcoding reduces maintainability. @ConfigurationProperties works but isn't specifically a test configuration approach.

---

## Question 17

Which approaches help achieve proper test data management? (Select all correct answers)

- a) Using @DataSet annotation to load predefined test data
- b) Using @Transactional with rollback to clean up after tests
- c) Creating test data programmatically in @BeforeEach methods
- d) Sharing test data across multiple test classes for consistency
- e) Using CLEAN_INSERT strategy to ensure clean state per test

**Correct Answers: a, b, c, e**
**Explanation:** These approaches help manage test data effectively. Sharing test data across classes creates dependencies and makes tests fragile, violating test isolation principles.

---

## Question 18

What are benefits of using MockMvc over TestRestTemplate for web layer testing? (Select all correct answers)

- a) No need to start a web server
- b) Faster test execution
- c) Better integration with Spring Security testing
- d) More detailed request/response inspection capabilities
- e) Automatic handling of authentication headers

**Correct Answers: a, b, c, d**
**Explanation:** MockMvc doesn't start a server, is faster, integrates well with Spring Security, and provides detailed inspection. Authentication handling depends on test configuration, not automatic.

---

## Question 19

Which statements about integration testing strategy are correct? (Select all correct answers)

- a) Integration tests should verify that separately tested components work together
- b) Integration tests can use real databases with controlled test data
- c) Integration tests should replace all unit tests for efficiency
- d) Integration tests help verify configuration correctness
- e) Integration tests should test end-to-end functionality without frontend

**Correct Answers: a, b, d, e**
**Explanation:** Integration tests complement unit tests by verifying component interactions, can use real databases, verify configuration, and test backend end-to-end flow. They don't replace unit tests - both are needed.

---

## Question 20

What are characteristics of a well-structured test suite for a Spring web application? (Select all correct answers)

- a) Unit tests for each layer (controllers, services, repositories)
- b) Integration tests verifying layer interactions
- c) Only integration tests since they cover more scenarios
- d) Mocked dependencies in unit tests for isolation
- e) Automated execution as part of the build process

**Correct Answers: a, b, d, e**
**Explanation:** A comprehensive test suite includes unit tests for each layer, integration tests for interactions, proper mocking for isolation, and automation. Integration tests alone don't provide the detailed feedback and fast execution that unit tests offer.
