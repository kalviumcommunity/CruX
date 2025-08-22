# CruX - AI-Powered News Aggregator & Summarizer

A modern, AI-powered news aggregator that fetches news from multiple sources, processes it with AI to summarize and categorize, and serves it to users through a clean frontend.

## 🚀 Features

- **AI-Powered Summarization**: Uses Google Gemini API for intelligent article summarization
- **Multi-Source News**: Integrates with newsdata.io and other news APIs
- **Smart Categorization**: Automatically categorizes articles using AI
- **Interactive Chat**: Chat with AI about any article for deeper insights
- **User Preferences**: Save favorite categories and sources
- **Modern UI**: Clean, responsive design built with React and Tailwind CSS
- **JWT Authentication**: Secure user authentication with refresh tokens
- **Production Ready**: Built for scalability and deployment

## 🏗️ Architecture

### Frontend (React + TypeScript)
- **Location**: `/client`
- **Framework**: React 19 with TypeScript
- **Styling**: Tailwind CSS
- **Build Tool**: Vite
- **State Management**: React hooks

### Backend (Node.js + Express + TypeScript)
- **Location**: `/server`
- **Framework**: Express.js with TypeScript
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT with refresh tokens
- **AI Integration**: Google Gemini API
- **News APIs**: newsdata.io integration
- **Deployment**: Railway-ready

## 📁 Project Structure

```
CruX/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── pages/         # Page components
│   │   ├── services/      # API services
│   │   ├── types/         # TypeScript types
│   │   └── ...
│   └── package.json
├── server/                 # Backend Node.js application
│   ├── src/
│   │   ├── controllers/   # Route controllers
│   │   ├── models/        # Database models
│   │   ├── routes/        # API routes
│   │   ├── services/      # Business logic
│   │   ├── middleware/    # Express middleware
│   │   └── ...
│   └── package.json
└── README.md
```

## 🛠️ Quick Start

### Prerequisites
- Node.js 18+
- MongoDB Atlas account
- Google Gemini API key
- newsdata.io API key

### Frontend Setup
```bash
cd client
npm install
npm run dev
```

### Backend Setup
```bash
cd server
npm install
cp env.example .env
# Edit .env with your API keys
npm run dev
```

### Environment Variables (Backend)
Create a `.env` file in the `/server` directory:

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# MongoDB Configuration
MONGODB_URI=your-mongodb-atlas-connection-string

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key
JWT_REFRESH_SECRET=your-super-secret-refresh-key

# AI Configuration
GEMINI_API_KEY=your-gemini-api-key

# News API Configuration
NEWSDATA_API_KEY=your-newsdata-api-key

# CORS Configuration
CORS_ORIGIN=http://localhost:5173
```

## 📡 API Endpoints

### News
- `GET /api/news` - Get latest news articles
- `GET /api/news/:id` - Get single article
- `POST /api/chat` - AI chat with article

### Authentication
- `POST /api/auth/signup` - Create account
- `POST /api/auth/login` - Login
- `POST /api/auth/refresh` - Refresh token

### User
- `GET /api/user/preferences` - Get user preferences
- `POST /api/user/preferences` - Update preferences

## 🔧 Development

### Frontend Commands
```bash
cd client
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
```

### Backend Commands
```bash
cd server
npm run dev      # Start development server
npm run build    # Build for production
npm start        # Start production server
```

## 🚀 Deployment

### Frontend (Vercel/Netlify)
1. Build the frontend: `cd client && npm run build`
2. Deploy the `dist` folder to your preferred platform

### Backend (Railway)
1. Push to GitHub
2. Connect repository to Railway
3. Set environment variables in Railway dashboard
4. Deploy automatically

## 🔒 Security Features

- JWT authentication with refresh tokens
- Rate limiting on API endpoints
- Input validation and sanitization
- CORS configuration
- Helmet.js security headers
- Password hashing with bcrypt

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

ISC License

## 🎯 Roadmap

- [ ] Add more news sources
- [ ] Implement user bookmarks
- [ ] Add email notifications
- [ ] Create mobile app
- [ ] Add analytics dashboard
- [ ] Implement caching layer
- [ ] Add unit and integration tests

---

Built with ❤️ for the modern news consumption experience.
