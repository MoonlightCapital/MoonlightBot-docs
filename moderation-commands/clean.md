# clean

This command deletes a large amount of messages from a channel. Determine which messages are deleted using criteria. Criteria are options that distinguish messages such as those that contain a specific phrase. Up to 100 messages can be deleted in a single execution of the command, and only those sent within the last 14 days.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* View Channel
* Send Messages
* Manage Messages
* Read Message History

By default, a user is required to have the following permissions to use this command:

* Manage Messages

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## Syntax

```text
/clean [amount] [user] [starts-with] [ends-with] [contains] [bots] [system] [preserve-pins] [no-trace]
```

### Options

* `amount`: The amount of messages you want to clean (The default/maximum amount is 100)
* `user`: The user you want to do delete the messages of
* `starts-with`: Delete messages that start with this value
* `ends-with`: Delete messages that end with this value
* `contains`: Delete messages that contain this value
* `bots`: Whether or not to delete messages sent by bots
* `system`: Whether or not to delete system messages. System messages are messages sent by Discord, such as join or pin messages
* `preserve-pins`: If true, pinned messages will not be deleted
* `no-trace`: If true, the confirmation message will only be visible to you

## Logs

* `CHANNEL_CLEAN`: MoonlightBot will send a message with two things: an HTML file that contains the history of the deleted messages and an embed detailing where messages were cleaned, how many were cleaned, who cleaned them, and the filters applied

![An example of logs sent by the bot after a clean command execution](/.gitbook/assets/CleanLogs.png "Clean Logs")

{% hint style="info" %}
To open an HTML file, download it and open the file explorer. Double-click the file, and your computer will open a new tab in your browser to display a visualization of the messages deleted
{% endhint %}

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)
