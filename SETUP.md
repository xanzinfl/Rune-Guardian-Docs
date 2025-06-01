## Setup Guide for Rune Guardian

This guide walks through setting up and configuring Rune Guardian in your Discord server. Follow these steps to configure various features and make the most of our bot!

### 1. **Basic Setup**

Start by using `/setup` to get an overview of the available configuration commands and ensure the bot has all required permissions to perform its functions.

This command will display a list of configuration commands and a link to the setup documentation.

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
Here’s a **Setup Guide** section specifically for your **Ticket System**, formatted to match the rest of your Rune Guardian setup documentation:

---

### 3. **Ticket System Setup**

Create a fully customizable ticket panel to help members open tickets based on categories you define.

**Command**:

```plaintext
/create-ticket-panel
```

**Parameters**:

| Option                             | Description                                                                  
| ---------------------------------  | ---------------------------------------------------------------------------- 
| `transcripts_channel`              | The **text channel** where transcripts and logs should be sent.              
| `open_category`                    | The **category ID** where active tickets will be created.                    
| `closed_category`                  | The **category ID** where closed tickets will be moved.                      
| `ticket1_name`                     | The name of the **first ticket type** (e.g., "Support").                     
| `ticket1_description`              | Description of the **first ticket type** (e.g., "Get help with a problem."). 
| `ticket2_name` *(optional)*        | Name of a **second ticket type** (e.g., "Ban Appeal").                       
| `ticket2_description` *(optional)* | Description for the second ticket type.                                      

**Example Usage**:

```plaintext
/create-ticket-panel
transcripts_channel: #ticket-logs
open_category: 123456789012345678
closed_category: 234567890123456789
ticket1_name: Support
ticket1_description: Need help with something? Open a ticket!
ticket2_name: Ban Appeal
ticket2_description: Submit your appeal for review.
```

⚠️ *Make sure the bot has permission to manage channels and messages in the categories specified.*

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