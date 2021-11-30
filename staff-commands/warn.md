# Warn

### **Description**

This command is used to warn people. Warnings are used to issue infractions with no additional punishment.

### **Required arguments**

* `user` - The user you want to warn

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs

### Flags

* `--dm-user` - Sends the reason for the warning to the user's DMs
* `--no-infraction` - Does not log an infraction. Log entry is still sent

### **Usage**

```
/warn <user> [reason]
```

### **Aliases**

`w`

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages **permissions in order to be able to execute this command.
