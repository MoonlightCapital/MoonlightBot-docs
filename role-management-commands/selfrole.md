# selfrole

This command allows you to assign or remove a role from yourself.

{% hint style="warning" %}
The server admins need to make a role self-assignable before you can use it. 
[**Learn how to do this.**](/management-commands/config.md#roles-self-assignable)
{% endhint %}

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

*No specific permissions required*

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## Syntax

```text
/selfrole [role]
```

### Options

* `role`: The role to assign/remove from yourself. If no role is specified, the command will list all self-assignable roles

## Logs

* `SELFROLE_REMOVE`: This log is triggered when a selfrole is removed by the user. It will log the user and the role that was removed
* `SELFROLE_ADD`: This log is triggered when a selfrole is added by the user. It will log the user and the role that was added

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)
