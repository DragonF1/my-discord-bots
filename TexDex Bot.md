# TexDex: Cloud-Native Texture Pack Distribution System

**TexDex** is a high-performance Discord bot engineered to revolutionize how the Minecraft community discovers, manages, and distributes texture packs. Unlike modifications that rely solely on local storage, TexDex implements a **hybrid cloud architecture**, integrating directly with the Google Drive API to serve large files at scale while maintaining a lightweight application footprint.

This project demonstrates advanced proficiency in **Python backend development**, **cloud API integration**, and **system architecture design**, solving the real-world problem of fragmented content distribution in gaming communities.

## 🤖 Add the Bot Now

Ready to elevate your server's texture pack experience?
**[🔗 Click Here to Add TexDex to Your Discord Server](https://discord.com/oauth2/authorize?client_id=1166499953749803059)**

## 🏗️ Technical Architecture

### 1. Cloud-Native Storage Engine

TexDex bypasses traditional server storage limitations by leveraging the **Google Drive API** as a backend CDN.

- **Resumable Upload Pipelines:** The `DriveManager` class implements chunked, resumable uploads via `MediaFileUpload`, ensuring reliability even when processing multi-gigabyte high-resolution packs.
- **Dynamic Permission Management:** Automates ACL (Access Control List) modifications, converting private uploads to public `reader` permissions instantly upon moderation approval.
- **Smart File Lifecycle:** Manages file movements between "Pending" and "Approved" folder structures programmatically, maintaining a clean state without manual intervention.

### 2. Hybrid Search Algorithm

The core utility of TexDex is its aggregated search engine, which unifies disparate sources into a single query interface.

- **Multi-Source Scraping:** Concurrent asynchronous workers (`asyncio`) query internal databases alongside external APIs like **Modrinth** and web-scraped sources like **CurseForge** and **ResourcePacks.gg**.
- **Resilient Web Scraping:** Utilizes `cloudscraper` to bypass Cloudflare protection on target sites and `BeautifulSoup4` for robust HTML parsing, extracting metadata, download links, and descriptions in real-time.
- **Optimized SQL Queries:** The local SQLite database uses complex compound indices to allow for sub-second filtering by resolution, game version, and color tags, even as the dataset grows.

### 3. SaaS-Inspired Tiered Access

TexDex mimics modern SaaS platforms with a robust user subscription model implemented purely in SQL and Python.

- **Quota Management Logic:** Real-time calculation of storage usage against tier limits (Free: 300MB, Premium: 5GB, Pro: 50GB).
- **Expiration Tracking:** Automated background tasks monitor subscription validity and "Promoted Pack" durations, reverting statuses automatically when periods lapse.
- **Acid-Compliant Transactions:** User upgrades and currency transactions utilize SQLite's transaction safety to prevent race conditions during concurrent command usage.

## 🔐 Security & Moderation

- **Viral Scanning Integration:** (Roadmap embedded) Architecture ready for file stream scanning before public availability.
- **Role-Based Access Control (RBAC):** Granular command permissions ensure only authorized staff can approve files, minimizing the risk of malicious content distribution.
- **Strict Input Validation:** All external URLs are sanitized and validated against allowed patterns before being committed to the database.

## 🛠️ Tech Stack

- **Language:** Python 3.9+
- **Core Framework:** Discord.py (Async/Await)
- **Data Persistence:** SQLite3 with custom schema migration tools
- **Cloud Infrastructure:** Google Drive API v3, OAuth2
- **Web Technologies:** Aiohttp, Cloudscraper, BeautifulSoup4
- **DevOps:** Docker-ready containerization

TexDex stands as a testament to building **scalable, user-centric applications** that seamlessly bridge the gap between chat interfaces and complex cloud infrastructure.
