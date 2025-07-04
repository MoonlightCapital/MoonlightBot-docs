# unban

The `unban` command unbans a user from the current server.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Ban Members

By default, a user is required to have the following permissions to use this command:

* Ban Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## Syntax

```text
/unban <user> [reason] [no-infraction]
```

### Options

* `user`: The user that you want to unban
* `reason`: The reason you want to unban them. This is an optional parameter, which can be used for record-keeping
* `no-infraction`: Whether the unban counts as an infraction or not (True/False)

## Logs

* `UNBAN`: This log is triggered when a user is successfully unbanned. It will log the user, the responsible moderator and the reason for the unban. If an infraction is created, it will also include the infraction ID

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)
