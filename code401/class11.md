# Spring

## Spring App Basics

### our tools : 

1. A favorite text editor or IDE

2. JDK 1.8 or later

3. Gradle 4+ or Maven 3.2+

4. You can also import the code straight into your IDE:

   - Spring Tool Suite (STS)

   - IntelliJ IDEA


### Steps :

* Spring starting with build an application that has a static home page and that will also accept HTTP GET requests at: `http://localhost:8080/greeting.`

**[Manual Initialization]**

1. Navigate to `https://start.spring.io`.

2. Choose either Gradle or Maven and the language you want to use.

3. Click Dependencies and select Spring Web, `Thymeleaf`, and Spring Boot DevTools.

4. Click Generate.

5. Download the resulting ZIP file, which is an archive of a web application that is configured with your choices.

**[Create a Web Controller]**

In Spring’s approach to building web sites, HTTP requests are handled by a controller. You can easily identify the controller by the `@Controller` annotation.

> Make sure you have Thymeleaf on your classpath (artifact co-ordinates: `org.springframework.boot:spring-boot-starter-thymeleaf`). It is already there in the "initial" and "complete" samples in Github.

**[Spring Boot Devtools]**

Spring Boot offers with a handy module known as spring-boot-devtools. Spring Boot Devtools:

- Enables hot swapping.
- Switches template engines to disable caching.
- Enables LiveReload to automatically refresh the browser.
- Other reasonable defaults based on development instead of production.

**[Run the Application]**

The Spring Initializr creates an application class for you. In this case, you need not further modify the class provided by the Spring Initializr. The following listing (from `src/main/java/com/example/servingwebcontent/ServingWebContentApplication.java`).

```java
package com.example.servingwebcontent;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
@SpringBootApplication
public class ServingWebContentApplication {
    public static void main(String[] args) {
        SpringApplication.run(ServingWebContentApplication.class, args);
    }
}
```

The `main()` method uses Spring Boot’s SpringApplication.`run()` method to launch an application.

## how to access data from templates

In a typical Spring MVC application, @Controller classes are responsible for preparing a model map with data and selecting a view to be rendered. This model map allows for the complete abstraction of the view technology and, in the case of Thymeleaf, it is transformed into a Thymeleaf context object that makes all the defined variables available to expressions executed in templates.

**[Spring model attributes]**

Spring MVC calls the pieces of data that can be accessed during the execution of views model attributes. The equivalent term in Thymeleaf language is context variables.

```java
// Example
    @RequestMapping(value = "message", method = RequestMethod.GET)
        public String messages(Model model) {
            model.addAttribute("messages", messageRepository.findAll());
            return "message/list";
        }
```

**[Request parameters]**

Request parameters can be easily accessed in Thymeleaf views. Request parameters are passed from the client to server like:

`https://example.com/query?q=Thymeleaf+Is+Great!`

**[Session attributes]**

add mySessionAttribute to session:

```java
    @RequestMapping({"/"})
        String index(HttpSession session) {
            session.setAttribute("mySessionAttribute", "someValue");
            return "index";
        }
```

**[ServletContext attributes]**

The ServletContext attributes are shared between requests and sessions. In order to access ServletContext attributes in Thymeleaf you can use the #servletContext.

**[Spring beans]**

Thymeleaf allows accessing beans registered at the Spring Application Context with the @beanName syntax, for example:

`<div th:text="${@urlService.getApplicationUrl()}">...</div>`
