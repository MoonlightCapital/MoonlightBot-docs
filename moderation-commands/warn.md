# warn

The `warn` command issues a warning to a user in the current server.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Moderate Members

By default, a user is required to have the following permissions to use this command:

* Moderate Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](../get-started/permission-tutorial.md)

## Syntax

```
/warn <user> [reason] [notify] [no-infraction]
```

### Options

* `user`: The user that you want to Warn - this is mandatory
* `reason`: The reason you want to warn them. This is an optional parameter, which can be used for record-keeping
* `notify`: Whether the target user will be notified by Direct Message (True/False)
* `no-infraction`: Whether the warning counts as an infraction or not (True/False). This is optional and contains the server name and reason

{% hint style="warning" %}
The user will not be notified if both `notify` and `no-infraction` are set to True
{% endhint %}

## Logs

* `WARN`: This log is triggered when a user is successfully warned. It will log the user, the responsible moderator and the reason for the warning. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](../#logging)
