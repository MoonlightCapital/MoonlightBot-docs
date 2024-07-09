# unmute

Unmute a user that is currently muted and allow them to interact with the server again - this must have been a mute enacted via MoonlightBot

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Moderate Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/unmute <user> [reason] [notify] [no-infraction]
```

### Options

* `user`: The user you wish to unmute - this is mandatory
* `reason`: You can enter a reason as to why the user was unmuted - this is optional but recommended and will show in the logs
* `notify`: You can choose to have the bot notify the unmuted user via DM if you wish - this may not work if the user has DM's disabled
* `no-infraction`: Set this to true if you DON'T want to record an infraction - this is optional and if left blank, an infraction will be recorded

## Logs

* `UNMUTE`: <TODO: describe>

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)