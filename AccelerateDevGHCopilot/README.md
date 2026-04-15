# Library App

## Description

Library App is a small .NET application that models library operations using a clean architecture style. It separates domain logic, data persistence, and presentation into distinct projects while using JSON-based storage for sample data and a console interface for interaction.

## Project Structure

- `src/`
  - `Library.ApplicationCore/`
    - Core entities, domain models, service interfaces, and business logic
  - `Library.Console/`
    - Console application entry point, configuration, dependency injection, and sample JSON data files
  - `Library.Infrastructure/`
    - JSON repository implementations and infrastructure services
- `tests/`
  - `UnitTests/`
    - xUnit test project for application core behavior

## Key Classes and Interfaces

- `Author` - Represents an author entity.
- `Book` - Represents a book entity.
- `BookItem` - Represents an individual physical copy of a book.
- `Patron` - Represents a library patron or member.
- `Loan` - Represents a loan record linking a patron to a borrowed book item.
- `ILoanService` - Defines loan operations such as extending or returning loans.
- `IPatronService` - Defines patron operations such as membership renewal.
- `ILoanRepository` - Defines persistence operations for loan storage.
- `IPatronRepository` - Defines persistence operations for patron storage.
- `JsonLoanRepository` - JSON-based repository implementation for loans.
- `JsonPatronRepository` - JSON-based repository implementation for patrons.

## Usage

1. Open the solution in Visual Studio or your preferred .NET IDE.
2. Set `Library.Console` as the startup project.
3. Build the solution targeting `.NET 9.0`.
4. Run the console app to interact with the sample library data and execute loan/patron workflows.

## License

This project is provided under the MIT License. See the LICENSE file for details if available.
