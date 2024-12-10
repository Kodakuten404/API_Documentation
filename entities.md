# Entities

### User : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| UserName          | string        |
| Password          | string        |
| Email             | string        |
| FavoriteIds       | string        |
| Token             | Token         |

### CategoryTag : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Name              | string        |

### Ingredient : IEntity

| **Property Name** | **Data Type** | **Comment** |
| ----------------- | ------------- | ----------- |
| Name              | string        |
| Amount            | double        |
| Unit              | string        |
| RecipeId          | Guid          | FK          |
| Recipe            | Recipe        | FK          |

### Recipe : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Name              | string        |
| Instructions      | string        |
| Ingredients       | Ingredient[]  |
| CategoryTags      | CategoryTag[] |
| ReviewIds         | Guid[]        |

### Review : IEntity

| **Property Name** | **Data Type**    |
| ----------------- | ---------------- |
| DatePublished     | DateTime         |
| AuthorId          | Guid             |
| RecipeId          | Guid             |
| ReviewText        | string           |
| Rating            | Enum.ReviewScore |

### Token : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| UserId            | Guid          |
| CreatedAt         | DateTime      |
| User              | User          |

### Notification

| **Property Name** | **Data Type**    |
| ----------------- | ---------------- |
| SentAt            | DateTime         |
| Topic             | Enum.Topics      |
| Message           | string           |
| NotificationType  | NotificationType |

### Subscriber : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| UserId            | Guid          |
| UserEmail         | string        |
| RegisteredAt      | DateTime      |

### NotificationLog : IEntity

| **Property Name** | **Data Type**    |
| ----------------- | ---------------- |
| UserId            | Guid[]           |
| SentAt            | DateTime         |
| Topic             | Enum.Topics      |
| Message           | string           |
| NotificationType  | NotificationType |

### NotificationType : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |

## Interfaces

### IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Id                | Guid          |
