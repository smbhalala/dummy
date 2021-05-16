# meinback
Automation Suite for Limendo

This is a selenium-java-maven framework wrapped with Cucumber wrapper around it.

Installation:
1. Prerequisites
- Eclips for JAVA
- Java/JDK
- Maven 

2. Download the framework using:
git clone https://github.com/cdevit/limendo.git //need to generate this location then it it available
- Once Open it in eclips then need to run following
- mvn clean
- mvn install
- mvn test (to execute the tests)

> Configuration:
url, username/password, and email/role can be changed via application.properties file in the cofig folder.

> Tests:
As it is a JAVA-MAVEN project, so it would typically have src\main and src\tests folder separately configured
- main\java folder consists of all the support that the framework would need to run the test resources.
- main\pageObjects is the folder where the element repository is located to make the tests abstract.

- test\java\stepDefinitions is the space where the code is written.
- test\java\resources is the space for feature files (The Gherkin format files with GWT statements).
- test\java\runners is the space that binds the feature step with the code and executes the test.

> Reports:
npm integrated reports are used in this framework which and can be accessed under src\target\report\index.html

> Execution of maven tags using Command Line:

Running a specific tag file we can use following command:
- mvn test -Dcucumber.filter.tags="@header"

Running mutiple tags we can use:
- mvn test -Dcucumber.filter.tags="@LIM-1024 or @add_user or @header"

Running mutiple tags and ignoring a particular tag:
- mvn test -Dcucumber.filter.tags="@LIM-2583 or @add_user or ~@header"
