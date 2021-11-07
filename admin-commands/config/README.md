# Config

The config command is used to edit server settings. Almost every setting available can be edited with this command. Please note due to the complexity of this command, this page is structured differently than the other pages of this documentation.

### Brief introduction

* Start a configuration process with `m:config`
* Follow instructions on screen by the bot messages
* Click on buttons to select options
* You can type `cancel` at any time to cancel the configuration process
* If you don't reply within 2 minutes, the process will be cancelled
* Read the tables below or in the sub pages to see what each option means
* Option names are case-sensitive

### One-line config

Tired of the guided procedure? You can supply the input as arguments of the command so you can make the edits without the need of sending multiple messages. This method does not support arguments with spaces.

### Data types

There are four main data types:

* **Number:** Any number without decimals
* **String:** Any piece of text
* **Boolean:** A value that can be either `true` or `false`. Think of it like "yes" and "no" or "on" and "off"
* **Duration:** Any duration in time (that is internally converted into a number)
* **List:** A series of values of the above types

### Main options

| Name                      | Description                                                                         | Type                                | Default | Notes                                                                                                                 |
| ------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------- | ------- | --------------------------------------------------------------------------------------------------------------------- |
| Commands                  | Contains the options for commands in the server                                     | List of commands                    | Empty   | See [configuring commands](configuring-commands.md)                                                                   |
| Channels                  | Contains the options for the channels in the server                                 | List of channels                    | Empty   | See [configuring channels](configuring-channels.md)                                                                   |
| Roles                     | Contains the options for the roles in the server                                    | List of roles                       | Empty   | See [configuring roles](configuring-roles.md)                                                                         |
| ReactionRoles             | Contains the options for reaction roles in the server                               | List of reaction role groups        | Empty   | See [configuring reaction roles](configuring-reaction-roles.md)                                                       |
| Prefix                    | The custom prefix of the bot in the server                                          | String                              | Not set | This will not replace the bot's default prefix or mention. Can be long up to 10 characters and cannot contain spaces. |
| Muterole                  | The role used to mute users                                                         | String (a role name, ID or mention) | Not set |                                                                                                                       |
| ShowPermissionError       | If this is `false`, the bot will not reply to errors in terms of access permissions | Boolean                             | true    |                                                                                                                       |
| MuteEvasionBan            | Bans an user if they send a message with the mute role on                           | Boolean                             | false   | Can be disabled in specific channels with the `IgnoreMuteEvasionBan` option                                           |
| TemproleExpirationActions | Actions to perform when a temporary role expires                                    | Category of options                 |         |                                                                                                                       |

### Aliases

`set`
