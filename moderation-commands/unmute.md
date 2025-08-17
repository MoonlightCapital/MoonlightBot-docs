# unmute

This command can be used to unmute a user that is currently muted - this must have been a mute enacted via MoonlightBot.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Moderate Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## Syntax

```text
/unmute <user> [reason] [notify] [no-infraction]
```

### Options

* `user`: The user that you want to unmute
* `reason`: The reason you want to unmute them. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether the target user will be notified by Direct Message (True/False)
* `no-infraction`: Whether the unmute counts as an infraction or not (True/False)

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True.
{% endhint %}

## Logs

* `UNMUTE`: This log is triggered when a user is successfully unmuted. It will log the user, the responsible moderator and the reason for the unmute. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)
