Implementation
=================

Overview
--------

This quiz game is quiz like game for multiple players that can be used in classrooms and lectures. It allows a host to create sessions with different kind of questions for students to join and answer. The game is designed to be interactive and engaging.

Architecture
------------

The project follows a client-server model:

- **Frontend**: Handles user interaction, question display, and answer selection.
- **Backend**: Manages game logic, player sessions, and real-time communication.
- **Database**: Stores questions, player data, and game sessions.

Key Components
--------------

- **Lobby**:
  - Players can join a game using a room code.
  - The host starts the game once all players have joined.

- **Questions**:
  - Loads different type of questions from a database or JSON file.
  - Sends questions to all connected players simultaneously.
  - Times each question and locks in answers after the timer expires.

Data Flow
---------

1. Host creates a game session → server generates room or QR code.
2. Players join using the room or QR code → server adds them to the session.
3. Host starts the quiz → server broadcasts questions.
4. Players answer → server records them.
5. Final → server sends results to all clients.

Technologies Used
-----------------

- **Frontend**: [Dart]
- **Backend**: [e.g., Python with Flask, Flask-SocketIO]
- **Database**: [e.g., SQLite, MongoDB, JSON file]

