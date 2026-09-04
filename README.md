# ZiuroDB - Universal AI Database Workspace

> **ZiuroDB** is a modern, high-performance, unified AI database administration workspace and query compilation engine designed to explore, query, design, manage, and convert multiple database engines—including **PostgreSQL**, **MySQL**, **MongoDB**, **Firebase (Cloud Firestore & RTDB)**, **Supabase**, **Redis**, and **Cloudinary**—into secure REST APIs and sub-second intelligent queries.

---

## Quick Links & Ecosystem

| Resource | URL | Description |
| :--- | :--- | :--- |
| **Official Website** | [https://ziurodb.com](https://ziurodb.com) | Official landing page, features overview, and ecosystem portal |
| **ZiuroDB Lite (Web App)** | [https://lite.ziurodb.com](https://lite.ziurodb.com) | Zero-installation online web client running directly in your browser |
| **Official Documentation** | [https://docs.ziurodb.com](https://docs.ziurodb.com) | Complete user guides, API references, ZQL specifications, and tutorials |
| **GitHub Releases** | [GitHub Releases](https://github.com/shanikumar001/ziurodb/releases) | Official desktop binary downloads for macOS, Windows, and Linux |
| **Core Engine Repo** | [https://github.com/shanikumar001/ziurodb-dev](https://github.com/shanikumar001/ziurodb-dev) | Core full-stack repository, backend services, and CLI tools |

---

## ZiuroDB Desktop vs. ZiuroDB Lite

ZiuroDB provides two distinct, seamlessly synchronized editions tailored for developers, database engineers, and teams:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                                    ZIURODB PLATFORM                                    │
├───────────────────────────────────────────┬────────────────────────────────────────────┤
│             ZIURODB DESKTOP               │                ZIURODB LITE                │
│       (Native Cross-Platform App)         │         (Zero-Install Browser App)         │
├───────────────────────────────────────────┼────────────────────────────────────────────┤
│ • Native Electron 33 runtime              │ • Instant access at lite.ziurodb.com       │
│ • Direct native DB driver bridges         │ • Runs in any modern browser               │
│ • Local storage pools & media server      │ • Zero software download required          │
│ • Offline SQLite and local disk files     │ • Connects to cloud and hosted DBs         │
│ • Local AES-256 encrypted credential store│ • Connects to localhost DBs via Local Agent│
│ • Auto-update engine (macOS, Win, Linux)  │ • Always up-to-date automatically          │
└───────────────────────────────────────────┴────────────────────────────────────────────┘
```

### ZiuroDB Desktop
**ZiuroDB Desktop** is a native, heavyweight desktop application built on Electron 33, React 18, and TypeScript. It includes direct database driver socket bridges, offline SQLite support, local storage node allocation, an embedded HTTP media streaming server (`http://localhost:19876`), and local AES-256 encrypted credentials storage (`electron-store`).

### ZiuroDB Lite
**ZiuroDB Lite** ([lite.ziurodb.com](https://lite.ziurodb.com)) is the official, zero-installation browser web client for ZiuroDB. It allows developers to connect, explore, query, and manage cloud-hosted databases (MongoDB Atlas, Supabase, Neon, AWS RDS, PlanetScale, Firebase) or local databases (via the **ZiuroDB Local Agent tunnel**) directly inside any web browser on any machine.

---

## Key Features

### 1. Universal Multi-Database Management
- Connect to **PostgreSQL**, **MySQL**, **MongoDB**, **Firebase (Firestore & Realtime Database)**, **Supabase**, **Redis**, and **Cloudinary** from a single workspace.
- Seamlessly explore database schemas, tables, collections, document trees, indexes, and constraints.
- Inline data editor: Edit table rows and NoSQL documents directly in the interactive data grid.

### 2. Ziuro-AI & Schema Intelligence Knowledge Graph
- **Sub-Second AI Query Generation:** Trims prompt context by **99.5%** (~180 tokens vs. ~38,000 tokens) using 1-hop sub-graph extraction for response times under **500 milliseconds**.
- **Deep Hierarchical Schema Inference:** Recursively inspects nested sub-documents and arrays of objects (e.g. `students.marks: [{ subject, mark }]`) to build clean prototype schemas with MongoDB `$unwind`/`$group` guardrails.
- **Persistent Schema Memory & Cache:** Retains hierarchical database knowledge (`Connection -> Database -> Collection/Table -> Fields`) across sessions with incremental delta merging.
- **7 Automated Schema Health Rules:** Evaluates missing indexes on foreign keys, wide tables, circular references, and deep NoSQL nesting to generate a 0–100 Schema Health Score.

### 3. Universal Ziuro Query Language (ZQL)
- Query any database using a standardized hierarchical model: `Database -> Tree (Table/Collection) -> Branch (Row/Document) -> Leaf (Field/Value)`.
- Compiles ZQL AST statements into optimized native SQL dialects (`SELECT`, `INSERT`, `UPDATE`) or MongoDB BSON pipelines (`find`, `aggregate`, `updateOne`).
- Interactive Live Playground with multi-dialect transpilation.

### 4. Instant Database-to-REST API Engine v2.0
- Convert any database connection into a high-performance REST API with clean JSON document formatting:
  - `POST /api/v1/public/query` — Single query execution with auto-parsed data types.
  - `POST /api/v1/public/batch` — Concurrent execution of up to 20 queries with unique ID mapping.
  - `POST /api/v1/public/transaction` — Multi-query atomic transactions with automated rollback on failure.

### 5. Monaco Query Console
- Full-featured SQL and NoSQL query editor powered by the industry-standard Monaco Editor.
- Multi-query execution tabs with individual execution time and row metadata.
- Syntax highlighting, auto-formatting (`Shift+Option+F` or `Shift+Alt+F`), bracket matching, and keyboard shortcut execution (`Cmd+Enter` / `Ctrl+Enter`).

### 6. Secure Reverse WebSocket Local Agent
- Connect databases on `localhost` or behind private VPNs/firewalls to ZiuroDB Cloud or ZiuroDB Lite.
- Uses reverse WebSockets (Socket.io) with one-time token authentication.
- Zero inbound firewall ports required; database credentials never leave your local machine memory.

### 7. Decentralized Storage Pool & Peer-to-Peer Cloud
- Share unused disk space to earn passive income (Rs. 2.40/GB/month) with AES-256-GCM encrypted chunks.
- Deploy managed cloud databases with 3x fault-tolerant replication across storage provider nodes.
- Built-in media library with local asset streaming HTTP server on port `19876`.

---

## Release Notes — ZiuroDB v1.0.7 (Latest Update)

### What is New in v1.0.7:
- **Deep Hierarchical Schema Intelligence:** Added recursive inspection for complex nested documents and arrays of objects in MongoDB, eliminating aggregation crashes.
- **Persistent AI Schema Memory & Settings Management:** Added a dedicated AI Schema Memory Cache Manager in Settings to inspect cached trees, re-sync schemas, and manage cache sizes per connection.
- **ZQL Direct Script Execution Fallback:** Added native fallback support for complex multi-line data generation scripts with `const`, `for` loops, and `insertMany`.
- **Electron 33 & Build Optimizations:** Upgraded to Electron 33.2.1 with updated native module rebuilds for macOS (Apple Silicon `arm64` and Intel `x64`), Windows (`x64`), and Linux (`AppImage`, `deb`, `rpm`).
- **Enhanced Auto-Updater Integration:** Seamless auto-update verification and blockmap generation for macOS, Windows, and Linux releases.

---

## Downloads & Installation (v1.0.7)

ZiuroDB Desktop binaries are available for all major operating systems. Download the installer for your system below:

### Direct Download Links (v1.0.7 Release)

| Operating System | Architecture | Package Format | Direct Download Link |
| :--- | :--- | :--- | :--- |
| **macOS** (Apple Silicon) | M1 / M2 / M3 / M4 (`arm64`) | **DMG Installer** | [Download `ZiuroDB-1.0.6-mac-arm64.dmg`](https://github.com/shanikumar001/ziurodb/releases/download/v1.0.7/ZiuroDB-1.0.6-mac-arm64.dmg) |
| **macOS** (Apple Silicon) | M1 / M2 / M3 / M4 (`arm64`) | **ZIP Archive** | [Download `ZiuroDB-1.0.6-mac-arm64.zip`](https://github.com/shanikumar001/ziurodb/releases/download/v1.0.7/ZiuroDB-1.0.6-mac-arm64.zip) |
| **macOS** (Intel) | Intel 64-bit (`x64`) | **DMG Installer** | [Download `ZiuroDB-1.0.6-mac-x64.dmg`](https://github.com/shanikumar001/ziurodb/releases/download/v1.0.7/ZiuroDB-1.0.6-mac-x64.dmg) |
| **macOS** (Intel) | Intel 64-bit (`x64`) | **ZIP Archive** | [Download `ZiuroDB-1.0.6-mac-x64.zip`](https://github.com/shanikumar001/ziurodb/releases/download/v1.0.7/ZiuroDB-1.0.6-mac-x64.zip) |
| **Windows** | Windows 10 / 11 (64-bit) | **Setup EXE** | [Download `ZiuroDB-1.0.6-win-x64.exe`](https://github.com/shanikumar001/ziurodb/releases/download/v1.0.7/ZiuroDB-1.0.6-win-x64.exe) |
| **Linux** | Universal 64-bit | **AppImage** | [Download `ZiuroDB-1.0.6-linux-x86_64.AppImage`](https://github.com/shanikumar001/ziurodb/releases/download/v1.0.7/ZiuroDB-1.0.6-linux-x86_64.AppImage) |
| **Linux** (Debian / Ubuntu) | `amd64` | **DEB Package** | [Download `ZiuroDB-1.0.6-linux-amd64.deb`](https://github.com/shanikumar001/ziurodb/releases/download/v1.0.7/ZiuroDB-1.0.6-linux-amd64.deb) |
| **Linux** (Fedora / RHEL) | `x86_64` | **RPM Package** | [Download `ZiuroDB-1.0.6-linux-x86_64.rpm`](https://github.com/shanikumar001/ziurodb/releases/download/v1.0.7/ZiuroDB-1.0.6-linux-x86_64.rpm) |

> You can also browse all version tags and source archives on the [GitHub Releases Page](https://github.com/shanikumar001/ziurodb/releases).

---

### Installation Instructions

#### macOS Installation
1. Download the `.dmg` file matching your Mac architecture (**Apple Silicon** for M1/M2/M3/M4 or **Intel** for older Macs).
2. Double-click the downloaded `.dmg` file to mount it.
3. Drag the **ZiuroDB** icon into your **Applications** folder.
4. Launch ZiuroDB from Spotlight or Launchpad.

#### Windows Installation
1. Download `ZiuroDB-1.0.7-win-x64.exe`.
2. Double-click the installer and follow the setup wizard.
3. Launch ZiuroDB from your Desktop shortcut or Start Menu.

#### Linux Installation

**Using AppImage (Universal):**
```bash
# 1. Make the AppImage executable
chmod +x ZiuroDB-1.0.7-linux-x86_64.AppImage

# 2. Run ZiuroDB
./ZiuroDB-1.0.7-linux-x86_64.AppImage
```

**Using Debian / Ubuntu (.deb):**
```bash
sudo dpkg -i ZiuroDB-1.0.7-linux-amd64.deb
sudo apt-get install -f # Fix any missing dependencies
```

**Using Fedora / RHEL / CentOS (.rpm):**
```bash
sudo rpm -i ZiuroDB-1.0.7-linux-x86_64.rpm
```

---

## In-Depth Documentation

Detailed technical guides and architectural specifications are located in the `docs/` directory:

- [ZQL Command Reference](docs/zql-command.md) — Complete reference for the ZiuroDB Query Language syntax and operations.
- [API Engine Documentation](docs/API.md) — Specifications for the Database-to-REST API Engine (`/query`, `/batch`, `/transaction`).
- [Schema Intelligence Engine](docs/schema-intelligence.md) — Technical deep dive into the Knowledge Graph and health score analyzer.
- [AI Flow Architecture](docs/ai-flow.md) — End-to-end documentation of Ziuro-AI, prompt trimming, and Groq LLM integration.
- [Data Storage Architecture](docs/DATA_STORAGE_ARCHITECTURE.md) — Storage mechanics of schema graphs and desktop storage pools.
- [Local Agent Guide](docs/AGENT.md) — Guide on deploying the standalone reverse WebSocket agent.
- [Package Guide](docs/ziurodb-package.md) — Complete API reference for the `ziurodb` universal JavaScript/TypeScript SDK.

---

## System Requirements

- **macOS:** macOS 10.15 (Catalina) or later (Apple Silicon or Intel).
- **Windows:** Windows 10 or Windows 11 (64-bit).
- **Linux:** Ubuntu 20.04+, Debian 11+, Fedora 36+, or any modern Linux distribution with glibc 2.28+.
- **Hardware:** 4 GB RAM minimum (8 GB recommended), 500 MB free storage space.

---

## Community & Support

- **Official Website:** [https://ziurodb.com](https://ziurodb.com)
- **Web App (ZiuroDB Lite):** [https://lite.ziurodb.com](https://lite.ziurodb.com)
- **Documentation:** [https://docs.ziurodb.com](https://docs.ziurodb.com)
- **Issue Tracker & Feature Requests:** [https://github.com/shanikumar001/ziurodb/issues](https://github.com/shanikumar001/ziurodb/issues)
- **Desktop Releases:** [https://github.com/shanikumar001/ziurodb-desktop/releases](https://github.com/shanikumar001/ziurodb-desktop/releases)

---

## License

ZiuroDB is open-source software licensed under the [MIT License](LICENSE).
