# Notification Kata - Data Access

Build data access object for the following entities:

## Entity Notification

| Column            | Type |
| ----------------- | ---- |
| customer_id       | text |
| notification_code | text |

## Entity NotificationStatus

One `Notification` have **one or more** `NotificationStatus`

| Column  | Type |
| ------- | ---- |
| channel | text |
| status  | text |

## Requirements

1. Should be able to save a `Notification` and its `NotificationStatuses`

2. Should be able to return `Notifications` and its `NotificationStatuses` by a **Notification Id**

3. Should be able to return `Notifications` for a specific `notification_code` in pages of **N** (e.g. 5)

4. Should be able to add new field `channel_recipient (text)` to `NotificationStatus`. Try to do this with Flyway.

5. Should be able to return Notifications details for a channel_recipient (e.g. what is the customer id for recipient `jim@example.com`)

## References

- https://www.baeldung.com/hibernate-one-to-many
- https://www.callicoder.com/hibernate-spring-boot-jpa-one-to-many-mapping-example/
- https://github.com/spring-guides/tut-spring-boot-kotlin
