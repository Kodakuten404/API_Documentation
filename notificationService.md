# Notification Service

| **Path**                      | **Method** | **Request**  | **Response**    | **ResponseCodes** | **Description**           |
| ----------------------------- | ---------- | ------------ | --------------- | ----------------- | ------------------------- |
| "/notification/notify/"       | POST       | Notification | NONE            | 200, 400          | Notify subscribers        |
| "/notification/subscription/" | POST       | Guid userId  | NONE            | 200, 404          | Subscribe user            |
| "/notification/"              | GET        | NONE         | NotificationLog | 200               | Get all notification logs |
| "/notification/{userId}"      | DELETE     | Guid userId  | NONE            | 200, 400          | Unsubscribe user          |
