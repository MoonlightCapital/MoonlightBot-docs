# Setting up reaction roles

## What are reaction roles?

MoonlightBot allows users to assign/remove roles to/from themselves by reacting to specific messages that server admins set up. There are several customization options to optimize your needs.

## Preliminary

Before beginning, make sure of the following things:

* MoonlightBot has View Messages, Send Messages, Add Reactions and Manage Messages permissions in both the channel you're using commands in and the one you want reaction roles to be applied to
* You have the Manage Server permission
* Plan ahead what roles and emojis you want to use
* There is an existing message to apply reactions to

## Creating a group

A group is a collection of emoji to role pairs and settings. Each group operates independently. After setting the appropriate pairs, you can apply the group to messages so members can use the reactions to manage their roles.

To create a group, use this command:

```
/config reaction-roles <group>
```

Replace `<group>` with a short, memorable name that you will remember later for every reaction roles operation.

![](<../.gitbook/assets/ReactionRoleSetup1.png>)

Group names can contain only alphanumeric characters, underscores and dashes. They must be unique and no longer than 32 characters.

## Matching the pairs together

Now that you have a group made, you need to configure which emojis users need to react with to get roles.

You do that with the `set` command in this fashion:

```
/reaction-roles set <group> <emoji> <role>
```

* `<group>` = the name of the group you set up before.
* `<emoji>` = the emoji you want to be used
* `<role>` = the role you want the emoji to be paired to

![](<../.gitbook/assets/ReactionRoleSetup2.png>)

You can use this command as many times as you want to add multiple pairs to your group. You can use custom emojis as well, but they must be uploaded in the same server as you're setting it up.

There are a few things to note:

* The same role can be given by multiple different emojis in the same group
* You can assign multiple roles to an emoji by using the set command multiple times.
  * Example: 
  `/ reaction-roles set group1 emoji1 role1`

  `/ reaction-roles set group1 emoji1 role2`

  Doing this will give both roles at the press of the reaction. To remove role1 from the emoji you can use the same command as to add it.

* You can only add up to 20 pairs per group (Discord only allows 20 different reactions per message)

## Applying your group to messages

This is the last required step to do before making reaction roles operative for your users. This consists of making the bot acknowledge that reactions in that group have to assign roles.

To do this, you simply need to follow the following steps:

1. Right click (or press and hold if you're on mobile) the message you want to apply reaction roles to.
2. Select the "`Apps`" option.
3. Select "`Apply Reaction Roles`" ![](<../.gitbook/assets/ReactionRoleSetup3.png>)
4. A private dropdown menu will be sent from the bot displaying the groups you have made. Select the one you want to use. ![](<../.gitbook/assets/ReactionRoleSetup4.png>)
5. And voila! The bot will ask you to confirm since already existing reactions will be removed, then, all reactions from the group will be added. This operation may take about 20 seconds to complete, depending on the amount of reactions. ![](<../.gitbook/assets/ReactionRoleSetup5.png>)

If you add more roles later on, you can use this command again to refresh the reactions.

You've done it! You can now pass to more advanced, optional customization.

## Group configuration

The `config` command offers a voice to edit group settings. Those are completely optional and are effective immediately, let's see some here:

```
/config reaction-roles <group>
```

* `join-only`: Prevents the user from removing their role(s).
* `leave-only`: Prevents the user from assigning the role(s).
* `reverse`: When the message is reacted on, it will remove the role instead of assigning it, and vice versa.
* `max-roles`: The maximum amount of roles within the group a user can assign themselves (0 = unrestricted).
* `dm-notification`: When a role is assigned/removed, the bot will message the user (true by default). 
* `freeze`: When true, the group will not function. This is intended to disable groups for maintenance or other purposes without having to reconfigure.
* `duration`: How long the user will keep their assigned role. This will *not* give a role back (in case of `reverse` being enabled).

For an in-depth view of all options, see the [Configuring Reaction Roles](../admin-commands/config/configuring-reaction-roles.md) page.

## Frequently Asked Questions

### How do I make reaction roles temporary?

Use `/config reaction-roles <group> <duration>` to add a timer that starts when the reaction is clicked. The duration is provided in, say, [the same way as](arguments.md#durations) you use the `temprole` command.

### Can I make a single click of a reaction give out more than one role?

Yes! While group settings are common for each role in the group, you can apply multiple groups to the same message, which will allow you to:

* Make some roles temporary, and other ones permanent
* Make some roles only joinable, while removing other ones on click
... And much more, you can experiment which settings works best for you.

### How do I disable notifications that are sent to the user?

#### If you are a server admin

Use `/config reaction-roles <group> [dm-notification: false]` to disable notifications for a group.

Doing this will only configure that specific group, so if there are multiple groups in the message, make sure to configure all of them to your liking.

#### If you are a user

You can disable all reaction role notifications with `/userconfig settings [reaction-role-notifications: false]`.

You can re-enable both at any time replacing `false` with `true`.
