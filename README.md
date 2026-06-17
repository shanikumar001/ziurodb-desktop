# ZiuroDB Desktop

Cross-platform database administration application for MongoDB, MySQL, and PostgreSQL.

ZiuroDB Desktop provides a modern desktop environment for connecting to, managing, and interacting with multiple database systems from a single application. Built with Electron, React, and Node.js, it combines powerful database management capabilities with a clean, developer-focused interface.

> This repository contains **pre-built desktop releases** of ZiuroDB for Windows, macOS, and Linux.

---

## Download

Download the latest release from the **Releases** page.

Supported platforms include:

| Platform | Architecture | Format |
|----------|-------------|---------|
| Windows | x64 | `.exe` |
| Windows | ARM64 | `.exe` |
| Windows | IA32 | `.exe` |
| macOS | Intel | `.dmg` |
| macOS | Apple Silicon | `.dmg` |
| Linux | x64 | `.AppImage`, `.rpm` |
| Linux | ARM64 | `.AppImage` |
| Debian | x64 | `.deb` |

---

## Features

ZiuroDB Desktop includes:

- Multi-database support
- MongoDB, MySQL, and PostgreSQL connections
- SQL & Mongo Query Editor
- Database Explorer
- Universal Database Workbench
- Database-to-REST API Engine
- Secure Connection Management
- Query History
- Real-time Database Monitoring
- Authentication & Access Control
- Cross-platform Desktop Application

---

## Technology

- Electron
- React
- TypeScript
- Node.js
- Express.js
- MongoDB
- MySQL
- PostgreSQL
- Redis
- BullMQ
- Socket.IO

---

## Installation

### Windows

Download the appropriate `.exe` installer and run it.

### macOS

Download the `.dmg` file for your processor.

- Apple Silicon → `mac-arm64.dmg`
- Intel → `mac-x64.dmg`

Open the installer and move ZiuroDB into the Applications folder.

### Linux

Choose one of the available packages.

**AppImage**

```bash
chmod +x ZiuroDB.AppImage
./ZiuroDB.AppImage
```

**Debian**

```bash
sudo dpkg -i ZiuroDB.deb
```

**RPM**

```bash
sudo rpm -i ZiuroDB.rpm
```

---

## Documentation

Documentation, source code, and development guides are available in the main repository.

Main Repository

https://github.com/shanikumar001/ziurodb

Official Website

https://ziurodb.ziuro.com

---

## Reporting Issues

If you encounter a bug or installation issue, please open an issue in the main repository.

https://github.com/shanikumar001/ziurodb/issues

---

## License

MIT License
