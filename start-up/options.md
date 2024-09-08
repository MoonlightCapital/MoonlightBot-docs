# Options

Options follow the name of the command and are used to give options to run the command itself. Separate each option with a space.

![Example of a command executed successfully with all the required option.](<../.gitbook/assets/slashrequiredoptions.png>)

## Required options

Required options need to be input for the command to work correctly. You will not be able to send the command otherwise.

In this guide, required options are marked as `<option>` with the angle brackets. It is important to **not put** the angle brackets in the actual command, as they are used as a placeholder to indicate that an option is required.

## Optional options

Optional options are not necessary for a command to work, but they may be used to provide additional information or add extra details to a command. In this guide, they are marked as `[option]`, with the square bracket not needed.

![The reason for the warning is optional.](<../.gitbook/assets/slashoptionaloptions.png>)

## Type of options

### Durations

Durations are a combination of numbers and letters representing units of a measure of time: for example, 4w5h means 4 weeks and 5 hours.
Below, you can see a table with all supported abbreviations.

| Duration                   | Supported Abbrevations          |
| -------------------------- | ------------------------------- |
| Week (7 days)              | w - week - weeks                |
| Day (24 hours)             | d - day - days                  |
| Hour (60 minutes)          | h - hour - hours                |
| Minute (60 seconds)        | m - minute - minutes            |
| Second (1000 milliseconds) | s - second - seconds            |
| Millisecond                | ms - millisecond - milliseconds |

{% hint style="warning" %}
If no unit is specified, the bot will default to millisecond
{% endhint %}

![A duration options.](<../.gitbook/assets/slashtypeofoptions.png>)

![Another example of duration. As you can see, you can extend or reduce the length to a temporary role by adding or substracting time to it.](<../.gitbook/assets/slashtypeofoptions2.png>)

### Entity IDs

Discord uses IDs, also called ["snowflakes"](https://discord.com/developers/docs/reference#snowflakes), internally to refer to users, roles, and messages, among other things. These can be used in commands as options in place of usernames, roles, and channels. For example, if you wanted to assign or remove a role with the ID `484794065825824778` from a user with the ID `314110696071888896`:

```
/role user:314110696071888896 role:484794065825824778
```

For more information on how to obtain these IDs, see the [Developer Mode](../advanced/developer-mode.md) page.