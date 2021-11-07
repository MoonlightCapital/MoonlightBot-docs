# Configuring channels

To start configuring a channel, enter its name, mention or ID.

{% hint style="info" %}
To edit the channel, you must have permission to view it. Only text channels can have options.
{% endhint %}

| Name                 | Description                                                                  | Type            | Default | Notes                                                                               |
| -------------------- | ---------------------------------------------------------------------------- | --------------- | ------- | ----------------------------------------------------------------------------------- |
| MinLevel             | The minimum level required to use commands in this channel                   | Number          | 0       | May be unused or behavior not implemented                                           |
| ShowPermissionError  | Like the global setting with the same name, but only applied to this channel | Boolean         | true    |                                                                                     |
| Logs                 | Logs to send in this channel                                                 | List of strings | Empty   | See the [list of log names](../../advanced/list-of-log-names.md) for allowed values |
| DisabledCommands     | List of commands to be disabled in this channel                              | List of strings | Empty   | Any command name or category is allowed. Putting `*` will disable every command     |
| IgnoreMuteEvasionBan | The global `MuteEvasionBan` setting will not have effect in this channel     | Boolean         | False   |                                                                                     |
