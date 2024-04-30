```
+-------------------+       +-------------------+       +-------------------+
|   Controller      |       |   Service         |       |   Repository      |
|                   |       |                   |       |                   |
| - EventController | <---> | - EventService    | <---> | - EventRepository |
+-------------------+       +-------------------+       +-------------------+
        |                           |                           |
        v                           v                           v
+-------------------+       +-------------------+       +-------------------+
|   Model           |       |   DTO             |       |   Database        |
|                   |       |                   |       |                   |
| - Event           |       | - EventDTO        |       | - MySQL/Postgres  |
+-------------------+       +-------------------+       +-------------------+
```

**Controller**: This is where you define your RESTful APIs. Each API maps to a specific service method.

**Service**: This is where you write your business logic. The service interacts with the repository to fetch or persist data.

**Repository**: This is where you interact with the database. You can define custom queries here if needed.

**Model**: These are your database entities. They map directly to your database tables.

**DTO (Data Transfer Object)**: These are objects that carry data between processes. You'll use them to transfer data from your APIs to your service layer and vice versa.

**Database**: This is your database (MySQL, Postgres, etc.). All data is stored here.
