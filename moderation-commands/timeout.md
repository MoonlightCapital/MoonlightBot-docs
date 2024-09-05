# timeout

The `timeout` command temporarily times out a user from the current server.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Moderate Members

By default, a user is required to have the following permissions to use this command:

* Moderate Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/timeout <user> <duration> [reason] [notify] [no-infraction]
```

### Options

* `user`: The user that you want to ban
* `duration`: The duration you want to time them out for. For more information on the duration format, refer to the [arguments page](../start-up/arguments.md#durations)
* `reason`: The reason you want to time them out. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether the target user will be notified by Direct Message (True/False). This is optional and contains the server name and reason
* `no-infraction`: Whether the ban counts as an infraction or not (True/False).

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True
{% endhint %}

## Logs

* `TIMEOUT_REMOVE`: This log is triggered when a user is removed from timeout. It will log the user, the responsible moderator and the reason for the timeout removal.
* `TIMEOUT`: This log is triggered when a user is timed out. It will log the user, the responsible moderator and the reason for the timeout. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)
