# JUnit

-   open source Unit Testing Frameowrk for Java
-   write and run repeatable tests.
-   used for unit testing of a small chunk of code
-   Following Test-Driven Development must write and execute unit test first before any code
-   Once you're done with code you should execute all tests and it should pass.
-   Everytime any code is added you need to re-execute all the test cases and makes sure nothing is broken
-   Portable API which provides all important classes and selenium annotations useful in writing unit tests

## Test-Driven Development

-   refers to a style of prgramming in which three activites are tightly interwoven
    -   coding
    -   testing
    -   design
-   Can be succinctly described by these rules:
    -   write a "single" unit test describing an aspect of the program
    -   run the test, which should fail due to lack of implementation
    -   write the most simple amount of code to make the test pass
    -   _refactor_ the code until it conforms to the simpliest criteria
    -   repeat, "accumulating" unit tests over time
-   **Advantages**
    -   significant reductions in defect rates, at the cost of moderate increase in initial development effort
    -   more than offset in the reduction of efforts towards the final phases of a project
    -   some say it leads to improved design qualities and a higher degree of technical quality
-   **Disadvantages/Pitfalls**
    -   _Individual_
        -   forgetting to run tests frequently
        -   writing too many tests at once
        -   writing tests that are too large or coarse-grained
        -   writing overly trivial test
        -   writing tetsts for trivial code
    -   _Team_
        -   partial adoption: where only a few developers on the team use TDD
        -   poor maintenance on tests: can lead to testing taking a prohibitively long time
        -   seldom or never used: eventually abandoned due to poor quality or lack of team members

## Setup & Teardown

-   Usually there are some repeated tasks that must be done prior to each test case
-   End of each test case, there may be some repeated tasks, i.e cleanup
-   JUnit provides annotations to help in Allocation(setup) and De-allocation(teardown)
    -   this ensures that resources are relesed and the test system is in a ready state for the next test case

## Annotations

-   **@Test**
    -   annotation is a replace of the org.junit.TestCase which indiciates that public void method to which it is attached can be executed as a test Case
    -   can add (timeout=500)
        -   this adds a timeout during test execution incase you are working under some service level agreement(SLA) where tests need to be completed within a specified time limit
    -   can add (expected=IllegalArgumentException.class)
        -   if you want to handle some exception during test execution
        -   If you want ot check whether a particular method is throwing specified exception or not.
-   **@Before**
    -   Setup annotation
    -   used on a method contianing java codde to run ebfore each test case
-   **@After**
    -   Teardown (regardless of result) Annotation
    -   used on a method containing java code to run after each test case
    -   Will run eeven if any exceptions are thown in the test case or in the case of assertion failures
-   _NOTE_:
    -   you can have as many annotations for those listed above
    -   all methods annotated with the @Before in JUnit will run before each test case, but they may run in _ANY_ order
    -   can inherit @Before and @After methods from a super class
-   **@BeforeClass**
    -   it is possible to run a method only once for the tentire test class before any of the tests are executedd
    -   "Once only setup" are useful for starting servers, opening communications, etc. It's time-consuming to close and re-open resources for each test
-   **@AfterClass**
    -   Similar to once only setup, this is a once only cleanup mthod
    -   Runs after all test case methods and @After annotations have been executed
    -   useful for stopping servers, closing communications etc

## Assert Class

-   This class provides a bunch of assertion methods useful in writing a test case
-   If all assert statements are passed, test results are successful
-   If any fail, failure!!!! OHHH NOOO!!!!
-   Methods
    -   asserEquals(expectedValue, actualValue)
    -   assertFalse(conditional)
    -   assertNotNull(object)
    -   assertNull(object)
    -   assertTrue(conditional)
    -   fail()
    -   assertSame()
    -   assertNotSame()

## Code coverage

-   Describes the percentage of code covered by automated tests
    -   checks what parts of code run during the test suite and which don't
-   primary goal is to create high quality, faultless applications that meet our requirements
-   **_We can't say that implementing unit tests gives our application realiable protection from bugs unless we're using the code coverage approach_**
-   **_Taking this approach from the very beginning of a the project eliminates possible bugs in the early stage of the development life cycle_**
-   These shorten development and maintenance times, from the business standpoints it all brings better return on investments (ROI)
-   Can calculate ourselves with the below methods
-   Can also implement things like JaCoCo in our Maven pom.xml file

### Measuring Code Coverage

-   **Statement Coverage**
    -   to run each executable statement in th eprograms code at least once
    -   can also be referred to as line coverage
    -   _Formula_:
        -   Statement coverage = Num of Executed Statements / Total Number of statements \* 100
    -   This allows us:
        -   to verify the do's and don'ts of written code
        -   find any dead/unused statements
        -   check what flow paths are covered
-   **Branch Coverage**
    -   ensures if each decision in a decision-making tree is executed at least once
    -   revolves around conditional statements, loops, switch
    -   _Formula_
        -   Branch Coverage = Number of executed branches / total number of branches \* 100
    -   Allows us to:
        -   verify if the execution of the test suite reaches all branches
        -   detexts any abnormal behaviors of each branch
        -   can test areas of the source code that other approaches may discount
-   **Function Coverage**
    -   verifies if each function of a prgram is being called at least once
    -   important to test functions with different input arguments
    -   broadest coverage compared to the rest
    -   _Formula_
        -   Function coverage = Number of executed functions / Total number of functions \* 100
    -   Allows us to:
        -   Identify any issues with functionality of our code
        -   Identify behavior of functions when incorrect input is incorporated

### Ideal Marks for Code Coverage

-   You'd think ideally 100% code coverage....
-   It's not the simple
-   Depends on the curent project state
    -   from start of software devleopment we can have coverage above 80
    -   taking on a large, legacy project with little to no testing implementation may be nearly impossible
        -   commonly create tests for new feautres and cover existing ones with tests while modifying, fixing or extending them.
-   Enforcing 100% code coverage can be counter productive
    -   could even be harmful to software quality
    -   Developers write useless or misguided tests just to reach the 100% goal
    -   result in missed or een wrongly implemented requirements because developers are more focused on covering as much code as they can
-   The implementation of your particular coverage matters too!
    -   100% coverage doesn't mean there are no bugs in the code
    -   feature can be faultless and tested well but they might not work as intended
-   **_Code coverage is an extremely useful too but shouldn't be treated as the primary goal!!!_**
-   Create high quality meaningful tests for features implemented as per requirements.

## Testing Best Practices

-   _Source Code_
    -   Keep the test classes seperate from the main source code
        -   developed, executed and maintined separately from production code
    -   follows the steps of build tools like Maven and Gradle that look for src/test directory for test implementations
-   _Package Naming Convention_
    -   similar package structure in the src/test directory for test classes
        -   thus improving readability of the testing code
    -   package of the test class should match the package of the source class whose unit of source code it'll test
        -   Main Source Code: com.revature.Daos
            -   Classes: EmployeeDaoImpl, ExpenseDaoImpl
        -   Test Code: com.revature.Daos
            -   Classes: EmployeeTest, ExpensesTest
-   _Test Case Naming Convention_
    -   the test names should be **_INSIGHTFUL_**
        -   users should understand behavior and expectations at a moments glance
    -   testEmployeeWithGetAllEmployees is a bit rough
    -   **Give, When, and Then** format
        -   desribes code blocks to help differentiate the test into three parts
            -   input
            -   action
            -   output
        -   Examples:
            -   givenGetAllRequest_whenEmployeePathSpecified_thenReturnAllEmployees
-   _Expected vs Actual_
    -   Test case should have an assertain between expected and avtual values.
        -   Think assertEquals!
-   _Prefer Simple Test Case_
    -   create simple test case with hard-coded expected value against the actual one returned from the method
    -   SHOULD NEVER implement production logic in a test case to pass the assertions
-   _Appropriate Assertions_
    -   using appropriate assertions to verify the expected vs actual
    -   check on other implementations from the JUnit Assert Class
-   _Specific Unit Tests_
    -   multiple assertions to the same unit test can get overly complicated and difficult to debug and maintain the tests
    -   write a unit test to test a single specific scenario
-   _Test Production Scenarios_
    -   write test considering production level scenarios in minnd
-   _Mock External Services_
    -   potential the code is dependent on external services for some logic
    -   mock the external services and merely test the logic and execution of our code for varying scenarios
    -   Various frameworks for implementation:
        -   Mockito
        -   EasyMock
        -   JMockit
-   _Avoid Code Redundancy_
    -   use more helper functions to generate the commonly-used objects and mock the data or external services.
    -   this improved readability as well
-   _Annotations_
    -   leverage the appropriate annotations to prepare the system for tests by creating data, arranging objects and dropping all of it after every test to keep test cases isolated from each other
-   _80% Test Coverage_
    -   **Rule of thumb** to reach this code coverage from unit tests
    -   Easier to calculated with other tools like JaCoCo
-   _TDD Approach_
    -   testable production code from the start
    -   robust implementation with easy refactoring
    -   fewer regressions
-   _Automation_
    -   can improve realiablity of code by automating the execution of the entire test quite while creating new builds
    -   helps avoid unfortunate regressions in various release environments
    -   rapid feedback before a broken code is released
    -   should be a part of our CI-CD pipelines and alert us incase of malfunctions
