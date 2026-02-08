arquitetura base:


my-api/
├── cmd/
│   ├── api/
│   │   └── main.go          # sobe o servidor HTTP
│   └── cli/
│       └── main.go          # CLI (cobra)
│
├── internal/
│   ├── app/
│   │   └── container.go     # dependências (db, services, repos)
│
│   ├── http/
│   │   ├── handlers/
│   │   │   └── users/
│   │   │       ├── create.go
│   │   │       ├── update.go
│   │   │       ├── delete.go
│   │   │       ├── get.go
│   │   │       └── routes.go
│   │   │
│   │   ├── middlewares/
│   │   └── responses/
│   │       ├── error.go
│   │       └── success.go
│
│   ├── services/
│   │   └── users/
│   │       ├── service.go
│   │       └── types.go
│
│   ├── repositories/
│   │   └── users/
│   │       ├── repository.go
│   │       └── model.go
│
│   ├── types/
│   │   ├── pagination.go
│   │   └── errors.go
│
│   └── database/
│       ├── postgres.go
│       └── migrate.go
│
├── migrations/
│   ├── 0001_create_users.up.sql
│   └── 0001_create_users.down.sql
│
├── go.mod
├── go.sum
└── Dockerfile
