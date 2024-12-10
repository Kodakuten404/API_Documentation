# Notification Service

| **Path**                      | **Method** | **Request**  | **Response**    | **ResponseCodes** | **Description**           |
| ----------------------------- | ---------- | ------------ | --------------- | ----------------- | ------------------------- |
| "/notification/subscribe/{user}" | POST       | Subscriber user  | NONE            | 200, 404          | Subscribe user            |
| "/notification/unsubscribe/{userId}"      | DELETE     | Guid userId  | NONE            | 200, 400          | Unsubscribe user          |
| "/notification/notify/{notification}"       | POST       | Notification | NONE            | 200, 400          | Notify subscribers        |
| "/notification/logs"              | GET        | NONE         | NotificationLog[] | 200               | Get all notification logs |
| "/notification/attach"              | POST        | NONE         | NONE | 200               | Get all notification logs |

