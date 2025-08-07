# Object-Oriented Programming Final Assignment
## Flight Management & Course Registration Systems

**Author:** Chanan Helman
**Course:** Introduction to Object-Oriented Programming  
**Institution:** Ariel University  
---

## 📋 Project Overview

This assignment demonstrates advanced Object-Oriented Programming concepts through the implementation of two comprehensive systems:

1. **Flight Management System** - A sophisticated airline management system
2. **Course Registration System** - A university course enrollment system

Both systems showcase multiple design patterns, inheritance hierarchies, abstract classes, interfaces, and comprehensive exception handling.

---

## 🎯 Assignment Structure

### Part A: Guided Design
**Flight Management System** implementing:
- **Strategy Pattern** - Dynamic flight search algorithms
- **Composite Pattern** - Hierarchical airline company structure  
- **Observer Pattern** - Real-time flight notifications

### Part B: Free Design
**Course Registration System** implementing:
- **Singleton Pattern** - Single registration system instance
- **Flyweight Pattern** - Efficient course object management
- **Observer Pattern** - Course availability notifications
- **Strategy Pattern** - Multiple notification methods
- **Facade Pattern** - Simplified system interface

### Part C: Code Analysis
Analysis of compilation errors, runtime errors, and logical bugs in provided code snippets.

---

## 🏗️ System Architecture

### Flight Management System (Ex1A Package)

#### Core Components
- **Airport** - Central hub managing flight companies (Singleton)
- **FlightCompany** - Main airline entity with hierarchical structure
- **Flight** - Individual flight representation
- **PersonFlight** - Abstract base for all flight-related personnel

#### Design Patterns Implementation

**🔍 Strategy Pattern - Flight Search**
```java
public interface FlightSearchStrategy {
    void search(List<Flight> flights, String searchRange);
}
```
- `searchByPriceStrategy` - Price-based filtering
- `searchByDestinationStrategy` - Destination-based search
- `searchByDateStrategy` - Date range filtering

**🏢 Composite Pattern - Company Hierarchy**
```java
public interface FlightComponent {
    void printData();
}
```
- Unified interface for companies and sub-companies
- Hierarchical data management and display

**👀 Observer Pattern - Flight Notifications**
```java
public interface FlightObserver {
    void update(String msg);
}
```
- Real-time notifications for flight delays, cancellations, and sales
- Automatic passenger and crew updates

### Course Registration System (Ex1B Package)

#### Core Components
- **RegisterSystem** - Central registration management (Singleton)
- **UniversityPerson** - Abstract base class for all users
- **Course** - Course representation with capacity management
- **Student/Lecturer/Practitioner** - Specialized user types

#### Design Patterns Implementation

**🏭 Singleton Pattern**
```java
public static RegisterSystem getInstance() {
    if (instance == null) {
        instance = new RegisterSystem();
    }
    return instance;
}
```

**🪶 Flyweight Pattern**
```java
public static Course getCourse(String name, int courseID, ...) {
    if (!courseMap.containsKey(courseID)) {
        Course course = new Course(name, courseID, ...);
        courseMap.put(courseID, course);
    }
    return courseMap.get(courseID);
}
```

**📢 Strategy Pattern - Notification Methods**
- `EmailNotificationStrategy`
- `SmsNotificationStrategy` 
- `PhoneNotificationStrategy`

---

## 🚀 Getting Started

### Prerequisites
- Java Development Kit (JDK) 8 or higher
- IDE (IntelliJ IDEA, Eclipse, or VS Code)

### Running the Application

#### Flight Management System
```bash
javac Ex1A/main.java
java Ex1A.main
```

#### Course Registration System
```bash
javac Ex1B/Main.java
java Ex1B.Main
```

---

## ✨ Key Features

### Flight Management System
- **Dynamic Flight Search**: Search by price range, destination, or date
- **Company Hierarchy**: Support for parent companies and subsidiaries
- **Real-time Notifications**: Instant updates for flight changes
- **Crew Management**: Automated crew assignment with validation
- **Exception Handling**: Custom exceptions for various scenarios

### Course Registration System
- **User Management**: Support for students, lecturers, and practitioners
- **Course Registration**: Automated enrollment with capacity checking
- **Notification System**: Multiple notification delivery methods
- **Access Control**: Role-based permissions for course creation
- **Waiting Lists**: Observer pattern for course availability alerts

---

## 🎨 Design Patterns Summary

| Pattern | System | Purpose | Implementation |
|---------|---------|---------|----------------|
| **Strategy** | Both | Algorithm selection at runtime | Flight search methods, Notification delivery |
| **Observer** | Both | Event notification system | Flight updates, Course availability |
| **Composite** | Flight | Hierarchical structure management | Company/Sub-company relationships |
| **Singleton** | Both | Single instance guarantee | Airport, RegisterSystem |
| **Flyweight** | Course | Memory-efficient object sharing | Course instance management |
| **Facade** | Course | Simplified interface | RegisterSystem operations |

---

## 🗂️ Project Structure

```
├── Ex1A/                          # Flight Management System
│   ├── FlightManegers/           # Manager classes
│   │   ├── FlightManager.java
│   │   ├── FlightObserverManager.java
│   │   └── SearchFlightManager.java
│   ├── FlightsExceptions/        # Custom exceptions
│   ├── PatternsInterfaces/       # Design pattern interfaces
│   ├── WorkerEnums/             # Enumerations
│   └── main.java                # Demo application
├── Ex1B/                          # Course Registration System
│   ├── courseBuilder/            # Core system classes
│   ├── Exceptions/               # Custom exceptions
│   └── Main.java                # Demo application
└── README.md                     # This file
```

---

## 🔧 Exception Handling

### Flight Management System
- `FlightNotExistsException` - Invalid flight operations
- `NotWorkingHereException` - Unauthorized crew assignments
- `NotCrewFlightException` - Invalid crew member types
- `InCorrectInputException` - Invalid user input

### Course Registration System  
- `IdTakenException` - Duplicate user registration
- `NotATeacherException` - Unauthorized course creation
- `NotLoggedInException` - Unauthenticated operations
- `SystemIsFullException` - System capacity exceeded
- `IncorrectPasswordException` - Authentication failure

---

## 🧪 Testing & Demonstration

Both systems include comprehensive main classes that demonstrate:
- Pattern implementation effectiveness
- Exception handling scenarios
- Real-world usage examples
- Edge case management

---

## 🎓 Learning Outcomes

This assignment demonstrates mastery of:
- **Design Patterns**: Practical implementation of 6+ patterns
- **OOP Principles**: Encapsulation, Inheritance, Polymorphism, Abstraction
- **Exception Handling**: Custom exception design and usage
- **Interface Design**: Clean separation of concerns
- **System Architecture**: Scalable and maintainable code structure

---

## 📝 Assignment Completion

- ✅ **Part A**: Flight Management System with 3 required patterns
- ✅ **Part B**: Course Registration System with 5 design patterns  
- ✅ **Part C**: Code analysis and debugging exercises
- ✅ **Documentation**: Comprehensive code comments and README
- ✅ **Exception Handling**: Robust error management throughout

---

## 🔗 Links

- **GitHub Repository**: [https://github.com/chanan-hash/OOP-Final-Assignment](https://github.com/chanan-hash/OOP-Final-Assignment)
- **Clone Command**: `git clone https://github.com/chanan-hash/OOP-Final-Assignment.git`

---

## 📧 Contact

**Student**: Chanan Helman  
**Course**: Introduction to Object-Oriented Programming  
---

*This project showcases advanced Object-Oriented Programming concepts through real-world system implementations, demonstrating both theoretical understanding and practical application of design patterns and software engineering principles.*
