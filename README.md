# ZiuroDB Desktop v1.0.1

We are excited to announce ZiuroDB Desktop v1.0.1. This release brings the all-new Ziuro AI Copilot Assistant v2.0, native Groq LLM integration, automated query diagnosis, enhanced monochrome UI styling, and cross-platform performance optimizations.

---

## What's New in v1.0.1

### Native Ziuro AI Copilot (v2.0)
- **Direct Groq REST API Integration**: Ziuro AI Copilot now calls the Groq LLaMA-3-70B engine directly, removing external proxy dependencies for seamless performance.
- **Auto-Retry & Smart Query Diagnosis**: Automatic query execution loop with 5-retry resilience. If a query fails, Ziuro AI diagnoses the exact root cause and provides step-by-step fix suggestions.
- **Strict Query & Chat Modes**: Switch effortlessly between conversational AI assistant mode and strict code output mode for SQL, ZQL, MongoDB, and Redis queries.
- **Session History Persistence**: In-memory session tracking with fast history recall across Query Console sessions.

### UI & Aesthetics Refresh
- **Left-Side AI Copilot Sidebar**: Positioned on the left side of the Query Console for an ergonomic workflow.
- **Monochrome & Pure Dark Styling**: High-contrast pure dark theme integration (dark:bg-black) with clean borders and active indicator dots.
- **Toolbar & Connection Bar Polish**: Icon-only toolbar buttons and smart connection name truncation (...) to prevent header overflow.

### Cross-Platform Build Pipeline
- Fresh, clean builds across macOS (Apple Silicon & Intel), Windows (Universal, x64, ia32), and Linux (AppImage, DEB, RPM).
- Automatic application bundle updating on macOS builds.

---

## Core Highlights

- **Multi-Database Support**: Connect, explore, and manage MongoDB, MySQL, PostgreSQL, and Firebase from one unified desktop interface.
- **ZQL & SQL Console**: Interactive Query Language console with sub-millisecond execution and real-time result viewing.
- **Database-to-REST API Engine**: Instantly expose database collections as secure RESTful APIs.
- **Native Performance**: Built with Electron, React, and TypeScript for low memory footprint and high performance.

---

## Supported Platforms

- **macOS**: Apple Silicon (M1/M2/M3/M4) & Intel x64 (.dmg, .zip)
- **Windows**: Windows 10 & 11 Universal, x64, ia32 (.exe)
- **Linux**: Universal x64 AppImage, Debian/Ubuntu (.deb), Fedora/RedHat (.rpm)

---

## Downloads & Installation

Choose the installer that matches your operating system and architecture from the Assets section below.

For documentation and source code, visit:
https://github.com/shanikumar001/ziurodb

Website:
https://ziurodb.com
