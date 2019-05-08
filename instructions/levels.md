# Power levels

MoonlightBot offers a very flexible power level system which dictates who can use commands. Levels are applied both at a role and at a command level.
A level is an integer between 0 and 100 (included)

## Example case uses

- You want your moderators to ban users, but not unban them
- You want to restrict a certain group of commands, or a single command to a role
- Anything else you can think of

## Role levels
You can tie a level to a role in the config file. An user's final level is calculated by the highest level tied to any of their roles. For example:

```
User:
  Roles:
    - Trusted: Level 10
    - Event winner: Level 15
    - Announcement notification: Level is not set in the config.
```

This user's level will be 15. Roles without a level set will be ignored in the calculation.

Now, here's another example:

```
User2:
  Roles:
    - Head admin: Level is not set in the config.
    - Admin: Level 100
    - Moderator: Level 50
    - Event winner: Level 15
    - Announcement notification: Level is not set in the config.
```

What will this user's level be? If you guessed 100, you're right!

>An user with no roles, or whose roles have no level set in the config will always have a level of 0.

## Command levels

A level can be tied to a command, too. You can raise or lower it as your liking in the config.
>An user will be allowed to use a command only if their role final level is equal or higher than the command level.

Commands will usually have a default level in the config, most common ones are 0, 50 and 100.
