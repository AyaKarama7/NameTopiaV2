# NameTopia

A real-time multiplayer room-based game platform built with C# and .NET 8, featuring a Windows Forms client and a multi-threaded TCP server.

---

## Tech Stack

- **Language:** C# 12
- **Framework:** .NET 8
- **UI:** Windows Forms
- **Networking:** TCP Sockets
- **Serialization:** Newtonsoft.Json
- **Shared Models:** SharedClasses project

---

## Architecture

NameTopia uses a client-server architecture. The server manages player connections, rooms, and categories, while the client provides a responsive Windows Forms interface for users to create, join, or spectate game rooms. Communication is handled via TCP sockets using JSON-serialized commands and shared DTOs.

---

## Features

- **Real-time Room Management:**  
  Players can create, join, or spectate rooms, with live updates on room status and participants.

- **Dynamic Category Loading:**  
  Game categories are loaded from server-side resources and presented to users when creating rooms.

- **Graceful Connection Handling:**  
  Both client and server handle connection closures and errors robustly, ensuring a smooth user experience.

- **Responsive UI:**  
  The client provides a modern, interactive interface for managing rooms and player actions.

---

## Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- Visual Studio 2022 or later

### Build & Run

1. **Clone the repository** and open the solution in Visual Studio.
2. **Build the solution** to restore NuGet packages and compile all projects.
3. **Start the server:**
   - Set `NameTopia` as the startup project.
   - Run the server (it listens on `127.0.0.1:5001` by default).
4. **Start the client:**
   - Set `Client` as the startup project.
   - Run the client and connect using your desired player name.

### Directory Structure

- `NameTopia/` - Server project
- `Client/` - Windows Forms client
- `SharedClasses/` - Shared DTOs and enums for communication

---

## Usage

- **Connect:** Enter your name in the client and connect to the server.
- **Create Room:** Click "Create Room" and select a category.
- **Join/Spectate:** Browse available rooms and join or spectate as desired.
- **Close:** Use the close button to disconnect gracefully.

---

## Customization

- **Categories:**  
  Add or remove category files in the `Categories` directory on the server. The server will automatically load available categories at startup.

---


