# Rune Guardian Command List

A complete list of commands for **Rune Guardian**, including descriptions, options, and permission requirements.

---

## General Commands

- **`/about`** - Displays information about the bot.

- **`/feedback`** - Send feedback to server admins or the bot support team.  
  **Options:**
  - `type` (required): `Bot` | `Server`
  - `message` (required): Your feedback message

- **`/bugreport`** - Send a bugreport to the bot support team.

- **`/setup`** - Initializes the server's database and displays configuration options.

- **`/showconfig`** - Shows the current server settings.  
  🔐 Requires: Administrator

- **`/serverinfo`, `!serverinfo`** - Displays server information.  
  *(Configured using `/setserverinfo`)*

- **`/help`** - Displays a list of available commands or detailed info for a specific command.  
  **Option:** `command`

- **`/modhelp`** - Lists all moderation commands.  
  🔐 Requires: Moderator Role

- **`/reminder`** - Manage reminders.  
  **Subcommands:**
  - `set`: Create a reminder  
    - `time` (required)  
    - `frequency` (required): once, daily, weekly  
    - `timezone` (required)  
    - `reason` (required)  
    - `day` (required)
  - `list`: View reminders
  - `remove`: Remove a reminder by ID

- **`/sendembed`** - Send a custom embed message.  
  **Options:** `message` (required), `title`, `color`, `footer`, `image`, `thumbnail`, `author`, `author_icon`

- **`!sticky`** - Make a message sticky in a channel.

- **`!rr`** - Add a reaction role to a message.  
  **Usage:** `!rr @role :emoji:`

- **`/starboard`** - Manage the starboard feature.  
  **Subcommands:** `setthreshold`, `setchannel`, `setemoji`, `ignore`, `unignore`, `enable`, `disable`

---

## Moderation Commands

> 🔐 All moderation commands require proper permissions.

- **`/ban`** - Ban a user.  
  **Options:** `user` (required), `reason` (required), `image` (optional)  
  🔐 Requires: Ban Members

- **`/unban`** - Unban a user by ID.  
  **Options:** `user` (required), `reason` (optional)  
  🔐 Requires: Ban Members

- **`/kick`** - Kick a user.  
  **Options:** `user` (required), `reason` (required), `image` (optional)  
  🔐 Requires: Kick Members

- **`/timeout`** - Temporarily mute a user.  
  **Options:** `user`, `reason`, `duration`, `image`  
  🔐 Requires: Moderate Members

- **`/warn`** - Issue a warning.  
  **Options:** `user`, `reason`, `image`  
  🔐 Requires: Moderate Members

- **`/punishmenthistory`** - View a user’s punishment history.  
  **Option:** `user`  
  🔐 Requires: Moderate Members

- **`/removepunishment`** - Remove a punishment from a user’s history.  
  **Option:** `punishment_id`  
  🔐 Requires: Moderate Members

- **`/verifymember`** - Assigns the `/configureroles` `slashverify_role`.  
  **Option:** `user`  
  🔐 Requires: Manage Roles

- **`/purge`** - Delete messages in bulk.  
  **Options:** `amount`, `user`  
  🔐 Requires: Manage Messages

- **`/user`** - View detailed information about a server member.  
  **Option:** `target`  
  🔐 Requires: Moderate Members (Only to show punishment history)

---

## XP & Leaderboard Commands

- **`/level`** - View a user's XP level.  
  **Option:** `user` *(blank = self)*

- **`/top`** - View XP leaderboard.  
  **Option:** `type`: `text` | `voice`

- **`/resetleaderboard`** - Reset leaderboard data.  
  **Option:** `type`: `text`, `voice`, or `all`  
  🔐 Requires: Administrator

- **`/activity`** - View user activity.  
  **Options:**  
  - `user`  
  - `timeframe`: 24 Hours, 7 Days, 30 Days

---

## Fun Commands

- **`!roll`** - Roll dice.  
  **Option:** `dice` (e.g. `d6`, `2d20`)

- **`!drinktime`, `!sesh`, `!chatrevive`** - Ping associated roles.  
  ⏱ Cooldowns:  
  - Drinktime / Sesh: 1 Hour  
  - Chatrevive: 45 Minutes

- **`/troll`** - Drag a user between two voice channels and spam ping them.  
  **Options:** `userid`, `channelid`, `vc1id`, `vc2id`  
  🔐 Requires: Moderator Role

- **`/trollstop`** - Stop an active troll session.  
  **Option:** `userid`  
  🔐 Requires: Moderator Role

- **`/spam`** - Spam ping a user.
  **Options:** `channel` (required), `user`, `role`  
  🔐 Requires: Moderator Role

- **`/420` or `!420`** - Displays the next 4:20.

---

## Member Count Commands

- **`/membercountconfig`** - Configure member count settings.  
  **Options:** `verified_role`, `eighteen_plus_role`, `embed_channel`, `voice_channel`  
  🔐 Requires: Moderate Members

- **`/updatecountembed`**, **`/updatecountvc`** - Manually update member count displays.  
  🔐 Requires: Administrator

---

## Server Settings

- **`/setlogchannel`** - Set log channels for various events.  
    **Options:** `moderation_log`, `call_log`, `member_log`, `role_log`, `message_log`, `channel_log`, `all_log_channel`  
  🔐 Requires: Administrator

- **`/welcomeconfig`** - Configure and set welcome messages for new members.  
  **Options:**
  - `set_target` — Choose `welcome_message` (public) or `welcome_dm_message` (DM), then reply to the bot with your welcome message.
  - `welcome_channel` — Optional (only used with `welcome_message`)

  > Buttons for ticket creation, staff applications, ban appeals, and staff reports are automatically included under the **DM welcome message**—if their respective links are provided via `/welcomeconfig`.

  🔐 **Requires:** Administrator

- **`/configureroles`** - Set roles used by the bot.  
  **Options:** `slashverify_role`, `admin_role`, `moderator_role`, `sesh_role`, `chatrevive_role`, `drink_role`  
  🔐 Requires: Administrator

- **`/autorole`** - Set or remove automatic roles for new members.  
  **Subcommands:** `set`, `remove`  
  🔐 Requires: Moderator Role

- **`/motm`** - Enable or disable Member of the Month.  
  **Subcommands:** `enable`, `disable`  
  **Option:** `role`  
  🔐 Requires: Administrator

- **`/setserverinfo`** - Set server info shown with `/serverinfo`.  
  🔐 Requires: Administrator

- **`/setcountingchannel`** - Set the counting game channel.  
  **Option:** `channel`  
  🔐 Requires: Administrator

- **`/setfeedbackchannel`** - Set where feedback is sent.  
  **Option:** `channel`  
  🔐 Requires: Administrator

- **`/xpexclude`** - Include or exclude a channel from gaining XP.
  -  **Subcommands:** `add`, `remove`
  -  **Option:** `channel`

  🔐 **Requires:** Administrator

* **`/messagelog`** - Manage which channels are included in message logging.
  - **Subcommands:** `include`, `exclude`
  - **Option:** `channel`

  🔐 **Requires:** Administrator

* **`/modapplication`** - Configure and manage moderator application systems.
  - **Subcommands:** `create-panel`, `preview`, `set-channel`, `toggle-approval`

  🔐 **Requires:** Administrator

---

## Developer-Only Commands
- **`/vban-connect`** - Connects to a VBAN stream and plays audio in VC.  

- **`/restart`** - Restarts the bot. 

- **`/blacklist`** - Blacklists a specific server from using the bot.

---