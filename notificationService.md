# Notification Service

| **Path**                      | **Method** | **Request**  | **Response**    | **ResponseCodes** | **Description**           |
| ----------------------------- | ---------- | ------------ | --------------- | ----------------- | ------------------------- |
| "/notifications/subscribe/{user}" | POST       | SubscriberDto subscriber  | NONE            | 200, 404          | Subscribe user            |
| "/notifications/unsubscribe/{userId}"      | DELETE     | Guid userId  | NONE            | 200, 400          | Unsubscribe user          |
| "/notifications/notify/{notification}"       | POST       | NotificationDto notification | NONE            | 200, 400          | Notify subscribers        |
| "/notifications/logs"              | GET        | NONE         | NotificationLog[] | 200               | Get all notification logs |

