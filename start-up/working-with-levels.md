---
description: A.K.A how to let your mods use temprole
---

# Working with levels

MoonlightBot uses its internal level system to consider who is able to use a specific command. This system aims to be detached from Discord's permission to allow the bot to be used as proxy and make your server more secure.

## Particular case uses

MoonlightBot's level permission system can come handy if you want more granularity on the permissions you give to your users. Say you have trial mods and you don't want to give them potentially disruptive permissions. You can arrange MoonlightBot so it only executes commands from users who are truly authorized to use them.

## General rules

Levels can be tied to roles and commands. You can do this with the `config` command. [Check its page](../admin-commands/config/) and the relative sub-pages to see how to do this.

The basic rule is that users are allowed to execute a command if their level is equal or higher to the command's level. Each role and command can be set to a different level. A level is a integer between 0 and 100 (both included). The higher the level, the higher the power. That's at least how I designed it to work \~MoonlightCapital.

{% hint style="info" %}
You're allowed to set levels within the 0-100 range as you wish. Get creative if you must!
{% endhint %}

A user's level is dictated by the highest of the levels of the roles they have, ignoring Discord's hierarchy, meaning that if their roles have levels "0, 15, 0, 0, 20, 80, 10, 0, 50" in no special order (those numbers are random and just for demonstrative purposes), their level will be 80 (the highest number of those).

## Defaults

Each role has a level of 0 if not initialized.

To protect servers from abuse, commands have their default level that is used if the command has no level explicitly set. See the documentation page of each command to see its default level.

{% hint style="warning" %}
If you are not the server owner, you're better off setting the admin role level to 100, so you won't encounter conflicts next time you edit other role settings.
{% endhint %}

## Exceptions

Those overrides to an user's level are applied in order:

1. The initial level is calculated by taking the highest level from the levels of their roles.
2. If for some reason the level is below 0 or above 100 it will fall back to 0.
3. If the user is the server owner, they always have level 100.
4. If their level is 0 and they have permission to manage server, their level will be 100 to make it easier to proceed in the initial setup of the bot.
5. MoonlightBot Staff members have level 100 globally, to edit server settings without the need of roles or permissions.
6. MoonlightBot's owner has level 101 globally. This is a special case that can be useful to sort out issues if necessary.

## Final notes

There are many creative things you can use levels with that are not listed here. Use them responsibly.

{% hint style="danger" %}
**MoonlightBot devs are not responsible if you screw up**. If someone gets to use the bot and bans everyone in your server because your levels were not configured correctly it's not our fault. Of course, there are some restrictions to prevent this abuse. If you feel like someone is working around our security measures to gain unauthorized privileges, please **report it to a developer immediately. **(Only in case a developer makes a mistake it's their fault).
{% endhint %}
