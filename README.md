# SpringMVC Maven demo
### QuickStart
- install from bash ``` mvn clean install```
- run from intellij - Maven menu>Plugins>tomcat7>tomcat7:run-war
- navigate to http://localhost:8080/SpringMVCMaven/home

### Requirments
- maven
- jdk 8+
- intellijCE

### Classes, Methods, & Annotations
- ApplicationInitializer.class - registers ApplicationConfig.class to read in Spring application context; servlet config

  - ApplicationConfig.class - stores bootstrapping config; Spring features config
    - @ComponentScan(basePackages = "com.test") - tells spring to spawn beans from classes in com.test package
    - addResourceHandlers() - sets springMVC path to static resouces (images, css, etc)
    - InternalResouceViewResolver() - jsp view resolver; ensures jsp templates are picked up from correct folders.
- HomeController.class
  - @Controller - marks class as controller component
  - @GetMapping - maps handler methods to url pattern
    - goHome() - mapped to "/home", returns "index" template