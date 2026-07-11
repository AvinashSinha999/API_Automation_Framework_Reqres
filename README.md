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

This repository contains a modular **API Automation Framework** developed for testing the **Reqres** APIs using **Java**, **Rest-Assured**, **TestNG**, and **Maven**.

The framework demonstrates industry-standard API automation practices including **user registration**, **authentication**, **CRUD operations**, **positive & negative testing**, **POJO-based request/response mapping**, **centralized assertions**, **end-to-end workflow testing**, **logging**, and **interactive Allure reporting**.

Using **Jackson ObjectMapper** for request and response serialization/deserialization, the framework provides a clean, scalable, and type-safe approach to API automation while promoting **clean architecture**, **code reusability**, and **maintainable test design**.

---

# ✨ Key Features

- ✅ Complete CRUD API Automation
- ✅ User Registration & Login Validation
- ✅ Positive & Negative API Testing
- ✅ Jackson ObjectMapper Serialization
- ✅ POJO-Based Request & Response Mapping
- ✅ Modular Framework Architecture
- ✅ Centralized Assertion Utilities
- ✅ End-to-End Workflow Testing
- ✅ TestNG Suite Execution
- ✅ Log4j2 Logging
- ✅ Rich Allure Reporting

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
├── .idea/                                                    # IntelliJ configuration
├── .mvn/                                                     # Maven wrapper files
├── allure-report/                                            # Generated Allure report
├── allure-results/                                           # Allure execution results
├── logs/
│   └── test.log                                              # Test execution logs
│
├── pom.xml                                                   # Maven dependencies & build configuration
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
│   │   │   │   └── PayloadManager.java                       # POJO payload manager
│   │   │   │
│   │   │   └── com.avinashsinha.pojos/                       # Request & response POJOs
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
│               ├── crud/                                     # CRUD test cases
│               │   ├── TestCreateUser.java
│               │   ├── TestLoginUser_Negative.java
│               │   ├── TestLoginUser_Positive.java
│               │   ├── TestRegisterUser_Negative.java
│               │   ├── TestRegisterUser_Positive.java
│               │   ├── TestUserDeletion.java
│               │   ├── TestUserDetails.java
│               │   ├── TestUserDetailsById.java
│               │   ├── TestUserFullUpdate.java
│               │   └── TestUserPartialUpdate.java
│               │
│               ├── integration/                              # End-to-end workflow tests
│               │   └── TestE2EFlow.java
│               │
│               └── sample/                                   # Sample test implementations
│                   └── TestIntegrationSample.java
│
└── README.md
```

---

# 📦 Framework Components

| Component | Description |
|------------|-------------|
| **APIConstants** | Stores all API endpoint constants |
| **PayloadManager** | Creates reusable request payloads using Jackson ObjectMapper |
| **POJOs** | Request and response models for serialization/deserialization |
| **BaseTest** | Provides common test initialization and configuration |
| **AssertActions** | Contains centralized assertion utilities |
| **CRUD Tests** | Implements user lifecycle API test scenarios |
| **Integration Tests** | Validates complete end-to-end workflows |
| **Resources** | Stores Log4j2 configuration files |

---

# 🌐 API Coverage

| Endpoint | Test Scenario |
|-----------|---------------|
| **POST** `/api/register` | Register User (Positive) |
| **POST** `/api/register` | Register User (Negative) |
| **POST** `/api/login` | Login User (Positive) |
| **POST** `/api/login` | Login User (Negative) |
| **POST** `/api/users` | Create User |
| **GET** `/api/users` | Retrieve All Users |
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

Generate and launch the Allure report using:

```bash
allure serve allure-results
```

<p align="center">
<img width="1100" src="https://github.com/user-attachments/assets/714983f1-f2e6-451a-8978-eba361e77f0d" alt="Reqres Allure Report">
</p>

The command generates and opens an interactive **Allure dashboard** displaying execution results, logs, and test statistics.

---

# 📝 Sample Jackson ObjectMapper Payload

```java
Register register = new Register();

register.setEmail("eve.holt@reqres.in");
register.setPassword("pistol");
```

---

# ⭐ Repository Highlights

- ✔ Modular API Automation Framework
- ✔ Industry-Standard Project Structure
- ✔ User Registration & Login Validation
- ✔ Positive & Negative API Testing
- ✔ CRUD Operations
- ✔ Jackson ObjectMapper Serialization
- ✔ POJO-Based Request & Response Mapping
- ✔ Centralized Assertions
- ✔ End-to-End Integration Testing
- ✔ Log4j2 Logging
- ✔ Rich Allure Reporting

---

# 👨‍💻 Author

**Avinash Sinha**

If you found this repository useful, consider giving it a ⭐.

---

# 📄 License

This repository is intended for **educational** and **learning purposes**.
