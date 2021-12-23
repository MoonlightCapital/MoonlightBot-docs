# Tempban

### **Description**

This command is used to temporarily ban an user from the server.

### **Required arguments**

* `user` - The user you want to tempban
* `duration` - Check the [duration](https://app.gitbook.com/@moonlightbot/s/docs/start-up/arguments#type-of-arguments) section for more information

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs
* `dm-user` - Sends the reason for the warning to the user's DMs - can be set to true or false
* `no-infraction` - Does not log an infraction. Log entry is still sent

### **Usage**

```
/tempban <user> <duration> [reason] [dm-user] [no-infraction]
```

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Ban Members **permissions in order to be able to execute this command.
