# Tempmute

### **Description**

This command is used to temporarily mute an user from the server. Just like `mute` except the role is removed after the set duration.

### **Required arguments**

* `user` - The user you want to tempmute
* `duration` - Check the [duration](https://app.gitbook.com/@moonlightbot/s/docs/start-up/arguments#type-of-arguments) section for more information

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs
* `dm-user` - Sends the reason for the warning to the user's DMs - can be True or False
* `no-infraction` - Does not log an infraction. Log entry is still sent
* `purge-roles` - This argument is used to remove every possible (counting hierarchy) role before muting.

### **Usage**

```
/tempmute <member> <duration> [...reason] [dm-user] [no-infraction] [purge-roles]
```

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Manage Roles** permissions in order to be able to execute this command.
