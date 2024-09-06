# softban

The `softban` command bans then immediately unbans a user from the current server, deleting all messages they sent in the past 7 days.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Ban Members

By default, a user is required to have the following permissions to use this command:

* Ban Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/softban <user> [reason] [notify] [no-infraction]
```

### Options

* `user`: The user that you want to softban
* `reason`: The reason you want to softban them. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether they will be notified by Direct Message (True/False)
* `no-infraction`: Whether the mute counts as an infraction or not (True/False)

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True
{% endhint %}

## Logs

* `SOFTBAN`: This log is triggered when a user is softbanned. It will log the user, the responsible moderator and the reason for the softban. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)
