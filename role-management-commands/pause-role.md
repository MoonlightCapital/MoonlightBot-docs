# pause-role

This command allows you to pause a role for a user for a specified duration. This means that the role is removed from
the user for the specified duration. After the duration has passed, the role will be automatically reassigned to the
user.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Manage Roles

For more information on editing permission requirements for specific users/roles, refer to
the [permissions tutorial](/start-up/permission-tutorial.md)

## Syntax

```text
/pause-role <user> <role> <duration> [reason] [notify]
```

### Options

* `user`: The user to pause the role for
* `role`: The role to pause for the user
* `duration`: The duration for which the role should be paused for the user. For more information on the duration
  format, refer to the [options page](/start-up/options.md#durations)
* `reason`: The reason for pausing the role for the user. This is an optional parameter, which can be used for
  record-keeping
* `notify`: Sends a Direct Message to inform the user about the role pause. This is optional and contains the role name, duration, expiration date and reason

## Logs

* `PAUSE_ROLE_EXTEND`: This log is triggered when a role pause's duration is extended/reduced.
  It will log the user, the role, the responsible moderator, the reason and the duration of the extension/reduction.
* `PAUSE_ROLE_ADD`: This log is triggered when a role is paused for a user.
  It will log the user, the role, the responsible moderator, the reason and the duration of the role pause.

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)
