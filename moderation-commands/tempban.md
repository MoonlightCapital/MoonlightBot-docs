# tempban

The `tempban` command temporarily bans a user from the current server.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Ban Members

By default, a user is required to have the following permissions to use this command:

* Ban Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md).

## Syntax

```text
/tempban <user> <duration> [reason] [notify] [no-infraction]
```

### Options

* `user`: The user that you want to ban
* `duration`: The duration you want to ban them for. For more information on the duration format, refer to the [options page](/start-up/options.md#durations)
* `reason`: The reason you want to ban them. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether the target user will be notified by Direct Message (True/False). This is optional and contains the server name and reason
* `no-infraction`: Whether the ban counts as an infraction or not (True/False)

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True.
{% endhint %}

## Logs

* `TEMPBAN_EXTEND`: This log is triggered when a tempban is successfully extended. It will log the user, the responsible moderator and the reason for the extended ban
* `BAN`: This log is triggered when a user is successfully banned. It will log the user, the responsible moderator and the reason for the ban. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging).
