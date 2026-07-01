# ATM Interface - Java OOP Project

A console-based ATM system built with Java, demonstrating core Object-Oriented
Programming principles: encapsulation, classes/objects, and input validation.

## Features
- PIN-based authentication (3 attempts before lockout)
- Balance inquiry
- Deposit and withdrawal with validation
- Graceful handling of invalid input (no crashes on bad data)

## Architecture
- `BankAccount.java` — encapsulates account data (balance, PIN) as private
  fields, exposed only through controlled methods (deposit, withdraw,
  checkBalance). No external code can modify the balance directly.
- `ATM.java` — handles the console interface: menus, user input, and
  Scanner-based validation. Delegates all financial logic to BankAccount.

## How to Run
```bash
javac ATM.java BankAccount.java
java ATM
```

Default test account: PIN `1234`, starting balance `$500.00`.

## Key Concepts Demonstrated
- Classes & objects
- Encapsulation (private fields, public accessor/mutator methods)
- Input validation (`hasNextInt`, `hasNextDouble`) to prevent crashes
- Separation of concerns (UI layer vs. business logic layer)
