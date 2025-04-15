# Inventory-Management-System

### PROBLEM STATEMENT: 

XYZ Company's outdated and inefficient inventory management system often results in stockouts, overstocking, inaccurate inventory records, and lost revenue. The business struggles to make informed decisions regarding stock replenishment, purchasing, and pricing due to the lack of real-time access to inventory data. Additionally, the reliance on spreadsheets and manual data entry increases the risk of errors, further reducing the system's accuracy and effectiveness. To address these issues, a new inventory management system is needed—one that provides real-time inventory data, automates tracking and replenishment, minimizes errors, and optimizes stock levels to improve operational efficiency and customer satisfaction.

### ARCHITECTURE:
1. Model-View-Controller (MVC): The application adopts the MVC architecture to separate concerns:
   - Model: Represents the data and business logic of the app. It handles the core functionality and data processing.
   - View: Responsible for the UI elements and presentation of the data. It interacts with the user and displays the model's data.
   - Controller: Acts as an intermediary between the Model and the View. It handles user input from the View and updates the Model accordingly.
   This separation allows for easier maintainability, as changes to the business logic (Model) or the user interface (View) can be made independently without affecting the other components.

2. Singleton: The Singleton pattern ensures that a class has only one instance throughout the lifecycle of the application. This is particularly useful for managing shared resources like database connections. The DatabaseHandler class, for example, implements this pattern to guarantee that only one instance manages all database interactions, preventing unnecessary overhead and resource conflicts.

3. Facade: The Facade pattern is used to simplify interactions with complex systems. By providing a unified and simplified interface, the app reduces the complexity of handling intricate internal systems. This pattern allows users or other components to interact with the system more easily, without needing to understand the underlying complexities.

### DESIGN PRINCIPLES:
1. Single Responsibility Principle (SRP): Each class in the application has one responsibility, and its behavior is tightly focused on that responsibility, ensuring that no class is burdened with multiple tasks. This makes the code more modular and maintainable.

2. Don't Repeat Yourself (DRY): The project avoids code duplication by creating reusable components, such as the DatabaseHandler class. This class is used throughout the project for database interactions, ensuring that the same logic isn't repeated multiple times.

3. Keep It Simple, Stupid (KISS): The app follows the KISS principle by keeping the design and code simple and intuitive. This minimizes complexity, making the system easier to understand, develop, and maintain.

4. Separation of Concerns (SoC): Different functionalities and concerns are separated into distinct classes or components. This improves the maintainability and scalability of the application, as each class handles a specific aspect of the app.

### DESIGN PATTERNS:
1. Singleton Pattern: The DatabaseHandler class uses the Singleton pattern to ensure that only a single instance of the class is created. This prevents multiple database connections from being opened simultaneously, optimizing resource usage.

2. MVC Design Pattern: The app's structure follows the MVC design pattern.
   - Model: Handles data, logic, and business rules, making the app more organized and easier to scale.
   - View: Handles the user interface and interacts with the user.
   - Controller: Receives the input from the user and updates the model based on the interaction.

3. Builder Pattern: The app uses the Builder pattern, especially in string manipulation, by employing the StringBuilder class. The pattern allows the construction of a string in an efficient manner, minimizing the overhead of concatenating strings and improving performance.
