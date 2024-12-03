# Review Service

| **Path**                     | **Method** | **Request**                                 | **Response** | **ResponseCodes** | **Description**                           |
| ---------------------------- | ---------- | ------------------------------------------- | ------------ | ----------------- | ----------------------------------------- |
| "/reviews/"                  | GET        | NONE                                        | Review[]     | 200               | Get all reviews                           |
| "/reviews/{reviewId}"        | GET        | Guid reviewId                               | Review       | 200, 404          | Get review by id                          |
| "/reviews/recipe/{recipeId}" | GET        | Guid recipeId                               | Review[]     | 200, 404          | Get reviews by recipe id                  |
| "/reviews/author/{authorId}" | GET        | Guid authorId                               | Review[]     | 200, 404          | Get reviews by author id                  |
| "/reviews/"                  | POST       | Review                                      | NONE         | 200, 400          | Add new review                            |
| "/reviews/{reviewId}"        | DELETE     | Guid reviewId                               | NONE         | 200, 404          | Delete review                             |

### Comments
