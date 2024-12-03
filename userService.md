# User Service

| **Path**               | **Method** | **Request**                  | **Response** | **ResponseCodes** | **Description**           |
| ---------------------- | ---------- | ---------------------------- | ------------ | ----------------- | ------------------------- |
| "/users/"              | GET        | NONE                         | User[]       | 200               | Get all users             |
| "/users/{userId}"      | GET        | Guid userId                  | User         | 200, 404          | Get user by id            |
| "/users/email/{email}" | GET        | string Email                 | User         | 200, 404          | Get user by email         |
| "/users/"              | POST       | User                         | NONE         | 200, 400          | Add new user              |
| "/users/"              | PATCH      | Guid userId, Guid favoriteId | NONE         | 200, 400          | Update user with favorite |
| "/users/{userId}"      | DELETE     | Guid userId                  | NONE         | 200, 404          | Delete user               |

### Comments
