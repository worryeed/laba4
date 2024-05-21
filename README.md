# 1. Бронирование номера в отеле  
```mermaid
classDiagram
    Customer --|> Reservation
    Reservation --|> Room
    Reservation --|> Payment
    Room --|> Hotel

    class Customer {
        +String name
        +String email
        +makeReservation()
        +cancelReservation()
    }
    
    class Reservation {
        +int reservationId
        +Date checkInDate
        +Date checkOutDate
        +confirmReservation()
        +cancelReservation()
    }

    class Room {
        +int roomId
        +String roomType
        +double price
        +checkAvailability()
    }

    class Payment {
        +int paymentId
        +String paymentType
        +double amount
        +processPayment()
    }

    class Hotel {
        +String name
        +String address
        +List<Room> rooms
        +getAvailableRooms()
    }
```

# 2. Оптовая закупка овощей из фермы на склад магазина
```mermaid
classDiagram
    Farm --|> Vegetable
    StoreWarehouse --|> Vegetable
    StoreWarehouse --|> Order
    Order --|> Payment

    class Farm {
        +String name
        +String location
        +List<Vegetable> availableVegetables
        +sendOrder(Order order)
    }

    class Vegetable {
        +String name
        +double pricePerKg
        +int quantity
    }

    class StoreWarehouse {
        +String address
        +List<Vegetable> stock
        +placeOrder(Order order)
        +receiveOrder(Order order)
    }

    class Order {
        +int orderId
        +Date orderDate
        +List<Vegetable> orderedVegetables
        +processOrder()
    }

    class Payment {
        +int paymentId
        +String paymentType
        +double amount
        +processPayment()
    }
```

# 3. Прохождение онлайн-курсов по программированию
```mermaid
classDiagram
    Student --|> Course
    Course --|> Lesson
    Course --|> Assignment
    Course --|> Certification
    Student --|> Payment

    class Student {
        +String name
        +String email
        +registerCourse(Course course)
        +completeCourse(Course course)
    }

    class Course {
        +String courseId
        +String courseName
        +String description
        +List<Lesson> lessons
        +List<Assignment> assignments
        +Certification certification
        +enrollStudent(Student student)
    }

    class Lesson {
        +String lessonId
        +String title
        +String content
        +completeLesson()
    }

    class Assignment {
        +String assignmentId
        +String title
        +String description
        +submitAssignment()
    }

    class Certification {
        +String certificationId
        +String certificationName
        +issueCertificate(Student student)
    }

    class Payment {
        +int paymentId
        +String paymentType
        +double amount
        +processPayment()
    }
```

# 4. Запись к врачу через мобильное приложение
```mermaid
classDiagram
    Patient --|> Appointment
    Appointment --|> Doctor
    Patient --|> Payment

    class Patient {
        +String name
        +String phoneNumber
        +String email
        +bookAppointment(Doctor doctor)
        +cancelAppointment(Appointment appointment)
    }

    class Appointment {
        +int appointmentId
        +Date appointmentDate
        +String reason
        +confirmAppointment()
        +cancelAppointment()
    }

    class Doctor {
        +String doctorId
        +String name
        +String specialization
        +List<Appointment> appointments
        +addAppointment(Appointment appointment)
        +removeAppointment(Appointment appointment)
    }

    class Payment {
        +int paymentId
        +String paymentType
        +double amount
        +processPayment()
    }
```

# 5. Оптовая закупка компьютеров в университет
```mermaid
classDiagram
    Supplier --|> Computer
    UniversityWarehouse --|> Computer
    UniversityWarehouse --|> PurchaseOrder
    PurchaseOrder --|> Payment

    class Supplier {
        +String name
        +String location
        +List<Computer> availableComputers
        +sendOrder(PurchaseOrder order)
    }

    class Computer {
        +String brand
        +String model
        +double price
        +int quantity
    }

    class UniversityWarehouse {
        +String address
        +List<Computer> stock
        +placeOrder(PurchaseOrder order)
        +receiveOrder(PurchaseOrder order)
    }

    class PurchaseOrder {
        +int orderId
        +Date orderDate
        +List<Computer> orderedComputers
        +processOrder()
    }

    class Payment {
        +int paymentId
        +String paymentType
        +double amount
        +processPayment()
    }
```
