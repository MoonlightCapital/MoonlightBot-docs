# Reaction-roles

## Description

This command is used to manage all settings for reaction roles.

{% hint style="info" %}

This page covers in-depth technical details about the command. For a start-up guide on reaction roles, see [Setting up reaction roles](../start-up/setting-up-reaction-roles.md).
{% endhint %}

### Subcommands

#### Set

This command adds pairs to the group (a pair being an emoji connect to a role). A group can have a maximum of 20 pairs.

![](<../.gitbook/assets/ReactionRoleSetup2.png>)

The required arguments for this option are `group`, `emoji`, and `role`. `Group` is the group that you want to apply pairs to and `emoji` is the emoji you want the user to react with to toggle the `role`.

#### Delete

This deletes a given group (`group` is the required argument.).

{% hint style="danger" %}
This action is irreversible. You will be allowed to create a new group with the same name as a deleted group.
{% endhint %}

#### Info

Takes a group name as required argument, and shows some information, such as the emoji/role couples and settings for the group.

{% hint style="info" %}
You can edit group options with the `config` command
{% endhint %}

#### List

This option lists all the available groups by name and amount of roles set. No arguments required.

#### Autorepair

This removes any deleted emoji/role from the group (the only required argument), cleaning things up. It will not search for deleted messages.

### Usage

```
/config reaction-roles <group>

/reaction-roles set <group> <emoji> <role>

/reaction-roles delete <group>

/reaction-roles info <group>

/reaction-roles list 

/reaction-roles autorepair <group>
```

### Required permissions

The bot needs **Send Messages, Embed Links, Manage Roles, and Add Reactions** permissions in order to be able to execute this command. For some options, the bot may need **Manage Messages, ViewChannel, and Add Reactions** in specific channels.

To utilize these commands, the **Manage Server** permission is required.