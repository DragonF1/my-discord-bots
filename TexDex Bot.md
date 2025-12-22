# TexDex Bot

A specialized Discord bot for managing, searching, and distributing Minecraft texture packs. Features include cloud storage integration, user tier systems, and advanced moderation tools.

## ⚡ Slash Commands

Slash commands are the primary way for users to interact with the bot.

### 🔍 Discovery

#### `/search`

Search for texture packs across the database and web sources (Modrinth, CurseForge, ResourcePacks.gg).

- **Usage**: `/search query:Name [limit:Number]`
- **Example**: `/search faithful 10`

#### `/database`

Browse all approved texture packs in the TexDex database.

- **Usage**: `/database`
- **Description**: Opens an interactive menu to browse packs.

### 👤 User Management

#### `/profile`

View a user's profile including tier, storage usage, and uploaded packs.

- **Usage**: `/profile [user:@User]`
- **Description**: Shows your own profile if no user is specified.

### 📦 Pack Management

#### `/uploadpack`

Upload a .zip texture pack file directly to the database.

- **Usage**: `/uploadpack name:Name description:Text file:Attachment`
- **Requirements**: Must be a valid `.zip` file containing `pack.mcmeta`.
- **Note**: Uploads require moderator approval.

#### `/addlink`

Submit a download link for a texture pack.

- **Usage**: `/addlink name:Name url:URL description:Text`
- **Note**: Links require moderator approval.

#### `/pack-promote`

Promote one of your approved packs to appear at the top of search results for 24 hours.

- **Usage**: `/pack-promote pack_name:Name`
- **Cooldown**: Depends on user tier.

## 🛡️ Admin Commands

Prefix commands (default prefix: `!`) for moderators and administrators.

### 🚫 Moderation

#### `!blacklist`

Toggle a user's blacklist status. Blacklisted users cannot upload packs.

- **Usage**: `!blacklist @User [reason]`

#### `!review`

Review all packs uploaded by a specific user.

- **Usage**: `!review @User`
- **Description**: Opens an interactive menu to Approve or Deny packs.

#### `!remove_pack`

Permanently delete a pack from the database and cloud storage.

- **Usage**: `!remove_pack <exact_pack_name>`

#### `!viewuser`

View detailed information about a user including hidden stats.

- **Usage**: `!viewuser @User`

#### `!setsponsored`

Set a pack as sponsored (highest priority in search results).

- **Usage**: `!setsponsored <pack_name> <on/off>`

### ⚙️ System

#### `!resync`

Clear and resync slash commands.

- **Usage**: `!resync <local/global>`
- **Options**:
  - `local`: Sync to current server only (Instant).
  - `global`: Sync to all servers (Takes up to 1 hour).

## 🛠️ Developer Commands

Restricted to bot developers.

#### `!settier`

Set a user's subscription tier.

- **Usage**: `!settier @User <free/premium/professional> [days]`
- **Tiers**:
  - `free`: 300MB Storage
  - `premium`: 5GB Storage
  - `professional`: 50GB Storage

#### `!clear`

Wipe the entire database.

- **Usage**: `!clear database`
- **Warning**: This action is irreversible.

---

**TexDex Bot** | **Resource Packs Simplified**
