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

When creating a Pull Request (PR), using a consistent and descriptive naming convention is essential. A well-named PR makes it easier for other team members to quickly understand what changes the PR contains and why.

We recommend using the following naming convention:

`[TYPE] Short description of the change`

Where `[TYPE]` is one of the following:
- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation changes
- **refactor**: Refactoring of existing code
- **test**: Adding or updating tests
- **chore**: Changes to build or development tools

For example, a Pull Request that adds a new endpoint to the API might have the following name:

`[feat] Add new API endpoint for user registration`

Using a consistent naming convention also makes it easier to search for and organize PRs. If your team uses an automated PR management tool, such as GitHub's Pull Request feature, a well-named PR will be automatically categorized and easier to track.

In addition to the naming convention, it's crucial to provide a clear and detailed description of the changes in the PR. This helps other team members understand the changes without reviewing the entire codebase.

By following these naming conventions and providing clear descriptions, we can improve the efficiency and effectiveness of our Pull Request process, leading to a more streamlined and productive development cycle.


## **Version Control**

We use Git for version control, and we follow these practices:

- Branches - We use the "main" branch as our main development branch. All pull requests should be submitted to the "dev" branch.
- Commit messages - We recommend using clear and descriptive commit messages that follow the present tense imperative style.
- Release tags - We use annotated tags to mark release points in our codebase.

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
## **Conclusion**

By following these style and best practices, we can create high quality and maintainable code that is consistent, readable, and efficient. By working together and adhering to these guidelines, we can ensure that our codebase is robust, reliable, and secure.
