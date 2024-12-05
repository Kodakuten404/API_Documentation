# API Gateway Routes

| Path                  | Method | Request | Response          | ResponseCodes | Description        |
| --------------------- | ------ | ------- | ----------------- | ------------- | ------------------ |
| "/gateway/recipes"    | GET    | NONE    | IResult, Recipe[] | 200, 404      | Get all recipes    |
| "/gateway/categories" | GET    | NONE    | IResult, Recipe[] | 200, 404      | Get all categories |
