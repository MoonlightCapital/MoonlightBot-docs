# infractions

Infractions are records of moderation actions such as mutes or warnings. This tool has various subcommands to assist moderators keep track of bad conduct and make informed decisions.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

*No specific permissions required*

By default, a user is required to have the following permissions to use this command:

* Moderate Members

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## summary

Shows the three most recent infractions of a user, along with counts of each different infraction type. If a tempban/mute is active, it will show that as well

```text
/infractions summary <user>
```

* `user`: The user you want to see the infractions summary of

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## detailed

Shows the type of infraction, the user the command targeted, who executed the infraction, the reason for the infraction, and the date it was executed.

```text
/infractions detailed <id>
```

* `id`: The ID of the infraction you want to view

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## reason

Changes the reason of the infraction. If the `reason` option is left blank, it will simply display the current one.

```text
/infractions reason <id> [reason]
```

* `id`: The ID of the infraction you want to edit
* `reason`: What you want to change the reason to. Use `%%%` to add on to the previous content. If this option is not set, the command will return the existing reason

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## search

Shows a list of infractions that fit all the specified criteria, such as the moderator who executed them.

```text
/infractions search [target] [moderator] [type] [before] [after]
```

* `target`: The user you want to see the infractions of
* `moderator`: The infractions executed by a specific moderator
* `type`: The type of the infractions you want to view
* `before`: View infractions executed before this duration
* `after`: View infractions after this duration

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## delete

Deletes an infraction.

{% hint style="danger" %}
This cannot be undone! Be absolutely sure that you want to delete the infraction before running this command.
{% endhint %}

```text
/infractions delete <id> [reason]
```

* `id`: The ID of the infraction you want to delete
* `reason`: The reason you are deleting the infraction

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## Logs

* `REASON_UPDATE`: Shows the user the infraction affects, the moderator who executed it, and the updated reason
* `INFRACTION_DELETE`: Same as above, with the reason being why the infraction was deleted

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)
