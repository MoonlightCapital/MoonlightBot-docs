# infractions

Infractions are records of moderation actions such as mutes or warnings. This tool has various subcommands to assist moderators keep track of bad conduct and make informed decisions.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

_No specific permissions required_

By default, a user is required to have the following permissions to use this command:

* Moderate Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](../get-started/permission-tutorial.md)

## summary

Shows the three most recent infractions of a user, along with counts of each different infraction type. If a tempban/mute is active, it will show that as well

```
/infractions summary <user>
```

* `user`: The user you want to see the infractions summary of

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## detailed

Shows the type of infraction, the user the command targeted, who executed the infraction, the reason for the infraction, and the date it was executed

```
/infractions detailed <id>
```

* `id`: The ID of the infraction you want to view

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## reason

Changes the reason of the infraction. If the `reason` option is left blank, it will simply display the current one. You can alternatively use `%%%` to automatically copy the old content so you don't have to type it again

```
/infractions reason <id> [reason]
```

* `id`: The ID of the infraction you want to edit
* `reason`: What you want to change the reason to

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## search

Shows a list of infractions that fit all the specified criteria, such as the moderator who executed them

```
/infractions search [target] [moderator] [type] [before] [after]
```

* `target`: The user you want to see the infractions of
* `moderator`: The infractions executed by a specific moderator
* `type`: The type of the infractions you want to view
* `before`: View infractions executed before this duration
* `after`: View infractions after this duration

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## delete

Deletes an infraction

{% hint style="danger" %}
This cannot be undone! Be absolutely sure that you want to delete the infraction before running this command.
{% endhint %}

```
/infractions delete <id> [reason]
```

* `id`: The ID of the infraction you want to delete
* `reason`: The reason you are deleting the infraction

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## Logs

* `REASON_UPDATE`: Shows the user the infraction affects, the moderator who executed it, and the updated reason
* `INFRACTION_DELETE`: Same as above, with the reason being why the infraction was deleted

For more information on setting up those logs, refer to the [log setup tutorial](../#logging)
