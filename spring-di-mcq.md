# Spring & Dependency Injection MCQ

### Question 1

What is the primary advantage of having attributes typed by required interfaces in component-based architecture?

- A) It allows for faster instantiation of components
- B) It eliminates the need for interfaces altogether
- C) It enables connection to any component that implements the required interface
- D) It automatically handles dependency resolution without configuration

**Correct Answer: C**

---

### Question 2

In the context of Spring beans, what is the key difference between "prototype" and "singleton" scopes?

- A) Prototype beans are faster, while singleton beans consume less memory
- B) Prototype beans allow multiple instances, while singleton beans ensure only one instance exists
- C) Prototype beans work only with XML configuration, while singleton beans work with annotations
- D) Prototype beans are used for web applications, while singleton beans are used for desktop applications

**Correct Answer: B**

---

### Question 3

Which of the following statements about auto-connecting beans by type is FALSE?

- A) It searches for beans with types compatible with the property to be auto-connected
- B) If multiple candidates are found, you can designate a primary candidate
- C) It resembles connections between components having required and provided interfaces
- D) It always prioritizes beans with the shortest class name when multiple candidates exist

**Correct Answer: D**

---

### Question 4

What happens when the `@Autowired(required=false)` annotation is used and no matching bean is found?

- A) An exception is raised immediately
- B) The application fails to start
- C) The property remains null
- D) A default implementation is automatically created

**Correct Answer: C**

---

### Question 5

Which Spring annotation serves the same core purpose as `@Autowired` but comes from the Java EE standard (JSR330)?

- A) `@Resource`
- B) `@Inject`
- C) `@Named`
- D) `@Component`

**Correct Answer: B**

---

### Question 6

When mixing auto-connection and explicit connections in Spring, which of the following is NOT possible?

- A) Using `@Autowired` on some properties and explicit XML configuration on others
- B) Using auto-connection by constructor and explicit connections of some constructor arguments
- C) Using auto-connection by type for some properties and by name for others
- D) Using XML auto-connection for some beans and annotation-based auto-connection for others

**Correct Answer: B**

---

### Question 7

Which statement best describes the benefit of using Spring Expression Language (SpEL) in dependency injection?

- A) It allows for defining connections that are resolved statically at compile time
- B) It eliminates the need for XML configuration entirely
- C) It enables defining connections that are resolved dynamically at runtime
- D) It reduces the memory footprint of Spring applications

**Correct Answer: C**

---

### Question 8

When a class is marked with `@Component` and component scanning is enabled, what happens if no explicit bean ID is provided?

- A) The bean is not created because an ID is mandatory
- B) A random ID is generated based on a UUID
- C) The class name (with the first letter in lowercase) is used as the bean ID
- D) The fully qualified class name is used as the bean ID

**Correct Answer: C**

---

### Question 9

What is the primary architectural advantage of having a separate class (like `MainApplication`) for describing component architecture and launching the application?

- A) It improves application performance
- B) It separates application logic from architecture description (separation of concerns)
- C) It enables multi-threading capabilities
- D) It reduces the number of required classes in the application

**Correct Answer: B**

---

### Question 10

When using `@Configuration` and `@Bean` annotations to declare beans in code, what happens when one bean method calls another bean method multiple times?

- A) A new instance is created for each call, regardless of the bean's scope
- B) An exception is thrown because bean methods cannot call other bean methods
- C) For singleton beans, Spring will return the existing bean instance rather than creating a new one
- D) The application will fail to start due to circular dependencies

**Correct Answer: C**
