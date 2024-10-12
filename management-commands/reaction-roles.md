# reaction-roles

This command allows you to set up reaction roles in your server. Reaction roles allow users to assign/remove roles to/from themselves by reacting to specific messages that server admins set up. There are several customization options to optimize your needs.

{% hint style="warning" %}
This is only the technical documentation of the command and not intended to be a tutorial on how to set up reaction roles. For a tutorial on how to set them up, refer to the respective [guide](../get-started/setting-up-reaction-roles.md).
{% endhint %}

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Manage Server

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](../get-started/permission-tutorial.md)

## set

This command allows you to pair a role with an emoji in a group, if the group is not set up, it will be created. You can use the same command to unpair the role from the emoji. Also, you can pair multiple roles to the same emoji, and they will be given to the user at the same time.

```
/reaction-roles set <group> <emoji> <role>
```

* `group`: The name of the group to add the pair to
* `emoji`: The emoji to be used
* `role`: The role to be assigned

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## list

This command allows you to view all the groups of reaction roles that have been set up.

```
/reaction-roles list
```

_This subcommand does not have any options._

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## info

This command allows you to view information about a group of reaction roles. It will list all options that can be set via the [`config reaction-roles`](config.md#reaction-roles) command.

```
/reaction-roles info <group>
```

* `group`: The name of the group to view information about

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## delete

This command allows you to delete a group of reaction roles.

```
/reaction-roles delete <group>
```

* `group`: The name of the group to be deleted

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## autorepair

This command automatically "repairs" errors in a group. With "repair" is meant that it will remove the IDs of roles that do not exist anymore from the pairings.

{% hint style="danger" %}
The `disconnect-messages` option is a dangerous option to use and only should be used if you know what you are doing. It is a disruptive operation and will make reaction roles on messages to which this group was applied non-functional. They need to be reapplied appropriately afterwards to work again.\
If you only want to remove a group from a message, right-click the message and select "Remove reaction roles" instead.
{% endhint %}

```
/reaction-roles autorepair <group> [disconnect-messages]
```

* `group`: The name of the group to be repaired
* `disconnect-messages`: Removes the group form all messages applied to (True/False)

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## Logs

_This command does not trigger any log events._

For more information on setting up those logs, refer to the [log setup tutorial](../#logging)
