# Payroll System in Java

This project is a simple **Payroll System** implemented in Java using **OOP principles** such as inheritance, polymorphism, and abstraction. The program allows for the management of employees, including adding, removing, and displaying details about their salaries.

---

## Features

1. **Employee Management**  
   - Add new employees (Full-Time and Part-Time).  
   - Remove employees by their ID.  
   - Display details of all employees.  

2. **Salary Calculation**  
   - Full-Time Employees: Salary is calculated based on a fixed monthly salary.  
   - Part-Time Employees: Salary is calculated based on the hours worked and hourly rate.

---

## Classes Overview

### 1. `Employee` (Abstract Class)  
- **Fields**:  
  - `name`: Name of the employee.  
  - `id`: Unique identifier for the employee.  

- **Methods**:  
  - `calculateSalary()`: Abstract method to calculate salary, implemented by subclasses.  
  - `toString()`: Displays employee details, including name, ID, and salary.

### 2. `FullTimeEmployee` (Subclass of Employee)  
- **Fields**:  
  - `monthlySalary`: Fixed monthly salary for the employee.  

- **Methods**:  
  - `calculateSalary()`: Returns the fixed monthly salary.

### 3. `PartTimeEmployee` (Subclass of Employee)  
- **Fields**:  
  - `hoursWorked`: Total hours worked by the employee.  
  - `hourlyRate`: Rate per hour.  

- **Methods**:  
  - `calculateSalary()`: Returns salary calculated as `hoursWorked * hourlyRate`.

### 4. `PayrollSystem`  
- **Fields**:  
  - `employeeList`: A list of all employees.  

- **Methods**:  
  - `addEmployee(Employee employee)`: Adds an employee to the system.  
  - `removeEmployee(int id)`: Removes an employee by their ID.  
  - `displayEmployees()`: Prints the details of all employees.  

### 5. `Main`  
- Demonstrates the functionality of the payroll system by creating instances of `FullTimeEmployee` and `PartTimeEmployee`, adding them to the system, and performing operations like removing and displaying employees.

---

## How to Run the Project

1. **Prerequisites**:  
   - Java Development Kit (JDK) installed.  
   - IDE/Text Editor (e.g., IntelliJ, Eclipse, or VS Code).  

2. **Steps**:  
   - Clone the repository.  
   - Open the project in your IDE or text editor.  
   - Compile and run the `Main` class.  

---

## Sample Output
Initial Employee Details: 
Employee [name=John Doe, id=101, salary=5000.0] 
Employee [name=Jane Smith, id=102, salary=450.0] 
Employee [name=John Doe, id=105, salary=5000.0]

Removing Employee...

Remaining Employee Details: 
Employee [name=John Doe, id=101, salary=5000.0] 
Employee [name=Jane Smith, id=102, salary=450.0] 
Employee [name=John Doe, id=103, salary=5000.0] 
Employee [name=John Doe, id=104, salary=5000.0]
