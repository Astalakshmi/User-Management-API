# User API Automation Testing

This repository contains automated test cases for the **User Management API**, which performs user CRUD operations: Create, Read, Update, and Delete. The tests ensure the API works as expected and adheres to business rules and schema validation.

---

##  Project Overview

The **User API** allows clients to manage user data through a RESTful interface. This test automation suite verifies the correctness of all API functionalities using real-time test data, schema validation, and various test cases.

---

##  Features Covered

- Create a new user (POST)
- Get user by ID (GET)
- Update full user data (PUT)
- Update partial user data (PATCH)
- Delete a user (DELETE)
- Status code validation
- Response body and message validation
- JSON schema validation
- Data-driven testing using CSV
- Bug report documentation 

---

## Tech Stack

- **Postman** – For creating and managing API requests.
- **Newman** – Command-line tool for running Postman collections.
- **CSV/Excel** – For data-driven test inputs.
- **JavaScript** – For scripting pre-request and test scripts inside Postman.
- **GitHub** – For version control and collaboration.

---

##  API Endpoints

| Method | Endpoint                                  | Description               |
|--------|-------------------------------------------|---------------------------|
| POST   | `/uap/createusers`                        | Create a new user         |
| GET    | `/uap/users`                              | Get user details          |
| GET    | `/uap/user/{id}`                          | Get userID details        |
| GET    | `/uap/users/username/{userFirstName}`     | Get userFirstName details |
| PUT    | `/user/updateUser/{userId}`               | Full update of user       |
| PATCH  | `/uap/updateuserfields/{userId}`          | Partial update of user    |
| DELETE | `​/uap​/deleteuser​/username​/{userFirstName}`| Delete a userFirstName    |
| DELETE | `/uap/deleteuser/{userId}`                | Delete a userID           |



##  How to Run the Tests

###  Using Postman GUI

1. Import the collection and environment files.
2. Update the `baseUrl` and authorization variables.
3. Open Collection Runner.
4. Upload the CSV test file.
5. Run the collection.

###  Using Newman CLI

newman run UserAPI.postman_collection.json \
  -e UserAPI.environment.json \
  -d testdata/userData.csv \
  -r htmlextra

##  Author

**Astalakshmi Amulraj** – QA Automation Engineer  
[GitHub](https://github.com/Astalakshmi) • [LinkedIn](https://www.linkedin.com/in/astaamul)

