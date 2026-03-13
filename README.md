# Product Service

A Node.js/Express REST API for managing products in the ecommerce platform.

## Technology Stack
- Node.js 22
- Express.js
- PostgreSQL
- Docker

## Local Development

### Prerequisites
- Node.js 22+
- npm
- PostgreSQL

### Install Dependencies
```bash
npm install
```

### Run Development Server
```bash
node src/index.js
```

Service runs on `http://localhost:3001`

### Run Tests
```bash
npm test
```

## API Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /products | Get all products |
| GET | /products/:id | Get product by ID |
| POST | /products | Create a product |
| PUT | /products/:id | Update a product |
| DELETE | /products/:id | Delete a product |
| GET | /health | Health check |

## Docker

### Build Image
```bash
docker build -t eronan22/product-service:latest .
```

### Run Container
```bash
docker run -p 3001:3001 eronan22/product-service:latest
```

## Environment Variables
| Variable | Description | Default |
|----------|-------------|---------|
| PORT | Service port | 3001 |
| DB_HOST | Database host | database |
| DB_PORT | Database port | 5432 |
| DB_NAME | Database name | ecommerce |
| DB_USER | Database user | admin |
| DB_PASSWORD | Database password | - |

## CI/CD
This service uses a Jenkins pipeline defined in `Jenkinsfile`.
Pipeline stages: PR Validation → Build → Test → Security Scan → 
Container Build & Push → Deploy

## Docker Hub
```
eronan22/product-service
```