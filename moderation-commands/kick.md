# kick

The `kick` command kicks a user from the current server. The user can rejoin the server if they have an invite link.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Kick Members

By default, a user is required to have the following permissions to use this command:

* Kick Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/kick <user> [reason] [notify] [no-infraction]
```

### Options

* `user`: The user that you want to kick
* `reason`: The reason you want to kick them. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether they will be notified by Direct Message (True/False)
* `no-infraction`: Whether the ban counts as an infraction or not (True/False). This is optional and contains the server name and reason

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True
{% endhint %}

## Logs

* `KICK`: This log is triggered when a user is kicked from a server. It will log the user, the responsible moderator and the reason for the kick. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)
