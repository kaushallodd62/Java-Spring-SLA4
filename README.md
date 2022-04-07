## Java Spring JDBC

***Name: Kaushal Lodd
Roll: BT19CSE052***

## Problem Statement

Create a project to connect to a database using Spring JDBC (Java Database Connectivity) with all the CRUD methods.

## Tools Used

1. Maven 3.0+ is our build tool.
2. You're favorite IDE.
3. Latest JDK from Oracle Website.

## Benefits of Spring JDBC over JDBC

* JDBC stands for Java Database Connectivity.
* It used concepts like Statement, PreparedStatement and ResultSet
* Spring JDBC provides a layer on top of JDBC
* It used concepts like JDBCTemplate
* Typically needs lesser number of lines compared to JDBC as following are simplified
    * mapping parameters to queries
    * liquidating resultsets to beans
    * zero exception handling needed because all exceptions are converted to RuntimeExceptions.

## Installation and Setup

1. Install JDK from Java Downloads in Oracle Website.
2. Install Eclipse or your favorite IDE which supports Maven Projects.
3. Install necessary Spring Boot Plugins depending on you IDE.
4. Go to Spring Initializr and generate a bare-bone Spring boot Maven Project. We select the following dependencies
    * Web
    * JDBC
    * H2
    * DevTools
5. Import that project in your repository and begin coding.

## Dependencies in pom.xml file

```
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-jdbc</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-devtools</artifactId>
        <scope>runtime</scope>
    </dependency>
    <dependency>
        <groupId>com.h2database</groupId>
        <artifactId>h2</artifactId>
        <scope>runtime</scope>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-test</artifactId>
        <scope>test</scope>
    </dependency>
</dependencies>
```

## H2 In-Memory Database

H2 is an open-source lightweight Java database. It can be embedded in Java applications or run in the client-server mode. H2 database can be configured to run as in-memory database, which means that data will not persist on the disk, It will be present in the memory, for fast access.

* H2 provides a web interface called H2 Console to see the data. h2 console needs to be enabled in the application.properties in the path
    ` /src/main/resources/application.properties ` by writing 
``` 
# Enabling H2 Console
spring.h2.console.enabled=true
spring.datasource.url=jdbc:h2:mem:testdb
spring.data.jpa.repositories.bootstrap-mode=default
```






