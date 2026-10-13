# Student REST API

## About the Project
This is a simple REST API developed using Java and Spring Boot to manage student details. It allows users to add, view, update, and delete student records using HTTP requests.

## Technologies Used
- Java
- Spring Boot
- REST API
- Maven
- Postman for API testing

## Student Details
Each student contains the following information:
- **Name:** Student's name
- **ID:** Student's unique ID
- **Course:** Student's course name

## API Endpoints

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/api/students` | Get all students |
| POST | `/api/students` | Add a new student |
| GET | `/api/students/{id}` | Get a student by ID |
| PUT | `/api/students/{id}` | Update a student's details |
| DELETE | `/api/students/{id}` | Delete a student by ID |

## Example JSON

Use the following JSON body to add a student:

```json
{
  "name": "Rahul",
  "id": 101,
  "course": "AIML"
}
```

## How to Run the Project
1. Open the project in IntelliJ IDEA, Eclipse, or another Java IDE.
2. Make sure Java and Maven are installed or configured.
3. Run the `RestApiApplication.java` file.
4. The Spring Boot application will start on the default port `8080`, unless configured differently.
5. Open Postman and test the API endpoints.

## Example Requests

**1. Get all students**
```http
GET http://localhost:8080/api/students
```

**2. Add a student**
```http
POST http://localhost:8080/api/students
```

Select **Body → raw → JSON** in Postman and enter the example JSON above.

**3. Get a student by ID**
```http
GET http://localhost:8080/api/students/101
```

**4. Update a student**
```http
PUT http://localhost:8080/api/students/101
```

Request body:
```json
{
  "name": "Rahul Sharma",
  "id": 101,
  "course": "Computer Science"
}
```

**5. Delete a student**
```http
DELETE http://localhost:8080/api/students/101
```

## Important Note
Currently, student records are stored in an `ArrayList`, so the data is temporary. All student records are lost when the application restarts. The API does not use a database.

## Future Improvements
- Connect the API to a database such as MySQL.
- Add input validation.
- Return appropriate HTTP status codes.
- Handle cases where a student does not exist.
