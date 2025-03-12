# Spring Boot Multiple Choice Questions

## Question 1

What is the primary purpose of Spring Boot's "starter" concept?

- A) To provide executable templates for Spring applications
- B) To group compatible dependencies that handle specific aspects of the application without version management concerns
- C) To reduce the application's startup time
- D) To automatically generate code for common application patterns

**Correct Answer: B) To group compatible dependencies that handle specific aspects of the application without version management concerns**

## Question 2

Which of the following accurately describes Spring Boot's approach to application server deployment?

- A) Spring Boot requires manual configuration of an external application server
- B) Spring Boot uses a "containerful architecture" by default
- C) Spring Boot embeds a server (Tomcat by default) in the framework, creating a "containerless architecture"
- D) Spring Boot applications can only be deployed as WAR files

**Correct Answer: C) Spring Boot embeds a server (Tomcat by default) in the framework, creating a "containerless architecture"**

## Question 3

In Spring Boot, what is the proper way to handle retrieving a non-existent entity from a repository to return a 404 error instead of a 500 error?

- A) Add a try-catch block and return null in the controller method
- B) Check if the repository's findById() result is empty and throw a ResponseStatusException with HttpStatus.NOT_FOUND
- C) Use the @ExceptionHandler annotation with a custom method
- D) Configure the error handling in application.properties

**Correct Answer: B) Check if the repository's findById() result is empty and throw a ResponseStatusException with HttpStatus.NOT_FOUND**

## Question 4

Which statement about Spring Boot configuration sources is FALSE?

- A) Spring Boot supports both .properties and .yml configuration files
- B) Environment variables take precedence over application.properties
- C) It's recommended to use only one configuration source for all parameters
- D) External configuration sources are recommended for sensitive parameters like passwords

**Correct Answer: C) It's recommended to use only one configuration source for all parameters**

## Question 5

What is the correct way to inject a custom property defined in application.properties into a Spring Bean?

- A) @Property("app.version")
- B) @ConfigurationProperty("${app.version}")
- C) @Value("${app.version}")
- D) @Inject("app.version")

**Correct Answer: C) @Value("${app.version}")**

## Question 6

In Spring Boot, which annotation combination is equivalent to the @RestController annotation?

- A) @Component and @ResponseBody
- B) @Controller and @ResponseBody
- C) @Controller and @RequestMapping
- D) @Service and @ResponseEntity

**Correct Answer: B) @Controller and @ResponseBody**

## Question 7

When working with profile-specific properties in Spring Boot, what is the correct way to set the active profile at runtime?

- A) Adding spring.active.profile=dev to application.properties
- B) Using the -Dspring.profiles.active=dev JVM option
- C) Annotating the main application class with @ActiveProfile("dev")
- D) Setting profile.active=dev as an environment variable

**Correct Answer: B) Using the -Dspring.profiles.active=dev JVM option**

## Question 8

Which of the following is NOT a primary advantage of Spring Boot as mentioned in the lecture?

- A) Faster development by eliminating boilerplate configuration
- B) Management of dependency versions and compatibility
- C) Providing standalone applications with embedded servers
- D) Automated database schema generation and migration

**Correct Answer: D) Automated database schema generation and migration**

## Question 9

What happens when you need to replace the default embedded Tomcat server with Jetty in a Spring Boot application?

- A) You must configure Jetty in application.properties only
- B) You add the spring-boot-starter-jetty dependency and exclude spring-boot-starter-tomcat using configurations.implementation
- C) You need to create a custom ServerFactory bean
- D) This is not possible without writing custom Java configuration code

**Correct Answer: B) You add the spring-boot-starter-jetty dependency and exclude spring-boot-starter-tomcat using configurations.implementation**

## Question 10

When preparing a Spring Boot application for containerful deployment as a WAR file, which of the following steps must be taken?

- A) Remove the embedded server dependency completely from the build
- B) Change the server dependency to compileOnly scope and extend SpringBootServletInitializer
- C) Add @EnableWebMvc to the main application class
- D) Implement the WebApplicationInitializer interface in the main class

**Correct Answer: B) Change the server dependency to compileOnly scope and extend SpringBootServletInitializer**
