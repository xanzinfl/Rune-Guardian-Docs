# Rune Guardian Command List

A comprehensive list of commands for Rune Guardian, including descriptions and usage.

## General Commands
- **/about**: Displays information about the bot.

- **/Feedback**: Send feedback to the server admins or to the bot support team.
  - Options:
    - `Type` (required)
      - `Bot`: Send feedback to the developers
      - `Server`: Send feedback to the servers feedback channel
    - `Message`: Your feedback (required)

- **/setup**: Sets up the database for the server, Displays configuration commands

- **/showconfig**: Shows the current server settings
  - Requires Administrator

- **/serverinfo, !serverinfo**: Displays server information 
  - Set with `/setserverinfo`

- **/help**: Displays a list of available commands or detailed information for a specific command.
  - Options
    - `command`: the name of the command

- **/modhelp**: Displays a list of available moderation commands.
  - Requires `Moderator Role ID`

- **/reminder**: 
  - Subcommands:
    - `set`: Sets a reminder
      - Options:
        - `time` (required)
        - `frequency`: Eg. once, daily, weekly (required)
        - `timezone` (required)
        - `reason` (required)
        - `day` (required)
    - `list`: Lists all reminders for a user.
    - `remove`: Removes a reminder by ID.

- **/sendembed**: Sends a message as an embed.
  - Options:
    - `message`: The message to send in the embed (required).
    - `title`: Big text at the top of the embed.
    - `color`: The color of the strip on the left side of the embed.
    - `footer`: The small text at the very bottom of the embed.
    - `image`: Big image under the text in the embed.
    - `thumbnail`: The small image in the top right of the embed
    - `author`: Small text at the top of the embed.
    - `author_icon`: Small circular image at the top left of the embed.

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

- **/punishmenthistory**: Shows punishment history for a user.
  - Options:
    - `user`: The user to fetch punishment history for.

- **/removepunishmen**: Removes a specifiec punishment from a user's history.
  - Options:
    - `punishment_id`: The id of the punishment entry to remove.

- **/verifymember**: Assigns a role defined in `/configureroles option:slashverify_role`
  - Options:
    - `user`: The user to verify
  - Requires Administrator.

## XP and Leaderboard Commands
- **/level**: Checks a user’s level.
  - Options:
    - `user`: The user to check. (Leave blank to shown own level.)

- **/top**: Displays the leaderboard for text or voice XP.
  - Options:
    - `type`: The leaderboard type to view (`text` or `voice`).

- **/resetleaderboard**: Resets the XP leaderboard for the server.
  - Options:
    - `type`: The type of leaderboard to reset (`text`, `voice`, or `all`).
  - Requires Administrator.

## Fun Commands
- **!roll**: Rolls dice.
  - Optins:
    - `dice`: Specify the size and amount of dice to roll. Eg. d6, 2d6
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

## Member Count Commands
- **/membercountconfig**: Updates member count system settings.
  - Options:
    - `verified_role`: The ID of your verified role
    - `eighteen_plus_role`: The ID of the 18+ role
    - `embed_channel`: The ID of the channel to send the embed
    - `voice_channel`: The ID of the voice channel to display member count
  - Requires Admin Permissions

- **/updatecountembed**: Manually updates the member count embed.
  - Requires Admin Permissions

- **/updatecountvc**: Manually updates the member count voice channel.
  - Requires Admin Permissions

## Server Settings Commands
- **/setlogchannel**: 
  - Options:
    - `moderation_log`: Logs Warns, kicks, bans, etc. 
    - `call_log`: Logs Voice join, leave, switch, server mute, server deafen
    - `member_log`: Logs Joins, leaves, command usage, guild updates
    - `role_log`: Logs role create, update, delete
    - `message_log`: Logs message edit, delete, reactions, etc.
    - `channel_log`: Logs channel create, update, delete
    - `all_log_channel`: Sets all logs to a single channel
  - Requires Admin Permissions

- **/welcomeconfig**: Allows you to configure the welcome messages.
  - Options:
    - `ticket_channel`: The ID of your ticket channel.
    - `ban_appeal`: Your ban appeal form.
    - `staff_app`: Your staff application form.
    - `staff_report`: Your staff report form.
    - `welcome_message`: The message to send to the welcome channel.
    - `welcome_dm_message`: The message to dm the user.
    - `welcome_dm_message_2`: The second message to dm the user.(Includes buttons set above)
    - `welcome_channel`: The channel to send welcome messages to.
  - Requires Admin Permissions

- **/configureroles**: Allows you to configure certain roles the bot needs to function. Eg. Permission checks.
  - Options:
    - `slashverify_role`: The role to assign with `/verifymember`.
    - `admin_role`: Not in use.
    - `moderator_role`: Used for moderation commands permission checks.
    - `sesh_role`: The role to ping with `!sesh`.
    - `chatrevive_role`: The role to ping with `!chatrevive`.
    - `drink_role`: The role to ping with `!drinktime`.
  - Requires Admin Permissions

- **/autorole**: Manages the autorole for new members.
  - Subcommands:
    - `set`: Assign a role to new members (requires `role`).
    - `remove`: Removes the autorole setting.
  - Requires `Moderator Role ID`

- **/setserverinfo**: Sets the server information; shown with `/serverinfo`
  - Requires Admin Permissions

- **/setcountingchannel**: Sets the channel for the counting game.
  - Options:
    - `channel`: The channel to set as the counting channel.
  - Requires Admin Permissions

- **/setfeedbackchannel**: 
  - Options:
    - `channel`
  - Requires Admin Permissions

- **/setafkchannel**: Sets the AFK channel to exclude from voice XP tracking.
  - Options:
    - `channel`: The channel to set as AFK.
  - Requires Admin Permissions

- **/excludechannel**: Excludes a channel from message logging.
  - Options:
    - `channel`: The channel to exclude.
  - Requires Admin Permissions

- **/includechannel**: Re-includes a channel in message logging.
  - Options:
    - `channel`: The channel to include.
  - Requires Admin Permissions

---

This list provides all available commands for Rune Guardian, along with their descriptions and required options. Use this as a reference to make the most out of Rune Guardian’s functionality!
