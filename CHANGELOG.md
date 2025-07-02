# Changelog

All notable changes to Rune Guardian will be documented here.

## [1.3.10] - 2025-07-02

### Added
- System status embed in our support server.
- Project status embed in our support server.
- `/blacklist` - Allows the bot developers to blacklist a guild if they are caught violating our or discords TOS.
- Ghost ping detection enabled via `/toggle-ghostping`
- `/user` Shoes variouse information about a user, shows punishment history if the executor has moderation permsissions.
- `/bugreport` Allows users to report a bug with specific features.
- `/motm` Allows users to set a member of the month role based off xp.

### Updates
- Fixed an issue where `/updatecountvc` would fail in large servers.
- Fixed not-bot ban logs.
- Revamped `/showconfig` for overall readablility.
- Replaced `setafkchannel` with `/xpexclude`
- Replaced `/excludechannel` with `/messagelog exclude`
- Replaced `/includechannel` with `/messagelog include`
- Fixed per-server cooldowns in `!sesh` `!chatrevive` and `!drinktime`
- Updated `/welcomeconfig` allows users to save message formatting properly now.
- Changed xp per message from 10 to anywhere between 5-20

### Deprecated
- `Welcome_DM_MSG2` Welcome dms now consist of one message with optional buttons.

### Known Issues
- Welcome messages will not work until reconfigured in your server.

---

## [1.3.8] - 2025-06-01

### Added
- Overrides for developers in all configuration commands.
- Invite details (code, inviter, etc.).
- Additional options for `/sendembed` command: `${field1name}`, `${field1value}`, ..., `${field4value}`.
- Ticket system with `/create-ticket-panel` and `/rename` *(now mostly functional)*.
- Display of all user roles in leave logs.
- `/modapplication` with subcommands:
  - `create-panel`, `preview`, `set-channel`, `toggle-approval`.
- `/purge` command.
- Console logger for formatting and optional debug disabling.
- `!sticky` command to pin a message at the bottom of a channel.
- Reaction roles via `!rr @role :emoji:`.
- Starboard feature with voting arrows.
- Auto-registration of guild ID in the database (no more `/setup` needed).
- Presence manager showing uptime percentage.
- `/activity` to track user message activity.
- `/vban-connect` to stream Spotify to voice channels.
- `!420` and `/420` displays the next 4:20

### Updates
- Moderation commands now respect user permissions and/or `moderator_role`.
- Fixes to bitfield errors in `/warn`, `/timeout`, `/ban`, `/kick`, `/punishmenthistory`, `/removepunishment`, `/unban`, `/verifymember`.
- Removed ephemeral from `/restart`.
- Reminder handler improved for timezone recognition and bug fixes.
- Fixed ratelimits in `!sesh`, `!drinktime`, and `!chatrevive`
- DMs added to moderation commands (`/ban`, `/kick`, `/warn`) and included in logs.
- Punishment DMs improved in appearance.
- SIGINT shutdown detection fixed for Windows and PM2.
- Ticket transcript cache path updated and now deletes correctly.
- Logger consolidated into one file.
- `/welcomeconfig` updated.
- `/about` updated with uptime and removed Discord.js version; added TOS and Privacy Policy.
- Countgame updates: reacts with ✅ on correct count, ❌ and user on incorrect count.
- MongoDB switched to local instance.
- `/warn` now has optional DM.
- `/ban` updated to ban non-server members.

### Deprecated
- Deprecated use of `ephemeral` and `fetchReply` interaction options in favor of flags.

### Known Issues
- Ticket system still has issues. (Please report any bugs in our official support server)

---

## [1.3.2] - 2025-1-7
### Added
- **Commands**
  - `/setserverinfo`: Sets the server information.
  - `/serverinfo, !serverinfo`: Displays the server information.
  - `/setup`: Shows the setup guide.
  - `/verifymember`: Gives the sepcified user the `slashverifyRoleID` Role
  - `/membercountconfig`: Setting related to the member count embed and vc
  - `/setlogchannel`: Allows you to set various channels for logging
  - `/configureroles`: Here you can setup roles the bot needs for permissions checks or other commands eg. `/verifymember`
  - `/welcomeconfig`: Allows you to configure various welcome message options
  - `/showconfig`: Shows the servers currents settings
  - `/help`: Intuitive help command that shows all avaiable commands and thier usage
  - `/feedback`: Allows you to send feedback to a server or to my support server for bot-related issues
  - `/setfeedbackchannel`: Sets the servers feedback channel
  - `/roll`: Rolls dice (Also works with `!roll`)
  - `/reminder`: Allows you to set reminders (Note this feature is still buggy)
  - `/removepunishment`: Removes a punishment from a users history
  - `/punishmenthistory`: Displays punishment history for a user
  - `/reset_user_xp`: Resets a specific members xp
  - `/restart`: Restarts the bot (Restricted to developers)

- **Backend**
  - Added several statuses that cycle every 15 seconds
  - Internal Uptime Monitoring
  - Added logging for dms sent from members
  - Added a feature for the bot to send changelogs to the support server
  - Added shutdown logging

- **General featrues**
  - Added punishment database


### Updates
- **Commands**
  - `/sendembed`: Added `title` `color` `footer` `image` `thumbnail` `author` and `author_icon`
  - `/top`: Updated to display different names for different leaderboards, Updated to show the requesters rank seperately if they arent within the top 10
  - `/showconfig`: Fixed the message not sending if the config is too long

- **Misc**
  - Updated several logging embed colors for a more uniform look
  - Fixed user levels not updating from 1

- **Backend**
  - Changed error logging to send to a channel 
  - Fixed ExpectedConstraintError in GuildMemberRemove.js
  - Restructured the way slashcommands are registered, they are now defined within the command file instead of index.js
  - Updated leaderboards to use lifetime xp instead of current level xp
  - Fixed errors from servers not having one or more welcome messages set

- **Database**
  - Moved mongodb to a cloud server instead of a local instance
  - Changed `VerifiedRoleID` to `slashverifyRoleID`
  - Reset Server leaderboards


### Deprecated
- **Commands**
  - `/setadminrole`
  - `/setmoderatorrole`
  - `/updatesettings`
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
  - Posts a welcome message in a designated channel.
  
### Enhanced
- **Logging**: Updated join logging with enhanced information.

### Added
- **Moderation Command**: `/warn` to issue warnings to members with optional image evidence.

---

## [1.0.1] - Initial Release
### Added
- **Basic Event Logging**: Tracks joins, leaves, and role updates.
- **Moderation Commands**: `/ban`, `/kick`, `/timeout`.
- **Fun Commands**: `/drinktime`, `/sesh`, `/chatrevive`.
- **Channel Management**: Auto role management for new members.
- **Member Count**: Initial support for member count embed and voice channel count.
