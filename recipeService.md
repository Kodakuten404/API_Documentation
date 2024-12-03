# Recipe Service

## Ingredient Endpoints

| **Path**                             | **Method** | **Request**           | **Response** | **ResponseCodes** | **Description**     |
| ------------------------------------ | ---------- | --------------------- | ------------ | ----------------- | ------------------- |
| "/ingredients/"                      | GET        | NONE                  | Ingredient[] | 200               | Get all ingredients |
| "/ingredients/{ingredientId}"        | GET        | Guid ingredientId     | Ingredient   | 200, 400          | Get by id           |
| "/ingredients/name/{ingredientName}" | GET        | string ingredientName | Ingredient   | 200, 400          | Get by name         |
| "/ingredients/"                      | POST       | Ingredient            | NONE         | 200, 404          | Add ingredient      |
| "/ingredients/{ingredientId}"        | DELETE     | Guid ingredientId     | NONE         | 200, 404          | Delete ingredient   |

## Category Endpoints

| **Path**                          | **Method** | **Request**         | **Response** | **ResponseCodes** | **Description**    |
| --------------------------------- | ---------- | ------------------- | ------------ | ----------------- | ------------------ |
| "/categories/"                    | GET        | NONE                | Category[]   | 200               | Get all categories |
| "/categories/{categoryId}"        | GET        | Guid categoryId     | Category     | 200, 400          | Get by id          |
| "/categories/name/{categoryName}" | GET        | string categoryName | Category     | 200, 400          | Get by name        |
| "/categories/"                    | POST       | Category            | NONE         | 200, 404          | Add category       |
| "/categories/{categoryId}"        | DELETE     | Guid categoryId     | NONE         | 200, 404          | Delete category    |

## Recipe Endpoints

| **Path**                     | **Method** | **Request**       | **Response** | **ResponseCodes** | **Description** |
| ---------------------------- | ---------- | ----------------- | ------------ | ----------------- | --------------- |
| "/recipes/"                  | GET        | NONE              | Recipe[]     | 200               | Get all recipes |
| "/recipes/{recipeId}"        | GET        | Guid recipeId     | Recipe       | 200, 400          | Get by id       |
| "/recipes/name/{recipeName}" | GET        | string recipeName | Recipe       | 200, 400          | Get by name     |
| "/recipes/"                  | POST       | Recipe            | NONE         | 200, 404          | Add recipe      |
| "/recipes/{recipeId}"        | DELETE     | Guid recipeId     | NONE         | 200, 404          | Delete recipe   |
