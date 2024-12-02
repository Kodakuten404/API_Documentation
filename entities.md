# Entities

### User : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| UserName          | string        |
| Password          | string        |
| Email             | string        |
| Favorites         | Recipe[]      |
| Reviews           | Review[]      |
| Token             | TokenF        |

### Ingredient : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Name              | string        |
| Amount            | double        |
| Unit              | string        |

### Category : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Name              | string        |

### Recipe : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Name              | string        |
| Instructions      | string        |
| Ingredients       | Ingredient[]  |
| Category          | Category[]    |
| Review            | Review[]      |

### Review : IEntity

| **Property Name** | **Data Type**    |
| ----------------- | ---------------- |
| DatePublished     | DateTime         |
| Author            | User             |
| Recipe            | Recipe           |
| ReviewText        | string           |
| Rating            | Enum.ReviewScore |

### Token

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Id                | int           |
| AccessToken       | string        |
| CreatedAt         | DateTime      |

## Interfaces

### IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Id                | Int           |
