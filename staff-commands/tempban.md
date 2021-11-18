# Tempban

### **Description**

This command is used to temporarily ban an user from the server.

### **Required arguments**

* `user` - The user you want to tempban
* `duration` - Check the [duration](https://app.gitbook.com/@moonlightbot/s/docs/start-up/arguments#type-of-arguments) section for more information

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs

### Flags

* `--dm-user` - Sends the reason for the warning to the user's DMs
* `--no-infraction` - Does not log an infraction. Log entry is still sent

### **Usage**

```
m:tempban <user> <duration> [reason]
/tempban <user> <duration> [reason]
```

### **Aliases**

`tb`

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Ban Members **permissions in order to be able to execute this command.
