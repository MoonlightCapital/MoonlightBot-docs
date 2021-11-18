# FAQs

## MoonlightBot is not responding to my commands

Try doing the following things:

* [ ] Make sure it's online. If it shows as offline, please join the support server and let the Staff know.
* [ ] Try checking channel permission. If needed, you can add to the bot channel-specific permissions such as Read Messages, Send Messages, Embed Links and View Message History.
* [ ] It can happen that the server admins disabled the `showPermissionError` option and you do not have permissions to use the command you're trying to use. Contact the server admins.

If the problem persists, please ask in the [support server](https://discord.gg/hNQWVVC).

## Can I use bots to trigger MoonlightBot commands?

For security reasons, MoonlightBot will ignore messages sent by bots and webhooks.

## How does the temprole feature work?

There are different types of temprole offered:

* The [Temprole](../staff-commands/temprole.md) command, which allows a privileged user (usually a moderator) to give someone a role, and make MoonlightBot remove the role after a set duration.
* Self-assignable temproles, that allow users to assign themselves a role through the [Selfrole](../public-commands/selfrole.md) command. See how to set this up at [Configuring roles](../admin-commands/config/configuring-roles.md).
* Join-assigned temproles. Take a look at [Configuring roles](../admin-commands/config/configuring-roles.md).
* Reaction roles have an option to make their roles temporary. To see how to set up reaction roles, see [Setting up reaction roles](setting-up-reaction-roles.md).

## How do I cancel a temprole?

You can cancel a temprole to force an immediate expiration by using the `temprole` command with a duration that would make it expire in the past. Say you want to cancel a temprole that has 3 days left of time:

```
m:temprole <user> <role> -3d
/temprole <user> <role> -3d
```

Any value lower than `-3d` will work.

## MoonlightBot is sending me offensive messages. What can I do?

This is happening because someone is abusing the infraction system to harass you. Our Staff does not tolerate this use at all. Please report it at the [support server](https://discord.gg/hNQWVVC).

## What language is MoonlightBot written in?

It's written in Node.js using the Discord.js library to interface with Discord's API.

## How can I get access to new features early?

Take a look at the [Beta](../versions-of-the-bot/beta.md) and [Test](../versions-of-the-bot/test.md) versions of MoonlightBot.

## I found a bug. How do I report it?

Report it in the support server. Make sure to include enough information for your bug to be reproducible.

If your bug can be used to compromise the bot or end user's security, **message the bot owner privately about it**, and please do not disclose it anywhere.

## Who is the owner of MoonlightBot?

MoonlightBot is owned by MoonlightCapital. With tag `MoonlightCapital#0001` and ID `256460316660072448` on Discord.

