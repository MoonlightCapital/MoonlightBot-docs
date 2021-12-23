# Arguments

Arguments follow the name of the command and are used to give options to run the command itself. Separe each argument with a space.

![Example of a command executed successfully with all the required arguments. Each argument is highlighted with a different color for clarity.](<../.gitbook/assets/immagine (14).png>)

## Required arguments

Required arguments need to be input for the command to work correctly. You will receive an error message or a warning otherwise.

In this guide, required arguments are marked as `<argument>` with the angle brackets. It is important to **not put** the angle brackets in the actual command, as they are used as a placeholder to indicate an argument is required.

![As you can see, the angle brackets cause the input to be different, so the command won't work.](<../.gitbook/assets/immagine (15).png>)

## Optional arguments

Optional arguments are not needed for a command to work, but they may be used to provide additional information or add extra details to a command. In this guide, they are marked as `[argument]`, with the square bracket not needed.

### Optional arguments with spaces

They are marked with `[...argument]` in this guide. They are joined together and allow spaces in there, unlike other arguments that break up on spaces.

![The reason for the warning is optional and allows spaces, as marked in green in the above image.](<../.gitbook/assets/immagine (16).png>)

## Type of arguments

### Durations

Durations are a combinations of numbers and letters rappresenting units of measure of time: for example 4w5h means 4 weeks and 5 hours. Below you can see a table with all supported abbreviations.

| Duration                   | Supported Abbrevations          |
| -------------------------- | ------------------------------- |
| Week (7 days)              | w - week - weeks                |
| Day (24 hours)             | d - day - days                  |
| Hour (60 minutes)          | h - hour - hours                |
| Minute (60 seconds)        | m - minute - minutes            |
| Second (1000 milliseconds) | s - second - seconds            |
| Millisecond                | ms - millisecond - milliseconds |

{% hint style="warning" %}
If no unit is specified the bot will default to millisecond
{% endhint %}

![Duration argument is highlighted in yellow.](<../.gitbook/assets/immagine (18).png>)

![Another example of duration.](<../.gitbook/assets/immagine (19).png>)
