# Reaction-roles

## Description

This command is used to manage all settings for reaction roles.


This page covers in-depth technical details about the command. For a start-up guide on reaction roles, see [Setting up reaction roles](../start-up/setting-up-reaction-roles.md).


### Subcommands

#### Config

This command creates a new group, given a name. A server can have a maximum of 10 groups.

The only required argument for this option is `group`, which will later be used to identify your group.

#### Set

This command adds pairs to the group (a pair being an emoji connect to a role). A group can have a maximum of 20 pairs.

The required arguments for this option are `group`, `emoji`, and `role`. `Group` is the group that you want to apply pairs to and `emoji` is the emoji you want the user to react with to toggle the `role`.


#### Apply

Applies the selected group to a given message. Instructions on how to do this are given [here](../start-up/setting-up-reaction-roles.md#applying-your-group-to-messages).

More than one group can be applied to a same message at any time. The same group can be applied to a maximum of 5 different messages.

#### Unapply

Has the opposite effect of `apply`, ergo, it will remove the group from the specified message. 

#### Delete

This deletes a given group(`group` is the required argument.).

This action is irreversible. You will be allowed to create a new group with the same name as a deleted group.

#### Info

Takes a group name as required argument, and shows some information, such as the emoji/role couples and settings for the group.

You can edit group options with the `config` command

#### List

This option lists all the available groups by name and amount of roles set. No arguments required.

#### Autorepair

This removes any deleted emoji/role from the group(the only required argument), cleaning things up. It will not search for deleted messages.

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

This command's level is 100 by default.\
The bot needs **Read Messages, Send Messages, Embed Links, Add Reactions** permissions in order to be able to execute this command. For some options, the bot may need **Manage Messages** and **Add Reactions** in specific channels.
