# Task report

[Code here](https://github.com/andlekbra/dat250-expass1)

## Software development environment

My software development environment consists of:

- Java version: 16.0.2, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk-16.0.2
- Apache Maven 3.8.2
- git version 2.33.0.windows.2
- VS Code with extensions for Java, Maven and Git
- Heroku CLI

No problems experienced during installation

Maven binaries were put in C:\Program Files\apache-maven-3.8.2 and C:\Program Files\apache-maven-3.8.2\bin was added to PATH to allow mvn commands from terminal

### Verification
Each pacakge was verified by checking version or in other way interacting with the package in the command line and checking that the expected result was received. Ie `mvn -v`
Further verification was done when following the Heroku tutorial and running the examples locally.

## Heroku tutorial

Carried out tutorial [Getting Started on Heroku with Java](https://devcenter.heroku.com/articles/getting-started-with-java)

Forked tutorial project from https://github.com/heroku/java-getting-started

### Issue with Java runtime version
Heroku uses systems.properties file to specifiy the java runtime version. The specified version in the template was `java.runtime.version=1.8`. This worked when running on the Heroku platform who has many runtime versions available but failed when running local since my installed version was JDK 16. Solved by changing runtime to `java.runtime.version=16`

### Not done
The following parts of the tutorial was not done:

- Did not add papertrail add-on because this required account verification
- Did not install local postgres database


### Link to project

The project is at:
https://andlekbra-dat250-expass1.herokuapp.com/