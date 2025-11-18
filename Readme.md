# 🎮 SteamEngine - Steam Game Discovery & Recommendation Platform

[![React](https://img.shields.io/badge/React-18.2.0-blue.svg)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-Express-green.svg)](https://nodejs.org/)
[![MySQL](https://img.shields.io/badge/MySQL-Database-orange.svg)](https://www.mysql.com/)
[![Material-UI](https://img.shields.io/badge/Material--UI-5.14.19-purple.svg)](https://mui.com/)

> **A comprehensive Steam game discovery and recommendation platform that helps users find their next favorite game through advanced search, filtering, and personalized recommendations.**

## 📋 Table of Contents

- [🚀 Features](#-features)
- [🛠️ Tech Stack](#️-tech-stack)
- [📦 Installation](#-installation)
- [⚡ Quick Start](#-quick-start)
- [🏗️ Project Structure](#️-project-structure)
- [🎯 Key Features](#-key-features)
- [🔧 API Endpoints](#-api-endpoints)
- [💾 Database Schema](#-database-schema)
- [👥 Team Information](#-team-information)
- [📚 Documentation](#-documentation)

## 🚀 Features

### 🎯 Core Functionality
- **🔍 Advanced Game Search**: Search games by title, genre, hardware requirements, and more
- **🎨 Interactive Filtering**: Filter games by multiple criteria including reviews, casual/non-casual, and system requirements
- **📊 Data Visualization**: Interactive breakdowns of Steam's library based on user-selected criteria
- **👤 User Authentication**: Secure login system with personalized features
- **❤️ Social Features**: Like games, add comments, and save favorites for future sessions
- **💻 System Compatibility**: Enter your PC specs for personalized game recommendations

### 🎮 User Experience
- **Responsive Design**: Modern, mobile-friendly interface built with Material-UI
- **Real-time Search**: Instant search results with dynamic filtering
- **Personalized Recommendations**: Get game suggestions based on your system specs and preferences
- **Community Features**: Share thoughts and discover games through user comments and ratings

## 🛠️ Tech Stack

### Frontend
- **React 18.2.0** - Modern UI framework
- **Material-UI 5.14.19** - Beautiful, responsive components
- **React Router DOM 6.20.0** - Client-side routing
- **Axios 1.6.2** - HTTP client for API calls
- **React Icons 4.12.0** - Icon library

### Backend
- **Node.js** - Server runtime
- **Express.js 4.18.2** - Web framework
- **MySQL 2.18.1** - Database
- **CORS 2.8.5** - Cross-origin resource sharing
- **Nodemon 3.0.1** - Development server

### Database
- **MySQL** - Relational database with stored procedures and triggers
- **Advanced Queries** - Optimized for game data retrieval
- **Content Moderation** - Automatic comment filtering

## 📦 Installation

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- MySQL database
- Git

### Clone the Repository
```bash
git clone https://github.com/yourusername/SteamEngine.git
cd SteamEngine
```

## ⚡ Quick Start

### 1. Install Dependencies

**Frontend (React App):**
```bash
cd src/client
npm install
```

**Backend (Express Server):**
```bash
cd src/server
npm install
```

### 2. Database Setup
1. Create a MySQL database
2. Import your Steam game data
3. Run the stored procedures from `ProcedureAndTrigger.sql`

### 3. Environment Configuration
Create a `.env` file in `src/server/`:
```env
PORT=4000
DB_HOST=localhost
DB_USER=your_username
DB_PASSWORD=your_password
DB_NAME=steam_engine
```

### 4. Start the Application

**Terminal 1 - Start the Backend:**
```bash
cd src/server
npm run dev
```
Server will run on `http://localhost:4000`

**Terminal 2 - Start the Frontend:**
```bash
cd src/client
npm start
```
App will open at `http://localhost:3000`

## 🏗️ Project Structure

```
SteamEngine/
├── 📁 src/
│   ├── 🎨 client/                 # React Frontend
│   │   ├── src/
│   │   │   ├── components/        # React Components
│   │   │   │   ├── GameCard.js    # Game display cards
│   │   │   │   ├── FilterBar.js   # Advanced filtering
│   │   │   │   ├── SearchBar.js   # Search functionality
│   │   │   │   ├── GameDetails.js # Detailed game view
│   │   │   │   ├── Login.js       # Authentication
│   │   │   │   └── ...
│   │   │   ├── api/              # API integration
│   │   │   └── App.js            # Main app component
│   │   └── package.json
│   │
│   └── ⚙️ server/                 # Express Backend
│       ├── routes/               # API routes
│       │   ├── game.js          # Game endpoints
│       │   ├── user.js          # User management
│       │   ├── comments.js      # Comment system
│       │   ├── rating.js        # Rating system
│       │   └── playtime.js      # Playtime tracking
│       ├── controllers/         # Business logic
│       ├── models/              # Data models
│       ├── app.js              # Server configuration
│       └── package.json
│
├── 📊 doc/                      # Project documentation
├── 🗄️ ProcedureAndTrigger.sql   # Database procedures
├── 📋 dependencies.txt          # Project dependencies
└── 📖 README.md                # This file
```

## 🎯 Key Features

### 🔍 Advanced Search & Filtering
- **Multi-criteria Search**: Find games by title, genre, developer, or publisher
- **Hardware-based Filtering**: Filter by minimum system requirements
- **Review-based Sorting**: Sort by user ratings and review counts
- **Category Filtering**: Filter by game categories (RPG, FPS, Strategy, etc.)

### 👤 User Management
- **Secure Authentication**: User registration and login system
- **Profile Management**: Save preferences and gaming history
- **Personal Library**: Save favorite games for quick access
- **System Specs**: Enter your PC specifications for personalized recommendations

### 💬 Social Features
- **Comment System**: Share thoughts and reviews on games
- **Rating System**: Upvote/downvote games
- **Community Interaction**: See what other users think about games
- **Content Moderation**: Automatic filtering of inappropriate content

### 📊 Data Visualization
- **Interactive Charts**: Visual breakdowns of Steam's game library
- **Genre Analysis**: See distribution of games by category
- **Trend Analysis**: Track popular games and genres
- **Custom Queries**: Create personalized data views

## 🔧 API Endpoints

### Games
- `GET /games` - Get all games with optional filtering
- `GET /games/:id` - Get specific game details
- `GET /games/search` - Search games by criteria

### Users
- `POST /user/login` - User authentication
- `POST /user/register` - User registration
- `GET /user/profile` - Get user profile
- `PUT /user/specs` - Update system specifications

### Comments
- `GET /comments/:gameId` - Get comments for a game
- `POST /comments` - Add a new comment
- `DELETE /comments/:id` - Delete a comment

### Ratings
- `GET /rating/:gameId` - Get ratings for a game
- `POST /rating` - Add/update a rating
- `GET /rating/stats/:gameId` - Get rating statistics

### Playtime
- `GET /playtime/:userId` - Get user playtime data
- `POST /playtime` - Add playtime entry

## 💾 Database Schema

### Core Tables
- **GameInfo**: Game metadata, requirements, categories
- **UserProfile**: User accounts and preferences
- **Comments**: User comments and reviews
- **Rating**: User ratings and votes
- **PlayTime**: User playtime tracking

### Advanced Features
- **Stored Procedures**: Optimized queries for game data retrieval
- **Triggers**: Automatic content moderation
- **Indexes**: Fast search and filtering performance

## 👥 Team Information

| Role | Name | Email |
|------|------|-------|
| 🎯 **Member** | Praveen Kalva | spkalva3@illinois.edu |
| 👨‍💻 **Member** | Krishna Konda | knkonda2@illinois.edu |
| 👨‍💻 **Member** | Justin Ansell | jansell2@illinois.edu |
| 👨‍💻 **Member** | Wyatt Sass | wpsass2@illinois.edu |

**Team ID**: Team-098  
**Project**: SteamEngine (PreQL)

## 📚 Documentation

- 📄 [Database Design](./doc/Database%20Design.pdf) - Complete database schema
- 📄 [PreQL Detailed Project Description](./doc/PreQL%20Detailed%20Project%20Description.pdf) - Project requirements
- 📄 [PreQL Stage 2](./doc/PreQL%20Stage%20.pdf) - Development stages

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Steam API** for game data
- **Material-UI** for beautiful components
- **React Community** for excellent documentation
- **CS 411 Course Staff** for guidance and support

---

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/krishnankonda/SteamEngine)

</div>
