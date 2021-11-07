# Unmute

### **Description**

This command is used to unmute an user from the server. It does this by removing the preset mute role.

{% hint style="info" %}
While this command creates an infraction, it cannot DM the reason to the user, nor the infraction will be shown in the global counter.
{% endhint %}

### **Required arguments**

* `user` - The user you want to unmute

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs

### Flags

* `--no-infraction` - Does not log an infraction. Log entry is still sent

### **Usage**

```
m:unmute <user> [reason]
```

### **Aliases**

`um`

### **Required permission:**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Manage Roles **permissions in order to be able to execute this command.
