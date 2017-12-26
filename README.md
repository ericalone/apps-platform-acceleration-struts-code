# Struts Example

## Build the app with maven

```
$ mvn clean package
```

## Deploy the war to PCF

```
$ cf push struts-example -p target/struts.war
```

```
mysql -uroot
create database struts;
mvn spring-boot:run
mvn clean package

cf push struts -p target/struts.war --random-route --no-start
cf create-service p-mysql 100mb struts-mysql
cf bind-service struts struts-mysql
cf start struts
```
