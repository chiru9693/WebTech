# Day 1 – Issue & Fix

## Issue: Hibernate MySQL Dialect Error

While running the Spring Boot project, the application failed to start and produced the following error:
```
ClassNotFoundException: org.hibernate.dialect.MySQL8Dialect
```
### Reason

This error occurs because Hibernate 7 (used in Spring Boot 4) no longer uses "MySQL8Dialect".

The class "org.hibernate.dialect.MySQL8Dialect" has been removed, so Hibernate cannot find it.

### Error Log

The log clearly showed:
```
ClassNotFoundException: org.hibernate.dialect.MySQL8Dialect
```
This means Hibernate cannot locate the dialect class defined in the configuration.

---

### Solution

Open the "application.properties" file.

You will probably see the following configuration:
```
spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect
```
### Replace it with:
```
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect
```
This change ensures compatibility with Hibernate 7 and resolves the startup error.

---

Screenshot of Error

"Hibernate Dialect Error" (./screenshot%20(255).png)

---

Outcome

After updating the dialect configuration, the Spring Boot application started successfully and connected to the MySQL database without errors.