# Java Web Programming Multiple Choice Questions

## Question 1
What is the primary purpose of using asynchronous servlets in Java web applications?
- A) To improve security by handling requests in separate threads
- B) To make a web application more scalable by freeing up HTTP worker threads
- C) To create more complex HTTP responses with multiple parts
- D) To ensure backward compatibility with older web servers

**Correct Answer: B**

## Question 2
In the context of Java web applications, what is the relationship between servlets and JSP in the MVC pattern?
- A) Servlets are the View, JSP pages are the Controller
- B) Servlets are the Model, JSP pages are the View
- C) Servlets are the Controller, JSP pages are the View
- D) Servlets and JSP pages both represent the Controller layer

**Correct Answer: C**

## Question 3
What is the significance of placing JSP files in the WEB-INF directory?
- A) It makes them load faster by the web server
- B) It improves security by making them accessible only through controllers
- C) It allows the application to use a more efficient compiler for the JSP files
- D) It's required for JSP pages to access the application context

**Correct Answer: B**

## Question 4
When implementing a Filter in Java web applications, which method contains the main filtering logic and must call chain.doFilter() to continue processing?
- A) init()
- B) process()
- C) doFilter()
- D) execute()

**Correct Answer: C**

## Question 5
What is the difference between ServletContext, HttpSession, and HttpServletRequest in terms of their scope and lifetime in a Java web application?
- A) ServletContext: entire application; HttpSession: multiple requests from one user; HttpServletRequest: single request
- B) ServletContext: single request; HttpSession: entire application; HttpServletRequest: multiple requests from one user
- C) ServletContext: multiple requests from one user; HttpSession: single request; HttpServletRequest: entire application
- D) They all have the same scope but different implementation details

**Correct Answer: A**

## Question 6
Which of the following correctly describes the process that occurs when a JSP page is accessed for the first time?
- A) The JSP file is interpreted directly by the web server's JSP engine at runtime
- B) The JSP is transformed into a servlet, then compiled and executed
- C) The JSP is validated against XML schemas before being rendered
- D) The JSP is converted to HTML on the server before being sent to the client

**Correct Answer: B**

## Question 7
When implementing an asynchronous servlet, which of the following is NOT a valid way to complete the asynchronous processing?
- A) Calling ctx.complete()
- B) Calling ctx.dispatch() to another servlet
- C) Allowing the timeout to expire without calling ctx.complete()
- D) Calling ctx.finishProcessing()

**Correct Answer: D**

## Question 8
What is the primary advantage of using Expression Language (EL) in JSP pages compared to using scriptlets?
- A) EL expressions are executed on the client-side, reducing server load
- B) EL expressions have better performance than scriptlets
- C) EL expressions reduce the amount of Java code, making JSP pages cleaner
- D) EL expressions allow access to resources that scriptlets cannot access

**Correct Answer: C**

## Question 9
In the context of Java web applications, what is the purpose of ServletRequestListener?
- A) To intercept and potentially modify HTTP requests before they reach servlets
- B) To be notified when request objects are created and destroyed
- C) To handle authentication for incoming requests
- D) To compress request data before processing

**Correct Answer: B**

## Question 10
Which statement best describes the chain of execution when multiple filters are configured for a servlet?
- A) Filters are executed in random order, and each filter must explicitly call the next filter
- B) Filters are executed in the order specified in web.xml or by annotation priority, with each filter calling chain.doFilter() to continue the chain
- C) All filters process the request in parallel to improve performance
- D) The servlet container determines which single filter is most appropriate for each request

**Correct Answer: B**
