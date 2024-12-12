# API Gateway Routes

## Recipe Service
| Path                  | Method | Request | Response          | ResponseCodes | Description        |
| --------------------- | ------ | ------- | ----------------- | ------------- | ------------------ |
| "/gateway/categories" | GET    | NONE    | IResult, Recipe[] | 200, 404      | Get all categories |
|"/gateway/categories"|POST|Category|IResult|200, 400|Add category|

## Recipe Service - Categories
| Path                  | Method | Request | Response          | ResponseCodes | Description        |
| --------------------- | ------ | ------- | ----------------- | ------------- | ------------------ |
| "/gateway/recipes"    | GET    | NONE    | IResult, Recipe[] | 200, 404      | Get all recipes    |
