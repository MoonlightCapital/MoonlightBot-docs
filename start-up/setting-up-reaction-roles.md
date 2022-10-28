# Setting up reaction roles

## What are reaction roles?

MoonlightBot allows users to assign or remove roles from themselves by reacting to specific messages that server admins set up for. There are several customization options to supercharge your server to the top.

## Preliminary

Before beginning, make sure of the following things:

* MoonlightBot has View Messages, Send Messages, Add Reactions and Manage Messages permissions in both the channel you're using commands in and the one you want reaction roles to be applied to
* Plan ahead what roles and emojis you want to use

## Creating a group

A group is a collection of emoji to role pairs and settings. Groups are independent for each other. After setting the appropriate pairs, you can apply the group to messages so users can start interacting with the bot and gain roles.

To create a group, use this command:

```
/reaction-roles create <name>
```

Replace `<name>` with a short, memorable name that you will remember later for every reaction roles operation.

{% hint style="info" %}
Screenshots in this page will show old, message-based commands. Type `/reaction-roles` while using any command now. We are working to replace the outdated illustrations as soon as possible.
{% endhint %}

![Creation of a group named "pets"](<../.gitbook/assets/immagine (9).png>)

Group names can contain only alphanumeric characters, underscores and dashes. They must be unique and no longer than 32 characters.

## Matching the pairs together

Now that you have a group made, you need to configure what emoji users need to react to get roles.

You do that with the `setroles` command in this fashion:

```
/reaction-roles setroles <group>
```

The argument, `<group>` is the name of your group. Using this command will begin a guided process to set your roles. First, you will be asked to input a role (with a name, ID or mention), then react to the reply message to tie it to an emoji.

![Step 1: the role (yellow), step 2: the reaction (green)](<../.gitbook/assets/immagine (10).png>)

Add as many as you want, or stop adding roles with `cancel`

![](<../.gitbook/assets/immagine (11).png>)

You can use custom emojis as well, but they must be uploaded in the same server as you're setting it up.

There are a few things to note:

* The same role can be given by multiple different emojis in the same group
* A single emoji can be paired with only **one** role (later you'll see how to make an emoji give multiple roles)
* You can only add up to 20 pairs per group (Discord only allows 20 different reactions per message)

## Applying your group to messages

This is the last required step to do before making reaction roles operative for your users. This consists in making the bot acknowledge that reactions in that group have to assign roles.

To do this, you simply need to use the following command:

```
/reaction-roles apply <group> <message>
```

Once again, `<group>` is a group you created before, and `<message>` is for the message the reaction roles will work on. The following are valid message identifiers:

* A simple message ID, like `663696313086509106`. This only works if the message was sent in the channel you're using the command in.
* A Channel ID and a message ID, separed by a single dash, like `659297716920254465-663696313086509106`. You can get this by holding the SHIFT key while copying the message ID. This works if you want to keep the reaction roles channel clean.
* **(recommended)** A message link, composed of Server ID/Channel ID/Message ID, like `https://discord.com/channels/359057740200673280/659297716920254465/663696313086509106`. Right click (or long press) the message from mobile then click "Copy Link". You can then paste the link from your clipboard.

{% hint style="warning" %}
To copy message IDs, you first need to [enable developer mode](../advanced/developer-mode.md). It is not necessary for links.
{% endhint %}

And voila! The bot will ask you to confirm since already existing reactions will be removed, then, all reactions from the group will be added. This operation may take about 20 seconds to complete, depending on the amount of reactions.

![](<../.gitbook/assets/immagine (12).png>)

If you add more roles later on, you can use this command again to refresh the reactions.

You've done it! You can now pass to more advanced, optional customization.

## Group configuration

The `config` command offers a voice to edit group settings. Those are completely optional and are effective immediately, let's see some here:

```
/config reactionroles <group>
```

* JoinOnly allows users to add themselves the roles, but not remove them.
* LeaveOnly works the opposite of JoinOnly: it allows users to remove themseves the roles, but not add them.
* MaxRoles is the amount of roles of the group the user can have at the same time. Useful if you want someone to choose one role but not have the others (this is a number, so it can be any higher value!)
* Duration is how long the role lasts after being added. This makes the group work like a temprole!

For an in-depth view of all options, see the [Configuring Reaction Roles](../admin-commands/config/configuring-reaction-roles.md) page.

## FAQ

### How do I make reaction roles temporary?

Use `/config arguments: reactionroles <group> duration <duration>` to add a timer that starts when the reaction is clicked. The duration is provided in, say, [the same way as](arguments.md#durations) you use the `temprole` command.

### Can I make a single click of a reaction give out more than one role?

Yes! However, group settings are common for each role in the group. Though you can apply multiple groups to the same message, which will allow you to:

- Make some roles temporary, and other ones permanent
- Make some roles only joinable, while removing other ones on click
... And much more, you can experiment which settings works best for you.

### How do I disable notifications that are sent to the user?

#### If you are a server admin:

Use `/config arguments:reactionroles <group> dmnotification false` to disable notifications for a group.

{% hint style="warning" %}
If a message has multiple groups, notifications will still be sent, providing at least one of the other groups has notifications enabled
{% endhint %}

#### If you are an user:

You can disable all reaction role notifications in every server with `/userconfig arguments: reactionrolenotifications false` for your account. This will take precedence over server settings regardless.

You can re-enable both at any time replacing `false` with `true`.
