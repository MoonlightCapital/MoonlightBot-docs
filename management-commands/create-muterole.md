# create-muterole

This command sets up a role to be used as the mute role for the server. It will edit the permissions of all channels to
deny the role from sending messages.


## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Channels
* Manage Roles

For the successful setup of the mute role, MoonlightBot requires permission to **Manage Permissions** in channels, as
well as the following permissions enabled, which will be denied to the mute role:

* Send Messages
* Send Messages In Threads
* Create Public Threads
* Create Private Threads
* Add Reactions
* Use Application Commands
* Speak

Channels where these conditions are not met will be skipped in the permission override setup procedure.

By default, a user is required to have the following permissions to use this command:

* Manage Server

For more information on editing permission requirements for specific users/roles, refer to
the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/create-muterole [role]
```

### Options

* `role`: The role to be used as the mute role. If not provided, a new role will be created

## Logs

*This command does not trigger any log events.*

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)