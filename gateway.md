# API Gateway Routes

## Recipe Service - Categories

| Path                  | Method | Request  | Response          | ResponseCodes | Description        |
| --------------------- | ------ | -------- | ----------------- | ------------- | ------------------ |
| "/gateway/categories" | POST   | Category | IResult           | 201, 400      | Add category       |
| "/gateway/categories" | GET    | NONE     | IResult, Recipe[] | 200, 404      | Get all categories |

## Recipe Service

| Path                         | Method | Request                          | Response          | ResponseCodes | Description                      |
| ---------------------------- | ------ | -------------------------------- | ----------------- | ------------- | -------------------------------- |
| "/gateway/recipes"           | POST   | Recipe                           | IResult           | 201, 400      | Add recipe                       |
| "/gateway/recipes"           | GET    | NONE                             | IResult, Recipe[] | 200, 404      | Get all recipes                  |
| "/gateway/name/{recipeName}" | GET    | string recipeName                | IResult, Recipe   | 200, 404      | Get recipe by name               |
| "/gateway/ingredients/"      | GET    | NONE                             | IResult, Recipe[] | 200, 404      | Get all recipes with ingredients |
| "/gateway/review/{recipeId}" | PUT    | string recipeId, string reviewId | IResult           | 200, 404      | Add review to recipe             |
| "/gateway/tag/{recipeId}"    | PUT    | string recipeId, string tagName  | IResult           | 200, 404      | Add tag to recipe                |

# Review Service

| **Path**                         | **Method** | **Request**                                 | **Response** | **ResponseCodes** | **Description**                           |
| -------------------------------- | ---------- | ------------------------------------------- | ------------ | ----------------- | ----------------------------------------- |
| "/gateway/reviews/"                      | GET        | NONE                                        | Review[]     | 200               | Get all reviews                           |
| "/gateway/reviews/{reviewId}"            | GET        | Guid reviewId                               | Review       | 200, 404          | Get review by id                          |
| "/gateway/reviews/recipe/{recipeId}"     | GET        | Guid recipeId                               | Review[]     | 200, 404          | Get reviews by recipe id                  |
| "/gateway/reviews/author/{authorId}"     | GET        | Guid authorId                               | Review[]     | 200, 404          | Get reviews by author id                  |
| "/gateway/reviews/{authorId}/{recipeId}" | POST       | ReviewDTO, authorId, recipeId               | NONE         | 201, 400          | Add new review                            |
| "/gateway/reviews/{reviewId}"            | DELETE     | Guid reviewId                               | NONE         | 200, 404          | Delete review                             |

## Notification Service

| **Path**                      | **Method** | **Request**  | **Response**    | **ResponseCodes** | **Description**           |
| ----------------------------- | ---------- | ------------ | --------------- | ----------------- | ------------------------- |
| "gateway/notifications/subscribe/{user}" | POST       | SubscriberDto subscriber  | NONE            | 200, 404          | Subscribe user            |
| "gateway/notifications/unsubscribe/{userId}"      | DELETE     | Guid userId  | NONE            | 200, 400          | Unsubscribe user          |
| "gateway/notifications/notify/{notification}"       | POST       | NotificationDto notification| NONE            | 200, 400          | Notify subscribers        |
| "gateway/notifications/logs"              | GET        | NONE         | NotificationLog[] | 200, 404               | Get all notification logs |


## User Service

| **Path**                      | **Method** | **Request**  | **Response**    | **ResponseCodes** | **Description**                               |
| ---------------------------- | ------ | -------------------------------- | ----------------- | ------------- | -------------------------------- |
| "/gateway/user"              | POST   | UserDto                          | IResult           | 201, 400      | Add User                         |
| "/gateway/user"              | GET    | NONE                             | IResult, user[]   | 200, 404      | Get all users                    |
| "/gateway/user"              | DELETE | Guid userId                      | IResult           | 200, 404      | Delete user                      |
| "/gateway/users/Id/{userId}" | GET    | Guid userId                      | IResult, user     | 200, 404      | Get user by id                   |
| "/gateway/users/Email/{email}| GET    | string email                     | IResult, user     | 200, 404      | Get user by email                |
| "/gateway/users/token/getToken"| POST | Guid userid                      | IResult, token    | 201, 404      | Add token to user                |
| "/gateway/users/token/validate/{userId}"| POST | Guid userId, string accessCode | IResult, bool | 200, 401      | Validate user token           |
| "/gateway/users/favorite/{userId}"| GET | Guid userId                    | IResult, Guid[]    | 200, 404      | Get favorites from user          |
| "/gateway/users/favorite/{userId}""| POST | Guid userid, Guid favoriteId | IResult           | 201, 404      | Add favorite to user             |


