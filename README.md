# Chat Application — PoE Part 1 (Registration and Login)

A console-only Java application that registers a user and logs them in, with
JUnit 5 unit tests and automated testing on every push via GitHub Actions.

## Project structure

```
pom.xml
.github/workflows/maven.yml
src/main/java/chatapp/Login.java   <- all validation and login logic
src/main/java/chatapp/App.java     <- console interface (no GUI)
src/test/java/chatapp/LoginTest.java
```

## Running

```
mvn test                 # run the unit tests
mvn compile exec:java    # run the console application
```

## Validation rules

| Rule | Requirement |
|---|---|
| Username | Contains an underscore, no more than 5 characters |
| Password | At least 8 characters, a capital letter, a number, a special character |
| Cell number | International code `+27` followed by no more than 10 digits |

## Suggested commit sequence 
1. `Initial commit: Maven project setup`
2. `Add Login class with checkUserName method`
3. `Add password complexity validation`
4. `Add regex-based cell phone number validation`
5. `Add registerUser, loginUser and returnLoginStatus methods`
6. `Add JUnit unit tests for all validation rules`
7. `Add GitHub Actions workflow for automated testing`
8. `Add console application and README`

## Reference

Oracle (2024) *Class Pattern*, Java SE 17 API Documentation. Available at:
https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/regex/Pattern.html
(Accessed: 17 September 2026).
