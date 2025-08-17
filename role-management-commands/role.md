# role

This command allows you to assign or remove a role from a user. If the role is already assigned to the user, it will be removed and vice versa.

{% hint style="info" %}
you can also target users who are currently not on the server. By doing so, it creates/removes a persistence, meaning the role will be assigned when the user joins the server.
{% endhint %}

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Manage Roles

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## Syntax

```text
/role <user> <role> [reason]
```

### Options

* `user`: The user to assign/remove the role to/from
* `role`: The role to assign/remove from the user
* `reason`: The reason for assigning/removing the role from the user. This is an optional parameter, which can be used for record-keeping

## Logs

* `ROLE_ADD`: This log is triggered when a role is assigned to a user. It will log the user, the role, the responsible moderator, and the reason for the role assignment
* `ROLE_REMOVE`: This log is triggered when a role is removed from a user. It will log the user, the role, the responsible moderator, and the reason for the role removal

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)
