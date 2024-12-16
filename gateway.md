# API Gateway Routes

## Recipe Service - Categories

| Path                  | Method | Request  | Response          | ResponseCodes | Description        |
| --------------------- | ------ | -------- | ----------------- | ------------- | ------------------ |
| "/gateway/categories" | POST   | Category | IResult           | 200, 400      | Add category       |
| "/gateway/categories" | GET    | NONE     | IResult, Recipe[] | 200, 404      | Get all categories |

## Recipe Service

| Path                         | Method | Request                          | Response          | ResponseCodes | Description                      |
| ---------------------------- | ------ | -------------------------------- | ----------------- | ------------- | -------------------------------- |
| "/gateway/recipes"           | POST   | Recipe                           | IResult           | 200, 400      | Add recipe                       |
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
| "/gateway/reviews/{authorId}/{recipeId}" | POST       | Review                                      | NONE         | 200, 400          | Add new review                            |
| "/gateway/reviews/{reviewId}"            | DELETE     | Guid reviewId                               | NONE         | 200, 404          | Delete review                             |

## Notification Service

| **Path**                      | **Method** | **Request**  | **Response**    | **ResponseCodes** | **Description**           |
| ----------------------------- | ---------- | ------------ | --------------- | ----------------- | ------------------------- |
| "gateway/notifications/subscribe/{user}" | POST       | Subscriber user  | NONE            | 200, 404          | Subscribe user            |
| "gateway/notifications/unsubscribe/{userId}"      | DELETE     | Guid userId  | NONE            | 200, 400          | Unsubscribe user          |
| "gateway/notifications/notify/{notification}"       | POST       | Notification | NONE            | 200, 400          | Notify subscribers        |
| "gateway/notifications/logs"              | GET        | NONE         | NotificationLog[] | 200               | Get all notification logs |
