# Temprole

### **Description**

This command is used to add a role to an user, and removes it after a specified amount of time (duration). If the user has already set that temprole, using this command again will add the new duration to the current one.

{% hint style="info" %}
You can reduce the total duration of a temprole by setting a negative duration
{% endhint %}

### **Required arguments**

* `user` - The user you want to assign the role to
* `role` - The role you want to assign to the user
* `duration` - Check the [duration](../start-up/arguments.md#durations) section for more information

### **Optional arguments**

* `reason` - The reason for this action for logging purposes.

### **Usage**

```
/temprole <user> <role> <duration> [reason]
```

{% hint style="info" %}
The [Frequently Asked Questions](../start-up/faqs.md) has answers for some of the most common temprole-related questions
{% endhint %}

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Manage Roles** permissions in order to be able to execute this command.
