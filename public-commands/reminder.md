# Reminder

## Description

This command is used to send reminders to you at a certain time in DMs.

## Options

### Add

Creates a new reminder. It will then be delivered once the duration expires.

#### Arguments

* `duration` - The time after the reminder is sent **(required)**
* `content` - The content of the reminder message. All markdown supported **(required)**

#### Usage

```
/reminder add <duration> <content>
```

#### Flags

* `recurring` - If set, the reminder will be sent every `<duration>` instead of only once. You will have to delete it manually to stop.

### Edit

Edits the content of an existing reminder.

#### Arguments

* `id` - The unique ID of the reminder
* `content` - The new content of the reminder. Putting the special tag `%OLD%` will be replaced with the previous content of the reminder

#### Usage

```
/reminder edit <id> <content>
```

### Delete

Deletes a reminder, meaning it will not be delivered anymore. You will be asked to confirm your choice through a reaction menu.

#### Arguments

* `id` - The unique ID of the reminder

#### Usage

```
/reminder delete <id>
```

### List

Sends a list of all your reminders, containing ID, expiration date and content. If this list is longer than 2048 characters, it will be sent as a file instead of as an embed.

#### Usage

```
/reminder list
```

### Clear

Deletes all your reminders at once. You will be asked to confirm your choice through a reaction menu.

#### Usage

```
/reminder clear
```

## Required permissions

This command is level 0 by default\
The bot needs **Read Messages, Send Messages, Embed Links, Attach Files **permissions in order to be able to execute this command.
