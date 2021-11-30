# Raid-cleanup

### **Description**

This command cleans up any raid invasion by banning all users who joined after a certain period of time.

### **Required arguments**

* `age` - The age of the accounts from the time the command is used. It's a duration type of argument.
  * For example, setting this to `1 hour` will only target accounts created less than one hour ago.
  * This value cannot exceed 14 days.

### **Optional arguments**

* `joinThreshold` - The difference between the moment the command is used and the server join time of the accounts. It's a duration type of argument.
  * For example, setting this to `1 hour` will target accounts who joined the server less than one hour ago.
  * If not a valid duration, this will be considered part of the `reason` argument.
  * This value cannot exceed 24 hours.
* `reason` - The reason to provide in the logs.

### Flags

* `--clean-messages` - Setting this flag will delete the messages sent by the banned users in the last 7 days.

### **Usage**

```
/raid-cleanup <age> [joinThreshold] [...reason]
```

{% hint style="info" %}
The `age` and `joinThreshold` parameters are connected through a logical AND, meaning both conditions need to be satisfied at the same time by the same user
{% endhint %}

{% hint style="warning" %}
This command does not issue infractions to the banned users.
{% endhint %}

### **Required permissions**

This command's level is 100 by default.\
The bot needs **Read Messages, Send Messages, Ban Members** permissions in order to be able to execute this command.
