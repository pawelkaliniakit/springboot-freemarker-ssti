# Spring Boot with FreeMarker - Server Side Template Injection example

## Movie with exploitation of SSTI
https://drive.google.com/open?id=158O4InnJtLf1pemxKcyNodUQXjWBQLAw

## What you'll need
- JDK 1.7 or later
- Maven 3 or later

## Stack
- Spring Boot
- Java

## Run & exploit
- Run application
`mvn spring-boot:run`
- Open another terminal and run nc in listen mode:
`nc -l -p 1234`
- Run postman, import collection 'Freemarker - SSTI.postman_collection.json' and environment 'local - 8080.postman_environment.json'
- Send request 'Hello World' from imported collection to check default behaviour of application
- Send 'Template-upload' request from imported collection to override default 'hello.ftl' template with malicious template.
- Send once again request 'Hello World'
- Check terminal with running nc in listen mode to check see content of your /etc/passwd sent by application.
