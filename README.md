# FamilyCashCard 💳

Welcome to the **FamilyCashCard** project! This is a RESTful web service built as part of the **Spring Academy Beginner** course. The application acts as a digital "cash card" system, allowing family members to manage and track allowances or funds safely and efficiently.

The primary focus of this project was learning the fundamentals of **Spring Boot**, implementing **REST APIs**, and mastering **Test-Driven Development (TDD)** using Spring's robust testing suite.

---

## 🚀 Features & Concepts Implemented

* **RESTful Architecture:** Designed and implemented standard HTTP methods (`GET`, `POST`, `PUT`, `DELETE`) for managing Cash Card resources.
* **Test-Driven Development (TDD):** Built using a strict TDD workflow, writing failing tests first before implementing the core business logic.
* **Spring Data JDBC:** Managed database interactions, object-relational mapping, and automated CrudRepositories.
* **Spring Security (Basic):** Implemented foundational authentication and authorization, ensuring users can only access and manage *their own* cash cards.
* **Pagination & Sorting:** Optimized data retrieval for `GET` requests to handle large sets of cash cards gracefully.

---

## 🛠️ Tech Stack

* **Framework:** Spring Boot
* **Language:** Java
* **Data Access:** Spring Data JDBC
* **Database:** H2 (In-Memory Database for development and testing)
* **Testing:** JUnit 5, AssertJ, Spring Boot Test (`TestRestTemplate`)
* **Build Tool:** Gradle

---

## 🛣️ API Endpoints

| Method | Endpoint | Description | Auth Required |
| :--- | :--- | :--- | :--- |
| **GET** | `/cashcards` | Retrieve a paginated, sorted list of owned cash cards | Yes |
| **GET** | `/cashcards/{id}` | Retrieve a specific cash card by ID | Yes |
| **POST** | `/cashcards` | Create a new cash card | Yes |
| **PUT** | `/cashcards/{id}` | Update an existing cash card's balance | Yes |
| **DELETE** | `/cashcards/{id}` | Delete a specific cash card | Yes |

### Example Request/Response Payload (`GET /cashcards/99`)

**Response (`200 OK`):**
```json
{
  "id": 99,
  "amount": 123.45,
  "owner": "sarah"
}
```
---

## 🧪 Testing Approach

A major milestone of this project was practicing **Red-Green-Refactor** cycles. The test suite includes:

* **Integration Tests:** Testing the entire slice of the application from the HTTP request down to the H2 database using `@SpringBootTest`.
* **Contract/JSON Testing:** Utilizing `@JsonTest` to ensure that Java objects serialize and deserialize correctly into the expected JSON formats.

### Running the Tests

To run the test suite and ensure everything passes, execute the following command in your terminal:

```bash
# Run tests:
./gradlew test

```

---

## 🏁 Getting Started

### Prerequisites

* Java 17 or higher
* An IDE (IntelliJ IDEA, VS Code, Eclipse)

```bash
# Build the project:
./gradlew build
```

---

## 🎓 Acknowledgments

* This project was built following the official curriculum on **Spring Academy**.
* Shout out to the Spring team for the excellent guide on getting started with Spring Boot, TDD, and Security!
