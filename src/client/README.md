# 🎮 SteamEngine Frontend

> **React-based frontend for the SteamEngine game discovery and recommendation platform**

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- Backend server running (see main README)

### Installation
```bash
cd src/client
npm install
```

### Development
```bash
npm start
```
The app will open at [http://localhost:3000](http://localhost:3000)

### Build for Production
```bash
npm run build
```

## 🏗️ Project Structure

```
src/client/
├── 📁 public/                 # Static assets
│   ├── index.html             # Main HTML template
│   ├── favicon.ico           # App icon
│   └── manifest.json         # PWA manifest
├── 📁 src/                   # Source code
│   ├── 📁 components/        # React components
│   │   ├── GameCard.js       # Game display cards
│   │   ├── GameDetails.js    # Detailed game view
│   │   ├── FilterBar.js      # Advanced filtering
│   │   ├── SearchBar.js      # Search functionality
│   │   ├── Login.js          # Authentication
│   │   ├── Home.js           # Main dashboard
│   │   ├── CommentForm.js    # Comment system
│   │   ├── CommentSection.js # Comments display
│   │   ├── Vote.js           # Rating system
│   │   └── PageHeader.js     # Navigation header
│   ├── 📁 api/              # API integration
│   │   ├── game.js          # Game-related API calls
│   │   ├── user.js          # User management
│   │   ├── comments.js      # Comment system
│   │   ├── rating.js        # Rating system
│   │   └── playtime.js      # Playtime tracking
│   ├── App.js               # Main app component
│   ├── App.css              # Main styles
│   ├── index.js             # App entry point
│   └── setupProxy.js        # Development proxy
└── package.json             # Dependencies and scripts
```

## 🎨 Key Components

### 🎮 Game Components
- **GameCard**: Displays game information in card format
- **GameDetails**: Detailed view with full game information
- **GameDisplay**: Grid layout for multiple games

### 🔍 Search & Filter Components
- **SearchBar**: Text-based game search
- **FilterBar**: Advanced filtering by multiple criteria
- **FilterBar.css**: Styling for filter components

### 👤 User Components
- **Login**: User authentication interface
- **PageHeader**: Navigation and user status
- **CommentForm**: Add comments to games
- **CommentSection**: Display game comments
- **Vote**: Rating and voting system

### 🎨 Styling
- **Material-UI**: Primary component library
- **Custom CSS**: Component-specific styling
- **Responsive Design**: Mobile-friendly interface

## 🔧 Available Scripts

### `npm start`
Runs the app in development mode at [http://localhost:3000](http://localhost:3000)

### `npm test`
Launches the test runner in interactive watch mode

### `npm run build`
Builds the app for production in the `build` folder

### `npm run eject`
**Note: This is a one-way operation!**
Removes the single build dependency and copies configuration files into the project

## 🌐 API Integration

The frontend communicates with the backend through the following API endpoints:

### Games
- `GET /games` - Fetch all games with filtering
- `GET /games/:id` - Get specific game details
- `GET /games/search` - Search games by criteria

### Users
- `POST /user/login` - User authentication
- `POST /user/register` - User registration
- `GET /user/profile` - Get user profile

### Comments
- `GET /comments/:gameId` - Get game comments
- `POST /comments` - Add new comment
- `DELETE /comments/:id` - Delete comment

### Ratings
- `GET /rating/:gameId` - Get game ratings
- `POST /rating` - Add/update rating

## 🎯 Features

### 🔍 Search & Discovery
- **Real-time Search**: Instant results as you type
- **Advanced Filtering**: Filter by genre, requirements, ratings
- **Smart Suggestions**: Intelligent game recommendations

### 👤 User Experience
- **Responsive Design**: Works on desktop and mobile
- **Modern UI**: Clean, intuitive interface
- **Fast Loading**: Optimized for performance

### 💬 Social Features
- **Comment System**: Share thoughts on games
- **Rating System**: Rate and review games
- **User Profiles**: Personalized experience

## 🛠️ Dependencies

### Core React
- **react**: ^18.2.0
- **react-dom**: ^18.2.0
- **react-router-dom**: ^6.20.0

### UI Framework
- **@mui/material**: ^5.14.19
- **@emotion/react**: ^11.11.1
- **@emotion/styled**: ^11.11.0
- **react-icons**: ^4.12.0

### HTTP Client
- **axios**: ^1.6.2
- **http-proxy-middleware**: ^2.0.6

### Development
- **react-scripts**: ^5.0.1
- **@testing-library/react**: ^13.4.0
- **@testing-library/jest-dom**: ^5.17.0

## 🔧 Configuration

### Development Proxy
The app uses a proxy configuration (`setupProxy.js`) to forward API requests to the backend server during development.

### Environment Variables
Create a `.env` file in the client directory for environment-specific configuration:

```env
REACT_APP_API_URL=http://localhost:4000
REACT_APP_ENV=development
```

## 🚀 Deployment

### Build Process
1. Run `npm run build` to create production build
2. The `build` folder contains optimized static files
3. Deploy the contents to your web server

### Production Considerations
- **Environment Variables**: Set production API URLs
- **HTTPS**: Enable for secure connections
- **CDN**: Consider using a CDN for static assets
- **Caching**: Implement proper caching strategies

## 🧪 Testing

### Running Tests
```bash
npm test
```

### Test Coverage
```bash
npm test -- --coverage
```

## 📚 Learn More

- [React Documentation](https://reactjs.org/)
- [Material-UI Documentation](https://mui.com/)
- [React Router Documentation](https://reactrouter.com/)
- [Create React App Documentation](https://facebook.github.io/create-react-app/)

---

<div align="center">

**🎮 SteamEngine Frontend - Built with React & Material-UI**

*Part of the SteamEngine project by Team PreQL*

</div>
