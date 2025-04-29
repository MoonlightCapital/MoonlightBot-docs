# Frequently Asked Questions

## Why is MoonlightBot not responding to my commands?

Try doing the following things:

* Make sure it's online. If it shows as offline, please join the support server and let the Staff know.
* Try checking channel permission. If needed, you can add to the bot channel-specific permissions such as Read Messages, Send Messages, Embed Links and View Message History.

If the problem persists, please [contact support](https://discord.gg/hNQWVVC).

## MoonlightBot is sending me offensive direct messages. What can I do?

This is happening because someone is abusing the infraction system to harass you. Our Staff does not tolerate this use at all. Please report it in the [support server](https://discord.gg/hNQWVVC).

## How does the Temporary Role feature work?

There are different types of Temporary Roles offered:

* The [`/temprole`](/role-management-commands/temprole.md) command, which allows a privileged user (usually a moderator) to give someone a role, and make MoonlightBot remove the role after a set duration
* [Self-assignable temproles](/management-commands/config.md#roles-self-assignable) that allow users to assign themselves a role through the [`/selfrole`](/role-management-commands/selfrole.md) command
* [Join-assigned temproles](/management-commands/config.md#roles-join-assignable) that assign a role automatically to a user upon joining the server
* [Reaction roles](setting-up-reaction-roles.md) have an option to make their roles temporary
* Any role assigned to a user can automatically be changed to a temporary role with the [`detect-assignment` config option](./management-commands/config.md#roles-detect-assignment)
* The [`/pause-role`](/role-management-commands/pause-role.md) command removes a role and automatically adds it back after the set duration

## How do I cancel a temporary action?

You can cancel a temporary action to force an immediate expiration by using the same command you used to enact the action, but with a duration that would make it expire in the past. Say you want to cancel a temprole that has 3 days left:

```
/temprole user:<user> role:<role> duration:-3d
```

Any value lower than `-3d` will work as well. This same principle applies to the [`/tempban`](/moderation-commands/tempban.md), [`/tempmute`](/moderation-commands/tempmute.md), [`/timeout`](/moderation-commands/timeout.md) and [`/pause-role`](/role-management-commands/pause-role.md) commands.

## How does the temprole sustain mechanic work?

In order to encourage good support practices, a system has been introduced for sustaining temproles to ensure they remain functional and fair for all servers and users.

When operating a temporary or pause role, you must satisfy at least one of the following conditions:

1. **Maximum Duration Consistency**: The [maximum duration allowed](/miscellaneous-commands/check-duration.md) for you at the time of the role's expiration must be equal to or greater than their maximum duration allowed at the time the role was added

2. **Vote Requirement**: The [number of votes](/support/upvote-moonlightbot.md) received from you must be equal to or greater than half the number of days the temporary role lasts, rounded up. For example, a 30-day temprole meets this requirement if you have cast at least 15 votes after its beginning. Each vote counts towards **all** of your active temporary/pause roles

3. **Premium Instance**: The server uses a [MoonlightBot Premium instance](/support/premium.md) (Advanced tier or higher)

4. **Be Exempted**: You must have requested and received an exemption from the above requirements from bot Staff. Simply ask in the support channel and they will guide you through the exemption process

If none of these conditions are met, the operation at the end of expiration will not be executed. You can check if your temproles are sustained with [`/list-temproles`](/role-management-commands/list-temproles.md).

If someone is threatening to stop sustaining temproles to damage your server, [contact support](https://discord.gg/hNQWVVC). We will begin investigating the threat and will work to prevent abuse towards your server.

## Will my temproles be erased if bot downtime happens?

No! There's absolutely no reason to worry about potential data losses as MoonlightBot is designed to be resilient. We are committed to 99% uptime, but if it ever happens that the bot goes down, your temproles will be removed as nothing happened.

## Can I use bots to trigger MoonlightBot commands?

No, other bots and webhooks cannot trigger MoonlightBot, due to safety reasons. Using [selfbots](https://support.discord.com/hc/en-us/articles/115002192352-Automated-User-Accounts-Self-Bots) is a violation of Discord's Terms of Service.

## What language is MoonlightBot written in?

It's written in Node.js using the Discord.js library to interface with Discord's API.

## Who is the owner of MoonlightBot?

MoonlightBot is owned by MoonlightCapital. With tag `moonlightcapital` and ID `256460316660072448` on Discord.

## How can I get access to new features early?

Take a look at the [Beta](/support/beta.md) version of MoonlightBot. We also have a more advanced [Tester Program](/support/volunteering.md#tester).

## I found a bug. How do I report it?

Report it in the [support server](https://discord.gg/hNQWVVC). Make sure to include enough information for your bug to be reproducible.

If your bug can be used to compromise the bot or end user's security, **message the bot owner privately about it**, and please do not disclose it anywhere.
