# Recipe Service

## Ingredient Endpoints

| **Path**                             | **Method** | **Request**           | **Response**          | **ResponseCodes** | **Description**     |
| ------------------------------------ | ---------- | --------------------- | --------------------- | ----------------- | ------------------- |
| "/ingredients/"                      | GET        | NONE                  | IResult, Ingredient[] | 201               | Get all ingredients |
| "/ingredients/{ingredientId}"        | GET        | Guid ingredientId     | IResult, Ingredient   | 200, 404          | Get by id           |
| "/ingredients/name/{ingredientName}" | GET        | string ingredientName | IResult, Ingredient   | 200, 404          | Get by name         |
| "/ingredients/"                      | POST       | Ingredient            | IResult               | 200, 400          | Add ingredient      |
| "/ingredients/{ingredientId}"        | DELETE     | Guid ingredientId     | IResult               | 200, 404          | Delete ingredient   |

## Category Endpoints

| **Path**                          | **Method** | **Request**         | **Response**        | **ResponseCodes** | **Description**    |
| --------------------------------- | ---------- | ------------------- | ------------------- | ----------------- | ------------------ |
| "/categories/"                    | GET        | NONE                | IResult, Category[] | 201               | Get all categories |
| "/categories/{categoryId}"        | GET        | Guid categoryId     | IResult, Category   | 200, 404          | Get by id          |
| "/categories/name/{categoryName}" | GET        | string categoryName | IResult, Category   | 200, 404          | Get by name        |
| "/categories/"                    | POST       | Category            | IResult             | 200, 400          | Add category       |
| "/categories/{categoryId}"        | DELETE     | Guid categoryId     | IResult             | 200, 404          | Delete category    |

## Recipe Endpoints

| **Path**                     | **Method** | **Request**       | **Response**      | **ResponseCodes** | **Description**             |
| ---------------------------- | ---------- | ----------------- | ----------------- | ----------------- | --------------------------- |
| "/recipes/"                  | GET        | NONE              | IResult, Recipe[] | 201               | Get all recipes             |
| "/recipes/{recipeId}"        | GET        | Guid recipeId     | IResult, Recipe   | 200, 404          | Get by id                   |
| "/recipes/name/{recipeName}" | GET        | string recipeName | IResult, Recipe   | 200, 404          | Get by name                 |
| "/recipes/ingredients/{id}"  | GET        | string id         | IResult, Recipe   | 200, 404          | Get recipe with ingredients |
| "/recipes/"                  | POST       | Recipe            | IResult           | 200, 400          | Add recipe                  |
| "/recipes/{recipeId}"        | DELETE     | Guid recipeId     | IResult           | 200, 404          | Delete recipe               |
