# create-muterole

This command sets up a role to be used as the mute role for the server. It will edit the permissions of all channels to deny the role from sending messages.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Channels
* Manage Roles

For the successful setup of the mute role, MoonlightBot requires permission to **Manage Permissions** in channels, as well as the following permissions enabled, which will be denied to the mute role:

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

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## Syntax

```text
/create-muterole [role]
```

### Options

* `role`: The role to be used as the mute role. If not provided, a new role will be created

## Logs

*This command does not trigger any log events.*

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)

## Troubleshooting

To troubleshoot why a muted member was able to send a message in an unintended channel despite having the role set up, check the following:

* Does the muted role have the `Send messages` permission?
  * Check in Server Settings > Roles > [Your Mute Role] > Permissions; If so, disable it.
* Does the muted role have a category-specific override with the `Send messages` permission?
  * Check by Right Clicking on the Channel's Category > Edit Category > Permissions; If so, remove the role override or disable the permission.
* Does the muted role have a channel-specific override, or is the channel not synced to the category?
  * Check by Right Clicking on the Channel > Edit Channel > Permissions; If so, sync the channel to the category, remove the override or disable the permission.