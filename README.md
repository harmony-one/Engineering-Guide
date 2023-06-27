#
# **Engineering Guide for Harmony Protocol**

Welcome to the engineering guide for Harmony Protocol! This guide is designed to provide our engineering team with a comprehensive set of styles and best practices to ensure that our code is high quality, efficient, and maintainable. By following these guidelines, we can create a consistent, readable, and well-documented codebase that is easier to maintain, debug, and extend.

## **Coding Style**

We recommend following the Google coding style guide ([https://google.github.io/styleguide/](https://google.github.io/styleguide/)), with the following modifications:

- Naming conventions - We use camelCase for variable and function names and PascalCase for class and struct names.
- Line length - We recommend keeping the maximum line length to 80 characters but allowing up to 120 characters for some instances.
- Braces - We use the K&R style, with the opening brace on the same line as the statement and the closing brace on its own line.
- Indentation - We use four spaces for indentation, not tabs.
- Comments - We recommend using descriptive comments to explain the purpose and functionality of the code.

## **Best Practices**

- Modular design - We recommend dividing our code into modules, each with a well-defined and narrow scope. This improves the maintainability of our codebase and makes it easier to test.
- Consistent error handling - We recommend consistent and uniform error handling throughout our codebase. By using a standard error-handling system, we can simplify our code and make it more reliable.
- Testing - We recommend writing tests for our code to ensure that it is correct and robust. Tests should be automated and run frequently.
- Code review - We recommend reviewing each other's code to catch bugs and ensure that it follows the style and best practices outlined in this guide.
- Documentation - We recommend documenting our code thoroughly, including its purpose, inputs, outputs, and any potential side effects.
- Performance - We recommend optimizing our code for performance by using efficient algorithms, minimizing I/O, and avoiding unnecessary computations.
- Security - We recommend ensuring that our code is secure by following best practices for cryptography, authentication, and authorization.

## **Pull Request Naming Conventions**

We follow a standardized format for naming our pull requests to help with organization and readability. The format we use is as follows:

`package/path: change XYZ`

Where `package/path` refers to the affected package or path, and "change XYZ" is a short summary of the change being made. For example, if we are making a change to the "utils" package to fix a bug, we would use the following format:

`utils: fix bug in helper function`

Using this naming convention makes it easy for reviewers and contributors to quickly understand the scope of the change, which can help with prioritization and decision-making. It also helps with maintaining a clean and organized git history.

When creating a pull request, please ensure that the name accurately reflects the changes being made, and avoid using vague or generic titles like "update" or "fix." Instead, provide a clear and concise summary of the change.

In addition to the pull request name, we also encourage including a detailed description of the changes being made, along with any relevant documentation or testing information. This can help with understanding the context and impact of the changes, and can also help with reviewing and testing.

## **Version Control**

We use Git for version control, and we follow these practices:

- Branches - We use the "main" branch as our main development branch. All pull requests should be submitted to the "dev" branch.
- Commit messages - We recommend using clear and descriptive commit messages that follow the present tense imperative style.
- Release tags - We use annotated tags to mark release points in our codebase.

## **Concurrency and Parallelism**

We recommend employing concurrency and parallelism when appropriate to improve the performance of our code. Concurrency enables multiple tasks to run concurrently, while parallelism allows tasks to be executed simultaneously on different processors. These concepts can be especially beneficial in blockchain and distributed systems.

## **Error Handling and Logging**

In addition to consistent error handling, we recommend incorporating a logging system to track important events, errors, and debugging information. Ensure that logs are detailed yet concise and stored securely to avoid information leaks. This can help troubleshoot and monitor our code's performance in both development and production environments.

## **Dependency Management**

We recommend keeping dependencies up-to-date and well-managed. This includes regular updates to maintain compatibility with the latest features, bug fixes, and security patches. Additionally, carefully vet any new dependencies for quality and security to minimize potential risks to our codebase.

## **Continuous Integration and Deployment**

We recommend using continuous integration (CI) and continuous deployment (CD) to automate the process of building, testing, and deploying our code. This can help ensure that our codebase remains stable and that new changes do not introduce breaking or regressions.

## **Static Code Analysis**

We recommend incorporating static code analysis tools into our development process to identify potential issues such as code smells, bugs, or security vulnerabilities. These tools help us catch problems early on before they become more challenging to fix and potentially compromise the integrity of our codebase.

## **Accessibility**

Ensure that our web-based applications and interfaces are accessible to all users, including those with disabilities. Follow the Web Content Accessibility Guidelines (WCAG) and test for accessibility to create a more inclusive experience.

## **Code Review Checklist**

Add a checklist for code reviewers to follow when reviewing pull requests. This can help standardize the review process and ensure that important aspects of the code are not overlooked. The checklist could include items like:

- Does the code follow the style guide?
- Are there any potential performance or security issues?
- Are there sufficient tests and documentation?
- Are there any unresolved merge conflicts or dependencies?

By incorporating these additional guidelines and updates, we can further enhance our codebase's quality, maintainability, and security.

## **Key Management**

We recommend the following practices for key management:

- Two-factor authentication - We recommend using two-factor authentication for all accounts that have access to our codebase and systems.
- Rotation - We recommend regularly rotating our keys and credentials to reduce the risk of compromise.
- Segmentation - We recommend separating our keys and credentials by function and level of access.

## **Code Example**

Here's an example of how to implement our coding style and best practices in Go:
```
package main

import (
	"fmt"
)

type MyStruct struct {
	myField int
}

func (m *MyStruct) DoSomething(arg1 int, arg2 string) error {
	// Do something here
	return nil
}

func main() {
	fmt.Println("Hello, World!")
}
```
Javascript:
```
// This is an example of a function using camelCase naming convention
function calculateTotalPrice(productPrice, taxRate) {
  const totalPrice = productPrice * (1 + taxRate);
  return totalPrice;
}

// This is an example of a class using PascalCase naming convention
class Customer {
  constructor(name, email, phone) {
    this.name = name;
    this.email = email;
    this.phone = phone;
  }
  
  getCustomerName() {
    return this.name;
  }
}

```
Typescript:
```
// This is an example of a function using camelCase naming convention
function calculateTotalPrice(productPrice: number, taxRate: number): number {
  const totalPrice = productPrice * (1 + taxRate);
  return totalPrice;
}

// This is an example of a class using PascalCase naming convention
class Customer {
  constructor(private name: string, private email: string, private phone: string) {}

  getCustomerName(): string {
    return this.name;
  }
}
```
Solidity:
```
pragma solidity ^0.8.0;

contract Counter {
    uint256 private count;

    constructor() {
        count = 0;
    }

    function getCount() public view returns (uint256) {
        return count;
    }

    function increment() public {
        count += 1;
    }
}
```

## **Github Issues Policy**
	
[Click here for Github Issues Cleanup Policies and Procedures](ISSUES.md "ISSUES.md")

## **Conclusion**

By following these style and best practices, we can create high quality and maintainable code that is consistent, readable, and efficient. By working together and adhering to these guidelines, we can ensure that our codebase is robust, reliable, and secure.
