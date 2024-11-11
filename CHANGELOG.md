# Changelog

All notable changes to Rune Guardian will be documented here.

---

## [1.3.0] - 2024-11-11
### Added
- **Commands**
  - `/about`: Displays information about the bot.
  - `/autorole set [role]`: Automatically assigns a role to new members.
  - `/autorole remove`: Removes the autorole setting.

### Fixed
- **Image Logging**: Fixed image attachments in `/ban` logging.

---

## [1.2.5] - 2024-11-10
### Added
- **Member Count Embed**: Added 18+ user count to the member count embed.
- **Bot Presence**: Bot presence updated to show total server and member count.

### Security
- **Token Reset**: Reset bot token for security reasons.

---

## [1.2.4] - 2024-11-09
### Added
- **Bulk Logging**
  - Message bulk delete logs.
  - Reaction bulk remove logs.

---

## [1.2.3] - 2024-11-08
### Edited
- **Invite Logger Format**: Improved format for invite logs.

### Added
- **Voice Mod Actions Logging**
  - Server mute/unmute.
  - Server deafen/undeafen.
  - Disconnect actions in voice channels.

### Removed
- **Message Logs**: Removed "Content" header for improved readability.

### Fixed
- **Timeout Duration**: Corrected formatting in timeout logs.

---

## [1.2.2] - 2024-11-07
### Added
- **Reaction Logs**: Added logging for message reactions.

---

## [1.2.1] - 2024-11-06
### Added
- **Counting Feature**: Introduced a counting minigame.

---

## [1.2.0] - 2024-11-04
### Added
- **Database Integration**: MongoDB support, allowing cross-server functionality.
- **Configuration**: New `/updatesettings` command to manage server settings.
- **Logging**
  - Channel logs, role logs (create, update, delete), unban logging, and logging for manual bans, kicks, etc.
  - Welcome DM customization with `{user}` for pinging new members.
  - XP System for tracking text and voice activity with rate-limiting on XP gain.
- **Role Management**: `/unban`, `/spam`, and `!drinktime` commands.

### Enhanced
- **Command Execution Location**: Commands such as `!sesh` and `!chatrevive` now execute in the same channel where triggered.

### Fixed
- **Exclude Channels**: Added ability to exclude specific channels from message logging.
- **Member Count**: Fixed both member count embed and voice channel count.

### Removed
- Deprecated `/setlogchannel`.

---

## [1.1.2] - 2024-11-01
### Added
- **Commands with Cooldowns**
  - `/sesh`: Pings Sesh Role with a message, with a 1-hour cooldown.
  - `/chatrevive`: Pings Chatrevive Role with a message, with a 45-minute cooldown.

### Changes
- **Command Format Updates**: Adjusted `/sesh` and `/chatrevive` to use the prefix and auto-delete command attempts and cooldown messages.
  - **/sesh**: Executed with `!sesh message`; pings only if a message is included.
  - **/chatrevive**: Executed with `!chatrevive message`; default ping if no message is provided.

### Fixed
- **Troll Command**: Removed the modal in `/troll` to allow channel selection directly within the command.

---

## [1.1.1] - 2024-10-31
### Added
- **Logging Enhancements**
  - Message edit logging with support for images.
  - Message delete logging.

---

## [1.1.0] - 2024-10-30
### Fixed
- Count embed and count voice channel.
- **Moderation Commands**
  - Ensured that only authorized users can use moderation commands.
  - Logs unauthorized command usage attempts.

### Added
- **Log Improvements**
  - Bot now DMs the owner whenever it comes online or has an error.
  - Call logs, join logs, leave logs, `/troll`, and `/trollstop` are now operational with additional logging.

---

## [1.0.2] - 2024-10-07
### Added
- **Welcome Features**
  - Sends welcome DM to new users.
  - Posts a welcome message in a designated lounge channel.
  
### Enhanced
- **Logging**: Updated join logging with enhanced information.

### Added
- **Moderation Command**: `/warn` to issue warnings to members with optional image evidence.

---

## [1.0.1] - Initial Release
### Added
- **Basic Event Logging**: Tracks joins, leaves, and role updates.
- **Moderation Commands**: `/ban`, `/kick`, `/timeout`, `/warn`.
- **Fun Commands**: `/drinktime`, `/sesh`, `/chatrevive`.
- **Channel Management**: Auto role management for new members.
- **Notifications**: DMs owner when it comes online.
- **Member Count**: Initial support for member count embed and voice channel count.
