# TaskFlow DDD Skeleton

An empty project scaffold implementing Domain-Driven Design (DDD) layered architecture for a task management application backed by MongoDB.

## Architecture

This project follows a strict DDD layered architecture:

```
src/domain/
├── index.js                          # Composition root
├── user/
│   ├── User.js                       # User entity
│   └── UserId.js                     # User identity value object
├── task/
│   ├── Task.js                       # Task aggregate root
│   ├── TaskId.js                     # Task identity value object
│   └── TaskStatus.js                 # Task status enum/value object
├── application/services/
│   └── TaskCommandService.js         # CQRS-style command handler
├── interfaces/http/controllers/
│   ├── taskController.js             # HTTP controller
│   └── routes.js                     # Route definitions
└── infrastructure/
    ├── db/
    │   └── mongoCClient.js           # MongoDB connection client
    └── repositories/
        └── TaskRepostitoryMongo.js   # MongoDB task repository
```

## Technologies

| Technology | Usage |
|------------|-------|
| JavaScript (Node.js) | Runtime environment |
| MongoDB | Database (intended) |
| Express.js | HTTP framework (intended) |

## Design Patterns

- **Domain-Driven Design (DDD)** — Layered architecture with domain, application, infrastructure, and interface layers
- **Repository Pattern** — Abstract repository interface with MongoDB implementation
- **CQRS** — Command/Query Responsibility Segregation via TaskCommandService
- **Value Objects** — TaskId, UserId wrapping unique identifiers

## Status

This is a **skeleton project** — all files are empty. It is designed as a learning exercise for implementing DDD layers step by step.

## Reference

See `Ddd Mongo Practical Example.pdf` for the accompanying tutorial material.
