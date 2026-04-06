# Chat App

A simple real-time chat application built with Node.js, Express, Socket.IO, and SQLite.

## Description

This project demonstrates a basic chat application where users can send and receive messages in real-time. Messages are persisted in an SQLite database, allowing for message recovery upon reconnection. The app uses WebSockets via Socket.IO for efficient real-time communication between the client and server.

## Technologies Used

- **Node.js**: JavaScript runtime for the server-side logic.
- **Express**: Web framework for handling HTTP requests and serving static files.
- **Socket.IO**: Library for real-time, bidirectional communication between web clients and servers using WebSockets.
- **SQLite**: Lightweight database for storing chat messages.
- **HTML/CSS/JavaScript**: Client-side interface for the chat functionality.

## Features

- Real-time messaging: Messages are sent and received instantly without page refreshes.
- Message persistence: All messages are stored in an SQLite database.
- Connection recovery: Upon reconnection, users can retrieve missed messages.
- Simple UI: Clean, responsive interface with a message list and input form.
- Disconnect/Connect toggle: Button to manually disconnect or reconnect to the chat server.

## Installation

1. Ensure you have Node.js installed on your system. You can download it from [nodejs.org](https://nodejs.org/).

2. Clone or download this repository to your local machine.

3. Navigate to the project directory:
   ```
   cd chat-app
   ```

4. Install the dependencies:
   ```
   npm install
   ```

## Running the Application

1. Start the server:
   ```
   node index.js
   ```

2. Open your web browser and go to `http://localhost:3000`.

3. Start chatting! Open multiple browser tabs or windows to simulate multiple users.

## How It Works

- The server (index.js) sets up an Express server and Socket.IO instance.
- It creates an SQLite database table to store messages.
- When a client connects, it listens for "chat message" events and broadcasts them to all connected clients while saving to the database.
- The client (index.html) uses Socket.IO to connect to the server, send messages, and display received messages.
- CSS styles the chat interface for a modern look.

## License

This project is licensed under the ISC License.