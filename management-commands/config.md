# config

The `config` command allows you to configure all settings for the server, such as roles, channels, reaction roles,
and other customizable behavior of MoonlightBot. To get the current configuration of a setting, just use the
corresponding sub command without any optional arguments.

{% hint style="info" %}
If an argument provides you with the option `Open Editor` like the argument `custom-notification-text` of
the [`roles on-expire`](../management-commands/config.md#on-expire) command, it means that a modal textbox will open for
you to input your desired text.
<br>
All default values are either `0`, `false` or empty for their respective arguments, unless stated otherwise.
{% endhint %}

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

*No specific permissions required*

By default, a user is required to have the following permissions to use this command:

* Manage Server

For more information on editing permission requirements for specific users/roles, refer to
the [permissions tutorial](<linkToPermissionsTutorial>)

## edit

This command allows you to set a role to be persistent or not. A persistent role means that when the user rejoins the
server, they will automatically get the role back.

{% hint style="info" %}
Note that this command may be expanded in the future to allow for more role settings.
{% endhint %}

```text
/config roles edit <role> [persistent]
```

* `role`: The role to be edited
* `persistent`: Whether the role should be persistent or not (True/False)

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## on-expire

This command allows you to set up a custom notification for when a temporary role expires.

```text
/config roles on-expire <role> [notify] [custom-notification-text]
```

* `role`: The role for which the notification should be set
* `notify`: Whether to notify the user when the role expires (True/False)
* `custom-notification-text`: This opens a modal textbox to set a custom notification message

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## self-assignable

This command allows you to set up a role to be self-assignable by users. This allows them to assign the role to
themselves via the [`selfrole`](../role-management-commands/selfrole.md) command without needing a moderator to do it
for them, and they can remove it themselves as well. It works on a vice versa basis.

```text
/config roles self-assignable <role> [enabled] [duration] [max-times]
```

* `role`: The role to be set as self-assignable
* `enabled`: Whether the role should be self-assignable or not (True/False)
* `duration`: The duration for which the role should be assigned
* `max-times`: The maximum number of times the role can be assigned

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## join-assignable

This command allows you to set up a role to be assigned to a user when they join the server. This role can be set up to
be a temporary role, and it can be set up to be assigned a maximum number of times.

```text
/config roles join-assignable <role> [enabled] [duration] [max-times]
```

* `role`: The role to be assigned when a user joins the server
* `enabled`: Whether the role should be assigned when a user joins the server (True/False)
* `duration`: The duration for which the role should be assigned
* `max-times`: The maximum number of times the role can be assigned

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## detect-assignment

This command allows you to set up a detection system for a role that is assigned to a user by another bot or a
moderator. It will change the role to a temporary role and remove it after a certain duration.

```text
/config roles detect-assignment <role> [enabled] [duration] [include-bots]
```

* `role`: The role to be detected
* `enabled`: Whether the detection system should be enabled or not (True/False)
* `duration`: The duration for which the role should be assigned
* `include-bots`: Whether to include bots in the detection system (True/False)

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*View Audit Log*

## channels

This command allows you to set up in which channels MoonlightBot logs, ignores mute evasion bans, and sends ephemeral
replies.

```text
/config channels <channel> [logs] [ignore-mute-evasion-ban] [ephemeral-replies]
```

* `channel`: The channel to be configured
* `logs`: To open the editor to set up the logs. You can view the available logs under
  the [List of log names](../advanced/list-of-log-names.md)
* `ignore-mute-evasion-ban`: Whether the Bot should consider messages sent in this channel to be an evasion of a mute or
  not (True/False)
* `ephemeral-replies`: Whether the Bot should mark command replies as only viewable by the user who triggered the
  command (True/False)

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## reaction-roles

This command allows you to set up and manage groups for reaction roles. If the group does not exist, it will be created.

{% hint style="info" %}
For information on how to delete a group, refer to
the [`reaction-roles`](../management-commands/reaction-roles.md#delete) command and for information on how to set up
reaction roles, refer to the [`Setting up reaction roles`](../start-up/setting-up-reaction-roles.md) tutorial.
{% endhint %}

```text
/config reaction-roles <group> [join-only] [leave-only] [reverse] [max-roles] [dm-notification] [freeze] [duration]
```

* `group`: The group to be configured or created
* `join-only`: Prevents the user from removing their role(s)
* `leave-only`: Prevents the user from assigning the role(s)
* `reverse`: When the message is reacted on, it will remove the role instead of assigning it, and vice versa
* `max-roles`: The maximum amount of roles within the group a user can assign themselves
* `dm-notification`: When a role is assigned/removed, the bot will message the user (true by default)
* `freeze`: When true, the group will not function. This is a quick way to disable reaction roles without taking
  irreversible actions, such as deleting group/message or removing reactions from the message
* `duration`: How long the user will keep their assigned role(s)

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## settings

This command allows you to set up the settings for the server, such as the mute role, mute evasion ban, and locale.

{% hint style="info" %}
Note that you can make exceptions to the `mute-evasion-ban` via the
[`channels`](../management-commands/config.md#channels) subcommand.
{% endhint %}

```text
/config settings [mute-role] [mute-evasion-ban] [locale]
```

* `mute-role`: The role to be used as the mute role which can be created via the
  [`create-muterole`](../management-commands/create-muterole.md#create-muterole) command
* `mute-evasion-ban`: If the bot should automatically ban anyone who sends a message and has the mute role to avoid
  punishment evasion
* `locale`: The language to be used for the server

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## Logs

*This command does not trigger any log events.*

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)