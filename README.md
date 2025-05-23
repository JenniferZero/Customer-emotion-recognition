# Customer Emotion Recognition System

A cutting-edge system designed for e-commerce websites that detects customer emotions through webcam analysis to predict product preferences and dynamically display personalized recommendations.

## 🚀 Features

- **Real-time Emotion Detection**: Analyzes facial expressions through webcam feeds using YOLO-based computer vision models
- **Intelligent Product Recommendations**: Suggests products based on detected emotions and user history
- **Emotion History Tracking**: Records and displays emotion patterns over time
- **Monorepo Architecture**: Organized with Turborepo for efficient development of multiple services
- **Modern Frontend**: Built with Next.js and Tailwind CSS for a responsive user experience
- **Powerful Backends**: NestJS (recommendations API) and FastAPI (AI processing) services
- **Cross-service Communication**: Shared types and API interfaces for consistent data handling

## 🏗️ Architecture

The project is structured as a monorepo using Turborepo and pnpm workspaces, consisting of:

### Frontend (Next.js)
- Emotion detection UI with webcam integration
- Product recommendations display
- Emotion history visualization
- Responsive layout with dark mode support

### API Service (NestJS)
- Product recommendation generation
- Emotion history storage and retrieval
- User preference tracking
- RESTful API with Swagger documentation

### AI Service (FastAPI)
- Real-time emotion recognition
- Face detection using YOLO models
- Emotion classification and confidence scoring
- API for emotion data processing

## 📋 Prerequisites

- Node.js 18+ 
- pnpm 8+ (`npm install -g pnpm`)
- Python 3.9+ (for AI service)

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/customer-emotion-recognition.git
   cd customer-emotion-recognition
   ```

2. Install dependencies:
   ```bash
   pnpm install
   ```

3. Build shared packages:
   ```bash
   pnpm build
   ```

4. Set up environment variables:
   - Copy `.env.example` to `.env` (or use the existing `.env` file)
   - Update the variables according to your setup

## 🚀 Running the Project

### Development Mode

1. Start all services in development mode:
   ```bash
   pnpm dev
   ```

   This will start:
   - Frontend: http://localhost:3000
   - API Service: http://localhost:3001
   - AI Service: http://localhost:5000

2. Alternatively, run individual services:
   ```bash
   # Frontend
   pnpm --filter="frontend" dev

   # API Service
   pnpm --filter="api-service" dev

   # AI Service
   pnpm --filter="ai-service" dev
   ```

### Production Mode

1. Build all services for production:
   ```bash
   # Windows PowerShell
   ./deploy.ps1
   
   # Unix/Linux/Mac
   chmod +x ./deploy.sh && ./deploy.sh
   ```

2. Start services in production mode:
   ```bash
   pnpm start
   ```

## 🧪 Testing

```bash
# Run all tests
pnpm test

# Run frontend tests
pnpm --filter="frontend" test

# Run API service tests
pnpm --filter="api-service" test
```

## 📝 API Documentation

- API Service Swagger: http://localhost:3001/api
- AI Service API docs: http://localhost:5000/docs

## 🧩 Project Structure

```
customer-emotion-recognition/
├── apps/                      # Application services
│   ├── frontend/              # Next.js frontend application
│   ├── api-service/           # NestJS recommendation API service
│   └── ai-service/            # FastAPI emotion detection service
├── packages/                  # Shared packages
│   ├── shared-types/          # TypeScript types used across services
│   ├── ui/                    # Shared UI components
│   ├── emotion-recognition/   # Emotion detection algorithms
│   └── ai-core/               # Core AI utilities
└── README.md                  # Project documentation
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.
- Real-time emotion detection using YOLO models
- Image processing and analysis
- LangChain/LangGraph integration for agent-based recommendations
- Asynchronous processing for better performance

### Shared Packages
- UI components (React)
- Type definitions (TypeScript)
- Utility functions

## 📊 Project Status

### ✅ COMPLETED:
1. Set up monorepo structure with Turborepo and pnpm
2. Implemented FastAPI backend service for emotion detection with YOLO
3. Created shared UI components and types
4. Implemented frontend components for emotion detection
5. Implemented NestJS backend service for recommendations
6. Integrated frontend with both FastAPI and NestJS backends
7. Created main page with integrated components
8. Added proper error handling and fallback mechanisms

### ⏳ PENDING:
1. Set up admin dashboard with Medusa.js
2. Implement CI/CD deployment
3. Add database integration with PostgreSQL and vector capabilities
4. Set up authentication and user management
5. Add product details pages and browsing
6. Deploy services to cloud providers

## 🔧 Setup & Installation

### Prerequisites
- Node.js (v18+)
- pnpm (v10+)
- Python (v3.9+)
- Git

### Installation

1. Clone the repository
   ```
   git clone https://github.com/yourusername/customer-emotion-recognition.git
   cd customer-emotion-recognition
   ```

2. Install dependencies
   ```
   pnpm install
   ```

3. Set up Python environment for FastAPI
   ```
   cd apps/ai-service/fastapi-service
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

### Configuration

1. Create `.env` files for each service:
   - Frontend: `apps/frontend/.env.local`
   - FastAPI: `apps/ai-service/fastapi-service/.env`
   - NestJS: `apps/api-service/nest-service/.env`

2. Configure environment variables (examples provided in `.env.example` files)

## 🚀 Running the Services

### Development Mode

1. Frontend (Next.js):
   ```
   cd apps/frontend && npm run dev
   ```

2. FastAPI Service:
   ```
   cd apps/ai-service/fastapi-service
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   uvicorn main:app --reload --port 8000
   ```

3. NestJS Service:
   ```
   cd apps/api-service/nest-service && npm run start:dev
   ```

4. All services (in development mode):
   ```
   pnpm dev
   ```

### Production Mode

1. Build all services:
   ```
   pnpm build
   ```

2. Start all services:
   ```
   pnpm start
   ```

## 🧪 Testing

Run tests for all services:
```
pnpm test
```

## 📝 API Documentation

- FastAPI Swagger UI: http://localhost:8000/docs
- NestJS Swagger UI: http://localhost:3001/api

## 🔮 Future Roadmap

1. Enhanced emotion detection using more sophisticated models
2. A/B testing framework for recommendation algorithms
3. Integration with popular e-commerce platforms
4. User behavior analytics dashboard
5. Multi-language support
6. Mobile application

## 📚 Tech Stack

- **Frontend**: Next.js, React, Tailwind CSS
- **Backend (API)**: NestJS, TypeScript
- **Backend (AI)**: FastAPI, Python, YOLO, LangChain, LangGraph
- **Monorepo Management**: Turborepo, pnpm
- **Planned Additions**: PostgreSQL, Redis, Medusa.js

## 📄 License

MIT
