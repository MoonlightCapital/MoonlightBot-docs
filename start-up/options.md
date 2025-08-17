# Options

Options are different values passed to the command to specify who it targets, what role it uses, duration, and more, separated by a space.

![Example of a command executed successfully with all required options.](</.gitbook/assets/RequiredOptions.png>)

## Required options

Required options must be provided for the command to work correctly, and you will not be able to send the command until all required options are specified. In this guide, required options are marked with angle brackets: `<option>`. **Do not** include the angle brackets in the actual command.

## Additional options

Additional options are not necessary for a command to work, but may be used to provide extra information or details to a command. In this guide, they are marked with square brackets: `[option]`. **Do not** include the square brackets in the actual command.

![The reason for a warning is optional.](</.gitbook/assets/OptionalOptions.png>)

## Types of options

### Durations

Durations are a combination of numbers and letters representing units of time; for example, `4w5h` means 4 weeks and 5 hours.
Below, you can see a table with all supported abbreviations.

| Duration                   | Supported Abbrevations          |
| -------------------------- | ------------------------------- |
| Week (7 days)              | w - week(s)                     |
| Day (24 hours)             | d - day(s)                      |
| Hour (60 minutes)          | h - hour(s)                     |
| Minute (60 seconds)        | m - minute(s)                   |
| Second (1000 milliseconds) | s - second(s)                   |
| Millisecond                | ms - millisecond(s)             |

{% hint style="warning" %}
If no unit is specified, the bot will default to milliseconds.
{% endhint %}

![An example of duration options.](</.gitbook/assets/OptionTypes1.png>)

![Another example of duration options. As shown, you can extend the length of an active temporary role by specifying the same user and role, followed by the time to be added.](</.gitbook/assets/OptionTypes2.png>)

### Entity IDs

Discord uses IDs, also called ["snowflakes"](https://discord.com/developers/docs/reference#snowflakes), to refer to users, roles, and messages, among other things. These can be used in options in place of usernames, roles, and channels. For example, if you wanted to assign or remove a role with the ID `484794065825824778` from a user with the ID `314110696071888896`:

```
/role user:314110696071888896 role:484794065825824778
```

For more information on how to obtain these IDs, see the [Developer Mode](/advanced/developer-mode.md) page.
