# pause-role

This command allows you to pause a role for a user for a specified duration. With a pause is meant that the role is
removed from the user for the specified duration. After the duration has passed, the role will be reassigned to the
user.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Manage Roles

For more information on editing permission requirements for specific users/roles, refer to
the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/pause-role <user> <role> <duration> [reason]
```

### Options

* `user`: The user to pause the role for. You can mention the user or use their ID to specify the user.
* `role`: The role to pause for the user. You can mention the role or use its ID to specify the role.
* `duration`: The duration for which the role should be paused for the user. You can specify the duration in the
  format `1w2d3h4m5s` where `w` stands for weeks, `d` for days, `h` for hours, `m` for minutes, and `s` for seconds.
  Note that you can omit any of the units if you don't want to specify them, know that you need to specify at least
  one unit.
* `reason`: The reason for pausing the role for the user. This is an optional parameter, which can be used for
  moderation.

## Logs

* `PAUSE_ROLE_EXTEND`: This log is triggered when a role pause's duration is extended/reduced.
  It will log the user, the role, the responsible moderator, the reason and the duration of the extension/reduction.
* `PAUSE_ROLE_ADD`: This log is triggered when a role is paused for a user.
  It will log the user, the role, the responsible moderator, the reason and the duration of the role pause.

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)