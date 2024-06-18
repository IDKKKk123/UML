# UML - Заказ шкафа в квартиру с необходимостью вызова замерщика:
```mermaid
classDiagram
class FurnitureStore {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Wardrobe {
  +String Model
  +String Description
  +Decimal Price
}

class Measurer {
  +String Name
  +String Phone
  +String Address
}

class Customer {
  +String Name
  +String Phone
  +String Address
}

class Order {
  +Int ID
  +Customer Customer
  +Wardrobe Wardrobe
  +Measurer Measurer
  +String PaymentMethod
  +String Statuses
  +DateTime Date/Time
  +String DeliveryAddress
}

class OrderItem {
  +Int ID
  +Wardrobe Wardrobe
  +Int Quantity
}

OrderItem .. Wardrobe
Order .. Customer
Order ..> OrderItem
FurnitureStore <|-- Wardrobe
Customer <|-- Order
Order <|-- OrderItem
Measurer <|-- Order
```
# UML - Покупка тура в турагенстве:
```mermaid
classDiagram
class TravelAgency {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Tour {
  +String Destination
  +DateTime DepartureDate
  +DateTime ReturnDate
  +Decimal Price
  +String Description
  +String ImageUrl
}

class Customer {
  +String Name
  +String Phone
  +String Address
}

class Booking {
  +Int ID
  +Customer Customer
  +Tour Tour
  +String PaymentMethod
  +String Status
  +DateTime BookingDate
}

class TourOption {
  +Int ID
  +Tour Tour
  +String OptionName
  +Decimal OptionPrice
}

TourOption .. Tour
Booking .. Customer
Booking ..> TourOption
TravelAgency <|-- Tour
Customer <|-- Booking
Booking <|-- TourOption
```
# UML - Заказ шкафа в квартиру с необходимостью вызова замерщика:
```mermaid
classDiagram
class FurnitureStore {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Wardrobe {
  +String Model
  +String Description
  +Decimal Price
}

class Measurer {
  +String Name
  +String Phone
  +String Address
}

class Customer {
  +String Name
  +String Phone
  +String Address
}

class Order {
  +Int ID
  +Customer Customer
  +Wardrobe Wardrobe
  +Measurer Measurer
  +String PaymentMethod
  +String Statuses
  +DateTime Date/Time
  +String DeliveryAddress
}

class OrderItem {
  +Int ID
  +Wardrobe Wardrobe
  +Int Quantity
}

OrderItem .. Wardrobe
Order .. Customer
Order ..> OrderItem
FurnitureStore <|-- Wardrobe
Customer <|-- Order
Order <|-- OrderItem
Measurer <|-- Order
```
# UML - Прохождение онлай-курсов по программированию:
```mermaid
classDiagram
class Course {
  +String Name
  +String Description
  +Decimal Price
  +String Level
  +String Language
}

class Student {
  +String Name
  +String Email
  +String Address
}

class Enrollment {
  +Int ID
  +Student Student
  +Course Course
  +String PaymentMethod
  +String Statuses
  +DateTime Date/Time
}

class CourseProgress {
  +Int ID
  +Enrollment Enrollment
  +Int ProgressPercentage
  +DateTime LastAccessed
}

CourseProgress .. Enrollment
Enrollment .. Student
Enrollment ..> CourseProgress
Course <|-- Enrollment
Student <|-- Enrollment
Enrollment <|-- CourseProgress
```
# UML - Заказ такси через мобильое приложение:
```mermaid
classDiagram
class TaxiCompany {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Driver {
  +String Name
  +String Phone
  +String CarModel
  +String CarNumber
}

class Customer {
  +String Name
  +String Phone
  +String Address
}

class Ride {
  +Int ID
  +Customer Customer
  +Driver Driver
  +String PickupLocation
  +String DropoffLocation
  +Decimal Fare
  +String PaymentMethod
  +String Status
  +DateTime RequestTime
  +DateTime PickupTime
  +DateTime DropoffTime
}

class CarType {
  +String Type
  +Decimal BaseFare
  +Decimal PerKmFare
}

Driver <|-- CarType
TaxiCompany <|-- Driver
Customer <|-- Ride
Ride ..> Driver
```
