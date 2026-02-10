# 🎵 Music App – Full Stack (Docker Setup)

This repository provides a Docker orchestration setup to run the full Music App project.

It connects:

🎯 **Backend** — Django + GraphQL

🎨 **Frontend** — Next.js (React)


## 📂 Project Structure (required)

You must organize your folders like this:

music-app-docker/
 ├── backend/
 ├── frontend/
 ├── docker-compose.yml
 └── README.md

## 🚀 Setup Instructions

1. Clone Backend & Frontend

```bash
git clone https://github.com/itskhashman/backend.git backend
git clone https://github.com/itskhashman/frontend.git frontend
```

This will create the required folder structure.

2. Create Environment Files
🔐 Backend .env

Create:

- backend/.env


   Add:
```bash
DJANGO_SECRET_KEY=dev-secret
DJANGO_DEBUG=True
DJANGO_ALLOWED_HOSTS=127.0.0.1,localhost,0.0.0.0
```
- Frontend .env

   Add:
```bash
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_GRAPHQL_ENDPOINT=/graphql/
```

3. Run the Full Project

   From the root folder:
```bash
docker compose up --build
```

Backend will be available at: http://localhost:8000

GraphQL endpoint: http://localhost:8000/graphql/

Frontend will be available at: http://localhost:3000
