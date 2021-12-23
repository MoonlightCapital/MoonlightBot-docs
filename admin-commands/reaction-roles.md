# Reaction-roles

## Description

This command is used to manage all settings for reaction roles.

{% hint style="info" %}
This page covers in-depth technical details about the command. For a start-up guide on reaction roles, see [Setting up reaction roles](../start-up/setting-up-reaction-roles.md).
{% endhint %}

### Subcommands

#### Create

This command creates a new group, given a name. A server can have a maximum of 10 groups.

The only required argument for this option is `name`, which will later be used to identify your group.

#### Setroles

This command starts a guided prompt to assign emojis and roles to a group. First, you will be asked to send a message with the role (can be a name, mention or ID), then, you'll be asked to add a reaction to confirm. You can end the guided configuration at any time.

{% hint style="warning" %}
Using this command on a group that has been previously set will delete all existing emojis and roles and make you start again. If you don't want to overwrite any previously set option, add the `no-overwrite` argument.
{% endhint %}

#### Apply

Applies the selected group to a given message. The arguments are `group`, which is the name of the group you want to assign and `message`, corresponding to a message ID or link to the message you want the group to be applied to.

{% hint style="info" %}
More than one group can be applied to a same message at any time. The same group can be applied to a maximum of 5 different messages.
{% endhint %}

#### Unapply

Has the opposite effect of `apply`, ergo, it will remove the group from the specified message. Arguments are the same as the apply option.

#### Delete-group

This deletes a given group as required argument.

{% hint style="danger" %}
This action is irreversible. You will be allowed to create a new group with the same name as a deleted group.
{% endhint %}

#### Group-info

Takes a group name as required argument, and shows some informations, such as the emoji/role couples and settings for the group.

{% hint style="info" %}
You can edit group options with the `config` command
{% endhint %}

#### Listgroups

This option lists all the available groups by name and n° of roles set. No arguments needed.

#### Autorepair

This removes any deleted emoji/role from the group passed as argument, cleaning things up. It will not search for deleted messages.

### Usage

```
/reaction-roles create <name>

/reaction-roles setroles <group> [no-overwrite]

/reaction-roles apply <group> <message>

/reaction-roles unapply <group> <message>

/reaction-roles delete-group <group>

/reaction-roles group-info <group>

/reaction-roles list-groups 

/reaction-roles autorepair <group>
```

### Required permissions

This command's level is 100 by default.\
The bot needs **Read Messages, Send Messages, Embed Links, Add Reactions** permissions in order to be able to execute this command. For some options, the bot may need **Manage Messages** and **Add Reactions** in specific channels.
