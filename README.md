# **Workflow OOP with Java**

## **Overview**

This project demonstrates an **Object-Oriented Programming (OOP)** approach to managing a car sales workflow in Java. It includes functionalities for creating clients and sellers, managing cars, and processing transactions with various payment methods.

## **Project Structure**

The project is organized into several packages, each responsible for different aspects of the workflow:

- **WorkFlow_OOP**: The main package containing the core classes and interfaces.
  - **Bills**: Manages billing and payment processing.
  - **Cars**: Handles car creation and selection.
  - **Enums**: Contains enumeration types used throughout the project.
  - **Exception**: Custom exceptions used in the project.
  - **Persons**: Manages client and seller details.

## **Packages**

### **WorkFlow_OOP.Bills**

- **Bills**: Defines the abstract `Bills` class and its concrete implementations for different payment methods.
  - **Halyk**: Implements payment processing through the Halyk payment method.
  - **Kaspi**: Implements payment processing through the Kaspi payment method.

### **WorkFlow_OOP.Cars**

- **CarSelector**: Creates different types of cars and assigns them to sellers.
- **TypeOfCars**: Contains classes for different car types:
  - **Jeep**
  - **SUV**
  - **Sedan**

### **WorkFlow_OOP.Enums**

- **TypeOfCar**: Enumeration for different car types (e.g., **JEEP**, **SUV**, **SEDAN**).
- **SellerOrClient**: Enumeration for user roles (e.g., **SELLER**, **CLIENT**).

### **WorkFlow_OOP.Exception**

- **WrongMessageException**: Custom exception for handling invalid operations and errors.

### **WorkFlow_OOP.Persons**

- **Client**: Manages client details and operations.
- **Seller**: Manages seller details and operations.
- **PersonsFactory**: Factory class for creating clients and sellers.

## **Usage**

1. **Create Clients and Sellers**:
   ```java
   PersonsFactory personsFactory = new PersonsFactory();
   CreatePersons client1 = personsFactory.createPersons("username", "Name", "Surname", age, "Address", "email@example.com", SellerOrClient.CLIENT);
   CreatePersons seller1 = personsFactory.createPersons("username", "Name", "Surname", age, "Address", "email@example.com", SellerOrClient.SELLER);

## Create Cars:
  CarSelector carSelector = new CarSelector();
  CarsInterface car = carSelector.createCar("CarName", "Company", "Address", TypeOfCar.SEDAN, (Seller) seller, price, year, engineCapacity, "Color", mileage);

## Exceptions
    WrongMessageException: Thrown when an invalid operation is attempted, such as creating a user with an existing username or insufficient funds for a purchase.


