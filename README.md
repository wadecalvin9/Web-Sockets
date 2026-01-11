# WebSocket Chat Application

Visit Live url at https://wadecalvin9.github.io/Web-Sockets/

A simple, real-time chat application built with Node.js and Native WebSockets. This project demonstrates how to create a bi-directional communication channel between a client (browser) and a server.

## Features

- **Real-time Communication**: Messages are delivered instantly between the server and connected clients.
- **Connection Status**: Visual indicators show real-time connection status (Connecting, Connected, Disconnected).
- **Responsive Design**: A clean, dark-themed UI that works well on different screen sizes.
- **Interactive UI**:
    - Message history with distinct styling for client and server messages.
    - Auto-scrolling to the latest message.
    - Input validation and disabled states when disconnected.

## Tech Stack

- **Backend**: Node.js, `ws` (WebSocket library).
- **Frontend**: HTML5, CSS3 (Flexbox, Animations), Vanilla JavaScript.
- **Design**: Custom CSS with Inter font.

## Getting Started

Follow these instructions to set up and run the project locally.
- you can customize it as you want right now it just returns an echo of your message from the server you can create rooms and have realtime communication between individuals or groups 

### Prerequisites

- [Node.js](https://nodejs.org/) (v12 or higher recommended)
- [npm](https://www.npmjs.com/) (usually comes with Node.js)

### Installation

1.  Clone the repository or download the source code.
2.  Navigate to the project directory:
    ```bash
    cd websock
    ```
3.  Install the dependencies:
    ```bash
    npm install
    ```

### Running the Application

1.  **Start the WebSocket Server:**

    ```bash
    npm start
    ```
    
    The server will start on port `8080` (or the port defined in your `.env` file). You should see:
    ```
    WebSocket server running on port 8080
    ```

2.  **Open the Client:**

    Simply open the `index.html` file in your web browser. Do not just drag and drop it, it is better to serve it, but for this simple example, opening the file directly usually works. 
    
    *Note: The current `index.html` is hardcoded to connect to `wss://websocks-gabghbgccncschfk.centralindia-01.azurewebsites.net`. To run it locally against your own server, you will need to update the connection URL.*

## Configuration

### Local Development

To connect the frontend to your local server, open `index.html` and find line ~285:

```javascript
// const ws = new WebSocket('wss://websocks-gabghbgccncschfk.centralindia-01.azurewebsites.net');
const ws = new WebSocket('ws://localhost:8080'); // Change to this for local dev
```

### Environment Variables

The server checks for a `PORT` environment variable. You can specify it in a `.env` file (if you add `dotenv` support) or set it in your shell.

## Project Structure

- `server.js`: The main entry point for the Node.js WebSocket server. Handles connections and message broadcasting.
- `index.html`: The frontend client containing the HTML structure, CSS styles, and client-side JavaScript logic.
- `package.json`: Project metadata and dependencies.


