# User Service
| **Path**                | **Method** | **Request** | **Response** | **ResponseCodes** | **Description** |
| ----------------------- | ------ | --------------- | -------- | ------------- | ---------------------- |
| "/users/"              | GET    | NONE                    | User[]   | 200           | Get all users     |
| "/users/{userId}"      | GET    | int userId              | User     | 200, 404      | Get user by id    |
| "/users/email/{email}" | GET    | string Email            | User     | 200, 404      | Get user by email |
| "/users/role/{role}"   | GET    | string Role             | User[]   | 200, 404      | Get users by role |
| "/users/"              | POST   | User                    | NONE     | 200, 400      | Add new user      |
| "/users/{userId}"      | PUT    | int User                 | NONE     | 200, 404      | Update user info  |
| "/users/{userId}"      | DELETE | int userId              | NONE     | 200, 404      | Delete user       |
