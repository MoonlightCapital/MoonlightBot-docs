# temprole

This command allows you to assign a role to a user for a specified duration. After the duration has passed, the role
will be removed from the user.

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

* `user`: The user to assign the role to. You can mention the user or use their ID to specify the user.
* `role`: The role to assign to the user. You can mention the role or use its ID to specify the role.
* `duration`: The duration for which the role should be assigned to the user. You can specify the duration in the
  format `1w2d3h4m5s` where `w` stands for weeks, `d` for days, `h` for hours, `m` for minutes, and `s` for seconds.
  Note that you can omit any of the units if you don't want to specify them, just know that you need to specify at least
  one unit.
* `reason`: The reason for assigning the role to the user. This is an optional parameter, which can be used for
  moderation purposes.

## Logs

* `TEMPROLE_EXTEND`: This log is triggered when a temporary role's duration is extended/reduced.
  It will log the user, the role the responsible moderator, the reason and the duration of the extension/reduction.
* `TEMPROLE_ADD`: This log is triggered when a temporary role is assigned to a user.
  It will log the user, the role, the responsible moderator, the reason and the duration of the role assignment.

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)