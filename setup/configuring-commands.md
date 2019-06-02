# Configuring commands

A command config object should look like this:

```json
{
    "name": "ping",
    "level": 0
}
```

Now, let's break this down:

- `name`: The command's name, necessary to point to what command the object is referred to.
- `category`: An alternative to `name`, this applies the config to a whole category of commands.
- `level`: The minimum level an user must have to use that command/any command in that category.
- `enabled`: Set this to `false` if you don't want anyone using that command/any command in that category.

## Examples

### Disable a whole category but allow one specific command from that

```json
{
    "category": "Other",
    "level": 100,
    "enabled": false
},
{
    "name": "ping",
    "level": 0,
    "enabled": true
}```

>The category must come first, otherwise it won't work.
>When you disable a command/category, you should set its level to 100 just for safety.
