# Greens - Next-Generation Niche Marketplace

## Overview

Greens is a cutting-edge niche marketplace platform designed for 2026 and beyond. Unlike traditional marketplaces, Greens focuses on **curation, expert validation, and community-driven quality** rather than sheer volume. Built with modern technologies and AI-powered features, it provides a premium shopping experience for specialized markets.

## 🎯 Core Principles

- **Curation as a Service**: High-quality filtering for niche markets
- **Trust & Safety**: 2026 standards for secure transactions
- **Community-First**: Expert validation and transparent history
- **Adaptive UX**: AI-driven personalization and contextual discovery

## 🏗️ Architecture

### Frontend (Next.js 15)
- **Framework**: Next.js 15 with App Router
- **Styling**: Tailwind CSS with custom design system
- **State Management**: TanStack Query for data fetching
- **Animations**: Framer Motion for micro-interactions
- **UI Components**: Custom component library with Radix UI primitives

### Backend (Go)
- **Framework**: Go with chi router
- **Database**: PostgreSQL with pgvector extension for semantic search
- **Caching**: Redis for performance and rate limiting
- **Authentication**: JWT with refresh tokens
- **API**: RESTful API with comprehensive middleware

### Infrastructure
- **Containerization**: Docker with multi-stage builds
- **Orchestration**: Docker Compose for local development
- **Deployment**: Render-ready configuration
- **Monitoring**: Structured logging with zerolog

## 🚀 Features

### AI-Powered Personalization
- **For You Feed**: AI-driven content recommendations
- **Predictive Search**: Context-aware search results
- **Smart Bundles**: "Shop the Look" with compatibility suggestions
- **Behavioral Analysis**: Real-time user preference adaptation

### Trust & Safety Infrastructure
- **Multi-tier Verification**: Basic, Pro, and Expert seller levels
- **Transaction Escrow**: Secure payment handling
- **AI Content Guard**: Fraud detection and prevention
- **Transparent History**: Seller reputation and transaction history

### Immersive Shopping Experience
- **AR Integration**: "View in Room" for physical products
- **High-Quality Media**: Professional product imagery and video
- **Interactive Customization**: Real-time product configuration
- **Contextual Discovery**: Smart recommendations based on browsing

### Community Features
- **Expert Reviews**: Verified buyer/seller feedback
- **Discussion Forums**: Niche-specific community hubs
- **Knowledge Sharing**: Tutorials and expert content
- **Collaborative Curation**: Community-driven product discovery

## 🛠️ Tech Stack

### Frontend Technologies
- **Next.js 15**: Latest React framework with App Router
- **TypeScript**: Type-safe development
- **Tailwind CSS**: Utility-first styling with custom design tokens
- **Framer Motion**: Smooth animations and transitions
- **TanStack Query**: Data fetching and state management
- **Radix UI**: Accessible component primitives
- **Lucide React**: Modern icon system

### Backend Technologies
- **Go 1.23**: High-performance backend language
- **chi**: Lightweight HTTP router
- **PostgreSQL**: Primary database with pgvector extension
- **Redis**: Caching, rate limiting, and session storage
- **JWT**: Secure authentication and authorization
- **zerolog**: Structured logging

### AI & Machine Learning
- **OpenAI API**: Text embeddings and content analysis
- **Semantic Search**: Vector-based product discovery
- **Recommendation Engine**: Collaborative filtering algorithms
- **Content Moderation**: AI-powered fraud detection

### Infrastructure & DevOps
- **Docker**: Containerization for consistent environments
- **Docker Compose**: Local development orchestration
- **Render**: Cloud deployment platform
- **GitHub Actions**: CI/CD pipeline (ready for implementation)

## 📁 Project Structure

```
greens-marketplace/
├── frontend/                    # Next.js 15 application
│   ├── src/
│   │   ├── app/                # App Router pages
│   │   ├── components/         # Reusable UI components
│   │   ├── lib/               # Utility functions
│   │   ├── hooks/             # Custom React hooks
│   │   ├── services/          # API service layer
│   │   ├── store/             # State management
│   │   ├── styles/            # Global styles and themes
│   │   └── types/             # TypeScript type definitions
│   ├── public/                # Static assets
│   └── Dockerfile             # Frontend container
├── backend/                     # Go API server
│   ├── cmd/server/            # Main application entry point
│   ├── internal/
│   │   ├── config/            # Configuration management
│   │   ├── database/          # Database connections and migrations
│   │   ├── handlers/          # HTTP request handlers
│   │   ├── middleware/        # HTTP middleware
│   │   ├── models/            # Data models and schemas
│   │   ├── services/          # Business logic services
│   │   ├── utils/             # Utility functions
│   │   └── validators/        # Input validation
│   ├── migrations/            # Database migration scripts
│   └── Dockerfile             # Backend container
├── docs/                      # Documentation and specifications
├── docker-compose.yml         # Local development setup
└── README.md                  # This file
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ (for frontend)
- Go 1.23+ (for backend)
- Docker & Docker Compose
- PostgreSQL with pgvector extension

### Installation Guide

#### Install Node.js (Frontend)
1. Download Node.js from [nodejs.org](https://nodejs.org/)
2. Choose the LTS version (recommended for stability)
3. Run the installer and follow the setup wizard
4. Verify installation:
   ```bash
   node --version  # Should show v18.x or higher
   npm --version   # Should show v8.x or higher
   ```

#### Install Go (Backend)
1. Download Go from [golang.org](https://golang.org/dl/)
2. Choose the appropriate version for your operating system (Go 1.23+)
3. Run the installer and follow the setup wizard
4. **Windows Users**: Ensure Go is added to your PATH environment variable
5. Verify installation:
   ```bash
   go version  # Should show go1.23.x or higher
   ```
6. Set up Go workspace (optional but recommended):
   
   **Linux/macOS:**
   ```bash
   # Create a workspace directory
   mkdir ~/go-workspace
   cd ~/go-workspace
   
   # Set GOPATH (optional in Go 1.11+, but useful for organization)
   export GOPATH=$HOME/go-workspace
   ```
   
   **Windows (Command Prompt):**
   ```cmd
   # Create a workspace directory
   mkdir %USERPROFILE%\go-workspace
   cd %USERPROFILE%\go-workspace
   
   # Set GOPATH (optional in Go 1.11+, but useful for organization)
   set GOPATH=%USERPROFILE%\go-workspace
   ```
   
   **Windows (PowerShell):**
   ```powershell
   # Create a workspace directory
   New-Item -ItemType Directory -Path "$env:USERPROFILE\go-workspace"
   Set-Location "$env:USERPROFILE\go-workspace"
   
   # Set GOPATH (optional in Go 1.11+, but useful for organization)
   $env:GOPATH = "$env:USERPROFILE\go-workspace"
   ```

### Environment Setup

#### 1. Create Virtual Environments

**Frontend (Node.js)**
```bash
# Navigate to frontend directory
cd greens-marketplace/frontend

# Create a virtual environment using nvm (if installed)
nvm use 18  # or your preferred Node.js version

# Or create a .nvmrc file to specify Node version
echo "18" > .nvmrc
nvm use

# Verify Node.js version
node --version
npm --version
```

**Backend (Go)**
```bash
# Navigate to the correct directory where you cloned the project
# If you're in a different location, navigate to the project root first
cd C:\Users\pmali\Documents\Color\greens-marketplace
# OR if you cloned it elsewhere, navigate to that location

# Then navigate to the backend directory
cd backend

# Go doesn't require virtual environments like Python,
# but you can use goenv for version management if needed
go version

# Initialize Go module (if not already done)
go mod init greens-marketplace
```

#### 2. Install Dependencies

**Frontend Dependencies**
```bash
cd greens-marketplace/frontend

# Install all frontend dependencies
npm install

# Verify installation
npm list --depth=0

# Expected packages include:
# - next@15.0.3
# - react@19.0.0
# - react-dom@19.0.0
# - tailwindcss@3.4.0
# - framer-motion@11.0.0
# - @tanstack/react-query@5.0.0
# - lucide-react@0.320.0
# - And many more...
```

**Backend Dependencies**
```bash
cd greens-marketplace/backend

# Download and install Go dependencies
go mod download

# Verify dependencies
go mod verify

# Build the application to check for any issues
go build ./cmd/server

# Expected dependencies include:
# - github.com/go-chi/chi/v5
# - github.com/lib/pq
# - github.com/go-redis/redis/v8
# - github.com/golang-jwt/jwt/v5
# - github.com/rs/zerolog
# - And many more...
```

### Local Development

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd greens-marketplace
   ```

2. **Set up environment variables**
   ```bash
   cp backend/.env.example backend/.env
   cp frontend/.env.example frontend/.env.local
   # Edit configuration as needed
   ```

3. **Start with Docker Compose**
   ```bash
   docker-compose up -d
   ```

4. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:8080
   - Database: localhost:5432

### Manual Setup

1. **Backend Setup**
   ```bash
   cd backend
   go mod download
   go run cmd/server/main.go
   ```

2. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

## 🔧 Configuration

### Environment Variables

#### Backend (.env)
```env
# Server Configuration
SERVER_PORT=8080
ENVIRONMENT=development

# Database Configuration
DB_HOST=localhost
DB_PORT=5432
DB_USER=greens_user
DB_PASSWORD=greens_password
DB_NAME=greens_marketplace
DB_SSL_MODE=disable

# Redis Configuration
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=
REDIS_DB=0

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key

# OpenAI Configuration
OPENAI_API_KEY=your-openai-api-key
```

#### Frontend (.env.local)
```env
NEXT_PUBLIC_API_URL=http://localhost:8080
NEXT_PUBLIC_ENVIRONMENT=development
```

## 🎨 Design System

### Color Palette
- **Primary**: Customizable based on theme
- **Secondary**: Complementary accent colors
- **Background**: Light/dark theme support
- **Foreground**: Text and icon colors
- **Muted**: Secondary text and borders

### Typography
- **Font Family**: System font stack with fallbacks
- **Font Sizes**: Responsive scale from xs to 2xl
- **Line Heights**: Optimized for readability
- **Font Weights**: Multiple weights for hierarchy

### Components
- **Buttons**: Primary, secondary, ghost variants
- **Cards**: Neubrutalism and softer UI styles
- **Forms**: Accessible inputs with validation
- **Navigation**: Responsive header and sidebar
- **Modals**: Overlay dialogs with proper focus management

### Animations
- **Micro-interactions**: Hover effects and transitions
- **Page Transitions**: Smooth navigation animations
- **Loading States**: Skeleton screens and spinners
- **Error States**: Animated error messages

## 🔄 API Endpoints

### Authentication
- `POST /api/v1/auth/register` - User registration
- `POST /api/v1/auth/login` - User login
- `POST /api/v1/auth/refresh` - Token refresh

### Users
- `GET /api/v1/users/profile` - Get user profile
- `PUT /api/v1/users/profile` - Update user profile
- `GET /api/v1/users/preferences` - Get user preferences
- `PUT /api/v1/users/preferences` - Update user preferences

### Products
- `GET /api/v1/products` - List products with filters
- `GET /api/v1/products/{id}` - Get product details
- `POST /api/v1/products` - Create new product
- `PUT /api/v1/products/{id}` - Update product
- `DELETE /api/v1/products/{id}` - Delete product
- `GET /api/v1/products/{id}/similar` - Get similar products
- `GET /api/v1/products/{id}/reviews` - Get product reviews

### Search
- `GET /api/v1/search` - Traditional search
- `POST /api/v1/search/semantic` - AI-powered semantic search

### Cart & Wishlist
- `GET /api/v1/cart` - Get user cart
- `POST /api/v1/cart` - Add to cart
- `PUT /api/v1/cart/{productId}` - Update cart item
- `DELETE /api/v1/cart/{productId}` - Remove from cart
- `GET /api/v1/wishlist` - Get user wishlist
- `POST /api/v1/wishlist/{productId}` - Add to wishlist
- `DELETE /api/v1/wishlist/{productId}` - Remove from wishlist

### Orders
- `POST /api/v1/orders` - Create new order
- `GET /api/v1/orders` - Get user orders
- `GET /api/v1/orders/{id}` - Get order details
- `PUT /api/v1/orders/{id}/status` - Update order status
- `POST /api/v1/orders/{id}/payment` - Process payment

## 🧪 Testing

### Frontend Testing
- **Unit Tests**: Component and utility testing with Jest
- **Integration Tests**: API integration testing
- **E2E Tests**: User flow testing with Playwright/Cypress

### Backend Testing
- **Unit Tests**: Service and model testing
- **Integration Tests**: Database and API testing
- **Load Tests**: Performance testing with k6

### Test Scripts
```bash
# Frontend tests
npm run test
npm run test:coverage

# Backend tests
go test ./...
go test -v ./internal/...

# E2E tests
npm run test:e2e
```

## 🚀 Deployment

### Render Deployment
1. Connect your GitHub repository to Render
2. Create Web Services for frontend and backend
3. Configure environment variables
4. Set up PostgreSQL and Redis add-ons
5. Configure custom domain and SSL

### Docker Deployment
```bash
# Build images
docker-compose build

# Deploy to production
docker-compose -f docker-compose.prod.yml up -d

# Monitor logs
docker-compose logs -f
```

### CI/CD Pipeline
- **GitHub Actions**: Automated testing and deployment
- **Docker Hub**: Container image registry
- **Render**: Cloud deployment platform
- **Monitoring**: Health checks and performance metrics

## 🔒 Security

### Authentication & Authorization
- JWT tokens with refresh mechanism
- Password hashing with bcrypt
- Rate limiting and IP blocking
- CORS configuration

### Data Protection
- Input validation and sanitization
- SQL injection prevention
- XSS protection
- CSRF protection

### Infrastructure Security
- HTTPS enforcement
- Secure headers
- Database encryption
- Environment variable management

## 📊 Monitoring & Analytics

### Application Monitoring
- Structured logging with zerolog
- Performance metrics and APM
- Error tracking and alerting
- Health check endpoints

### Business Analytics
- User behavior tracking
- Conversion funnel analysis
- Product performance metrics
- Revenue and transaction tracking

### Infrastructure Monitoring
- Resource utilization monitoring
- Database performance metrics
- Cache hit rates
- API response times

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Write tests for your changes
5. Run the test suite
6. Submit a pull request

### Code Style
- Follow Go and TypeScript best practices
- Use meaningful variable names
- Write comprehensive tests
- Document public APIs
- Follow the existing code style

### Development Workflow
- Feature branches for new functionality
- Pull requests for code review
- Automated testing and linting
- Continuous integration and deployment

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Next.js Team** - For the excellent React framework
- **Go Community** - For the powerful backend language
- **OpenAI** - For AI capabilities and APIs
- **PostgreSQL Community** - For the robust database
- **All Contributors** - For their valuable contributions

## 📞 Support

For support and questions:
- Create an issue on GitHub
- Join our Discord community
- Email us at support@greens.marketplace

---

**Greens Marketplace** - Redefining niche marketplaces for 2026 and beyond.