# create-muterole

This command sets up a role to be used as the mute role for the server. It will edit the permissions of all channels to
deny the role from sending messages.

It will edit the following permissions form channels and set them to `false` for the role:

* Send Messages
* Send Messages In Threads
* Create Public Threads
* Create Private Threads
* Add Reactions
* Use Application Commands
* Speak

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Channels
* Manage Roles

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