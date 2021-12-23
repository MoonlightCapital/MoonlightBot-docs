# Warn

### **Description**

This command is used to warn people. Warnings are used to issue infractions with no additional punishment.

### **Required arguments**

* `user` - The user you want to warn

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs
* `dm-user` - Sends the reason for the warning to the user's DMs. Can be set to true or false
* `no-infraction` - Does not log an infraction. Log entry is still sent

Optional arguments can be specified in any order, as long as they're part of the same Slash Command.

### **Usage**

```
/warn <user> [reason]
```

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages **permissions in order to be able to execute this command.
