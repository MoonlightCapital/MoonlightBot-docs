# Clean

### **Description**

This command is used to delete multiple messages from the channel it's used in. Additional options can be provided to delete only messages meeting certain characteristics.

### Required arguments

* `amount` - The amount of messages to delete. If not provided, the default is 100

### Optional arguments

* `data` - Data to supply for the filter

### Flags

* `--preserve-pins` - This flag is used to not purge pinned messages
* `--no-trace` - Putting this flag deletes the command message, plus the bot will not reply if the execution is successful

### **Options**

| Option name | Description                                                                                    | Data wanted                                      |
| ----------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| all         | Cleans all messages                                                                            | None                                             |
| user        | Cleans messages sent by a specific user                                                        | The user you want to clean the messages of       |
| matching    | Cleans all messages matching a specific regex                                                  | The regex you want the messages to match with    |
| notmatching | Opposite of matching                                                                           | The regex you want the messages to match without |
| bots        | Cleans messages sent by bots                                                                   | None                                             |
| system      | Cleans system messages (like boost notifications, "User pinned a message to this channel" etc) | None                                             |
| startswith  | Cleans messages that start with a specific content                                             | The content the messages have to start with      |
| endswith    | Cleans messages that end with a specific content                                               | The content the messages have to end with        |

### Usage

```
/clean (all|user|matching|notmatching|bots|system|startswith|endswith) [...data] <amount>
```

### Required permission

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Manage Messages** permissions in order to be able to execute this command.
