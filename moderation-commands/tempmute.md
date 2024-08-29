# tempmute

The `tempmute` command temporarily mutes a user from the current server.

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
* `duration`: The duration of the tempmute
* `reason`: The reason you want to mute them. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether the target user will be notified by Direct Message (True/False)
* `no-infraction`: Whether the tempmute counts as an infraction or not (True/False). This is optional and contains the server name and reason
* `remove-roles`: Whether to temporarily remove the users roles or not (True/False)

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True
{% endhint %}

## Logs

* `TEMPMUTE_EXTEND`: <TODO: describe>
* `MUTE`: <TODO: describe>

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)
