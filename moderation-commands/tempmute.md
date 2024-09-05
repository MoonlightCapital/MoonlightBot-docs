# tempmute

The `tempmute` command temporarily mutes a user from the current server. This is intended to revoke the user's permissions to talk in the server while still being able to read messages, or otherwise restrict accordingly to the server's preferences.

{% hint style="info" %}
A server administrator needs to configure a mute role in order to enable this command. This can be done quickly with the [`/create-muterole`](../management-commands/create-muterole.md) command.
{% endhint %}

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Moderate Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/tempmute <user> <duration> [reason] [notify] [no-infraction] [remove-roles]
```

### Options

* `user`: The user that you want to mute
* `duration`: The duration of the tempmute. For more information on the duration format, refer to the [arguments page](../start-up/arguments.md#durations)
* `reason`: The reason you want to mute them. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether they will be notified by Direct Message (True/False)
* `no-infraction`: Whether the tempmute counts as an infraction or not (True/False). This is optional and contains the server name and reason
* `remove-roles`: Whether to temporarily remove the users roles or not (True/False)

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True
{% endhint %}

## Logs

* `TEMPMUTE_EXTEND`: This log is triggered when a tempmute is successfully extended. It will log the user, the responsible moderator and the reason for the extended mute.
* `MUTE`: This log is triggered when a user is muted. It will log the user, the responsible moderator and the reason for the muting. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)
