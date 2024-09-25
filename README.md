# Chat App Backend

This is the backend for a chat application built with Node.js and Express. It provides the necessary API endpoints to manage users, rooms, and messages.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Authentication](#authentication)
- [Database](#database)
- [Environment Variables](#environment-variables)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/your-username/chat-app-backend.git
   ```
2. Install dependencies:
   ```
   cd chat-app-backend
   npm install
   ```
3. Start the development server:
   ```
   npm run dev
   ```

## Usage

To start the development server, run the following command:

```
npm run dev
```

## API Endpoints

### Authentication

- `POST /api/auth/register`: Register a new user.
- `POST /api/auth/login`: Log in to the application.
- `POST /api/auth/logout`: Log out from the application.

### Users

- `GET /api/users`: Get all users.
- `GET /api/users/:id`: Get a user by ID.
- `PUT /api/users/:id`: Update a user by ID.
- `DELETE /api/users/:id`: Delete a user by ID.

### Rooms

- `GET /api/rooms`: Get all rooms.
- `GET /api/rooms/:id`: Get a room by ID.
- `POST /api/rooms`: Create a new room.
- `PUT /api/rooms/:id`: Update a room by ID.
- `DELETE /api/rooms/:id`: Delete a room by ID.

### Messages

- `GET /api/rooms/:roomId/messages`: Get all messages for a room.
- `POST /api/rooms/:roomId/messages`: Create a new message for a room.

## Authentication

Authentication is handled using JSON Web Tokens (JWT). The token is sent in the Authorization header as a Bearer token.

## Database

The application uses a PostgreSQL, Kafka and Redis to store user and room data.

## Environment Variables

Create a `.env` file in the root of the project and set the following environment variables:

- `PORT`: The port number to run the server on.
- `DB_HOST`: The host address of the PostgreSQL database.
- `DB_PORT`: The port number to connect to the PostgreSQL database.
- `DB_USER`: The username to connect to the PostgreSQL database.
- `DB_PASSWORD`: The password to connect to the PostgreSQL database.
- `DB_NAME`: The name of the PostgreSQL database.
- `KAFKA_BROKER`: The address of the Kafka broker.
- `REDIS_HOST`: The host address of the Redis server.
- `REDIS_PORT`: The port number to connect to the Redis server.
- `JWT_SECRET`: The secret used to sign the JWT tokens.
- `JWT_EXPIRES_IN`: The duration for which the JWT token remains valid (in seconds).

## Contributing

Contributions are welcome! Please feel free to submit a PR.

## License

This project is licensed under the ISC License.
