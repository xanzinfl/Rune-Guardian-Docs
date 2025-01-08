## Setup Guide for Rune Guardian

This guide walks through setting up and configuring Rune Guardian Bot in your Discord server. Follow these steps to configure various features and make the most of your bot!

### 1. **Basic Setup**

Start by using `/setup` to get an overview of the available configuration commands and ensure the bot has all required permissions to perform its functions.

This command will display a list of configuration commands and a link to the setup documentation.
**Note**: The bot may not work properly if this command isnt run

---

### 2. **Auto Role Setup**

Set up automatic role assignment for new members.

**Commands**:
1. **Set Auto Role**: Automatically assign a role to new members.
   ```usage
   /autorole set role:@RoleName
   ```
2. **Remove Auto Role**: Remove the auto-role assignment.
   ```usage
   /autorole remove
   ```

---

### 3. **Moderation Commands**

Moderate your server with commands to ban, kick, and timeout users.

**Commands**:
- **Ban Member**:
   ```plaintext
   /ban user:@User reason:"Reason for the ban" image: (optional)
   ```
- **Unban Member**:
   ```plaintext
   /unban user:"User ID" reason:"Optional reason"
   ```
- **Kick Member**:
   ```plaintext
   /kick user:@User reason:"Reason for the kick" image: (optional)
   ```
- **Timeout Member**:
   ```plaintext
   /timeout user:@User duration:<Choose duration> reason:"Reason for timeout" image: (optional)
   ```

- **Warn Member**:
   ```usage
   /warn user:@User reason:"Reason for warning" image: (optional)
   ```

**Note** the bot sends the punished user a message 
```example
You have been timed out in [Server Name] for the following reason: [reason].
```

---

### 4. **Counting System**

Set up a counting channel for users to participate in counting.

- **Set Counting Channel**:
   ```usage
   /setcountingchannel channel:#ChannelName
   ```

---

### 5. **Member Count System**

- **Configure Member Count System**:
   - Configure settings for displaying member counts, verified roles, and other member-related settings.
   ```usage
   /membercountconfig verified_role:"Verified Role ID" eighteen_plus_role:"18+ Role ID" embed_channel:#EmbedChannel voice_channel:#VoiceChannel
   ```
- **Manually update the counts**
   ```usage
   /updatecountembed
   /updatecountvc
   ```
---

### 6. **Welcome System Configuration**

Customize the welcome messages.

**Commands**:
- **Configure Welcome Settings**:
   ```usage
   /welcomeconfig ticket_channel:#TicketChannel ban_appeal:"Ban Appeal Link" staff_app:"Staff Application Link" staff_report:"Staff Report Link" welcome_message:"Welcome to our server!" welcome_dm_message:"Welcome DM text" welcome_dm_message_2:"Additional DM text" welcome_channel:#WelcomeChannel
   ```
**Note**: The links and ticket channel id are for buttons under the second welcome message

---

### 7. **Log Channels Setup**

Specify channels for different types of logs such as moderation actions, member joins/leaves, and message edits/deletes.

**Commands**:
- **Set Log Channels**:
   ```plaintext
   /setlogchannel moderation_log:#ModerationLog call_log:#CallLog member_log:#MemberLog role_log:#RoleLog message_log:#MessageLog channel_log:#ChannelLog all_log_channel:#GeneralLogChannel
   ```

---

### 8. **Feedback System**

Set up a feedback channel for server-related feedback and enable bot-related feedback to be sent to our support server.

**Commands**:
1. **Set Feedback Channel**:
   ```plaintext
   /setfeedbackchannel channel:#FeedbackChannel
   ```
2. **Send Feedback**:
   ```plaintext
   /feedback type:<server or bot> message:"Your feedback message"
   ```

---

### 9. **Role Configuration**

Configure special roles for admin, moderator, verified members, and additional roles like the sesh or drink role.

**Command**:
```plaintext
/configureroles slashverify_role:@Role admin_role:@Role moderator_role:@Role sesh_role:@Role chatrevive_role:@Role drink_role:@Role
```

---

### 10. **AFK Channel Setup**

Define an AFK channel to exclude from voice activity tracking.

**Command**:
```plaintext
/setafkchannel channel:#AFKChannel
```

---

### 11. **Embed Messaging**

Send rich embed messages with customizable options like title, color, footer, images, and author details.

**Command**:
```plaintext
/sendembed message:"Your main message" title:"Title" color:"#3498db" footer:"Footer text" image:"Image URL" thumbnail:"Thumbnail URL" author:"Author Name" author_icon:"Author Icon URL"
```

---

### 12. **Leaderboard and XP System**

**Commands**:
- **Check Level**:
   ```plaintext
   /level user:@User (optional)
   ```
- **View Top Leaderboard**:
   ```plaintext
   /top type:<text or voice>
   ```
- **Reset Leaderboard**:
   ```plaintext
   /resetleaderboard type:<text, voice, or all>
   ```

---

### 13. **Server Information and Verification**

**Commands**:
- **Display Server Information**:
   ```plaintext
   /serverinfo
   ```
- **Set Server Information**:
   ```plaintext
   /setserverinfo info:"Description or information about the server"
   ```
- **Verify Member**:
   ```plaintext
   /verifymember user:@User
   ```

---

### 14. **Show Current Configuration**

Use this command to view all currently configured settings for your guild.

**Command**:
```plaintext
/showconfig
```

This displays a summary of all active configuration settings in your guild.

---

### 15. **Help Command**

If you need help with any specific command, use `/help` followed by the command name.

**Command**:
```plaintext
/help command:<command_name>
```

---

This setup guide should help you get all the necessary configurations in place. For further assistance [Contact Us](https://linktr.ee/Rune.gg).