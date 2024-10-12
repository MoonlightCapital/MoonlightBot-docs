# userconfig

This command lets you configure some personal settings regarding the notifications you get from MoonlightBot, and other preferences regarding your experience with MoonlightBot.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

_No specific permissions required_

By default, a user is required to have the following permissions to use this command:

_No specific permissions required_

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](../get-started/permission-tutorial.md)

## settings

This command lets you configure some personal settings regarding the types of notifications you get from MoonlightBot, and other preferences to customize your experience with the bot.

```
/userconfig settings [reaction-role-notifications] [vote-reminders]
```

* `reaction-role-notifications`: This option allows you to enable or disable notifications for adding or removing [a reaction role.](../get-started/setting-up-reaction-roles.md) By default, it’s set to true, meaning the server’s settings control whether you receive notifications. Setting it to false overrides the server settings and prevents notifications
* `vote-reminders`: This option will remind you daily to [vote for MoonlightBot.](../MoonlightBot-docs/support/upvote-moonlightbot.md) By voting for the first time, it will remind you to vote again and this option can be used to turn reminders off
* `locale`: This option lets you choose what language you want your interactions with MoonlightBot to be in. If you'd rather have the bot automatically determine the locale from the language you have the Discord app set to, you can set it to "Auto" and it will automatically determine the locale (this is done by default unless you first explicitly change this value)

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

_No specific permissions required_

## Logs

_This command does not trigger any log events._

For more information on setting up those logs, refer to the [log setup tutorial](../#logging)
