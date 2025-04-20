# Microservices Security MCQ

# Question 1

What is the primary purpose of the "Principle of Least Privilege" in enterprise application security?

- To simplify the authentication process for users
- To grant minimal access levels to individuals or services for a limited time
- To implement multi-factor authentication systems
- To eliminate the need for user credentials altogether

Correct answer: To grant minimal access levels to individuals or services for a limited time

# Question 2

In Spring Security, what does the BCryptPasswordEncoder do?

- Creates authorization tokens for REST APIs
- Decrypts user passwords during authentication
- Provides a hashing function for securely storing passwords
- Generates one-time passwords for multi-factor authentication

Correct answer: Provides a hashing function for securely storing passwords

# Question 3

Which of the following is NOT mentioned as a type of credential in the document?

- User credentials
- Secrets
- Biometric identifiers
- API keys

Correct answer: Biometric identifiers

# Question 4

What tables are required for implementing the "Remember Me" functionality in Spring Security with JDBC authentication?

- users, authorities, and remember_tokens
- persistent_logins only
- users, authorities, and persistent_logins
- users, remember_me, and sessions

Correct answer: users, authorities, and persistent_logins

# Question 5

What is the purpose of the @EnableGlobalMethodSecurity annotation in Spring Security?

- To enable authentication across multiple microservices
- To allow method-level security with various types of annotations
- To encrypt all data transmitted between methods
- To globally disable security for testing purposes

Correct answer: To allow method-level security with various types of annotations

# Question 6

What is the lifecycle stage of a secret that involves ensuring it reaches only the authorized destination?

- Creation
- Distribution
- Storage
- Monitoring

Correct answer: Distribution

# Question 7

Which Spring Security filter chain property would make your application MORE vulnerable to Cross-Site Request Forgery attacks?

- .headers().frameOptions().deny()
- .csrf().disable()
- .requiresChannel().anyRequest().requiresSecure()
- .sessionManagement().sessionCreationPolicy(SessionCreationPolicy.STATELESS)

Correct answer: .csrf().disable()

# Question 8

When implementing user registration with email confirmation in Spring Security, what is the purpose of the VerificationToken entity?

- To authenticate the user during their first login
- To store the user's password temporarily before hashing
- To generate a time-limited token for confirming email addresses
- To encrypt communication between the server and the user's email provider

Correct answer: To generate a time-limited token for confirming email addresses

# Question 9

In the context of the document, what is "Defense in Depth"?

- A security strategy that involves hiring multiple security professionals
- Implementing multiple layers of protection rather than relying on a single one
- A technique for detecting intrusion attempts at the network perimeter
- A method of backing up data in multiple locations

Correct answer: Implementing multiple layers of protection rather than relying on a single one

# Question 10

What Spring Security tag is used to display content only if a user is authenticated?

- <sec:authenticated>
- <sec:authorize access="isAuthenticated()">
- <sec:user-present>
- <sec:if-logged-in>

Correct answer: <sec:authorize access="isAuthenticated()">

# Question 11

Which method in the Spring Security configuration class needs to be overridden to customize authentication?

- protected void configure(final AuthenticationManagerBuilder auth)
- protected void setupAuthentication(final AuthenticationProvider provider)
- public void defineAuthentication(final SecurityBuilder auth)
- protected AuthenticationManager createAuthenticationManager()

Correct answer: protected void configure(final AuthenticationManagerBuilder auth)

# Question 12

What is a key concern regarding JWT tokens in microservice architectures according to the document?

- They are too small to contain all necessary user information
- They require a server to store them if the microservice container restarts
- They cannot be encrypted effectively
- They expire too quickly for practical use

Correct answer: They require a server to store them if the microservice container restarts

# Question 13

What does HSTS (HTTP Strict Transport Security) protect against?

- Cross-site scripting attacks
- SQL injection attempts
- Man-in-the-middle attacks
- Brute force password cracking

Correct answer: Man-in-the-middle attacks

# Question 14

When implementing the "Forgot Password" feature, what is the correct sequence of steps?

- Send token email → User clicks link → User enters new password → Password is updated
- User enters email → Token is stored in database → User receives link → Password is updated automatically
- User enters username and email → Send email with token link → User clicks link → Update password
- User enters username → System generates temporary password → Password is emailed → User changes on first login

Correct answer: User enters username and email → Send email with token link → User clicks link → Update password

# Question 15

What is the purpose of the OnCreateUserEvent class in the registration implementation?

- To handle exceptions during user creation
- To extend the ApplicationEvent for asynchronous email sending
- To validate user input before database insertion
- To log user creation activities for auditing

Correct answer: To extend the ApplicationEvent for asynchronous email sending

# Question 16

Which Spring Security annotation would be used to restrict a method to only users with the ADMIN role?

- @RoleRequired("ADMIN")
- @Restricted(roles="ADMIN")
- @Secured("ROLE_ADMIN")
- @AuthorizeRoles(value="ADMIN")

Correct answer: @Secured("ROLE_ADMIN")

# Question 17

In the context of microservice security, what does "Zero Trust" mean?

- Operating as if the environment is already compromised
- Not implementing any security measures
- Requiring multi-factor authentication for all users
- Encrypting 100% of all data at rest and in transit

Correct answer: Operating as if the environment is already compromised

# Question 18

What security feature does TLS provide when using HTTPS that protects against data tampering?

- Data compression
- Message integrity verification
- Forward secrecy
- Certificate revocation

Correct answer: Message integrity verification

# Question 19

What is required to implement custom password encoding in Spring Security?

- Override the PasswordEncoder interface and provide a @Bean
- Extend the BCryptPasswordEncoder class with a custom salt
- Implement a new authentication provider
- Register a custom AuthenticationManager

Correct answer: Override the PasswordEncoder interface and provide a @Bean

# Question 20

When securing front-end elements in Spring Security, what tag attribute is used to access the current authenticated user's username?

- <sec:authentication property="principal.username"/>
- <sec:user attribute="name"/>
- <sec:principal property="name"/>
- <sec:currentUser property="login"/>

Correct answer: <sec:authentication property="principal.username"/>
