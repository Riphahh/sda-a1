# Banking System in Java

This project implements a simple banking system in Java. It demonstrates the application of SOLID design principles to create a flexible, maintainable, and scalable application.

## SOLID Principles

### Single Responsibility Principle (SRP)

- **Account Classes**: Each class (`SavingsAccount`, `CheckingAccount`, and `CreditCardAccount`) has a single responsibility related to handling financial transactions (deposits, withdrawals, balance checks) and does not mix other functionalities.
- **Bank Class**: Responsible solely for managing the lifecycle of accounts, such as creating and retrieving accounts, separating concerns from the financial operations handled by account classes.

### Open/Closed Principle (OCP)

- **Account Class**: Serves as an abstract base for different types of accounts. It is open for extension but closed for modification, meaning new account types can be added without altering the existing system.
- **Bank Class**: Adds new account types without changing its existing code structure, showcasing its adaptability to new requirements without affecting existing functionalities.

### Liskov Substitution Principle (LSP)

- **Account Subclasses**: `SavingsAccount`, `CheckingAccount`, and `CreditCardAccount` can be used interchangeably in place of their base class `Account` without altering the correct functioning of the program, fulfilling the LSP.

### Interface Segregation Principle (ISP)

- While our project has not explicitly defined interfaces due to its scope, it inherently follows ISP by ensuring that classes like `CreditCardAccount` don't implement unnecessary methods from the `Account` class, thereby avoiding the forcing of irrelevant method implementations on classes.

### Dependency Inversion Principle (DIP)

- **Bank Class**: Interacts with accounts through the abstract `Account` class rather than concrete implementations, showcasing the DIP by depending on abstractions not on concretions.

