# Configuring roles

In the config file, you're given a lot of freedom in deciding what you can do with roles. Currently, a role config object looks like this:

```json
{
  "name": "Trusted",
  "level": 10,
  "selfAssignable": false
}
```

Now, let's break this down:

- `name` is the name of your Discord role. Make sure it **exactly** matches with the role name, including uppercase/lowercase letters. This is required as it dictates which role the data is tied to.
- `id` is an alternative to `name`. This is your Discord role ID. It offers more precision than the name parameter
- `level` is the level for the role. For more info on what this does, see the [Power levels](https://github.com/MoonlightCapital/MoonlightBot-docs/blob/master/instructions/levels.md) section. This parameter is optional and defaults to 0.
- `selfAssignable` is an optional parameter that is handy when you want to set up self-assignable roles in your server. We'll take a look at this in a later section.
- `selfAssignableDuration` is for self-assignable temproles. It's a string that contains a duration like you would set it with the `temprole` command.

## `name` vs `id`
As it's a bit tedious to get role IDs on discord, we let you use the role name to make it easier for you to config the bot.
ID is always reccomended over the name property, as it does not change if you change the role name. However, it makes it harder for you to see what role the settings are for.

>If you have both `name` and `id` on the same role, `id` will take priority.
>Having both makes it easier for you to navigate through the config.

## Examples

### Setting up a moderator role
```json
{
  "name": "Moderator",
  "level": 50
}
```
>Every mod-only command has a default level of 50. Use this at your advantage.
> We omitted the `selfAssignable` parameter, as it's pointless if the role cannot be self-assigned.

### Notification roles
Let's assume you're a streamer and want users to be notified when you go live. MoonlightBot offers a selfrole command that lets users give themselves roles that have been configured for this use.
```json
{
  "name": "Stream notification",
  "selfAssignable": true
}
```
