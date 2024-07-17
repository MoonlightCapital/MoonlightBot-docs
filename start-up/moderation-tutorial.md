# Moderation Tutorial

This guide will give you the basic information needed to moderate your Discord server with MoonlightBot. It features a list of commands and how they work, complete with their options, infractions, and log information to help you better understand how to use them.

## Command Options

These are options you may use while executing moderation commands. You can find a more in-depth guide about options in the [arguments page](/start-up/arguments.md)

![A list of example options in a mute command](/.gitbook/assets/MuteArguments.png "Options Example")

- `user`: The user to execute the moderation action on
- `reason`: The reason for which you are taking the action, useful for record keeping. The reason shows up in infractions, logs, and notifications from the bot
- `notify`: Whether or not the bot will message the user after the command is executed, as shown below
![An example of a notification from the bot](/.gitbook/assets/NotifyExample.png "Notify Example")
- `no-infraction`: Whether or not the command will count towards the user's infractions

{% hint style="info" %}
If both the `notify` and `no-infraction` options are true, the target will not be notified in order to prevent harassment via MoonlightBot
{% endhint %}

- `duration`: The amount of time for which the user will be affected by the effects of the command. You can use any duration ranging from weeks to milliseconds. For example, `1w2d` and `1 week 2 days` will both affect the target of the command for 1 week and 2 days.
- `remove-roles`: Exclusive to the mute commands, this option will remove all of the user's roles except the muterole if true. This is to ensure the permissions of other roles don't interfere with the effectiveness of the mute.
- `role`: The role to assign/remove in a role command

## Moderation Tools

These features help ensure a seamless moderation experience with MoonlightBot

### Infractions

![An example of the Infractions Summary command](/.gitbook/assets/InfractionsExample.png "Infractions Example")

Infractions help staff members keep track of a user's bad conduct and make informed decisions while moderating. This is a versatile tool with multiple submcommands to assist your moderation needs.

More information about infractions can be found in the [infractions page](/moderation-commands/infractions.md)

### Logs

![A log example containg a mute infraction](/.gitbook/assets/LogExample.png "Logs Example")

When moderators execute an action such as a warn, MoonlightBot will send a message in the designated logs channel in order to keep track of moderation events. For more information on setting up logs, refer to the logs section of the [main page](/README.md)

## Commands

All the commands listed can be found in the "Moderation Commands" and "Role Management Commands" categories

### Ban/Kick

- [**`/kick`**](/moderation-commands/kick.md): This command removes a user from the server, but they are able to rejoin if they have an invite
- [**`/ban`**](/moderation-commands/ban.md): This command kicks a user from the server and prohibits them from rejoining
- [**`/tempban`**](/moderation-commands/tempban.md): This command temporarily bans a user for a set amount of time
- [**`/softban`**](/moderation-commands/softban.md): This command bans a user then immediately unbans them. Though similar to the kick command, this command deletes the user's messages (useful for cleaning up spam)
- [**`/unban`**](/moderation-commands/unban.md): This command unbans a user from the server, allowing them to rejoin (if they have an invite)
  
### Mute

{% hint style="info" %}
The mute commands requires a mute role. You can make one by using [`/create-muterole`](/management-commands/create-muterole.md); MoonlightBot will set everything up for you!
{% endhint %}

- [**`/mute`**](/moderation-commands/mute.md): This command suppresses a user from sending messages, creating threads, and adding reactions.
- [**`/tempmute`**](/moderation-commands/tempmute.md): This command temporarily mutes a user for a set amount of time
- [**`/unmute`**](/moderation-commands/unmute.md): This command unmutes a user, allowing them to send messages again

### Role

- [**`/role`**](/role-management-commands/role.md): This command gives/takes a role from a user
- [**`/temprole`**](/role-management-commands/temprole.md): This command temporarily gives a role to a user for a set amount of time
- [**`/list-temproles`**](/role-management-commands/list-temproles.md): This command lists the active temproles
- [**`/pause-role`**](/role-management-commands/pause-role.md): This command takes a role from a user and gives it back after a set amount of time
