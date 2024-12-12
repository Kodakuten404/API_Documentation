# Recipe Service

## Category Endpoints

| **Path**                          | **Method** | **Request**          | **Response**        | **ResponseCodes** | **Description**    |
| --------------------------------- | ---------- | -------------------- | ------------------- | ----------------- | ------------------ |
| "/categories/"                    | GET        | NONE                 | IResult, Category[] | 201               | Get all categories |
| "/categories/{categoryId}"        | GET        | string categoryId    | IResult, Category   | 200, 404          | Get by id          |
| "/categories/name/{categoryName}" | GET        | string categoryName  | IResult, Category   | 200, 404          | Get by name        |
| "/categories/"                    | POST       | CreateCategoryTagDto | IResult             | 200, 400          | Add category       |
| "/categories/{categoryId}"        | DELETE     | string categoryId    | IResult             | 200, 404          | Delete category    |

## Recipe Endpoints

| **Path**                          | **Method** | **Request**                      | **Response**      | **ResponseCodes** | **Description**                  |
| --------------------------------- | ---------- | -------------------------------- | ----------------- | ----------------- | -------------------------------- |
| "/recipes/"                       | GET        | NONE                             | IResult, Recipe[] | 201               | Get all recipes                  |
| "/recipes/{recipeId}"             | GET        | string recipeId                  | IResult, Recipe   | 200, 404          | Get by id                        |
| "/recipes/name/{recipeName}"      | GET        | string recipeName                | IResult, Recipe   | 200, 404          | Get by name                      |
| "/recipes/ingredients/{recipeId}" | GET        | string recipeId                  | IResult, Recipe   | 200, 404          | Get recipe with ingredients      |
| "/recipes/ingredients/"           | GET        | NONE                             | IResult, Recipe[] | 200, 404          | Get all recipes with ingredients |
| "/recipes/"                       | POST       | CreateRecipeDto                  | IResult           | 200, 400          | Add recipe                       |
| "/recipes/review/{recipeId}"      | PUT        | string recipeId, string reviewId | IResult           | 200, 404          | Add review to recipe             |
| "/recipes/tag/{recipeId}"         | PUT        | string recipeId, string tagName  | IResult           | 200, 404          | Add tag to recipe                |
| "/recipes/{recipeId}"             | DELETE     | string recipeId                  | IResult           | 200, 404          | Delete recipe                    |
