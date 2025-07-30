# ♟️ Multiplayer Terminal Chess Engine

A fully-functional, terminal-based multiplayer chess engine written in modern C++. This project focuses on strong object-oriented design and utilizes key software design patterns such as **Strategy**, **Factory**, **Mediator**, and **Singleton** to model a real-time, interactive, and extendable multiplayer chess system.

## 📌 Features

- ✅ Complete standard chess rules (legal moves, checks, checkmate, castling, en passant, promotion)
- 🤝 Multiplayer support via terminal (matchmaking + messaging)
- 🧠 Object-oriented design using SOLID principles
- 🏗️ Design patterns used:
  - Strategy Pattern (for piece movement logic, matchmaking strategies)
  - Factory Pattern (to create chess pieces)
  - Singleton Pattern (for game and matchmaking session management)
  - Mediator Pattern (for player-to-player chat/messaging)
- 🧪 Valid move checking and turn-based control
- 💬 In-game terminal-based chat
- ♻️ Easily extendable for GUI or network support in the future

---

## 🧱 Architecture

### 🗂️ High-Level Components

- `Game`: Singleton managing game lifecycle
- `Board`: 8x8 grid with Piece* pointers
- `Piece` and derived classes (King, Queen, Rook, etc.)
- `User`, `Player`, `Match`
- `MatchmakingSystem`: Strategy pattern used here
- `PieceFactory`: Factory to create appropriate pieces
- `ChatMediator`: Mediator for messaging
- `Position`: Utility class to manage board coordinates

### 🔁 Design Patterns Used

<table>
  <thead>
    <tr>
      <th>Pattern</th>
      <th>Applied In</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Strategy</td>
      <td>Movement logic, Matchmaking</td>
      <td>Enables flexible and interchangeable movement logic per piece and matchmaking rules</td>
    </tr>
    <tr>
      <td>Factory</td>
      <td>Piece creation</td>
      <td>Decouples creation logic from the Board setup logic</td>
    </tr>
    <tr>
      <td>Singleton</td>
      <td>GameManager, MatchmakingSystem</td>
      <td>Ensures centralized control and single-point game instance</td>
    </tr>
    <tr>
      <td>Mediator</td>
      <td>Chat functionality</td>
      <td>Manages communication between players without tight coupling</td>
    </tr>
  </tbody>
</table>

