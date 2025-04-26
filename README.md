# Paper Plane Wars - Web Application

The web platform of the Paper Plane Wars game, including the React frontend and Node.js backend.

## About the Project

This repository contains the frontend and backend code necessary for the web platform version of the Paper Plane Wars game developed with Unity. It provides features like user accounts, multiplayer mode, and a payment system.

## Technology Stack

- **Frontend**: React.js (TypeScript)
- **Backend**: Node.js + Express
- **Database**: MongoDB
- **Real-time Communication**: Socket.io
- **Authentication**: JWT

## Installation

### Requirements

- Node.js 18.x or newer
- npm or yarn
- MongoDB (local or Atlas)

### Setting Up the Development Environment

1. Clone this repository:
    ```bash
    git clone https://github.com/flymp/Flymp_Web.git
    ```

2. Install dependencies:
    ```bash
    # At the root level
    npm install

    # Inside the client directory
    cd client
    npm install

    # Inside the server directory
    cd server
    npm install
    ```

3. Create a `.env` file:
    ```env
    # server/.env
    PORT=5000
    MONGODB_URI=mongodb://localhost:27017/flymp
    JWT_SECRET=supersecretkey
    ```

4. Start the application:
    ```bash
    # Start frontend in development mode
    cd client
    npm start

    # Start backend in development mode
    cd server
    npm run dev
    ```

## Project Structure
```
Flymp_Web/
├── client/                 # React frontend
│   ├── public/
│   │   └── unity/          # Unity WebGL build folder
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── services/
│       └── ...
├── server/                 # Node.js backend
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── socket/
│   │   └── ...
│   └── package.json
└── package.json            # Root package.json
```
## Branching Strategy

- `main`: Stable and production-ready releases
- `develop`: Ongoing development branch
- `feature/<feature-name>`: New feature development
- `bugfix/<bug-name>`: Bug fixes and patches

## Commit Guidelines

Use the following format for commit messages:

    [area]: Describe the action in the present tense

    - Detail 1
    - Detail 2

## Unity Integration

Unity WebGL build files should be placed in the `client/public/unity` directory. The React application will load and integrate the Unity game from this folder into the web page.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

