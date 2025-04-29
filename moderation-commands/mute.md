# mute

The `mute` command mutes a user by giving them the server's configured mute role. This is intended to revoke the user's permissions to talk in the server while still being able to read messages, or otherwise restrict accordingly to the server's preferences.

{% hint style="info" %}
A server administrator needs to configure a mute role in order to enable this command. This can be done quickly with the [`/create-muterole`](/management-commands/create-muterole.md) command.
{% endhint %}

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Moderate Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md).

## Syntax

```
/mute <user> [reason] [notify] [no-infraction] [remove-roles]
```

### Options

* `user`: The user that you want to mute
* `reason`: The reason you want to mute them. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether they will be notified by Direct Message (True/False) This is optional and contains the server name and reason
* `no-infraction`: Whether the mute counts as an infraction or not (True/False)
* `remove-roles`: Whether the user's other roles will be removed (True/False)

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True.
{% endhint %}

## Logs

* `MUTE`: This log is triggered when a user is muted. It will log the user, the responsible moderator and the reason for the muting. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging).
