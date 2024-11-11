# Rune Guardian Setup Guide

Welcome to the Rune Guardian Setup Guide! Follow these instructions to configure Rune Guardian and make the most of its features.

## Step 1: Add Rune Guardian to Your Server
1. **Invite the Bot**: Use the [invite link](https://discord.com/oauth2/authorize?client_id=1285116010822893579) to add Rune Bot to your server.

---

## Step 2: Configuring Server Settings Using `/updatesettings`

Rune Bot’s functionality is highly customizable. Use `/updatesettings` to configure essential settings, logging channels, role assignments, and more. **Many features depend on setting specific values using this command.** Here’s a breakdown of each setting and its purpose:

### Logging Channels
Configure specific channels for Rune Guardian’s logs:
- **Moderation Log Channel ID**: Logs actions like bans, kicks, and timeouts.
- **Call Log Channel ID**: Logs call join and leave events.
- **Member Log Channel ID**: Logs member joins and leaves, aswell as server events.
- **Role Log Channel ID**: Logs role updates.
- **Message Log Channel ID**: Logs message edits and deletions, aswell as reactions.
- **Channel Log Channel ID**: Logs channel updates.
- **Ticket Channel ID**: Sets the destination for the "Create a Ticket" button in the welcome message.

**Example Usage**:
```bash
/updatesettings setting:ModerationLogChannelId value:#moderation-logs
```

### Role Settings
Specify roles that are used in certain bot functionalities:
- **Verified Role ID**: The role given to verified members.
- **Admin Role ID**: The role for server admins (required for certain moderation commands).
- **Moderator Role ID**: The role for moderators (required for some moderation commands).
- **Sesh Role ID**: The role to ping during `!sesh`.
- **Chat Revive Role ID**: The role to ping during `!chatrevive`.
- **Drink Time Role ID**: The role to ping during `!drinktime`.

**Example Usage**:
```bash
/updatesettings setting:Verified_ROLE_ID value:@Verified
```

### Welcome Messages and Customization
Customize the welcome messages sent to new members:
- **Welcome Channel ID**: Channel where the bot will send welcome messages.
- **Welcome DM Message**: Custom DM message sent to new members. You can mention the member by using `{user}` in the message.
- **Welcome DM Message 2**: A follow-up DM message for new members.
- **Welcome Message**: The message posted in the designated welcome channel.

#### Welcome Message 2 Buttons
- **Ban Appeal Link**: Link for members to appeal bans, accessible as a button in the 2nd welcome DM.
- **Staff Application Link**: Link for staff applications, accessible as a button in the 2nd welcome DM.
- **Staff Report Link**: Link for staff reports, accessible as a button in the 2nd welcome DM.

**Example Usage**:
```bash
/updatesettings setting:Welcome_DM_MSG value:Welcome {user} to our server! We’re glad to have you.
/updatesettings setting:BAN_APPEAL value:https://example.com/ban-appeal
/updatesettings setting:STAFF_APP value:https://example.com/staff-application
/updatesettings setting:STAFF_REPORT value:https://example.com/staff-report
/updatesettings setting:TicketChannelId value:#support
```

### Miscellaneous Settings
- **Embed Channel ID**: Used for count embed.
- **Voice Channel ID**: Used for shwoing the member count in a voice channel.

**Note**: If these settings aren’t configured, certain commands or features may not work as intended.

---

## Step 3: Enable Auto Role Assignment
If you want new members to be automatically assigned a role upon joining, you can enable the autorole feature:

1. Use the command `/autorole set [role]` to specify the role that should be assigned automatically.
   - Example: `/autorole set role:@NewMember`
2. To remove autorole, use `/autorole remove`.

---

## Step 4: Using the XP System and Leaderboards
Rune Bot can track user activity and provide an XP leaderboard based on text and voice activity.

1. **Check a User's Level**: Use `/level [user]` to display the XP level of a specified user.
2. **View the Leaderboard**: Use `/top [type]` to display a leaderboard for either text or voice activity.

**Note**: XP gain has rate-limiting to prevent spam and ensure fair tracking.

---

## Step 5: Configure the AFK Channel for Voice XP Exclusion
Set up a dedicated AFK channel where users won’t accumulate voice XP, ensuring XP is only tracked in active voice channels.

1. Use `/setafkchannel [channel]` to designate the AFK channel.
   - Example: `/setafkchannel channel:#afk`

---

## Step 6: Using Moderation Commands
Rune Bot provides a suite of moderation commands. These commands require moderator or admin permissions, depending on your role setup.

- **Ban a Member**: `/ban [user] [reason] [image]` - Bans a specified user with a reason.
- **Kick a Member**: `/kick [user] [reason] [image]` - Kicks a specified user with a reason.
- **Timeout a Member**: `/timeout [user] [duration] [image]` - Temporarily mutes a member.
- **Warn a Member**: `/warn [user] [reason] [image]` - Issues a warning to a user.

**Note**: These commands DM the user with the [reason] input.

These commands require specific log channels and roles to be set up using `/updatesettings` for proper functionality.

---

## Step 7: Set Up Counting Channel
Rune Bot includes a counting game that can be set up in any designated channel.

1. Use `/setcountingchannel [channel]` to assign the channel where the counting game will take place.
   - Example: `/setcountingchannel channel:#counting`

---

## Step 8: Configure Engagement Commands

- **Chat Revive**: `!chatrevive` -
- **Drink Time**: `!drinktime` - Announces a drinking break.
- **Sesh Command**: `!sesh` - Pings the designated session role for group activities.
  
These commands have cooldowns to prevent spam, and roles should be configured in `/updatesettings` for functionality.

---

## Step 9: More Information and Help
You can use `/modhelp` and `/about` within your server for basic info.

If you need additional support or guidance, contact one of the [developers](https://linktr.ee/Rune.gg).

