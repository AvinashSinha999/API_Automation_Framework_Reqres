# 🚀 API Automation Framework | Reqres

> A modular **API Automation Framework** built using **Java**, **Rest-Assured**, **TestNG**, **Maven**, **Jackson**, **AssertJ**, and **Allure Reports** to automate testing of the **Reqres** APIs.

<p align="center">

![Java](https://img.shields.io/badge/Java-11+-blue?logo=openjdk)
![Maven](https://img.shields.io/badge/Maven-Build%20Tool-C71A36?logo=apachemaven&logoColor=white)
![RestAssured](https://img.shields.io/badge/RestAssured-API--Testing-yellowgreen)
![TestNG](https://img.shields.io/badge/TestNG-Framework-brightgreen)
![AssertJ](https://img.shields.io/badge/AssertJ-Assertions-orange)
![Jackson](https://img.shields.io/badge/Jackson-ObjectMapper-lightgrey)
![Allure](https://img.shields.io/badge/Allure-Reports-ff69b4)
![Log4j2](https://img.shields.io/badge/Log4j2-Logging-yellow)

</p>

---

# 🗂️ Overview

This repository contains a modular **API Automation Framework** for testing the **Reqres** APIs.

Built with **Java**, **Rest-Assured**, **TestNG**, and **Maven**, the framework demonstrates industry-standard API automation practices including **Jackson ObjectMapper-based serialization**, reusable assertion utilities, authentication scenarios, CRUD operations, end-to-end workflow testing, logging, and interactive Allure reporting.

The framework uses **Jackson** for request and response serialization/deserialization, providing a clean, scalable, and type-safe approach to API automation using POJOs.

---

# ✨ Features

- ✅ Complete CRUD API Automation
- ✅ User Registration & Login Validation
- ✅ Positive & Negative API Testing
- ✅ Jackson ObjectMapper Serialization
- ✅ POJO-Based Request & Response Mapping
- ✅ Modular Framework Design
- ✅ Centralized Assertion Utilities
- ✅ End-to-End Integration Testing
- ✅ TestNG Suite Execution
- ✅ Log4j2 Logging
- ✅ Allure Reporting

---

# 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| Java 11+ | Programming Language |
| Maven | Dependency & Build Management |
| Rest-Assured | API Automation |
| TestNG | Test Framework |
| AssertJ | Fluent Assertions |
| Jackson | POJO Serialization & Deserialization |
| Log4j2 | Logging |
| Allure Reports | Test Reporting |
| IntelliJ IDEA | Development IDE |

---

# 🏗️ Project Structure

```text
API_Automation_Framework_Reqres/
│
├── .idea/                                                    # IntelliJ config
├── .mvn/                                                     # Maven wrapper files
├── allure-report/
├── allure-results/
│
├── pom.xml                                                   # Project dependencies & build config
├── .gitignore
├── testng_*.xml                                              # TestNG suite files
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com.avinashsinha.endpoints/
│   │   │   │   └── APIConstants.java                         # API endpoint constants
│   │   │   │
│   │   │   ├── com.avinashsinha.modules/
│   │   │   │   └── PayloadManager.java                       # Payload manager
│   │   │   │
│   │   │   └── com.avinashsinha.pojos/                       # Request/Response POJOs
│   │   │       ├── DataResponse.java
│   │   │       ├── DetailsResponse.java
│   │   │       ├── Login.java
│   │   │       ├── LoginResponse.java
│   │   │       ├── Register.java
│   │   │       ├── RegisterResponse.java
│   │   │       ├── SupportResponse.java
│   │   │       ├── UpdateResponse.java
│   │   │       ├── UserResponse.java
│   │   │       └── Users.java
│   │   │
│   │   └── resources/
│   │       └── log4j2.xml                                    # Logging configuration
│   │
│   └── test/
│       └── java/
│           ├── com.avinashsinha.asserts/
│           │   └── AssertActions.java                        # Assertion utilities
│           │
│           ├── com.avinashsinha.base/
│           │   └── BaseTest.java                             # Base test configuration
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

# 📦 Framework Components

| Component | Description |
|------------|-------------|
| **APIConstants** | Stores all API endpoint constants |
| **PayloadManager** | Creates reusable request payloads using Jackson |
| **POJOs** | Request and response serialization models |
| **BaseTest** | Provides common test setup and configuration |
| **AssertActions** | Centralized assertion utilities |
| **CRUD Tests** | User lifecycle API test scenarios |
| **Integration Tests** | End-to-end workflow validation |
| **Resources** | Log4j2 configuration files |

---

# ✅ Test Coverage

| Endpoint | Test Scenario |
|-----------|---------------|
| **POST** `/api/register` | Register User (Positive) |
| **POST** `/api/register` | Register User (Negative) |
| **POST** `/api/login` | Login User (Positive) |
| **POST** `/api/login` | Login User (Negative) |
| **POST** `/api/users` | Create User |
| **GET** `/api/users` | Retrieve Users |
| **GET** `/api/users/{id}` | Retrieve User by ID |
| **PUT** `/api/users/{id}` | Full Update User |
| **PATCH** `/api/users/{id}` | Partial Update User |
| **DELETE** `/api/users/{id}` | Delete User |
| Workflow | End-to-End Integration Testing |

---

# ▶️ Running Tests

Execute any TestNG suite using Maven.

### Example

```bash
mvn clean test -DsuiteXmlFile=testng_integration.xml
```

### Available Test Suites

| Suite | XML File |
|--------|----------|
| Create User | `testng_createUser.xml` |
| Delete User | `testng_deleteUser.xml` |
| User Details | `testng_detailById.xml` |
| Full Update | `testng_fullUpdate.xml` |
| Partial Update | `testng_partialUpdate.xml` |
| Register User | `testng_registerUser.xml` |
| Login User | `testng_loginUser.xml` |
| Sample Tests | `testng_sample.xml` |
| End-to-End Flow | `testng_integration.xml` |

---

# 📊 Allure Reports

Generate the report using:

```bash
allure serve allure-results
```

<p align="center">
<img width="1100" src="https://github.com/user-attachments/assets/714983f1-f2e6-451a-8978-eba361e77f0d" alt="Reqres Allure Report">
</p>

The command launches an interactive Allure dashboard in your default browser.

---

# 📝 Sample Jackson Payload

```java
Register register = new Register();

register.setEmail("eve.holt@reqres.in");
register.setPassword("pistol");
```

---

# 👨‍💻 Author

**Avinash Sinha**

If you found this repository helpful, consider giving it a ⭐ on GitHub.

---

# 📄 License

This project is intended for **educational** and **learning purposes**.
