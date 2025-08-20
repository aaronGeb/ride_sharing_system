# Ride Sharing System
A simplified ride-sharing system built with Python using Object-Oriented Programming principles.  
This project demonstrates the use of classes, inheritance, polymorphism, encapsulation, and clean architecture.  
```mermaid
classDiagram
    class User {
        - user_id
        - name
        - email
        - ride_history
        + request_ride()
        + add_ride()
    }

    class Driver {
        - driver_id
        - name
        - vehicle
        - is_available
        + accept_ride()
    }

    class Vehicle {
        - vehicle_type
        - base_fare
        + calculate_fare()
    }

    class Car {
        base_fare = 15
    }

    class Bike {
        base_fare = 8
    }

    class Ride {
        - ride_id
        - user
        - driver
        - origin
        - destination
        - vehicle_type
        - status
        - fare
        - start_time
        - end_time
        + assign_driver()
        + start_ride()
        + end_ride()
    }

    %% Relationships
    User --> Ride : 
    Ride --> Driver : 
    Driver --> Vehicle : 
    Vehicle <|-- Car
    Vehicle <|-- Bike
```
## Features

- User registration and ride requests  
- Driver registration and ride acceptance  
- Vehicle types with different fare calculation (Car, Bike, etc.)  
- Ride lifecycle: Requested → Accepted → Ongoing → Completed  
- Ride history for users  
- Extendable to include payments, ratings, and admin dashboards  

## Tech Stack

- **Python 3.9+**  
- Object-Oriented Programming (OOP) principles  
- JSON for data persistence (can be extended to databases)  
- Unit tests with `unittest` 
  
## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/aarongeb/ride_sharing_system.git
cd ride_sharing_system
```
### 2. Run the Project
```bash
python main.py
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.