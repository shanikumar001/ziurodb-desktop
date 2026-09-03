# ZiuroDB

ZiuroDB is a modern, high-performance, cross-platform database administration platform designed for connecting, exploring, querying, and managing multiple database engines—including MongoDB, MySQL, PostgreSQL, Redis, and Firebase—from a unified interface.

Built on Electron, React, and TypeScript, ZiuroDB Desktop integrates a native AI Copilot powered directly by Groq LLM engines, a universal query language engine (ZQL), an automated Database-to-REST API generator, and an enterprise-grade dark monochrome interface.

---

## Release Notes — ZiuroDB Desktop v1.0.1

### Native Ziuro AI Copilot (v2.0)
- **Direct Groq REST API Integration**: Calls the Groq LLaMA-3-70B engine directly from the application layer, eliminating external proxy latency for sub-second AI responses.
- **Automated Query Diagnosis & Retry Loop**: Features an automated query execution loop with 5-retry resilience. When a query fails, Ziuro AI analyzes the exact error stack and provides actionable, step-by-step fix recommendations.
- **Dual Query & Chat Modes**: Toggle between conversational AI assistant mode and strict code output mode for SQL, ZQL, MongoDB aggregation pipelines, and Redis commands.
- **Session History Persistence**: In-memory session tracking with instant history recall across Query Console tabs.

### Interface & Aesthetics Polish
- **Ergonomic Copilot Sidebar**: Positioned on the left side of the Query Console for efficient side-by-side query composition and AI assistance.
- **Monochrome Pure Dark Theme**: High-contrast pure dark interface (`dark:bg-black`) with clean borders, active indicator badges, and optimized contrast.
- **Toolbar & Header Optimization**: Icon-only toolbar controls and smart connection title truncation to prevent layout overflow on smaller displays.

### Build & Distribution Pipeline
- Clean release builds compiled for macOS (Apple Silicon and Intel), Windows (Universal, x64, ia32), and Linux (AppImage, DEB, RPM).
- Automated application bundle updates for macOS distributions.

---

## Core Features

- **Multi-Database Management**: Connect to MongoDB, MySQL, PostgreSQL, Redis, and Firebase within a single workspace.
- **Universal Query Console**: Execute raw SQL, NoSQL queries, or ZQL (ZiuroDB Query Language) with sub-millisecond execution and formatted result grids.
- **Database-to-REST API Engine**: Convert any database collection or table into a secure, RESTful API endpoint with a single click.
- **Schema Intelligence**: Automatic schema discovery, field type detection, index inspection, and structural visualization.
- **Local-First Security**: Connection strings, secrets, and credentials are encrypted locally using 256-bit encryption before storage.
- **Export & Import**: Export query results into JSON, CSV, or raw SQL inserts.

---

## Downloads & Installation

ZiuroDB Desktop binaries are available for all major operating systems. Download the latest installer for your system from the [GitHub Releases](https://github.com/shanikumar001/ziurodb-desktop/releases) section.

### Operating System Support

| Operating System | Supported Architecture | Download Formats |
| :--- | :--- | :--- |
| **macOS** | Apple Silicon (M1 / M2 / M3 / M4) & Intel x64 | `.dmg`, `.zip` |
| **Windows** | Windows 10 & 11 (x64, ia32, Universal) | `.exe` Installer |
| **Linux** | Ubuntu, Debian, Fedora, RedHat, Arch | `.AppImage`, `.deb`, `.rpm` |

### Installation Instructions

#### macOS
1. Download the `.dmg` file matching your CPU architecture (Apple Silicon or Intel).
2. Double-click the downloaded `.dmg` file.
3. Drag **ZiuroDB Desktop** into your **Applications** folder.
4. Launch ZiuroDB Desktop from Launchpad or Spotlight.

#### Windows
1. Download the `ZiuroDB-Desktop-Setup-1.0.1.exe` installer.
2. Run the executable and follow the setup wizard.
3. Launch ZiuroDB Desktop from the Start Menu or Desktop shortcut.

#### Linux
- **AppImage**: Grant execution permissions (`chmod +x ZiuroDB-Desktop-1.0.1.AppImage`) and run directly.
- **Debian / Ubuntu**: Install via `sudo dpkg -i ziurodb-desktop_1.0.1_amd64.deb`.
- **Fedora / RedHat**: Install via `sudo rpm -i ziurodb-desktop-1.0.1.x86_64.rpm`.

---

## Getting Started

### 1. Adding a Database Connection
1. Launch ZiuroDB Desktop.
2. Click **New Connection** on the sidebar.
3. Select your database engine (MongoDB, MySQL, PostgreSQL, Redis, or Firebase).
4. Enter your connection URI or host credentials.
5. Click **Test Connection** and save.

### 2. Using the Query Console & ZQL
- Open any connection from the left navigation panel.
- Select the **Query Console**.
- Choose your preferred query syntax (SQL, native MongoDB, or ZQL).
- Press `Ctrl + Enter` (or `Cmd + Enter` on macOS) to execute.

### 3. Using Ziuro AI Copilot
- Open the AI Copilot sidebar on the left side of the Query Console.
- Type natural language queries such as *"Find all active users created in the last 7 days"* or *"Optimize this SQL join query"*.
- Click **Apply Code** to inject the AI-generated query directly into your console.

---

## Documentation

Full technical documentation, architecture specs, and reference guides are included in the repository:

- [ZQL Command Reference](docs/zql-command.md) — Complete guide to ZiuroDB Query Language syntax and command structures.
- [API Documentation](docs/API.md) — Comprehensive API endpoint specifications and integration guides.
- [Data Storage Architecture](docs/DATA_STORAGE_ARCHITECTURE.md) — Technical overview of schema modeling and encryption.
- [AI Flow & Copilot Engine](docs/ai-flow.md) — Architecture of the Groq LLM integration and diagnostic loop.
- [Schema Intelligence Engine](docs/schema-intelligence.md) — Deep dive into auto-schema detection and indexing.
- [ZiuroDB AI Agent Specification](docs/AGENT.md) — Technical specification for AI agent interactions and tools.
- [Package Architecture](docs/ziurodb-package.md) — Detailed breakdown of package dependencies and build manifests.

---

## System Requirements

- **macOS**: macOS 10.15 (Catalina) or later.
- **Windows**: Windows 10 (64-bit) or later.
- **Linux**: Kernel 5.4+ with glibc 2.28+.
- **Hardware**: Minimum 4 GB RAM (8 GB recommended), 500 MB free disk space.

---

## Community & Resources

- **Source Code & Core Engine**: [https://github.com/shanikumar001/ziurodb](https://github.com/shanikumar001/ziurodb)
- **Desktop Releases Repository**: [https://github.com/shanikumar001/ziurodb-desktop](https://github.com/shanikumar001/ziurodb-desktop)
- **Official Website**: [https://ziurodb.com](https://ziurodb.com)

---

## License

ZiuroDB Desktop is licensed under the [MIT License](LICENSE).
