# Moderation Tutorial

## Intro

This guide will give you the basic information needed to moderate your Discord server with MoonlightBot. It includes a list of commands and how they work, complete with their arguments, infractions, and log information to help you better understand how to use them

## Arguments

Arguments are options you may use while executing moderation commands. You can find a more in-depth guide about arguments in the [arguments page](/start-up/arguments.md)

![](/.gitbook/assets/MuteArguments.png)

- **`user`**: The target member of the command
- **`reason`**: The reason for which you are executing the command
- **`notify`**: Whether or not the bot will message the user after the command is executed
- **`no-infraction`**: Whether or not the command will count towards the user's infractions

{% hint style="info" %}
If both the `notify` and `no-infraction` arguments are true, the target will not be notified in order to prevent harrassment via MoonlightBot
{% endhint %}

- **`duration`**: The amount of time for which the user will be affected by the command. For more information about this argument, refer to the [arguments page](/start-up/arguments.md#durations)
- **`remove-roles`**: Exclusive to the mute commands, this argument will remove all of the user's roles except the muterole if true
- **`role`**: The role to assign/remove in a role command

## Moderation Tools

These features help ensure a seamless moderation experience with MoonlightBot

### Infractions

![](/.gitbook/assets/InfractionsExample.png)

Infractions help staff members organize actions taken while moderating, such as mutes. This is a versatile tool with multiple submcommands to assist your moderation needs. More information about infractions can be found in the [infractions page](/moderation-commands/infractions.md)

### Logs

![](/.gitbook/assets/LogExample.png)

When moderators execute an action such as a warn, MoonlightBot will send a message in the designated logs channel in order to keep track of moderation events. For more information on setting up logs, refer to the logs section of the [main page](/README.md)

## Commands

All the commands listed can be found in the "moderation-commands" and "role-management-commands" categories

### Ban/Kick

- [**`/kick`**](/moderation-commands/kick.md): This command removes a user from the server, but they are able to rejoin if they have an invite
- [**`/ban`**](/moderation-commands/ban.md): This command kicks a user from the server and prohibits them from rejoining
- [**`/tempban`**](/moderation-commands/tempban.md): This command temporarily bans a user for a set amount of time
- [**`/softban`**](/moderation-commands/softban.md): This command bans a user then immediately unbans them. Though similar to the kick command, this command deletes the user's messages
- [**`/unban`**](/moderation-commands/unban.md): This command unbans a user from the server, allowing them to rejoin (if they have an invite)
  
### Mute

{% hint style="info" %}
The mute commands requires a mute role. You can make one by using [`/create-muterole`](/management-commands/create-muterole.md); MoonlightBot will set everything up for you!
{% endhint %}

- [**`/mute`**](/moderation-commands/mute.md): This command suppresses a user from sending messages
- [**`/tempmute`**](/moderation-commands/tempmute.md): This command temporarily mutes a user for a set amount of time
- [**`/unmute`**](/moderation-commands/unmute.md): This command unmutes a user, allowing them to send messages again

### Role

- [**`/role`**](/role-management-commands/role.md): This command gives a role to a user
- [**`/temprole`**](/role-management-commands/temprole.md): This command temporarily gives a role to a user for a set amount of time
- [**`/list-temproles`**](/role-management-commands/list-temproles.md): This command lists the active temproles
- [**`/pause-role`**](/role-management-commands/pause-role.md): This command takes a role from a user and gives it back after a set amount of time
