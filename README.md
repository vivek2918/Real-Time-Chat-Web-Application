# Real-Time Chat Web Application

A real-time chat web application built using Spring Boot, WebSocket, and STOMP protocol. Users can join the chat, send messages, and see who is online or has left the chat.

## Features

- Real-time messaging
- User join/leave notifications
- Simple and responsive UI
- Built using Spring Boot and WebSocket

## Technology Stack

- **Backend**: Spring Boot, WebSocket, STOMP
- **Frontend**: HTML, CSS, JavaScript
- **Build Tool**: Maven
- **Database**: In-memory (if required in future)

## Endpoints

### WebSocket Endpoints

- **Connect to WebSocket**
  - **URL**: `/ws`
  - **Protocol**: WebSocket
  - **Description**: The endpoint for WebSocket connections.

### STOMP Messaging Endpoints

- **Send Message**
  - **URL**: `/app/chat.sendMessage`
  - **Method**: `SEND`
  - **Payload**:
    ```json
    {
      "sender": "username",
      "content": "Your message",
      "type": "CHAT"
    }
    ```
  - **Description**: Sends a chat message to the public chat room.

- **Add User**
  - **URL**: `/app/chat.addUser`
  - **Method**: `SEND`
  - **Payload**:
    ```json
    {
      "sender": "username",
      "type": "JOIN"
    }
    ```
  - **Description**: Adds a user to the chat and notifies others in the chat room.
 
## Application URL

- **Access the Application**: After starting the application, you can access the chat application at: `http://localhost:8080/index.html`

## Frontend Structure

- `src/main/resources/static/index.html`: The main HTML file for the chat application.
- `src/main/resources/static/css/main.css`: The CSS file for styling the chat application.
- `src/main/resources/static/js/main.js`: The JavaScript file for handling WebSocket connections and chat functionality.


### Key Addition:
- Added a section titled **Application URL** to clearly mention how to access the application after it's started.

Feel free to adjust any specific details to fit your project! Let me know if you need further modifications.


