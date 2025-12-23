# BPM_D

Document management system with advanced BPM support.

## Features

### Document Management
- **Upload/Download**: Multi-file upload with drag-and-drop support
- **Version Control**: Full document versioning with diff comparison
- **Search**: Full-text search powered by Elasticsearch
- **OCR**: Automatic text extraction from images and scanned PDFs
- **Templates**: Document templates with variable substitution
- **Access Control**: Role-based permissions (RBAC) with CASL

### BPM (Business Process Management)
- **Visual Workflow Designer**: BPMN 2.0 compatible workflow editor
- **Task Assignment**: Automatic and manual task routing
- **Approval Workflows**: Multi-level approval with escalation
- **Form Builder**: Dynamic form creation with validation
- **Notifications**: Email and push notifications
- **Analytics**: Process performance dashboards and reports
- **Integrations**: Webhook support for external systems

## Tech Stack

| Layer | Technology |
|-------|------------|
| **Backend** | NestJS, TypeORM, PostgreSQL |
| **Frontend** | React, TypeScript, Vite |
| **Workflow Engine** | bpmn-js, bpmn-engine |
| **Search** | Elasticsearch |
| **Storage** | MinIO (S3-compatible) |
| **Cache/Queue** | Redis, Bull |
| **Auth** | JWT, Passport |

## Getting Started

### Prerequisites
- Node.js >= 20.x
- Docker & Docker Compose
- npm >= 10.x

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd BPM_D
```

2. Copy environment variables:
```bash
cp .env.example .env
```

3. Start infrastructure services:
```bash
npm run docker:up
```

4. Install dependencies:
```bash
npm install
```

5. Run database migrations:
```bash
npm run db:migrate
```

6. Start development servers:
```bash
npm run start:dev
```

### Access Points
- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:3000
- **API Docs**: http://localhost:3000/api/docs
- **MinIO Console**: http://localhost:9001

## Project Structure

```
BPM_D/
├── apps/
│   ├── backend/          # NestJS API server
│   └── frontend/         # React SPA
├── packages/
│   └── shared/           # Shared types and utilities
├── docker/               # Docker configuration
├── docker-compose.yml    # Docker services
└── package.json          # Root workspace config
```

## Scripts

| Command | Description |
|---------|-------------|
| `npm run start:dev` | Start all services in development mode |
| `npm run build` | Build all packages |
| `npm run test` | Run all tests |
| `npm run lint` | Lint all packages |
| `npm run docker:up` | Start Docker services |
| `npm run docker:down` | Stop Docker services |
| `npm run db:migrate` | Run database migrations |

## License

MIT
