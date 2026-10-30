 <p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="proprietary/images/OpenFrontLogoDark.svg">
    <source media="(prefers-color-scheme: light)" srcset="proprietary/images/OpenFrontLogo.svg">
    <img src="proprietary/images/OpenFrontLogo.svg" alt="OpenFront Logo" width="360">
  </picture>
</p>

<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1000&color=2563EB&center=true&vCenter=true&width=550&lines=Real-Time+Territorial+Strategy;Multiplayer+Global+Warfare;Build.+Expand.+Conquer." alt="OpenFront animated heading">
</h1>

<p align="center">
  <strong>Expand your territory. Build alliances. Compete for global domination.</strong>
</p>

<p align="center">
  An open-source, real-time multiplayer strategy game inspired by territorial warfare and real-world geography.
</p>

<p align="center">
  <a href="https://openfront.io/">
    <img src="https://img.shields.io/badge/PLAY_NOW-OpenFront.io-16A34A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Play OpenFront">
  </a>
  <a href="https://github.com/openfrontio/OpenFrontIO">
    <img src="https://img.shields.io/badge/SOURCE_CODE-GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub repository">
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/openfrontio/OpenFrontIO?style=flat-square&logo=github&label=Stars" alt="GitHub Stars">
  <img src="https://img.shields.io/github/forks/openfrontio/OpenFrontIO?style=flat-square&logo=git&label=Forks" alt="GitHub Forks">
  <img src="https://img.shields.io/github/license/openfrontio/OpenFrontIO?style=flat-square&label=License" alt="License">
  <img src="https://img.shields.io/badge/Node.js-24.15%2B-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/npm-12.1%2B-CB3837?style=flat-square&logo=npm&logoColor=white" alt="npm">
</p>

---

## 🌍 Overview

**[OpenFront.io](https://openfront.io/)** is an open-source, browser-based, real-time multiplayer strategy game centered around territorial expansion, strategic alliances, and resource management.

Players compete across geographical maps, expand their borders, manage military resources, construct structures, and coordinate with other players to dominate the battlefield.

OpenFront is a complete architectural rewrite and evolution of [WarFront.io](https://github.com/WarFrontIO).

## ✨ Features

| Feature | Description |
|:---|:---|
| 🌐 **Real-Time Multiplayer** | Compete against other players in continuously evolving strategy battles. |
| 🗺️ **Geographical Maps** | Explore and conquer territories across maps inspired by real-world geography. |
| 🤝 **Alliance System** | Form strategic alliances and coordinate with other players. |
| ⚔️ **Military Strategy** | Expand territory, manage resources, and defend your borders. |
| 🏗️ **Resource Management** | Balance economic growth, expansion, and military strength. |
| ⚡ **Browser-Based Gameplay** | Play directly through a modern web browser without a traditional desktop installation. |
| ⚙️ **Simulation Engine** | A dedicated game engine powers the simulation and game-state updates. |

## 🖥️ Screenshots

<p align="center">
  <!-- Add official gameplay screenshots here when available. -->
</p>

## 🛠️ Technology & Architecture

OpenFront is organized into modular packages that separate the game simulation, shared contracts, client, and server.

| Component | Responsibility |
|:---|:---|
| **Client** | Game interface, rendering, user interactions, and networking. |
| **Server** | Authoritative game orchestration and multiplayer sessions. |
| **Engine** | Deterministic game simulation. |
| **Engine API** | Types, schemas, game updates, and worker protocols. |
| **Engine Lib** | Shared game rules, map grids, and utility functions. |
| **Shared** | Common schemas, environment configuration, and asset paths. |
| **Zbin** | Compact binary serialization for Zod schemas. |

## 📋 Prerequisites

Before setting up the project locally, make sure you have:

| Requirement | Version |
|:---|:---|
| Node.js | 24.15.0 or newer (Node 24 release line) |
| npm | 12.1.0 or newer (npm 12 release line) |
| Git | Latest stable version |
| Browser | Modern Chrome, Firefox, Edge, or Safari |

If Node.js bundles an older npm version, upgrade npm before proceeding:

```bash
npm install --global --ignore-scripts npm@12.1.0
```

## 🚀 Getting Started

### 1. Fork the Repository

Fork the official repository:

[https://github.com/openfrontio/OpenFrontIO](https://github.com/openfrontio/OpenFrontIO)

### 2. Clone Your Fork

```bash
git clone https://github.com/YOUR_USERNAME/OpenFrontIO.git

cd OpenFrontIO
```

### 3. Install Dependencies

Use the repository's prescribed installation command:

```bash
npm run inst
```

> **Important:** Do not use `npm install` or `npm i` for project dependencies. `npm run inst` executes `npm ci --ignore-scripts` to install the locked dependencies without running lifecycle scripts.

The repository also enforces a seven-day minimum age for dependency releases and restricts certain dependency sources. Refer to the contribution guidelines before changing dependencies.

## 🎮 Running the Game

### Full Development Environment

Start the client and server together:

```bash
npm run dev
```

This starts the development environment, launches the game server, and opens the game in your default browser.

### Client Only

```bash
npm run start:client
```

### Server Only

```bash
npm run start:server-dev
```

### Connect to Staging Backend

```bash
npm run dev:staging
```

### Connect to Production Backend

```bash
npm run dev:prod
```

<details>
<summary><strong>🔍 Replaying Production Games</strong></summary>

To replay a production game locally, your local Git commit must match the commit used by the recorded game.

You can retrieve the `gitCommit` property through:

```text
https://api.openfront.io/game/[gameId]
```

Unfinished games cannot be replayed locally.

</details>

## 🧰 Development Toolkit

The repository provides commands for formatting, static analysis, and testing.

| Command | Purpose |
|:---|:---|
| `npm run format` | Format the codebase. |
| `npm run lint` | Run static analysis. |
| `npm run lint:fix` | Automatically fix supported lint issues. |
| `npm test` | Run the test suite. |
| `npm run test:coverage` | Run tests with coverage reporting. |

## 🏗️ Project Structure

```text
OpenFrontIO/
│
├── proprietary/          # Proprietary project resources
├── resources/            # Maps, textures, audio, and static assets
│
├── packages/
│   ├── engine/           # Deterministic game simulation
│   ├── engine-api/       # Game contracts, schemas, and worker protocols
│   ├── engine-lib/       # Map grids, rules, and shared helpers
│   ├── shared/           # Shared schemas and environment utilities
│   └── zbin/             # Compact binary serialization
│
├── src/
│   ├── client/           # Frontend game client
│   └── server/           # Backend game server
│
├── tests/                # Automated tests
│
├── CONTRIBUTING.md       # Contribution guidelines
├── LICENSE               # Source code license
├── LICENSE-ASSETS        # Asset licensing
└── README.md
```

## 🤝 Contributing

Contributions from the open-source community help improve OpenFront.

Whether you're interested in fixing bugs, improving the user interface, enhancing performance, or contributing to the game's development, please follow the official contribution guidelines.

Before submitting changes:

1. Check the existing issues and development discussions.
2. Find an issue labelled `approved`, or propose a new issue and wait for approval.
3. Request assignment before starting significant work.
4. Follow the repository's coding standards.
5. Include relevant tests and documentation.
6. Submit a focused pull request with a clear description.

**Read the official [CONTRIBUTING.md](CONTRIBUTING.md) before making changes.**

## 📄 License & Attribution

OpenFront uses separate licenses for its source code and assets.

- **Source Code:** GNU Affero General Public License v3.0 (AGPL-3.0).
- **Assets:** See [LICENSE-ASSETS](LICENSE-ASSETS) for the applicable asset licensing terms.
- **License History:** Refer to [LICENSING.md](LICENSING.md).

Modified distributions must preserve the project's required copyright notices:

`© OpenFront and Contributors`

Refer to the official license files for the complete requirements.

## 🌐 Community & Resources

<p align="center">
  <a href="https://openfront.io/">Official Website</a> •
  <a href="https://github.com/openfrontio/OpenFrontIO">GitHub Repository</a> •
  <a href="CONTRIBUTING.md">Contribution Guidelines</a> •
  <a href="https://crowdin.com/project/openfront-mls">Translations</a>
</p>

<p align="center">
  <strong>Built by the OpenFront community.</strong>
  <br>
  <sub>Explore. Expand. Conquer.</sub>
</p>
