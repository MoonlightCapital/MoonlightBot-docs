# Mute

### **Description**

This command is used to mute an user from the server. It does this by adding a specially preset mute role.

{% hint style="info" %}
We are not responsible if the muted user can still talk even with the mute role on. Check your channel overrides.
{% endhint %}

### **Required arguments**

* `user` - The user you want to mute

### **Optional arguments**

* `reason` - The reason for the infraction. It will be shown in bot logs
* `dm-user` - Sends the reason for the warning to the user's DMs
* `no-infraction` - Does not log an infraction. Log entry is still sent
* `purge-roles` - This flag is used to remove every possible (counting hierarchy) role before muting.

### **Usage**

```
/mute <member> [...reason] [dm-user] [no-infraction] [purge-roles]
```

### **Required permission:**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Manage Roles** permissions in order to be able to execute this command.
