# Sample Code

## Maven  Cycle

when you run a Maven goal, it will run any previous goal. The order of basic phases is:
```
- Validate
- Compile
- Test
- Package
- Verify
- Install
- Deploy
```
Based on official documentation:

TEST - test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed

VERIFY - run any checks on results of integration tests to ensure quality criteria are met

To run unit tests, the Surefire plugin is recommended. And Failsafe for integration tests.
## Bootstrap  Theme
- https://startbootstrap.com/

## JPA One to Many
https://www.baeldung.com/hibernate-one-to-many

* Spring Data JPA find by embedded object property --  Booking|User
```java
List<Booking> findByUser_username(String username);
```

https://www.logicbig.com/tutorials/spring-framework/spring-data/nested-properties-resolution.html

```java
List<Employee> findByDeptartementName(String deptName);

List<Employee> findByDeptartement_name(String deptName);
```


## JPA One Many + REST API
https://netsurfingzone.com/hibernate/one-to-many-mapping-annotation-example-in-hibernate-jpa-using-spring-boot-and-oracle/


##  Spring DATA JPA  FindBy---

- https://www.baeldung.com/spring-jpa-like-queries

- https://www.baeldung.com/spring-data-derived-queries
## Javadoc  Command

C:\b2b\com\steve\util\
C:\b2b\com\steve\app\
C:\b2b\com\steve\gui\


* javadoc -d "C:\docs" -sourcepath "C:\b2b" -subpackages com

* javadoc -d "C:\projectjee\projetdegestionsdestocks\docs\MyJavaDocs" -sourcepath "C:\projectjee\projetdegestionsdestocks\src\main\java" -subpackages comjavadoc -d "C:\projectjee\projetdegestionsdestocks\docs\MyJavaDocs" -sourcepath "C:\projectjee\projetdegestionsdestocks\src\main\java" -subpackages com


***  Test en Mode  DEV

0. mvn  spring-boot:run

1. http://localhost:8088

user/pwd :    admin@test.com / admin2017

2. http://localhost:8088/h2web

url :  jdbc:h2:mem:contactmanager
user: sa
pwd:

Pour voir la base en mémoire.


** Spring DATA REST 

-  Add   spring data rest starter with spring data : pom.xml

-  Implemente Default @Repository with findby?

- ADD spring.data.rest.basePath=/api  to application.properties

- http://localhost:8088/api/   (display all Rest Urls)

- First page=0

- User findByEmail(String email) in repository --->  /api/search -->  http://localhost:8088/api/users/search/findByEmail?email=myemail@yahoo.fr

- Exemple Url with pagination and sort on attribute: http://localhost:8088/api/users?page=0&size=5&sort=name,desc

---- HIBERNATE Performance Tips Sample:
*https://dzone.com/articles/50-best-performance-practices-for-hibernate-5-amp
* https://github.com/AnghelLeonard/Hibernate-SpringBoot
the n+1 select issue is the most common performance problem.
---------------------
-  https://www.baeldung.com/spring-data-rest-customize-http-endpoints
- https://www.mkyong.com/spring-data/spring-data-add-custom-method-to-repository/
- https://www.blazemeter.com/blog/spring-boot-rest-api-unit-testing-with-junit/
https://www.blazemeter.com/blog/api-testing-with-jmeter-and-the-json-extractor/
https://www.blazemeter.com/api-functional-testing/?utm_source=blog&utm_medium=BM_blog&utm_campaign=spring-boot-rest-api-unit-testing-with-junit
- "A Java class can only extend one parent class. Multiple inheritance is not allowed.
 Interfaces are not classes, however, and an interface can extend more than one parent interface. 
The extends keyword is used once, and the parent interfaces are declared in a comma-separated list".
- https://dzone.com/articles/applying-hateoas-to-a-rest-api-with-spring-boot
- "HATEOAS is an acronym for Hypermedia As The Engine Of Application State. Even after expanding that for you, it still might not mean a lot. 
HATEOAS is an extra level upon REST and is used to present information about a REST API to a client, allowing for a better understanding of the API without the need to bring up the specification or documentation. This is done by including links in a returned response and using only these links to further communicate with the server."
- Session server security vs JWT Token (client) https://dev.to/thecodearcher/what-really-is-the-difference-between-session-and-token-based-authentication-2o39
- https://medium.com/@sherryhsu/session-vs-token-based-authentication-11a6c5ac45e4
