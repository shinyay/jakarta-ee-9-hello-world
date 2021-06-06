# Getting Started With Jakarta EE 9: Hello World

**Jakarta EE** is a set of specifications that enables the world wide community of java developers to work on cloud native java enterprise applications. Formerly it is knows as `Java Platform, Enterprise Edition (Java EE)`

## Description
Jakarta EE 9 was released at the end of 2020. 
This relase changed the package names that `javax` changed to `jakarta`
Older technologies was removed like support for CORBA. SOAP is also not evolved anymore.

You can create simple Jakarta EE App with the following tutorials. This sample project is created by Maven and Gradle.

## Demo
### Maven Project

```shell
$ mvn archetype:generate -DarchetypeGroupId=org.apache.maven.archetypes -DarchetypeArtifactId=maven-archetype-quickstar

Define value for property 'groupId': com.google.shinyay
Define value for property 'artifactId': jakarta-ee-hello-world
Define value for property 'version' 1.0-SNAPSHOT: :
Define value for property 'package' com.google.shinyay: :
```

#### Maven Wrapper
```
$ mvn -N io.takari:maven:wrapper
```

#### Package Application with Maven
```
$ ./mvnw clean package
```

### Gradle Project
```
$ mkdir jakarta-ee-hello-world
$ gradle init -p jakarta-ee-hello-world \
    --type java-application \
    --dsl groovy \
    --test-framework junit-jupiter \
    --project-name jakarta-ee-hello-world \
    --package com.google.shinyay
```

#### Package Application with Gradle
```
$ ./gradlew clean assemble -x test --build-cache --quiet
```


### Servlert Application
```java
@WebServlet("/hello")
public class App extends HttpServlet
{
    @Override
    protected void doGet(HttpServletRequest req, HttpServletResponse res) throws ServletException, IOException {
        res.getOutputStream().println("Hello, Jakarta");
    }
}
```

- `jakarta.servlet.http.HttpServlet`
  - It allows you to implement methods like `doGet()` and `doPost()` to respond to the specific HTTP Methods that are sent to the application
- `jakarta.servlet.annotation.WebServlet` `@WebServlet`
  - It defines the URL `http://localhost:8080/<root>/<@WebServlet-value>`

## Features

- feature:1
- feature:2

## Requirement

## Usage

## Installation

## References

## Licence

Released under the [MIT license](https://gist.githubusercontent.com/shinyay/56e54ee4c0e22db8211e05e70a63247e/raw/34c6fdd50d54aa8e23560c296424aeb61599aa71/LICENSE)

## Author

[shinyay](https://github.com/shinyay)
