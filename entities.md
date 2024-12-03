# Entities

### User : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| UserName          | string        |
| Password          | string        |
| Email             | string        |
| FavoriteIds       | Guid[]        |
| Token             | Token         |

### CategoryTag : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Name              | string        |

### Ingredient : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Name              | string        |
| Amount            | double        |
| Unit              | string        |

### Recipe : IEntity

| **Property Name** | **Data Type** |
| ----------------- | ------------- |
| Name              | string        |
| Instructions      | string        |
| Ingredients       | Ingredient[]  |
| TagIds            | Guid[]        |
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
| AccessToken       | string        |
| CreatedAt         | DateTime      |

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
