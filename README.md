# BDD in Action - Chapter 3: Infographic & .NET Implementation
This repository contains two projects based on the concepts from Chapter 3 of **"BDD in Action, Second Edition" by John Ferguson Smart**:
1. An **interactive infographic** that visually explains the BDD lifecycle.
2. A **.NET implementation** of the "Train Timetables" example from the chapter.
## 📊 Part 1: Interactive Infographic
This project includes an interactive, single-page application that visualizes the key concepts of the Behavior-Driven Development lifecycle. It's built with HTML, Tailwind CSS, and Chart.js.
### 🚀 Live Demo
You can view the live, interactive infographic here:
**[View the BDD Infographic](https://aghazadehm.github.io/TrainTimetables/)**
### How to Run Locally
1. Clone the repository.
2. Open the `index.html` file in your web browser.
## 💻 Part 2: .NET Implementation
This project is a practical implementation of the "Train Timetables" example described in the book. The goal of this repository is to demonstrate how to apply BDD and TDD principles using modern tools from the .NET ecosystem.
### About This Project
This project follows the step-by-step development process explained in the book: from defining business requirements using concrete examples (scenarios) to implementing the application logic using unit tests (TDD).
The main workflow includes:
1. **Formulate:** Writing executable specifications in the form of Gherkin scenarios.
2. **Automate:** Turning these scenarios into automated acceptance tests.
3. **Drive Development:** Using unit tests to implement the underlying logic that makes the acceptance tests pass.
### Technology Stack
This example is built using the following tools and frameworks:
* .NET 8: The primary development platform.
* C# 12: The programming language.
* Reqnroll: A modern alternative to SpecFlow for running Gherkin-based BDD scenarios.
* xUnit: The main framework for running both acceptance and unit tests.
* FluentAssertions: A popular library for writing more readable and fluent assertions in tests.
### Project Structure
The project is divided into three main parts to clearly separate responsibilities:
* `TrainTimetables.Domain/`: This project contains the core application logic (domain classes) like `ItineraryService` and `InMemoryTimetable`. It has no dependencies on testing frameworks.
* `TrainTimetables.AcceptanceTests/`: This project contains the BDD tests.
    * `Features/`: The `.feature` files where Gherkin scenarios are defined.
    * `Steps/`: The `Step Definition` classes that connect each step of the scenarios to C# code.
* `TrainTimetables.UnitTests/`: This project contains the low-level unit tests written with a TDD approach to drive the implementation of the domain classes.
### Getting Started
Follow these steps to run the project and see the test results.
### Prerequisites
Ensure you have the **.NET 8 SDK** or a higher version installed on your system. You can download it from the **[official .NET website](https://dotnet.microsoft.com/download)**.
### Running the Tests
After cloning the repository, open a terminal or command line in the root folder of the project and run the following command:
`dotnet test`
This command will automatically discover and run all acceptance tests (Reqnroll) and unit tests (xUnit) across the solution and display the results in the console.
### ✨ Acknowledgments
This project is entirely based on the excellent and informative example provided in the book **"BDD in Action, Second Edition" by John Ferguson Smart**. All credit for the concepts and the development flow belongs to the author and his book. This repository is solely an attempt to implement those concepts using the .NET technology stack.