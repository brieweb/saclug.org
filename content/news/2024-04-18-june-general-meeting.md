Title: June General Meeting
Tags: general meeting
Event: 2024-06-18 6:00 pm to 8:00 pm
Speaker: TBD
Location: SEGR
Author: Brian E. Lavender
Slug: june-2024

We will be back at Bel Aire in their meeting room. 

## Full Stack Development with React

We will walk through various aspects of the [Full Stack Development with Spring Boot and React](https://www.packtpub.com/product/full-stack-development-with-spring-boot-and-react/9781803234588).

[Examples](https://github.com/PacktPublishing/Full-Stack-Development-with-Spring-Boot-and-React.git)

## Tools in use

1. Eclipse
2. VS Code
3. MySQL
4. Postman
5. [nvm](https://github.com/nvm-sh/nvm)
6. [Mysql JDBC driver](https://mvnrepository.com/artifact/mysql/mysql-connector-java/5.1.49)
7. Fedora Java Alternatives

Create the database and the user

```
create database cardb character set utf8;

GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, DROP, INDEX, ALTER,
CREATE TEMPORARY TABLES ON cardb.*
TO 'brian'@'localhost' IDENTIFIED BY 'Rockit2';
```

Spring resource to connect to mysql

```
spring.datasource.url=jdbc:mariadb://localhost:3306/cardb 
spring.datasource.username=brian
spring.datasource.password=Rockit2
spring.datasource.driver-class-name=org.mariadb.jdbc.Driver
spring.jpa.generate-ddl=true 
spring.jpa.hibernate.ddl-auto=create-drop

spring.jpa.show-sql=true
spring.jackson.serialization.FAIL_ON_EMPTY_BEANS=false
spring.data.rest.basePath=/api
```

Fix eclipse crashing. Add this to `.bashrc`

```
export WEBKIT_DISABLE_COMPOSITING_MODE=1
```

Verify `nvm` configuration for the shell. 

```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```


Brian
