# Softban

### **Description**

This command is used to Ban an user from the server and immediately unban it. This acts like a kick that deletes the user's recent messages.

### **Required arguments**

* `user` - The user you want to softban

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs

### **Options**

* `dm-user` - Sends the reason for the warning to the user's DMs
* `no-infraction` - Does not log an infraction. Log entry is still sent

### **Usage**

```
/softban <user> [reason]
```

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Ban Members **permissions in order to be able to execute this command.
