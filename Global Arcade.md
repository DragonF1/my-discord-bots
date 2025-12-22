# Global Arcade Bot

Global Arcade is a comprehensive, production-grade Discord bot built to demonstrate advanced Python capabilities, asynchronous system design, and persistent state management. It simulated a complete economy ecosystem within Discord, featuring real-time stock markets, social guilds, and competitive gaming.

## 🤖 Add to Your Server

[**Invite Global Arcade**](https://discord.com/oauth2/authorize?client_id=1287837668889329714)

Click the link above to add the bot to your Discord server or authorize it to run in any server!

---

## 🏗️ System Architecture

The project follows a **Modular Monolith** architecture using `discord.py`'s Cog system to separate concerns.

- **Core Core**: `main.py` handles lifecycle events, intent configuration, and extension loading.
- **Service Layer**: Dedicated Manager classes (`StockManager`, `GuildManager`, `CoinManager`) encapsulate business logic, decoupling it from the UI layer.
- **Data Access Layer**: centralized `utils.database` module managing SQLite connections with proper connection pooling and transaction safety.
- **UI Layer**: Extensive use of Discord's `discord.ui` (Views, Modals, Buttons) for rich, interactive user experiences.

## 🚀 Key Features In-Depth

### 📈 Stock Market Simulation

A fully autonomous background simulation of a stock market.

- **Engine**: The `StockManager` class runs a volatility algorithm every 5 minutes (via `tasks.loop`).
- **Volatility**: Prices fluctuate based on a standard deviation model (±5%), with rare "Black Swan" events (1% chance) triggering crashes or rallies (±20%).
- **Persistence**: User portfolios track Average Cost Basis (ACB) and calculate real-time Unrealized P/L.

### � Guild & Community System

A social layer allowing users to form persistent groups.

- **Leveling Logic**: Guilds earn XP when members win games. Leveling up unlocks higher member caps and global coin multipliers.
- **RBAC**: Role-based access control for Guild Owners to invite/kick members.
- **Dynamic Multipliers**: A hook in `CoinManager` checks the user's guild level during any coin transaction to apply bonus multipliers automatically.

### 💰 Economy & Transaction Safety

- **ACID-compliant**: All financial transactions (Shop, Betting, Trading) use SQL transactions to prevent race conditions or data loss.
- **Cooldowns**: Custom decorators (`@commands.cooldown`) prevent economy inflation and spam.
- **Admin Tools**: A dashboard for resolving user disputes, refunding currency, and auditing user states.

## 🛠️ Technical Highlights

- **Asynchronous Programming**: Heavy use of `async/await` for non-blocking I/O (Database, API calls).
- **Error Handling**: Global error handlers catch domain-specific errors (e.g., `TransformerError` for input validation) and present user-friendly feedback.
- **Input Validation**: type-hinted arguments (`discord.User` vs `discord.Member`) ensure commands work robustly across different Discord contexts.
- **Dependency Injection**: Managers are injected into Cogs, allowing for easier testing and state sharing.

## 🔧 Tech Stack

- **Language**: Python 3.10+
- **Framework**: discord.py 2.0+
- **Database**: SQLite3
- **Environment**: Docker & Docker Compose
- **Version Control**: Git
