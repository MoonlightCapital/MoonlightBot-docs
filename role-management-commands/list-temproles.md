# list-temproles

This command allows you to view all active temporary roles and paused roles in the server. It will display the user,
role, and the time remaining for each temporary/paused role.

{% hint style="info" %}
For information on how to assign a temporary role to a user, refer to
the [`temprole`](../role-management-commands/temprole.md#temprole) command and
for information on how to pause a role for a user, refer to
the [`pause-role`](../role-management-commands/pause-role.md#pause-role) command.

If an entry is shown as *Unsustained* it means that the conditions to sustain the role are currently not being met by the moderator who added the temporary action.
For more information on how this protective mechanic works, check the [FAQ](../start-up/faqs.md#how-does-the-temprole-sustain-mechanic-work)
{% endhint %}

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

*No specific permissions required*

By default, a user is required to have the following permissions to use this command:

* Manage Roles

For more information on editing permission requirements for specific users/roles, refer to
the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/list-temproles [target]
```

### Options

* `target`: Here you can specify a user or a role to filter the results

## Logs

*This command does not trigger any log events.*

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)
