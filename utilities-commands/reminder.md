# reminder

The `reminder` command allows you to use the bot to manage reminder messages that will be delivered to Direct Messages. You can have up to 10 reminders active at once, which increases to 20 with [MoonlightBot Premium](/support/premium.md).

Each reminder is automatically assigned an ID to perform operations on it. All options that require an ID will show a brief list of your reminders in the autocomplete menu along with the beginning of the reminder content.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

*No specific permissions required*

By default, a user is required to have the following permissions to use this command:

*No specific permissions required*

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## add

The `reminder add` subcommand allows you to write a reminder to yourself sometime in the future. You can write anything and set any time.

```text
/reminder add <reminder> <time> [recurring]
```

- `reminder`: The reminder to be set
- `time`: The time in the future when you will receive the reminder. For more information on the duration format, refer to the [options page](/start-up/options.md#durations)
- `recurring`: Whether the reminder will be recurring or not (True/False); uses `time` as the interval. For example, if you set the time as `3 days`, the bot will send it to you every three days until you delete it manually.

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## list

The `reminder list` command lists your currently active reminders.

```text
/reminder list
```

*This subcommand does not have any options.*

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## delete

The `reminder delete` subcommand deletes a pending reminder.

{% hint style="danger" %}
This cannot be undone! Be absolutely sure that you want to delete the reminder before running this command.
{% endhint %}

```text
/reminder delete <id>
```

- `id`: The ID assigned to your reminder; the bot will ask you to press a button to confirm the deletion.

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## edit

The `reminder edit` subcommand allows you to edit a pending reminder. It asks you to change the content of the reminder and/or the time you receive it.

```text
/reminder edit <id> [reminder] [time]
```

- `id`: The ID of your reminder
- `reminder`: The new content of the reminder; you can insert `%%%` to copy over the old content so you don't have to type it again.
- `time`: How much time you would like to add or subtract to the reminder. For more information on the duration format, refer to the [options page](/start-up/options.md#durations)

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## clear

The `reminder clear` subcommand deletes all your pending reminders; the bot will ask you to press a button to confirm the deletion.

{% hint style="danger" %}
The deletion is irreversible, and you cannot restore the deleted reminders.
{% endhint %}

```text
/reminder clear
```

*This subcommand does not have any options.*

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## Logs

*This command does not trigger any log events.*

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)
