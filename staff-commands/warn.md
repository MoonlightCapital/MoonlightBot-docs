# Warn

### **Description**

This command is used to warn people. Warnings are used to issue infractions with no additional punishment.

### **Required arguments**

* `user` - The user you want to warn

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs

### **Options**

* `dm-user` - Sends the reason for the warning to the user's DMs. Can be set to true or false
* `no-infraction` - Does not log an infraction. Log entry is still sent

Options can be specified in any order, as long as they're part of the same Slash Command.

### **Usage**

```
/warn <member> [...reason] [dm-user] [no-infraction]
```

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages** permissions in order to be able to execute this command.
