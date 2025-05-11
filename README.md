# RestAssured API Automation Framework

A comprehensive test automation framework for API testing using RestAssured, TestNG, and ExtentReports.

## Project Overview

This framework provides an organized structure for automating API tests, particularly focused on the Pet Store API. It includes data-driven testing capabilities, reporting, and logging functionalities.

## Table of Contents

- [Project Structure](#project-structure)
- [Technology Stack](#technology-stack)
- [Setup Instructions](#setup-instructions)
- [Framework Architecture](#framework-architecture)
- [Running Tests](#running-tests)
- [Reporting](#reporting)
- [Logging](#logging)
- [Data-Driven Testing](#data-driven-testing)

## Project Structure

```
├───logs                      # Log files directory
├───Reports                   # Test execution reports
├───src
│   └───test
│       ├───java
│       │   └───api
│       │       ├───endpoints # API endpoint implementations
│       │       ├───payload   # Request payload models
│       │       ├───testcases # Test case implementations
│       │       └───utilities # Utility classes for the framework
│       └───resources         # Configuration files
├───test-output              # TestNG output files
└───TestData                 # Test data files
```

## Technology Stack

- Java
- Maven
- RestAssured
- TestNG
- Extent Reports
- log4j2
- Apache POI (for Excel operations)

## Setup Instructions

### Prerequisites

- Java JDK 8 or higher
- Maven 3.6.x or higher
- Git

### Installation

1. Clone the repository
   ```
   git clone <repository-url>
   ```

2. Navigate to the project directory
   ```
   cd RestAssured-Automation-Framework
   ```

3. Install dependencies
   ```
   mvn clean install
   ```

## Framework Architecture

### Key Components

- **Routes.java**: Contains API endpoint URLs as constants
- **userEndPoints.java**: Implementation of API actions (CRUD operations)
- **userEndPoints2.java**: Alternative implementation using properties file
- **user.java**: POJO class for user data
- **DataProviders.java**: Data provider methods for TestNG
- **ExtentListenerClass.java**: Listener for generating Extent Reports
- **ReadExcelFile.java**: Utility for reading test data from Excel files

## Running Tests

### Running via Maven

```
mvn test
```

### Running Specific Test Classes

```
mvn test -Dtest=UserTest
```

### Running with TestNG XML

```
mvn test -DsuiteXmlFile=testng.xml
```

## Reporting

The framework generates detailed HTML reports using Extent Reports. After test execution, the reports can be found in the `Reports` directory.

## Logging

Log4j2 is configured to generate logs in the `logs/mylog.log` file.

## Data-Driven Testing

The framework supports data-driven testing using:

1. Excel data source (TestData/TestData.xlsx)
2. TestNG data providers (defined in DataProviders.java)

### Example Test Classes

- **UserTest.java**: Basic API tests
- **UserTest2.java**: Tests using alternative endpoint implementation
- **UserTestDD.java**: Data-driven tests using Excel data

## Configuration

- **Routes.properties**: Contains API endpoints configuration
- **log4j2.properties**: Logging configuration

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
