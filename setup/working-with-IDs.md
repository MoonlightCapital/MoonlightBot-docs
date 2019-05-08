# Working with IDs

Discord uses an unique ID system to track every object, ranging from users, to roles and channels. MoonlightBot fully supports roles as command arguments and as config values.

# Developer mode
This is not what it sounds, seriously. You don't have to be a bot developer to have this enabled. At most, it helps you with some magic trickery and server moderation.
Developer mode adds a "Copy ID" options in most right click menus. There, that's all it does.

To enable developer mode:

- Go to User settings (the cog icon in the bottom left of the window)
- Go to Appearance tab
- Scroll down
- Toggle dev mode on

Yay! You did it!

## Copying IDs
After enabling developer mode, right click any menu (channel, user, server, message) and you should see the "Copy ID" button. When you click it, a string of numbers will magically appear in your clipboard, and you can Ctrl+V them.

## Role IDs
That's all, right? Unfortunately, you cannot copy role IDs at the moment. However there are a few workarounds.

### Backslash trick
- Tick "Allow anyone to mention this role" in the role settings page
- Go to any channel in the server, and type `@role name` as you want to mention it
- Put a `\` (backslash) character before the role mention, like this: `\@role name`
- Send the message. You should see something like `<@&165511591545143296>` in the message content
- The numbers are what you're looking for

>This **will ping** the users with that role, which may be a bit annoying for some. Make sure to do this in a channel where not many people can see.

### Using a bot
If you have any bot with a roleinfo command, you can try to use it and search for the ID. We'll add this to MoonlightBot, don't worry.
