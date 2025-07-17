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

- **`/setup`** - Displays configuration options.
  🔐 Requires: Manage Guild

- **`/showconfig`** - Shows the current server settings.  
  🔐 Requires: Manage Guild

- **`/dashboard`** - Shows the bots dashboard.
  🔐 Requires: Manage Guild

- **`/serverinfo`, `!serverinfo`** - Displays server information.  
  *(Configured using `/setserverinfo`)*

- **`/help`** - Displays a list of available commands or detailed info for a specific command.  
  **Option:** `command`

- **`/modhelp`** - Lists all moderation commands.  
  🔐 Requires: Moderate Members

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

---

## Ticket Commands

- **`/rename`** - Rename the current ticket.
  **Option:** `new_name`
  🔐 Requires: Manage Guild, Support Roles

- **`/close`** - Close the current ticket.
  **Option:** `reason`
  🔐 Requires: Manage Guild, Support Roles

- **`/reopen`** - Reopen the current ticket.
  **Option:** `reason`
  🔐 Requires: Manage Guild, Support Roles

- **`/claim`** - Claim the current ticket.
  🔐 Requires: Manage Guild, Support Roles

- **`/unclaim`** - Unclaim the current ticket.
  🔐 Requires: Manage Guild, Support Roles

---

## Moderation Commands

- **`/ban`** - Ban a user.  
  **Options:** `user`, `reason`, `dm`, `image`  
  🔐 Requires: Ban Members

- **`/unban`** - Unban a user by ID.  
  **Options:** `user`, `reason`
  🔐 Requires: Ban Members

- **`/kick`** - Kick a user.  
  **Options:** `user`, `reason`, `dm`, `image`  
  🔐 Requires: Kick Members

- **`/timeout`** - Temporarily mute a user.  
  **Options:** `user`, `reason`, `duration`, `dm`, `image`  
  🔐 Requires: Moderate Members

- **`/warn`** - Issue a warning.  
  **Options:** `user`, `reason`, `dm`, `image`  
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
  🔐 Requires: Manage Guild

- **`/activity`** - View user activity.  
  **Options:**  
  - `user`  
  - `timeframe`: 24 Hours, 7 Days, 30 Days

---

## Fun Commands

- **`!roll`** - Roll dice.  
  **Option:** `dice` (e.g. `d6`, `2d20`)

- **`!drinktime`, `!sesh`, `!chatrevive`** - Ping associated roles.  
  ⏱ Cooldown: 45 Minutes

- **`/troll`** - Drag a user between two voice channels and spam ping them.  
  **Options:** `userid`, `channelid`, `vc1id`, `vc2id`  
  🔐 Requires: Manage Messages

- **`/trollstop`** - Stop an active troll session.  
  **Option:** `userid`  
  🔐 Requires: Manage Messages

- **`/spam`** - Spam ping a user.
  **Options:** `channel` (required), `user`, `role`  
  🔐 Requires: Manage Messages

- **`/420` or `!420`** - Displays the next 4:20.

---

## Member Count Commands

- **`/updatecountembed`**, **`/updatecountvc`** - Manually update member count displays.  
  🔐 Requires: Manage Guild

---

## Developer-Only Commands
- **`/vban-connect`** - Connects to a VBAN stream and plays audio in VC.  

- **`/restart`** - Restarts the bot. 

- **`/blacklist`** - Blacklists a specific server from using the bot.

---