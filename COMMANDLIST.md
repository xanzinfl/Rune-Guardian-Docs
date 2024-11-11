# Rune Bot Command List

A comprehensive list of commands for Rune Guardian, including descriptions and usage.

## General Commands
- **/about**: Displays information about the bot.

## Moderation Commands
- **/ban**: Bans a member from the server.
  - Options: 
    - `user`: The user to ban (required).
    - `reason`: Reason for the ban (required).
    - `image`: Optional image as evidence.
  - Requires `Moderator Role ID`

- **/unban**: Unbans a member by their user ID.
  - Options:
    - `user`: The user ID to unban (required).
    - `reason`: Reason for the unban (optional).
  - Requires `Moderator Role ID`

- **/kick**: Kicks a member from the server.
  - Options:
    - `user`: The user to kick (required).
    - `reason`: Reason for the kick (required).
    - `image`: Optional image as evidence.
  - Requires `Moderator Role ID`

- **/timeout**: Temporarily mutes a member for a specified duration.
  - Options:
    - `user`: The user to timeout (required).
    - `reason`: Reason for the timeout (required).
    - `duration`: Duration of the timeout (required).
    - `image`: Optional image as evidence.
  - Requires `Moderator Role ID`

- **/warn**: Issues a warning to a member in the server.
  - Options:
    - `user`: The member to warn (required).
    - `reason`: The reason for the warning (required).
    - `image`: Optional image as evidence.
  - Requires `Moderator Role ID`

## XP and Leaderboard Commands
- **/level**: Checks a user’s level.
  - Options:
    - `user`: The user to check.

- **/top**: Displays the leaderboard for text or voice XP.
  - Options:
    - `type`: The leaderboard type to view (`text` or `voice`).

- **/resetleaderboard**: Resets the XP leaderboard for the server.
  - Options:
    - `type`: The type of leaderboard to reset (`text`, `voice`, or `all`).
    - Requires Administrator.

## Fun Commands
- **!drinktime**: pings drinktime role with a message.
  - Cooldown: 1 Hour
- **!sesh**: pings sesh role with a message.
  - Cooldown: 1 Hour
- **!chatrevive**: pings chat revive role with a message.
  - Cooldown: 45 Minutes

- **/troll**: Drags a user between two voice channels.
  - Options:
    - `userid`: The user to troll (required).
    - `channelid`: The text channel to send @mentions to (required).
    - `vc1id`: The first voice channel to move the user to (required).
    - `vc2id`: The second voice channel to move the user to (required).
  - Requires `Moderator Role ID`

- **/trollstop**: Stops the active troll action for a user.
  - Options:
    - `userid`: The user to stop trolling (required).
  - Requires `Moderator Role ID`

- **/spam**: Sends spam messages to a specified user, role, or channel.
  - Options:
    - `channel`: The channel to send spam messages in (required).
    - `user`: The user to spam (optional).
    - `role`: The role to spam (optional).
  - Requires `Moderator Role ID`

## Miscellaneous Commands
- **/sendembed**: Sends a message as an embed.
  - Options:
    - `message`: The message to send in the embed (required).

- **/updatecountembed**: Manually updates the member count embed.
  - Requires Admin Permissions
- **/updatecountvc**: Manually updates the member count voice channel.
  - Requires Admin Permissions

## Server Settings Commands
- **/updatesettings**: Updates server-specific settings stored in the database.
  - Options:
    - `setting`: The setting to update (required). Choices include various log channel IDs, role IDs, welcome messages, and links.
    - `value`: The new value for the specified setting (required).
  - Requires Admin Permissions

- **/autorole**: Manages the autorole for new members.
  - Subcommands:
    - `set`: Assign a role to new members (requires `role`).
    - `remove`: Removes the autorole setting.
  - Requires `Moderator Role ID`

- **/setcountingchannel**: Sets the channel for the counting game.
  - Options:
    - `channel`: The channel to set as the counting channel.
  - Requires Admin Permissions

- **/setafkchannel**: Sets the AFK channel to exclude from voice XP tracking.
  - Options:
    - `channel`: The channel to set as AFK.
  - Requires Admin Permissions

- **/excludechannel**: Excludes a channel from message logging.
  - Options:
    - `channel`: The channel to exclude.
  - Requires Admin Permissions

- **/includechannel**: Re-includes a channel back in message logging.
  - Options:
    - `channel`: The channel to include.
  - Requires Admin Permissions

- **/modhelp**: Displays a list of available moderation commands.
  - Requires `Moderator Role ID`

---

This list provides all available commands for Rune Guardian, along with their descriptions and required options. Use this as a reference to make the most out of Rune Guardian’s functionality!
