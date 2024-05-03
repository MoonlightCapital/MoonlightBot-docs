# temprole

This command allows you to assign a role to a user for a specified duration. After the duration has passed, the role
will be automatically removed from the user.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Manage Roles

For more information on editing permission requirements for specific users/roles, refer to
the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/temprole <user> <role> <duration> [reason]
```

### Options

* `user`: The user to assign the role to
* `role`: The role to assign to the user
* `duration`: The duration for which the role should be assigned to the user. For more information on the duration
  format, refer to the [arguments page](../start-up/arguments.md#durations)
* `reason`: The reason for assigning the role to the user. This is an optional parameter, which can be used for
  record-keeping

## Logs

* `TEMPROLE_EXTEND`: This log is triggered when a temporary role's duration is extended/reduced.
  It will log the user, the role, the responsible moderator, the reason and the duration of the extension/reduction.
* `TEMPROLE_ADD`: This log is triggered when a temporary role is assigned to a user.
  It will log the user, the role, the responsible moderator, the reason and the duration of the role assignment.

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)