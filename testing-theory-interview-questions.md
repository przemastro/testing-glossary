## Testing theory

1. What should a typical Test Strategy document include?	
 - A typical document should include: Scope and Objectives, Roles and Responsibilities, Test deliverables, Testing metrics - created by the Project Manager. High-Level document
2. What components should be included in a Test Plan document?	
 - A typical document should include: Test Scope, Type of tests, Entry Criteria, Exit Criteria, Bugs definitions, Environments, Testing approach (manual, automated) - Lower-level document
3. What is Traceability Matrix?	
 - It's the coverage of requirements with tests
4. How would you define a Test Scenario?	
 - It's a broader concept than a test case. It may contain multiple test cases. It's simply a testing procedure for a particular functionality
5. What comprises a Test Case?	
 - A set of steps to reproduce, expected results, and a brief description of the test
6. What is meant by Test Approach?	
 - CRUD
7. What is a Test Oracle?	
 - A source providing expected results allowing comparison with obtained results. It can be an existing system user manual, tester's knowledge, but cannot be code
8. What metrics are included in Testing Metrics?	
 - Requirements coverage, number of defects found (critical, blockers, major), and fixed, time taken to fix a defect
9. What are the stages of SDLC?	
 - Analysis, planning, Requirement gathering, Development and Testing, Maintenance, Project closure activities
10. What are the characteristics of the Waterfall model?	
 - Each development step of the application follows the other. Drawbacks: project takes longer, difficult to introduce changes. Advantages: more organized, documentation exists
11. What are the stages of the Defect Life Cycle?	
 - Report, assign, fix, resolve, test, approve or reject and assign, close
12. What components are typically included in Defect Reporting?	
 - Title, environment, sometimes sprint number, steps to reproduce, expected result, actual result, screenshot
13. What are some common Testing Techniques?	
 - Equivalence classes, Boundary values, State transition, Decision table
14. What are Smoke Tests?	
 - Core functionality tests
15. When are Regression Tests conducted?	
 - After smoke tests, verifying if the system didn't break after changes, new features introduction, bug fixes
16. What criteria determine what to automate in testing?	
 - Core functionalities (used in multiple places), Tests run multiple times (regression, smoke tests), Tests with a large amount of test data, Tests run on multiple browsers, Functionalities prone to breaking
17. What is White Box Testing?	
 - Unit testing, we look into the code internals. We verify the operation of methods, classes, procedures, tables, etc.
18. What is Black Box Testing?	
 - Without looking into the code. We test based on testing techniques
19. What is Ad Hoc Testing?	
 - Without preparation, based solely on our own experience
20. What is Exploratory Testing?	
 - Based on our own experience. We prepare for it. There may be some documentation
21. What is an Exploratory Session?	
 - Session-based testing (2-3 sessions) each session 30-45 minutes. The session metrics are the primary means to express the status of the exploratory test process. They contain the following elements: Number of sessions completed, Number of problems found, Function areas covered, Percentage of session time spent setting up for testing, Percentage of session time spent testing, Percentage of session time spent investigating problems
22. What is Test-Driven Development (TDD)?	
 - A development concept where we first write a test for functionality, write the functionality, if it fails, we fix the functionality and run the test again
23. What is Behavior-Driven Development (BDD)?	
 - An extension of the TDD concept with an additional layer presenting tests in a natural language understandable to the business
24. What is the purpose of Testing in software development?	
 - Checking if the requirements have been implemented correctly
25. How does Quality Assurance (QA) differ from Testing?	
 - QA is a broader concept than testing. Testing is a component of QA, but QA also cares about customer experience, e.g., aesthetics, innovation, as well as whether any standards have been maintained
26. What is Severity in defect management?	
 - How important the bug is for the business
27. What is Priority in defect management?	
 - How quickly to resolve the bug
28. What are the different levels of testing?	
 - Unit testing, Integration testing, System testing, Acceptance testing
29. What is Static Analysis in testing?	
 - Testing of the module or system at the stage of writing specifications and design without running the code
30. What is Dynamic Analysis in testing?	
 - Here we run the code and review the code manually
31. What is the Waterfall Model in software development?	
 - In this model, each phase of software development follows the other: Requirement Gathering -> Design -> Development -> Testing -> Maintenance
32. What is the V Model in software development?	
 - An extension of the waterfall model, where each design stage has its verification counterpart. Thus, requirements are checked by acceptance tests, component architecture is checked by component tests, system architecture is checked by system tests, etc. Implementation is at the bottom
33. What are Non-Functional Tests?	
 - Performance, security, usability, portability, accessibility
34. What are Load Tests?	
 - How many requests the system can handle in a specified time
35. What are Stress Tests?	
 - We check when the system crashes and whether it crashes in the expected way
36. What are Performance Tests?	
 - How long it takes to perform a certain action, a certain request
37. What is a Usability Session?	
 - Tests with users. We examine how long the user spent on the page, what are the feelings about the application, time needed to complete a task
38. What is Security Testing?	
 - e.g., sql injection, cross-site scripting
39. What is the Testing Pyramid?	
 - In a sense, a quantitative systematization of tests. The pyramid assumes that we run the most unit tests, then functional and acceptance tests. The least End-to-End
40. What is UML (Unified Modeling Language)?	
 - Object modeling. Example diagrams: Activity, Use cases, Classes
41. What is WSDL (Web Services Description Language)?	
 - (Web Services Description Language) - information regarding the web service- accepted data types, operational port, operations, endpoint information
42. What is Pairwise Testing?	
 - Black-box technique of designing test cases, aiming to reduce the number of test cases to complete testing faster. Proper application of this technique should not reduce coverage
43. What is a Test Harness?	
 - Test environment consisting of stubs and drivers needed to execute a test
44. What is a Hot-Fix?	
 - A fix introduced into an application already in production without a new release of the entire application. The fix is first tested on the acceptance environment, which is a copy of the production environment
45. What is a Change Request?	
 - A request from the business to make changes to the functionality of the application in production
46. What are the different Environments used in software development?	
 - DEV - usually locally at the developer's but also often shared by other developers. TEST - dedicated to testers for automated and manual testing, UAT - environment intended for client acceptance testing, PROD - I probably don't need to explain what this means
47. What is SSH?	
 - It's a communication protocol that allows user authentication during communication
48. What is a JSON array?	
 - An array of objects - [{},{}]
49. What is a JSON object?	
 - For example: { name: "name", lastName: "lastName"}
50. What happens when an Assert step fails in test execution?	
 - The test execution stops
51. What happens when a Verify step fails in test execution?	
 - The test execution continues
52. What is Implicit Wait?	
 - It's a global wait for all elements. Wait until an exception is thrown that the element cannot be found
53. What is Explicit Wait?	
 - It's a local wait for a specific element
54. What is Fluent Wait?	
 - It's intended for elements whose appearance time is highly variable
55. What is the Page Object Pattern?	
 - It's a mapping of, for example, a web page in the form of a class with methods corresponding to a given functionality. From such an object, i.e., an instance of a class, we call methods
56. What is the Page Object Model?	
 - An extension or addition to the Page Object pattern. Created to avoid duplicating code and store and initialize web elements in one place. The simplest way is to create a class with web elements and initialize them (find). This way, we don't have to change the locator in many places if it changes. We save time and space
57. What is Page Factory?	
 - We can create such a model ourselves, but why, when Selenium WebDriver has it already created and optimized. It's called Page Factory
58. How is BDD implemented in practice?	
 - BDD binding in C# and Java - [Binding] and @Binding. Examples of frameworks: Specflow - BDD for C# uses attributes [], JBhave - BDD for Java uses annotations, Cucumber - BDD for Java uses annotations and importantly, gluing steps with features is done through the "glue" keyword in the test runner class. Jasmine - BDD for JS
59. What is TestNG?	
 - It's a Java framework for unit tests and functional tests. Most commonly used in combination with selenium. TestNG Annotations: @Test, @BeforeClass, @AfterClass, @BeforeSuite, @AfterSuite, @BeforeMethod, @AfterMethod
60. What are Locators in Selenium?	
 - They can generally be divided into two groups: related to the DOM (xpath, id, name) and CSS
61. What are the types of Mobile Applications?	
 - Native - installed on devices from sources such as Google Play. They are dedicated to specific devices. They can use phone functionalities like the Camera. Hybrid - They are available from Google Play but run browser-based. Web - applications run through the browser, usually written in HTML5
62. What are tools for Mobile Testing?	
 - Tools for automatic testing of mobile devices: appium, robotium, espresso. In the case of web applications, you can use selenium webdriver emulators for mobile applications
63. What are Event Listeners in Selenium?	
 - A set of methods that allow logging actions but only those related to webdriver
64. What is RegExp?	
 - A character string defining a search pattern. For example, .* we are looking for files of any format
65. What is Low-Level Programming?	
 - Low-level programming is a language understandable by a computer [machine language (binary code)] e.g., assembly
66. What is High-Level Programming?	
 - High-level programming is programming understandable by humans e.g., Java
67. What is Cache?	
 - Cache is a cache memory. It is used for faster access to data. e.g., Browser cache memory means that elements already loaded once do not have to be loaded again; they are simply retrieved from the cache
68. What is a Runtime Environment?	
 - In high-level languages, a special interpreter is needed to translate code into binary form understandable by the machine. Examples include node.js and JRE
69. What is a Package Manager?	
 - A system for automatic installation, configuration, updating, and removal of software packages
