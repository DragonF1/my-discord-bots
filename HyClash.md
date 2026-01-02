HyClash: Enterprise-Grade Moderation & Community Management System
HyClash is a sophisticated, modular Discord bot engineered to serve as the administrative backbone for high-traffic gaming communities. It integrates automated content filtering, multi layered punishment tracking, and a dynamic UI component system into a resilient, production ready framework.

This project showcases expertise in asynchronous system design, cloud database integration, and hierarchical access control, providing a comprehensive solution for large scale social platform management.

🚀 Key Technical Features
1. Intelligent Automod Engine (AutomodCog)
The bot utilizes a multi layered detection system to maintain community standards without manual intervention.

Contextual Pattern Matching: Employs advanced Regex and Leet-speak detection to identify bypassed terms by mapping character substitutions (e.g., 3 to e).

Fuzzy Logic Integration: Leverages the thefuzz library to catch intentional misspellings and variations that traditional word-filters miss.

Rate Limited Spam Prevention: Tracks message velocity per user with configurable thresholds, executing automated silences or deletions based on real-time velocity analysis.

2. Discord Components V2 UI Framework
HyClash moves beyond standard embeds by implementing a custom template based UI system for rich user interactions.

Layout Engine: Uses a proprietary LayoutView system to render complex, nested components like Containers, Sections, and ActionRows with dynamic data interpolation.

Persistent Interactivity: Manages stateful UI elements—such as FAQ dropdowns and appeal buttons—that remain functional across bot restarts using custom UUID mapping.

Modular Component API: Simplifies the creation of multi-step workflows (like the punishment system) through a recursive child-processing architecture.

3. Cloud Native Persistence & Data Integrity
Designed for high availability, the bot utilizes a modern cloud stack to ensure no data is lost during scaling or maintenance.

Relational Persistence: Built on Supabase (PostgreSQL), managing complex relations between user profiles, punishment history, and active appeals with atomic integrity.

Environment Aware Configuration: A robust config.py system handles hot-swappable environment variables, allowing seamless transitions between Production and Development modes with automatic ID remapping.

Stateful Caching: Implements a 5-minute TTL (Time-to-Live) cache for guild settings and regex patterns to minimize database latency and optimize API overhead.

4. Robust Hierarchical Architecture
The system is built on a strictly modular "Cog" architecture, ensuring clean separation of concerns and easy extensibility.

Permission Enforcement: Features a 5-tier role hierarchy (Level 0–4) defined via permissions.json, supporting "plus" notation (e.g., moderator+) for inherited access.

AI Assisted Moderation: Integrates Google GenAI to provide moderators with recommended punishment durations based on a user's historical offense patterns.

Containerized Deployment: Fully orchestrated via Docker and docker-compose, ensuring consistent environments across local development and cloud VPS hosting.

🛠️ Technologies & Skills
Language: Python 3.9+

Framework: Discord.py (v2.3.0+)

Database: Supabase / PostgreSQL (Cloud-based relational management)

Infrastructure: Docker, Docker-Compose, Linux VPS

Logic & AI: Fuzzy String Matching, Regular Expressions (Regex), Google Gemini API

Integrations: Google Sheets API (gspread), ClickUp API, System Monitoring (psutil)

HyClash demonstrates the ability to manage extreme complexity within a stateful, real time application. It serves as a proof of concept for building secure, scalable, and user centric software for the modern web.
