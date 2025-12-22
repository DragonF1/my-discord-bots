# Soria Bot - Enterprise-Grade Discord Support System

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg) ![Python](https://img.shields.io/badge/python-3.9+-yellow.svg) ![Discord.py](https://img.shields.io/badge/discord.py-2.0+-7289da.svg)

**Soria** is a sophisticated, asynchronous Discord bot designed to revolutionize customer support within Discord communities. Built with Python and the modern `discord.py` library, Soria transforms a standard Discord server into a fully-featured helpdesk platform. It is engineered to bring a **Zendesk-style experience** directly to Discord, replacing clunky bot commands with professional, streamlined workflows.

This project demonstrates advanced usage of the Discord API, featuring persistent state management, complex UI interactions (Modals, Select Menus), and intelligent automation logic. It was architected to be robust, scalable, and user-friendly, providing a seamless experience for both customers and support agents.

## 🚀 Key Features

### 🎫 Intelligent Ticket Management

Soria moves beyond simple "open ticket" commands. It implements a **dynamic intake system** using Discord's latest UI components:

- **Context-Aware Modals**: Users are presented with custom forms based on their selected department (e.g., Technical Support vs. Billing), collecting relevant structured data upfront.
- **Smart Priority Detection**: The system analyzes form inputs for keywords (e.g., "emergency", "broken") and combines them with department weighting to automatically assign urgency levels (Normal vs. High).
- **Private Thread Integration**: Tickets are isolated in private threads, keeping the main channels clean and ensuring privacy while leveraging Discord's native threading capabilities for conversation history.

### 👨‍💻 Agent Workflow & Analytics

Designed for teams, Soria includes a comprehensive suite of tools for support staff:

- **Auto-Assignment System**: The first agent to respond to a ticket is automatically assigned ownership, preventing collision and ensuring clear accountability.
- **Performance Tracking**: The bot tracks critical metrics for every agent, including response times, resolution rates, and ticket volume (Daily/Monthly stats).
- **Role-Based Access Control (RBAC)**: secure commands for `Support`, `Senior`, `Manager`, and `Admin` roles ensure that sensitive actions like agent management are restricted to authorized personnel.

### 🤖 Automation & Compliance

Soria reduces manual overhead with smart background tasks:

- **Lifecycle Management**: Automated background tasks monitor ticket activity, issuing warnings after 12 hours of silence and auto-closing abandoned tickets after 24 hours to maintain a healthy queue.
- **Audit Logging**: Every action—from ticket creation to closure—is immutably logged to a persistent data store, ensuring full accountability.
- **Instant Transcripts**: Upon closure, the bot generates and attaches a downloadable text transcript of the entire conversation, essential for record-keeping and dispute resolution.

## 🔧 Technical Architecture

The core of Soria is built on a custom **JSON-based persistent data store**, designed for portability and speed. This lightweight database structure manages relational data between Users, Tickets, and Agents without the overhead of a heavy SQL server for smaller deployments.

- **Asynchronous Core**: Leverages `asyncio` for non-blocking I/O, allowing the bot to handle multiple tickets, background tasks, and API calls concurrently without latency.
- **Modular Design**: Business logic is separated into distinct utility functions (e.g., `close_ticket_logic`, `generate_transcript_file`), promoting code reusability and testing.
- **Error Handling**: Robust error catching and user-facing feedback messages ensure the bot remains stable even during edge cases or API outages.

## 🌟 Add to Server Now!

Soria represents the intersection of community management and professional software engineering. It is not just a bot; it is a complete support infrastructure.

Ready to elevate your Discord support experience? **[Add Soria to your server now!](https://discord.com/oauth2/authorize?client_id=1426803349801402449)**
