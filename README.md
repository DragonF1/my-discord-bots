# Discord Bot Portfolio

A showcase of custom Discord bots developed by **DragonF1**, demonstrating proficiency in bot logic, cloud architecture, database management, and user interaction.

## 📂 Project Index

### 1. Global Arcade
*[Documentation](./Global%20Arcade.md) | [Invite Bot](https://discord.com/oauth2/authorize?client_id=1073737033221902427&permissions=8&scope=bot%20applications.commands)*
* **Description:** A comprehensive, production-grade Discord bot that simulates a complete economy ecosystem. It features real-time stock markets, social guilds, and competitive gaming, demonstrating advanced Python capabilities and persistent state management.
* **Tech Stack:**
    * **Language:** Python 3.10+
    * **Framework:** discord.py 2.0+
    * **Database:** SQLite / LibSQL (Turso)
    * **Infrastructure:** Docker & Docker Compose
* **Key Features:**
    * **Stock Market Simulation:** Autonomous background simulation with volatility algorithms and "Black Swan" events.
    * **Guild System:** Persistent social groups with leveling logic, RBAC, and dynamic currency multipliers.
    * **Transaction Safety:** ACID-compliant financial transactions using SQL transactions to prevent race conditions.

### 2. Swuab's Optimizations (SO Bot)
*[Documentation](./SO%20Bot.md)*
* **Description:** An enterprise-grade community management system designed as a monolithic "operating system" for high-traffic servers. It unifies advanced moderation, economy, and dynamic media generation into a single cohesive codebase.
* **Tech Stack:**
    * **Language:** Python 3.10+
    * **Framework:** discord.py (Nextcord-style architecture)
    * **Database:** SQLite / LibSQL (Turso)
    * **Libraries:** Pillow (PIL), Regex
* **Key Features:**
    * **Intelligent Moderation (FilterCog):** Context-aware filtering that detects ghost pings, resolves invite links to check against whitelists, and tracks message velocity to prevent spam.
    * **Dynamic Image Generation:** Generates pixel-perfect profile and level cards on the fly using threading to prevent blocking the main asyncio event loop.
    * **Robust Architecture:** Features a modular "Cog" design with global error boundaries and atomic database transactions to ensure data integrity.

### 3. Soria (Enterprise Support System)
*[Documentation](./Soria.md)*
* **Description:** A sophisticated helpdesk platform designed to replace external tools like Zendesk. It transforms a Discord server into a professional support hub with structured workflows, automation, and analytics.
* **Tech Stack:**
    * **Language:** Python 3.9+
    * **Framework:** discord.py 2.0+
    * **Database:** Custom JSON-based persistent data store (NoSQL-style)
    * **Concepts:** Advanced UI (Modals, Select Menus), Asynchronous I/O
* **Key Features:**
    * **Intelligent Intake:** Uses context-aware modals to collect structured data and algorithms to automatically detect priority.
    * **Agent Tools:** Features auto-assignment to prevent collisions, performance tracking (response times/resolution rates), and Role-Based Access Control (RBAC).
    * **Compliance:** Automated audit logging, lifecycle management (auto-closing abandoned tickets), and downloadable conversation transcripts.

### 4. TexDex (Cloud-Native Content Distribution)
*[Documentation](./TexDex%20Bot.md)*
* **Description:** A high-performance bot engineered to revolutionize Minecraft texture pack discovery. It utilizes a hybrid cloud architecture to serve large files and aggregates content from multiple external sources.
* **Tech Stack:**
    * **Language:** Python 3.9+
    * **Cloud API:** Google Drive API v3 (OAuth2)
    * **Web Scraping:** Aiohttp, Cloudscraper, BeautifulSoup4
    * **Database:** SQLite3 with custom schema migration
* **Key Features:**
    * **Cloud Storage Engine:** Bypasses local storage limits by using Google Drive as a backend CDN with resumable upload pipelines.
    * **Hybrid Search Algorithm:** Asynchronously scrapes external sites (Modrinth, CurseForge) and combines results with local databases for a unified search experience.
    * **SaaS-Inspired Logic:** Implements subscription tiers (Free/Premium/Pro) with strict quota management and automatic expiration tracking.

### 5. HyClash (Enterprise Moderation System)
[Documentation](./HyClash.md)

**Description:** A sophisticated, production-grade Discord bot built for the Hytale community. It serves as a comprehensive administrative backbone, integrating intelligent content filtering, hierarchical punishment tracking, and a dynamic UI component system.

**Tech Stack:**
* **Language:** Python 3.9+
* **Framework:** discord.py 2.3.0+
* **Database:** Supabase (PostgreSQL)
* **Infrastructure:** Docker & Docker Compose

**Key Features:**
* **Intelligent Automod Engine:** Utilizes Regex pattern matching and fuzzy string detection to identify bypassed terms and mitigate spam in real-time.
* **Discord Components V2 UI:** Implements a custom template-based UI framework for rich, persistent interactions such as interactive FAQ menus and punishment appeals.
* **Robust Punishment Tracking:** Features a multi-layered system for logging warns, mutes, and bans with AI-driven recommendations based on user history.
* **Cloud-Native Persistence:** Leverages Supabase for resilient data management of user profiles, moderation logs, and server-wide settings.
---

## 🛠️ General Technical Competencies
* **Core Proficiencies:** discord.py, REST API, Discord APIs, AWS Hosting
* **Languages:** Python 3.9+, SQL, JavaScript (discord.js), Basic HTML/CSS
* **Cloud & Infrastructure:** AWS, Google Drive API, Docker, Docker Compose
* **Databases:** Cloud-based Databases, SQLite3, LibSQL (Turso), Custom JSON Data Stores
* **Core Libraries:** asyncio, Aiohttp, Pillow (PIL), Regex, BeautifulSoup4
* **Key Concepts:**
    * **Concurrency:** Asynchronous I/O, Threading, Event-Driven Programming
    * **Data Integrity:** ACID Compliance, Atomic Transactions, Schema Migration
    * **Web Technologies:** REST API Integration, Advanced Web Searching

## 📬 Contact
For inquiries regarding these projects or development opportunities, please contact **@dragonf1** on discord.
