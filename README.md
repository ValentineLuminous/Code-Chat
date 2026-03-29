# Real-Time Collaborative Coding Platform

A full-stack web application that enables real-time collaborative coding with AI assistance. Users can create projects, chat with friends, generate code using AI, and run JavaScript code in-browser using WebContainers.

## Features

### Core Functionality
- **User Authentication**: Secure registration and login with JWT tokens
- **Project Management**: Create and manage coding projects
- **Collaborative Workspaces**: Add collaborators to projects for team coding
- **Real-Time Chat**: Instant messaging within project workspaces
- **AI Code Generation**: Chat with AI to generate code snippets and complete applications
- **In-Browser Code Execution**: Run JavaScript code directly in the browser using WebContainers
- **File Management**: Organize project files in a tree structure
- **Code Editor**: Built-in code editor with syntax highlighting

### Technical Features
- **Real-Time Communication**: Socket.IO for instant messaging
- **Caching**: Redis for session management and token blacklisting
- **Database**: MongoDB for user and project data storage
- **AI Integration**: Google Gemini AI for code generation
- **Responsive Design**: Tailwind CSS for modern UI

## Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **Socket.IO** - Real-time communication
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **Redis** - Caching and session management
- **JWT** - Authentication
- **bcrypt** - Password hashing
- **Google Generative AI** - AI code generation

### Frontend
- **React** - UI library
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Styling
- **Axios** - HTTP client
- **Socket.IO Client** - Real-time communication
- **WebContainer API** - In-browser code execution
- **Highlight.js** - Code syntax highlighting
- **Markdown-to-JSX** - Markdown rendering

## Prerequisites

- Node.js (v16 or higher)
- MongoDB
- Redis
- Google AI API key (for AI features)

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd soen
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   cp .env.example .env
   # Edit .env with your configuration
   npm start
   ```

3. **Frontend Setup**
   ```bash
   cd ../frontend
   npm install
   cp .env.example .env  # If needed
   npm run dev
   ```

## Environment Variables

### Backend (.env)
```env
PORT=3000
JWT_SECRET=your_jwt_secret_key
MONGODB_URI=mongodb://localhost:27017/your_database
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=your_redis_password
GOOGLE_AI_KEY=your_google_ai_api_key
```

### Frontend (.env)
```env
VITE_API_URL=http://localhost:3000
```

## Usage

1. **Register/Login**: Create an account or log in
2. **Create Project**: Start a new coding project
3. **Add Collaborators**: Invite friends to join your project
4. **Chat**: Communicate in real-time with team members
5. **AI Assistance**: Ask AI to generate code or explain concepts
6. **Code Editor**: Write and edit code files
7. **Run Code**: Execute JavaScript code in-browser

## API Endpoints

### Authentication
- `POST /users/register` - User registration
- `POST /users/login` - User login
- `GET /users/profile` - Get user profile
- `GET /users/logout` - Logout user

### Projects
- `POST /projects/create` - Create new project
- `GET /projects/all` - Get all user projects
- `PUT /projects/add-user` - Add users to project
- `GET /projects/get-project/:projectId` - Get project details
- `PUT /projects/update-file-tree` - Update project file tree

### AI
- `GET /ai/get-result?prompt=<prompt>` - Generate code/response from AI

## Socket Events

- `project-message` - Send/receive chat messages
- `user-joined` - User joined project
- `user-left` - User left project

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the ISC License.</content>
<parameter name="filePath">c:\Users\as\Downloads\soen\soen\README.md