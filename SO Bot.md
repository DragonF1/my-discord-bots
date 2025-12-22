# SO Bot (Swuab's Optimizer Bot)

A comprehensive Discord bot designed for community management, moderation, and automation. This bot includes advanced punishment systems, user tracking, giveaways, and automated utilities.

## ⚡ Slash Commands

Slash commands are the primary way to interact with the bot's modern features.

### 🛡️ Moderation

#### `/punish`

The core moderation command for issuing punishments.

- **Usage**: `/punish target:@User type:Type reason:Reason [duration:Duration] [evidence:Evidence]`
- **Parameters**:
  - `target`: The user to punish.
  - `type`: One of `warn`, `mute`, `kick`, `ban`, `change name`.
  - `reason`: The reason for the punishment.
  - `duration`: (Optional) Duration for mutes/bans (e.g., `1d`, `1h`).
  - `evidence`: (Optional) Text evidence or link.
- **Features**:
  - Opens an interactive menu to confirm details.
  - Sends a DM to the user with the reason and an appeal link (if applicable).
  - Logs the punishment to the database and log channels.

#### `/user`

View detailed information about a member.

- **Usage**: `/user target:@User`
- **Permission**: Moderators only.
- **Displays**:
  - Account creation and join dates.
  - Roles and permissions.
  - Filter bypass status.
  - User configuration (mentions/replies settings).

#### `/nick`

Request a nickname change.

- **Usage**: `/nick member:@User nickname:NewName`
- **Description**: Submits a nickname change request to the moderators.
- **Note**: The `member` argument is currently a placeholder; the command requests a change for the _user running the command_.

### 🔧 Utilities

#### `/profile-card`

Generate a custom profile card image.

- **Usage**: `/profile-card [member:@User]`
- **Description**: Creates a visual profile card with the user's avatar, roles, and join date.

#### `/info`

Display server information.

- **Usage**: `/info`
- **Description**: Shows server stats, member counts, channel counts, and owner info.

## 💬 Message Commands

Prefix commands (default prefix: `!`) for quick management and utilities.

### 🛠️ General & Utility

#### `!help`

Shows the help menu or detailed info about a specific command.

- **Usage**: `!help [command]`
- **Example**: `!help ping`

#### `!ping`

Shows bot statistics.

- **Usage**: `!ping`
- **Displays**: Latency, uptime, memory usage, and server stats.

#### `!remind`

Set a reminder for yourself.

- **Usage**: `!remind <time> <message>`
- **Example**: `!remind 10m Check the logs`

#### `!userconfig` (Alias: `!uc`)

Manage your personal notification settings.

- **Usage**: `!uc <replies/mentions/ghost> <on/off>`
- **Options**:
  - `replies`: Block/allow reply pings.
  - `mentions`: Block/allow direct mentions.
  - `ghost`: Enable/disable DMs for ghost pings.

### 🛡️ Moderation & Management

#### `!purge`

Bulk delete messages in the current channel.

- **Usage**: `!purge <amount>`
- **Limit**: Max 100 messages.

#### `!lockdown`

Locks or unlocks the current channel for the default role.

- **Usage**: `!lockdown [channel]`

#### `!slowmode`

Sets the channel slowmode delay.

- **Usage**: `!slowmode <seconds>`

#### `!verify`

Manually verify a member (Chief Officers only).

- **Usage**: `!verify @User`

#### `!log`

Generates a transcript of the last N messages in the channel and DMs it to you.

- **Usage**: `!log <limit>` (Max 100)

#### `!perm`

Manage the bot's internal permission system.

- **Usage**:
  - `!perm grant <user/role> <node>`
  - `!perm revoke <user/role> <node>`
  - `!perm list <user/role>`
- **Example**: `!perm grant @Staff command.msg.giveaway`

### 🎉 Giveaways

#### `!giveaway`

Manage server giveaways.

- **Start**: `!giveaway start <duration> <winners> <requirement> <prize>`
  - Example: `!giveaway start 24h 1 @Role "Nitro"`
  - Use `none` for no requirement.
- **End**: `!giveaway end <message_id>`
- **Reroll**: `!giveaway reroll <message_id>`


**SO Bot** | **Optimizing Your Community**
