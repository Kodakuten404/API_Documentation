# User Service

## User Endpoints

| **Path**                  | **Method** | **Request**                     | **Response** | **ResponseCodes** | **Description**           |
| ------------------------- | ---------- | ------------------------------- | ------------ | ----------------- | ------------------------- |
| "/users/"                 | GET        | NONE                            | User[]       | 200               | Get all users             |
| "/users/Id/{userId}"      | GET        | Guid userId                     | User         | 200, 404          | Get user by id            |
| "/users/email/{email}"    | GET        | string Email                    | User         | 200, 404          | Get user by email         |
| "/users/"                 | POST       | User                            | NONE         | 201, 400          | Add new user              |
| "/users/{userId}"         | DELETE     | Guid userId                     | NONE         | 200, 404          | Delete user               |
| "/users/favorite/{userId}"| POST       | Guid userId, Guid[] favoritesId | NONE         | 200, 400          | Add favorites to user     |
| "/users/favorite/{userId}"| GET        | Guid userId                     | Guid[]       | 200, 400          | Get favorites from user   |

### Comments
favorites handled in string form and GET method breaks down string and Guid.parses it and returns a GUID[]