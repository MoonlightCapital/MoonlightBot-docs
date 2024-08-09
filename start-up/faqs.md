# Frequently Asked Questions

## MoonlightBot is not responding to my commands

Try doing the following things:

* Make sure it's online. If it shows as offline, please join the support server and let the Staff know.
* Try checking channel permission. If needed, you can add to the bot channel-specific permissions such as Read Messages, Send Messages, Embed Links and View Message History.

If the problem persists, please [contact support](https://discord.gg/hNQWVVC).

## MoonlightBot is sending me offensive direct messages. What can I do?

This is happening because someone is abusing the infraction system to harass you. Our Staff does not tolerate this use at all. Please report it at the [support server](https://discord.gg/hNQWVVC).


## Can I use bots to trigger MoonlightBot commands?

No, other bots and webhooks cannot trigger MoonlightBot, due to safety reasons. Using [selfbots](https://support.discord.com/hc/en-us/articles/115002192352-Automated-User-Accounts-Self-Bots) is a violation of Discord's Terms of Service.

## What language is MoonlightBot written in?

It's written in Node.js using the Discord.js library to interface with Discord's API.

## Who is the owner of MoonlightBot?

MoonlightBot is owned by MoonlightCapital. With tag `moonlightcapital` and ID `256460316660072448` on Discord.


## How does the temprole feature work?

There are different types of temprole offered:

* The [Temprole](../role-management-commands/temprole.md) command, which allows a privileged user (usually a moderator) to give someone a role, and make MoonlightBot remove the role after a set duration.
* Self-assignable temproles, that allow users to assign themselves a role through the [Selfrole](../role-management-commands/selfrole.md) command. See how to set this up at [Configuring roles](../management-commands/config.md#roles-self-assignable).
* Join-assigned temproles. Take a look at [Configuring roles](../management-commands/config.md#roles-join-assignable).
* Reaction roles have an option to make their roles temporary. To see how to set up reaction roles, see [Setting up reaction roles](setting-up-reaction-roles.md).

## How do I cancel a temprole?

You can cancel a temprole to force an immediate expiration by using the `temprole` command with a duration that would make it expire in the past. Say you want to cancel a temprole that has 3 days left:

```
/temprole <user> <role> -3d
```

Any value lower than `-3d` will work as well.

## How does the temprole sustain mechanic work?

In order to encourage good support practices, a system has been introduced for sustaining temproles to ensure they remain functional.

When operating a temporary or pause role, you must satisfy at least one of the following conditions:

1. **Maximum Duration Consistency**: The maximum duration allowed for the role setter (adder) at the time of the role's expiration must be equal to or greater than the maximum duration allowed at the time the role was added.

2. **Vote Requirement**: The number of votes received by the adder must be equal to or greater than the number of days the temporary role lasts. For example, a 30-day temprole requires at least 30 votes to be sustained.

3. **Premium Instance**: The server must be on a premium instance (Advance+ tier).

4. **Exemption Request**: The adder must have requested and received an exemption from bot staff

If none of these conditions are met, the temprole will be removed from the target user.

If someone is threatening to stop sustaining temproles to damage your server, [contact support](https://discord.gg/hNQWVVC). We will investigate the matter and render any threat ineffective.

## Will my temproles be erased if bot downtime happens?

No! There's absolutely no reason to worry about potential data losses as MoonlightBot is designed to be resilient. We are committed to 99% uptime, but if it ever happens that the bot goes down, your temproles will be removed as nothing happened.

## How can I get access to new features early?

Take a look at the [Beta](../support/beta.md) version of MoonlightBot.

## I found a bug. How do I report it?

Report it in the support server. Make sure to include enough information for your bug to be reproducible.

If your bug can be used to compromise the bot or end user's security, **message the bot owner privately about it**, and please do not disclose it anywhere.


