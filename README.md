# API Automation Framework - Reqres

![Java](https://img.shields.io/badge/Java-11%2B-blue)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ%20IDEA-IDE-000000?logo=intellijidea&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-Build%20Tool-C71A36?logo=apachemaven&logoColor=white)
![TestNG](https://img.shields.io/badge/TestNG-Framework-brightgreen)
![RestAssured](https://img.shields.io/badge/RestAssured-API--Testing-yellowgreen)
![Jackson](https://img.shields.io/badge/Jackson-Payload%20Mapper-lightgrey)
![Allure](https://img.shields.io/badge/Allure-Reports-ff69b4)

---

## 🗂️ Overview

This project is an **API Automation Framework** built to test the [Reqres](https://reqres.in/) APIs.  

The framework is developed using **Java**, **Rest-Assured**, **TestNG**, **Jackson** for payload management, **Allure** for reporting, and **IntelliJ IDEA** as the IDE.

---

## ⚙️ Tech Stack

- **Java 11+**
- **IntelliJ IDEA** – IDE for development
- **Maven** – Build & dependency management
- **Rest-Assured** – HTTP client for API automation
- **TestNG** – Testing framework
- **AssertJ** – Advanced assertions
- **Jackson** – Payload serialization & deserialization
- **Allure Reports** – Reporting framework
- **Full Folder Structure** – Hybrid Framework

---

## 🚀 Features
- Automated API testing for **Reqres endpoints** (User creation, fetching, updating, deleting).
- Payload creation and serialisation using **Jackson ObjectMapper**.
- Modular design with separation of concerns:
  - **Endpoints** for constants
  - **Modules** for payload management
  - **POJOs** for request/response mapping
  - **Tests** organised by CRUD, Integration, and Sample flows
- Assertion layer for reusable validations.
- Integrated with **Allure Reports** for rich test reporting.
- Test execution controlled via **TestNG XMLs**.

---

## 🏗️ Project Structure

```bash
API_Automation_Framework_Reqres/
│
├── .idea/                                                          # IntelliJ config
├── .mvn/                                                           # Maven wrapper files
├── allure-results/                                                 # Allure results (auto-generated)
│
├── pom.xml                                                         # Maven dependencies & build config
├── testng_*.xml                                                    # TestNG suite files
├── .gitignore
│                                       
├── src/
│   ├── main/
│   │   └── java/
│   │       ├── com.avinashsinha.endpoints/
│   │       │   └── APIConstants.java                               # API Endpoints & Constants
│   │       │
│   │       ├── com.avinashsinha.modules/
│   │       │   └── PayloadManager.java                             # Payload Builders
│   │       │
│   │       └── com.avinashsinha.pojos/                             # Request/Response POJOs
│   │       	├── DataResponse.java
│   │       	├── DetailResponse.java
│   │       	├── Login.java
│   │       	├── LoginResponse.java
│   │       	├── SupportResponse.java
│   │       	├── UpdateResponse.java
│   │       	├── UserResponse.java
│   │       	└── Users.java
│   │
│   └── test/
│       └── java/
│           ├── com.avinashsinha.asserts/
│           │   └── AssertActions.java                              # Custom Assertions
│           │
│           ├── com.avinashsinha.base/
│           │   └── BaseTest.java                                   # Base Test Setup
│           │
│           └── com.avinashsinha.tests/
│               ├── crud/                                           # CRUD Test Cases
│           	│   ├── TestCreateUser.java
│           	│   ├── TestLoginUser_Negative.java
│           	│   ├── TestLoginUser_Positive.java
│           	│   ├── TestRegisterUser_Negative.java
│           	│   ├── TestRegisterUser_Positive.java
│           	│   ├── TestUserDeletion.java
│           	│   ├── TestUserDetails.java
│           	│   ├── TestUserDetailsById.java
│           	│   ├── TestUserFullUpdate.java
│           	│   └── TestUserPartialUpdate.java
│           	│
│           	├── integration/                                    # Integration Test Cases
│           	│   └── TestE2EFlow.java
│           	│
│           	└── sample/                                         # Sample Tests
│               	└── TestIntegrationSample.java
│
└── README.md
```
---

## ▶️ Running Tests

### Integration Test (Create User, Details, Update and Delete User)
```bash
mvn clean test -DsuiteXmlFile=testng_Integration.xml
```

#### Available TestNG XMLs

- `testng_createUser.xml`
- `testng_deleteUser.xml`
- `testng_detailById.xml`
- `testng_fullUpdate.xml`
- `testng_loginUser.xml`
- `testng_partialUpdate.xml`
- `testng_registerUser.xml`
- `testng_sample.xml`

---

## 📊 Reporting
### Generate Allure Report

```bash
allure serve allure-results
```
  <img src="https://github.com/user-attachments/assets/714983f1-f2e6-451a-8978-eba361e77f0d" alt="Reqres Allure Report" width="1100">

This will launch an interactive report in your browser.

---

## ✅ Example Payload with Jackson

```java
Register register = new Register();
register.setEmail("eve.holt@reqres.in");
register.setPassword("pistol");
```

---

## 📌 Author
👤 Avinash Sinha

---
