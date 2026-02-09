**HiveBoard**
A collaborative whiteboard application designed for creatives, enabling real-time drawing, brainstorming, and project collaboration.

**Features**
Real-time Collaboration: Draw and edit on a shared canvas with multiple users simultaneously using WebSockets.
User Authentication: Secure login and registration with email/password and Google OAuth.
Canvas Tools: Comprehensive drawing tools including pens, shapes, text, and more.
AI Integration: Built-in AI chat for creative assistance and idea generation.
Meeting Management: Schedule and manage virtual meetings within the platform.
Room-based Sessions: Create and join rooms for organized collaboration.
Responsive Design: Optimized for desktop and mobile devices.
Dark/Light Mode: Theme switching for user preference.

**Tech Stack**

**Frontend**
React with TypeScript
Vite for build tooling
Tailwind CSS for styling
ShadCN UI for component library
Socket.io Client for real-time communication
React Router for navigation
Framer Motion for animations

**Backend**
Node.js with Express
MongoDB with Mongoose for database
Socket.io for real-time features
Passport.js for authentication
JWT for token-based auth
Google OAuth for social login

**DevOps**
Docker for containerization
GitHub Actions for CI/CD
ESLint for code linting

**Installation
Prerequisites**
Node.js (v18 or higher)
MongoDB (local or cloud instance)
Docker (optional, for containerized setup)
Backend Setup
Navigate to the server directory:


cd server
Install dependencies:


npm install
Create a .env file in the server directory with the following variables:


PORT=5000
MONGODB_URI=mongodb://localhost:27017/hiveboard
JWT_SECRET=your_jwt_secret
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GEMINI_API_KEY=your_gemini_api_key
Start the backend server:


npm run dev
Frontend Setup
Navigate to the root directory:


cd ..
Install dependencies:


npm install
Start the development server:


npm run dev
The application will be available at http://localhost:5173 (frontend) and http://localhost:5000 (backend API).

Docker Setup (Optional)
Ensure Docker and Docker Compose are installed.
Run the application using Docker Compose:

docker-compose up --build

**Usage**
Registration/Login: Create an account or log in using email/password or Google OAuth.
Create a Room: Start a new collaborative session by creating a room.
Invite Participants: Share the room link to invite others to join.
Drawing: Use the toolbar to draw, add shapes, text, and collaborate in real-time.
AI Chat: Access the AI panel for creative suggestions and assistance.
Meetings: Schedule and join meetings within the platform.

**API Documentation**
Authentication Endpoints
POST /api/auth/register - User registration
POST /api/auth/login - User login
GET /api/auth/google - Google OAuth initiation
GET /api/auth/logout - User logout
Meeting Endpoints
GET /api/meetings - Get user's meetings
POST /api/meetings - Create a new meeting
PUT /api/meetings/:id - Update a meeting
DELETE /api/meetings/:id - Delete a meeting
Room Endpoints
GET /api/rooms - Get user's rooms
POST /api/rooms - Create a new room
GET /api/rooms/:id - Get room details
AI Endpoints
POST /api/ai/chat - Send message to AI
GET /api/ai/history - Get chat history
For detailed API documentation, refer to the Postman collection or Swagger docs (if implemented).

Contributing
Fork the repository
Create a feature branch: git checkout -b feature/your-feature-name
Commit your changes: git commit -m 'Add some feature'
Push to the branch: git push origin feature/your-feature-name
Open a pull request
Please ensure all tests pass and code follows the project's linting rules.

Testing
Run tests using:


npm test
For backend tests, navigate to the server directory and run:


npm test
