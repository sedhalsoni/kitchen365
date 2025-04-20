# Kitchen365

**Kitchen365** is a full-stack application designed to manage and showcase kitchen products using a microservice architecture. It includes:

- **NestJS backend microservice** with two services:
  - **Auth Service** (located in `/auth-service`) running on port `8000`
  - **Product Service** (located in `/product-service`) running on port `8001`
- **Next.js frontend application** (located in `/product-catalog`)
- **Docker Compose setup** for running all services together seamlessly

## Project Structure

```bash
kitchen365
├── backend-microservice/
│   ├── auth-service/
│   └── product-service/
├── product-catalog/
├── docker-compose.yml
└── README.md
```

## 🚀 Getting Started with Docker Compose

> Ensure you have **Docker** and **Docker Compose** installed on your machine.

### ✅ Steps to Run Both Backend & Frontend:

1. **Navigate to the project root folder:**
    ```bash
    cd kitchen365
    ```

2. **Build and run the containers:**
    ```bash
    docker-compose up --build
    ```

    This command will:
    - Build Docker images for both backend and frontend
    - Start both containers

3. **Access the applications:**

    - **Frontend (Next.js)**: [http://localhost:3000](http://localhost:3000)
    - **Backend Services**:
      - Auth Service: [http://localhost:8000](http://localhost:8000)
      - Product Service: [http://localhost:8001](http://localhost:8001)

4. **To stop the services:**

    In the terminal where Docker is running, press `Ctrl + C`, or run:
    ```bash
    docker-compose down
    ```

## 🛠 Manual Setup (Without Docker)

If you prefer to set up the services manually without Docker, follow these steps:

### 1. **Auth Service (NestJS)**

Navigate to the `auth-service` folder:

```bash
cd auth-service
npm install
npm start
```

Auth service will be available at: [http://localhost:8000](http://localhost:8000)

### 2. **Product Service (NestJS)**

Navigate to the `product-service` folder:

```bash
cd product-service
npm install
npm start
```

Product service will be available at: [http://localhost:8001](http://localhost:8001)

### 3. **Frontend Product Catalog (Next.js)**

Navigate to the `frontend` folder:

```bash
cd product-catalog
npm install
npm run dev
```

Frontend will be available at: [http://localhost:3000](http://localhost:3000)
