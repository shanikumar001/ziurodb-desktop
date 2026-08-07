# 🛰️ ziuroDB Local Agent Guide

The ziuroDB Local Agent is a secure, standalone tunnel that allows the ziuroDB cloud dashboard to interact with databases running on your private network (like `localhost`).

## 🛠️ How it Works

The agent uses a **Reversed WebSocket Tunnel** (Socket.io) to bridge the gap between your local environment and the ziuroDB backend.

1.  **Authentication**: The agent connects to the ziuroDB backend using a secure `AGENT_ID` and `AGENT_TOKEN`.
2.  **Persistent Tunnel**: Once connected, it maintains an active WebSocket.
3.  **Command Execution**: When you run a query on the ziuroDB dashboard, the backend sends a "command" through the tunnel. The agent executes this command against your local database (MongoDB, MySQL, or PostgreSQL) and sends the results back.
4.  **Security**: Your database credentials and data never "sit" on our servers; they are only passed through the agent's memory during active requests.

## 📦 Technologies Used

- **Node.js & TypeScript**: Core runtime and language.
- **Socket.io-client**: For the real-time tunnel.
- **Database Adapters**:
  - `mongodb`: Native MongoDB driver.
  - `mysql2`: Promise-based MySQL driver.
  - `pg`: Non-blocking PostgreSQL driver.
- **Adm-Zip**: Used by the backend to pack the agent into a zero-config bundle.

## Getting Started

### Prerequisites

- **Node.js (v18 or higher)**: Required to run the agent. [Download here](https://nodejs.org/).

### 1. Download & Extract

Download the **"Pre-configured Bundle"** from the ziuroDB Connections page. This ZIP contains everything you need, including your pre-filled `config.json`. Extract it to a folder of your choice.

### 2. Initial Setup (First Time)

#### 🍎 macOS / Linux

Open your Terminal, navigate to the folder, and run:

```bash
# Give execution permission to the script
chmod +x start.sh

# Start the agent
./start.sh
```

#### 🪟 Windows

Open Command Prompt or PowerShell, navigate to the folder, and run:

```cmd
start.bat
```

_(Alternatively, you can just double-click `start.bat` in File Explorer)_

### 3. What happens next?

- The script will automatically run `npm install` to download dependencies.
- The agent will initialize and show a **"✅ Tunnel Online"** message.
- Your dashboard status will turn **Online**.

## 🌙 Running in the Background

If you want the agent to stay online even after you close your terminal window, use one of the following methods:

### Option 1: Using `nohup` (Mac/Linux)

This is the quickest way to keep the process running after logout:

```bash
nohup ./start.sh > agent.log 2>&1 &
```

The agent logs will be saved to `agent.log`.

### Option 2: Using `PM2` (Recommended for Stability)

PM2 is a production process manager that can automatically restart the agent if it crashes.

```bash
# Install PM2 globally (Mac/Linux users may need sudo)
sudo npm install -g pm2

# Start the agent using the npm wrapper (most reliable)
pm2 start npm --name ziuroDB-agent -- start

# Monitor logs
pm2 logs ziuroDB-agent
```

### Managing the Background Agent

Once your agent is running in PM2, use these commands to control it:

- **Check Status**: `pm2 status`
- **Stop**: `pm2 stop ziuroDB-agent`
- **Restart**: `pm2 restart ziuroDB-agent`
- **View Logs**: `pm2 logs ziuroDB-agent`
- **Remove**: `pm2 delete ziuroDB-agent`

## 📋 Quick Reference Cheat Sheet

| Action               | Command (Mac/Linux)                           | Command (Windows)                             |
| :------------------- | :-------------------------------------------- | :-------------------------------------------- |
| **First-time Setup** | `chmod +x start.sh && ./start.sh`             | `start.bat`                                   |
| **Normal Start**     | `./start.sh`                                  | `start.bat`                                   |
| **Install PM2**      | `sudo npm install -g pm2`                     | `npm install -g pm2`                          |
| **Start Background** | `pm2 start npm --name ziuroDB-agent -- start` | `pm2 start npm --name ziuroDB-agent -- start` |
| **Stop Background**  | `pm2 stop ziuroDB-agent`                      | `pm2 stop ziuroDB-agent`                      |
| **See Live Logs**    | `pm2 logs ziuroDB-agent`                      | `pm2 logs ziuroDB-agent`                      |
| **Clean Background** | `pm2 delete ziuroDB-agent`                    | `pm2 delete ziuroDB-agent`                    |

## 🔄 Reconnecting

You do **not** need to create a new agent or download a new bundle if you go offline. Simply run the same `start.sh` or `start.bat` script whenever you want to bring the agent back online.

## 📁 File Structure

- `index.ts`: The core logic of the agent.
- `config.json`: Contains your `AGENT_ID`, `AGENT_TOKEN`, and `BACKEND_URL`.
- `adapters/`: Contains the database-specific logic.
- `start.sh` / `start.bat`: The automation scripts for easy startup.
