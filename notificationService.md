# Notification Service

| **Path**                              | **Method** | **Request**  | **Response**    | **ResponseCodes** | **Description**           |
| ------------------------------------- | ---------- | ------------ | --------------- | ----------------- | ------------------------- |
| "/notification/subscribe/{userId}"    | POST       | Guid userId  | NONE            | 200, 404          | Subscribe user            |
| "/notification/unsubscribe/{userId}"  | DELETE     | Guid userId  | NONE            | 200, 400          | Unsubscribe user          |
| "/notification/notify/{notification}" | POST       | Notification | NONE            | 200, 400          | Notify subscribers        |
| "/notification/"                      | GET        | NONE         | NotificationLog | 200               | Get all notification logs |
