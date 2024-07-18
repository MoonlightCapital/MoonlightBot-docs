# softban

Softbans the user to clear recent messages - this will cause the bot to ban and then immediately unban the user once the messages have been cleared.

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

* `user`: The user you wish to softban - this is mandatory
* `reason`: You can enter a reason as to why the user was softbanned - this is optional but recommended and will show in the logs
* `notify`: You can choose to have the bot notify the softbanned user via DM if you wish - this may not work if the user has DM's disabled
* `no-infraction`: Set this to true if you DON'T want to record an infraction - this is optional and if left blank, an infraction will be recorded

## Logs

* `SOFTBAN`: <TODO: describe>

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)
