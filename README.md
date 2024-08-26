# Appium Automation Testing with Java

![image](https://github.com/user-attachments/assets/29ef384b-747e-4059-978e-3fb78081a84b)



## Introduction

This repository contains a comprehensive setup for automated testing using Appium and Java. It is designed to help automate mobile application testing across various platforms, including Android and iOS. The framework is built with scalability, maintainability, and ease of use in mind.

## Features

- Cross-platform testing (Android and iOS)
- Supports both real devices and emulators/simulators
- TestNG integration for test management
- Extensive use of Page Object Model (POM) for clear separation of concerns
- Configurable environment for different testing scenarios
- Parallel execution capability
- Continuous Integration (CI) ready

## Prerequisites

Before you can run the tests, make sure you have the following installed:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) (Version 8 or above)
- [Maven](https://maven.apache.org/download.cgi)
- [Appium Server](http://appium.io/)
- [Android SDK](https://developer.android.com/studio) (for Android testing)
- Xcode (for iOS testing)
- A device or emulator/simulator to test on


## Project Structure
- **tests**: Contains the test classes.
- **pages**: Houses the Page Object Model classes.
- **utils**: Utility classes like configurations, helpers, etc.
- **config**: Configuration files (e.g., properties files).
- **testdata**: Test data files (e.g., Excel, JSON).
- **pom.xml**: Maven configuration file.
- **testng.xml**: TestNG configuration file.

## Getting Started

### 1. Clone the Repository

```sh
git clone https://github.com/ksuraj20/MobileApplicationAutomationFrameWork.git
cd your-repo-name
```

### 2. Install Dependencies

```sh
mvn clean install
```

### 3. Run Appium Server

Make sure the Appium server is running before executing the tests. You can start Appium from the command line:

```sh
appium
```

Or use the Appium Desktop application.

### 4. Set Up Android/iOS Devices

Ensure that your device/emulator is connected and recognized by ADB or Xcode.

### 5. Execute Tests

To run tests, use the following Maven command:

```sh
mvn test
```

You can also specify a particular TestNG suite:

```sh
mvn test -DsuiteXmlFile=testng.xml
```

## Configuration

- **appium.properties**: Located in `src/test/resources/config`, it contains key-value pairs for environment-specific configurations such as `platformName`, `deviceName`, `appPath`, etc.
- **testng.xml**: Contains the suite and test configurations for TestNG.

## Writing Tests

Follow the Page Object Model (POM) pattern for writing new tests. Create a new page class in the `pages` package and a corresponding test class in the `tests` package.

```java
public class LoginPage {
    // Page elements and actions
}

public class LoginTest {
    @Test
    public void testLogin() {
        // Test logic
    }
}
```

## Reporting

After the tests are executed, you can find the test reports under the `target/surefire-reports` directory. The report includes detailed information about test execution, including passed, failed, and skipped tests.

## Continuous Integration (CI)

This project is CI-ready. You can integrate it with Jenkins, GitHub Actions, or any other CI tool of your choice. Just configure the CI tool to execute the Maven commands as part of your build process.

## Contributing

Contributions are welcome! Please fork this repository, make your changes, and submit a pull request. Make sure to follow the existing code style and write tests for your changes.


