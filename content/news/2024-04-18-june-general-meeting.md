Title: June General Meeting
Tags: general meeting
Event: 2024-06-18 6:00 pm to 8:00 pm
Speaker: Brian E. Lavender
Location: SEGR
Author: Brian E. Lavender
Slug: june-2024

We will be back at Bel Aire in their meeting room. 

## Full Stack Development with React

We will walk through various aspects of the [Full Stack Development with Spring Boot and React](https://www.packtpub.com/product/full-stack-development-with-spring-boot-and-react-third-edition/9781801816786) using [Fedora 40](https://fedoraproject.org/workstation/download).

[Examples](https://github.com/PacktPublishing/Full-Stack-Development-with-Spring-Boot-and-React.git)

## Tools in use

1. [Fedora 40](https://fedoraproject.org/workstation/download)
1. [Eclipse](https://www.eclipse.org)
2. [VS Code](https://code.visualstudio.com/)
3. MariaDB `sudo dnf install mariadb-server`
4. [Postman](https://www.postman.com/downloads/)
5. [nvm](https://github.com/nvm-sh/nvm)
6. [Mysql JDBC driver](https://mvnrepository.com/artifact/mysql/mysql-connector-java/5.1.49)
7. [Fedora Java Alternatives](https://fedoraproject.org/wiki/Java#Switching_alternatives)

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

Start database

```
sudo service mariadb start
```

Check that user can connect to MariaDB

```
mysql -u brian -p cardb
```

Import [Chapter 5 example code](https://github.com/PacktPublishing/Full-Stack-Development-with-Spring-Boot-and-React/tree/main/Chapter05) and modify `SecurityConfig.java` per book [Hinkula,238]. We will not have security settings for this **demonstration**. 


```
http.csrf().disable().cors().and()
	.authorizeRequests().anyRequest().permitAll();
```

Update `application.properties`

Start `CarDatabaseApplication.java`.

Verify [REST interface](http://localhost:8080/api/cars/) for cars with PostMan

Check npm conifuguration. Create `carfront` skeleton and install 
library dependencies [Hinkula,239].

```
npx create-react-app carfront
cd carfront
npm install @mui/material @emotion/react @emotion/styled
```

Add the `components` folder to `carfront` project [Hinkula,245]. Create
`Carlist.js` and add content.

Verify that the Spring Boot backend is running `CardatabaseApplication`.
Start the React application from the terminal `npm start`.

Brian
