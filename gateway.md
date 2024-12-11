# API Gateway Routes

## Recipes

| Path               | Method | Request | Response          | ResponseCodes | Description     |
| ------------------ | ------ | ------- | ----------------- | ------------- | --------------- |
| "/gateway/recipes" | GET    | NONE    | IResult, Recipe[] | 200, 404      | Get all recipes |
| "/gateway/recipes" | POST   | Recipe  | IResult           | 200, 404      | Add recipe      |

## Categories

| Path                  | Method | Request  | Response          | ResponseCodes | Description        |
| --------------------- | ------ | -------- | ----------------- | ------------- | ------------------ |
| "/gateway/categories" | GET    | NONE     | IResult, Recipe[] | 200, 404      | Get all categories |
| "/gateway/categories" | POST   | Category | IResult           | 200, 404      | Add category       |

## Reviews

| Path               | Method | Request | Response | ResponseCodes | Description     |
| ------------------ | ------ | ------- | -------- | ------------- | --------------- |
| "/gateway/reviews" | GET    | NONE    | Review[] | 200, 404      | Get all reviews |
| "/gateway/reviews" | POST   | Review  | IResult  | 200, 404      | Add review      |

## Notifications

| Path | Method | Request | Response | ResponseCodes | Description |
| ---- | ------ | ------- | -------- | ------------- | ----------- |
|      |        |         |          |               |             |

## Users

| Path             | Method | Request | Response | ResponseCodes | Description   |
| ---------------- | ------ | ------- | -------- | ------------- | ------------- |
| "/gateway/users" | GET    | NONE    | User[]   | 200, 404      | Get all users |
| "/gateway/users" | POST   | User    | IResult  | 200, 404      | Add user      |
