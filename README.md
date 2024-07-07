## Hi developers! 👋

Hi I am Andrea a Full-Stack Developer ready to learn more every day and show my growing knowledge.

Tech Stack:
![Tech Stack](https://github.com/Andrea0o0/Andrea0o0/assets/116817220/0d5b54cd-78a6-4987-9371-019cd0cb66e4)


# 📑 Menu

- Projects ✨
  - FULLSTACK MERN: 
    - [Console.log(KATA) ⚡ - MODULE 3](#consolelogkata-) 
    - [COURSE4U 📖 - MODULE 2](#course4u-)
    - [GAME ZOMBIELAND 🧟‍ - MODULE 1](#zombieland-%EF%B8%8F)
  - JAVA + SPRING BOOT:
    - [TRAVEL AGENCY Be_travel 🧳​ ](#travel-agency-be_travel-)
    - [SHIFT-OPERATOR 👩🏻‍💻](#shift-operator-)
    - [EMPLOYEE MANAGEMENT 🤖](#employee-management-)

---
# Big proyects! 🫡 

## Console.log(KATA) ⚡

### 📜 Description

**Important concepts of the app:**

**Katas**: are unresolved javascript functions with pre-instructions to resolve them by returning what the instructions ask for

**Champions**: Games with users, to solve katas, where there is only one winner

This application is called Console.log(KATA) and it is an application to solve katas, such as function puzzles with instructions.

It's fully responsive in all the pages! 🙃


 ![Mobile](https://i.ibb.co/njSczzk/Console-log-KATA-Mobile.png)

https://user-images.githubusercontent.com/116817220/234442234-dd5e3361-d1f9-45bb-b5a6-579601fc9e4c.mp4



### Useful links 🔭

- [Presentation slides](https://slides.com/andrea_0o0_/console-log-kata/fullscreen)
- [Frontend repository](https://github.com/Andrea0o0/Console.log-Frontend)
- [Backend repository](https://github.com/Andrea0o0/Console.log-Backend)
- [Backend deploy](https://kataapp.fly.dev/)
- [Deployed app](https://console-log-kata.netlify.app/)



## COURSE4U 📖

### 📜 Description

**This project has been carried out in partnership with [Monica Camargo](https://github.com/MoniCamargo37)**

COURSE4u is a state-of-the-art online learning platform and it provides users with a comprehensive and dynamic learning experience, offering the ability to browse, explore (search), and subscribe as a premium member for courses, as well as add courses to their Account and leave reviews. Course4u also provides the admin interface that can create new courses, edit current ones, and delete them.

It's fully responsive in all the pages! 🙃


https://user-images.githubusercontent.com/116817220/234450405-f42d01f9-fec3-4211-b056-7031fc5a34b7.mp4

![Course4u Mobile](https://user-images.githubusercontent.com/116817220/234451459-4c6eec52-f2d0-4c3e-8b02-3b879e1a5242.png)



### Useful links 🔭

- [Shared Github Repo](https://github.com/Module-2-Project-COURSE4U/COURSE4U)
- [Github Repo](https://github.com/Andrea0o0/MODULE-2-PROJECT-COURSE4U)
- [Trello kanban](https://github.com/orgs/Module-2-Project-COURSE4U/projects/1/views/1?layout=board)
- [Deployed version](https://course4uu.fly.dev/courses)
- [Presentation slides](https://1drv.ms/p/s!Akm3TPUfj8PLhmOWcd6_o-DQ-JKr?e=zK0Nfy)



## ZOMBIELAND 🧟‍♀️ 

### 📜 Description

This is a game with two avatars to choose from, six worlds, and various opponents depending on the level.

It can be shot, the player has 10 lives and must survive 2 minutes to win.

**[The presentation explains in detail how the game works and the characters, enemies and worlds that exist](https://slides.com/andrea_0o0_/deck/fullscreen)**


![ZOMBIELAND](https://user-images.githubusercontent.com/116817220/234453891-c9da0005-d10b-4268-91e6-3f58e36e46c7.png)


### Useful links 🔭

- [Github Repo](https://github.com/Andrea0o0/Zombieland)
- [Presentation slides](https://slides.com/andrea_0o0_/deck/fullscreen)
- [Deployed game](https://andrea0o0.github.io/Zombieland/)


## TRAVEL AGENCY Be_travel 🧳​ 

### 📜 Description

The Be_travel project is a Spring Boot application designed to manage reservations, including flights and hotels, with public routes for reservation creation due to the absence of linked users. It meets strict requirements, such as unique room numbers, accurate hotel descriptions, non-overlapping booked dates, and accurate flight details. Integrated with the MySQL database, it ensures seamless data management and validation for comprehensive travel planning.

``` mermaid
classDiagram

class Hotel {
  + id: String
  + name: String
  + checkIn: String
+ checkOut: String
  + activeFlag: Boolean
  + description: String
  + rooms: List<Room>
}

class ReservedDate {
  + id: Long
+ date: LocalDate
+ room: Room
}

class HotelBooking {
    super: 
    - id: Long
    - activeFlag: Boolean
    ______________________
 + fromDate: LocalDate
+ untilDate: LocalDate
+ room: Room
+ peopleNumber: Integer
+ guests: List<Guest>
+ totalPrice: Double
}

class FlightBooking {
     super: 
    - id: Long
    - activeFlag: Boolean
    ______________________
  + origin: String
+ destination: String
+ bookingType: Boolean
+ flightOneWay: Flight
+ flightReturn: Flight
+ peopleNumber: Integer
+ seatType: String
+ infoPassengers: List<Passenger>
+ totalPrice: Double
}

class SeatFlight {
  + id: Long
+ rowSeat: Integer
+ columnSeat: Integer
+ seatString: String
+ price: Double
+ passengerOneWay: Passenger
+ passengerReturn: Passenger
+ flightId: Flight
}

class Passenger {
  + id: Long
+ name: String
+ lastName: String
+ identification: String
+ email: String
+ luggageList: List<Luggage>
+ luggagePrice: Double
+ seatFlightRowColumnOneWay: SeatFlight
+ seatFlightRowColumnReturn: SeatFlight
+ seatsPrice: Double
+ totalPrice: Double
+ flightBooking: FlightBooking
}

class Luggage {
  + id: Long
+ luggageType: String
+ description: String
+ invoiced: Boolean
+ model: Boolean
+ kg: Double
+ price: Double
+ passenger: Passenger
}

class Booking {
    - id: Long
    - activeFlag: Boolean
}

class Room {
    + id: Long
    + hotelName: String
    + place: String
    + roomNumber: String
    + roomType: Integer
    + roomTypeString: String
    + priceNight: Double
    + fromDate: LocalDate
    + untilDate: LocalDate
    + activeFlag: Boolean
    + reservedDates: List<ReservedDate>
    + description: String
    + bookings: List<HotelBooking>
    + hotel: Hotel
}

class Flight {
    + flightNumber: String
    + origin: String
    + destination: String
    + seatType: String
    + price: Double
    + takeoffDate: LocalDateTime
    + arrivalDate: LocalDateTime
    + rowsSeat: Integer
    + columnsSeat: Integer
    + seatPrice: Double
    + seatsNumber: Integer
    + reservedSeats: Integer
    + activeFlag: Boolean
    + oneWayBookings: List<FlightBooking>
    + returnBookings: List<FlightBooking>
    + seatsBooked: List<SeatFlight>
}

Booking <|-- HotelBooking: extends from Booking
Booking <|-- FlightBooking: extends from Booking

Hotel --|> Room: 1 to n
Room --|> Hotel: n to 1

Room --|> ReservedDate: 1 to n
ReservedDate --|> Room: n to 1

HotelBooking --|> Room: 1 to 1
Room --|> HotelBooking: 1 to n

FlightBooking --|> Flight: 1 to 1
Flight --|> FlightBooking: 1 to n

FlightBooking --|> SeatFlight: 1 to n
SeatFlight --|> FlightBooking: n to 1

Passenger --|> FlightBooking: 1 to n
FlightBooking --|> Passenger: n to 1

Luggage --|> Passenger: 1 to n
Passenger --|> Luggage: n to 1

```



### Useful links 🔭

- [Github Repo](https://github.com/Andrea0o0/Andrea0o0-Garcia-Gonzalez-Manchon-Andrea_pruebatec4)
- [Be_Travel Database MySql](https://github.com/Andrea0o0/Andrea0o0-Garcia-Gonzalez-Manchon-Andrea_pruebatec4/tree/main/sql)
- [PostMan](https://github.com/Andrea0o0/Andrea0o0-Garcia-Gonzalez-Manchon-Andrea_pruebatec4/tree/main/postman)


## SHIFT-OPERATOR 👩🏻‍💻

### 📜 Description

This Java-based shift management system efficiently handles shifts and procedures, ensuring strict input validation and MySQL integration. It offers comprehensive functions for shift management, procedure tracking, and user authentication, improving usability for citizens and administrators.

``` mermaid
classDiagram

class Person {
  -id: Long
  -username: String
  -password: String
}

class Citizen {
    super: 
    - id: Long
    - username: String
    - password: String
    ______________________
  + name: String
  + lastName:String
  + dateOfBirth: LocalDate
  + shifts: List<Shift>
  + getusername(): String
  + getpassword(): String
}

class Administrator {
      super: 
    - id: Long
    - username: String
    - password: String
    ______________________
  +procedures: List<ProcedureEntity>
}

class ProcedureEntity {
  -id: Long
  -title: String
  -description: String
  -requirements: String
  +admin: Administrator
  +shifts: List<Shift>
}

class Shift {
  -id: Long
  -dateHour: LocalDateTime
  -shiftStatus: boolean
  -additionalInformation: String
  +procedure: ProcedureEntity
  +citizen: Citizen
}

Person <|-- Citizen: extends from Person
Person <|-- Administrator: extends from Person
Administrator --|> ProcedureEntity: 1 to n
ProcedureEntity --|> Shift : 1 to n
ProcedureEntity --|> Administrator : 1 to 1
Shift --|> ProcedureEntity : 1 to 1
Shift --|> Citizen : 1 to 1
Citizen --|> Shift: 1 to n
```


### Useful links 🔭

- [Github Repo](https://github.com/Andrea0o0/Andrea0o0-Garcia-Gonzalez-Manchon-Andrea_pruebatec2)
- [Employee Database MySql](https://github.com/Andrea0o0/Andrea0o0-Garcia-Gonzalez-Manchon-Andrea_pruebatec2/tree/main/mysql)



## EMPLOYEE MANAGEMENT 🤖​ 

### 📜 Description

It is a Java-based system that facilitates employee management, offering CRUD functionality, input validation and an easy-to-use menu-driven interface. It ensures seamless integration with MySQL databases for efficient data manipulation and management.


```mermaid
mindmap
   id)MENU 
   Employee(
    1. Add employee(
        1 Add employee
        CREATE)
      First Name(First Name)
      Last Name(Last Name)
      Job Title(Job Title)
      Salary(Salary)
      Start Date (Start Date)
    2. List of all employees (2 List all Employees)
    3. Update employee information (
        3 Update employee
            EDIT)
      (Find employee By ID)
        (New Input 
        MODIFY)
            First Name(First Name)
            Last Name(Last Name)
            Job Title(Job Title)
            Salary(Salary)
            Start Date (Start Date)
    4. Search employee by Job title (
        4 Employee By JOB Title
        SEARCH)
        (Input Job Title)
            (MATCH)
            (CONTAINS)
            (NO COINCIDENCES)
    5. Search employee by Name (
        5 Employee by Name
        SEARCH)
            (Input Name)
                (MATCH)
                (CONTAINS)
                (NO COINCIDENCES)
    6. Search employee by Last Name (
        6 Employee by Last Name
        SEARCH)
            (Input Last Name)
                (MATCH)
                (CONTAINS)
                (NO COINCIDENCES)
      
    7. Delete employee (
        7 Delete employee)
            Input ID
                Delete employee by ID     
    8. Reset Base Data (8 Delete all employees)
      
    9. Exit (9 EXIT)
```


### Useful links 🔭

- [Github Repo](https://github.com/Andrea0o0/Garcia-Gonzalez-Manchon-Andrea_pruebatec1)
- [Javadoc](https://github.com/Andrea0o0/Garcia-Gonzalez-Manchon-Andrea_pruebatec1/tree/main/src/javadoc)
- [Employee Database MySql](https://github.com/Andrea0o0/Garcia-Gonzalez-Manchon-Andrea_pruebatec1/tree/main/src/mysqlEmployee)


<!--
**Andrea0o0/Andrea0o0** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on my profile
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
