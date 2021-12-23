# Clean

### **Description**

This command is used to delete multiple messages from the channel it's used in. Arguments serve as filter to fine-tune which criteria the messages must meet to be deleted. If multiple filters are provided, messages will be deleted if they meet all the requirements.

### Required arguments

None

### Optional arguments

* `user` - Deletes messages sent by this user
* `startswith` - Deletes messages with the content starting with this option
* `endswith` - Deletes messages with the content ending with this option
* `contains` - Deletes messages containing this option
* `bots` - Deletes messages sent by bots
* `system` - Deletes system messages
* `amount` - The amount of messages to delete (defaults to 100)
* `preserve-pins` - This flag is used to not purge pinned messages
* `no-trace` - Makes the response ephemeral, effectively leaving no trace in the cleaned channel


### Usage

```
/clean [user] [startswith] [endswith] [contains] [bots] [system] [amount] [no-trace] [preserve-pins]
```

### Required permission

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Manage Messages** permissions in order to be able to execute this command.
