# Permission Tutorial

Discord has a built-in permission system to configure who can or cannot execute certain commands of the bot. This tutorial will guide you through the process of setting up permissions for MoonlightBot.

## Open the Server Settings

1. Click on the server name to open the context menu, then click on Server Settings
2. In the server settings, click on Integrations in the left sidebar
3. Here you'll see a list of all the bots and integrations in your server. Click on the "MoonlightBot" entry to open the bot command permissions menu

<figure><img src="/.gitbook/assets/PermissionTutorialStep1.png" alt=""><figcaption><p>The Integrations tab of server settings</p></figcaption></figure>

## Set up Permissions

{% hint style="warning" %}
**Remember to save your changes!**

From now on, each time you make a change on the permissions configuration, be sure to click on the "Save Changes" to make the changes effective.
{% endhint %}

On the command permissions menu, you can configure two types of permissions:

* **General Permissions**: These permissions apply to all commands of the bot, the default option is that everyone can use bot commands in every channel. If you want to restrict commands to specific roles, users or channels click the corresponding "Add" button and be sure to deny the default "everyone" role or "All channels" setting

{% hint style="warning" %}
Members who have Administrator permission can bypass these restrictions.
{% endhint %}

![Command permissions page](/.gitbook/assets/PermissionTutorialStep2.png)

* **Command-specific Permissions**: These permissions apply to specific commands of the bot and they override the general permissions. To set up command-specific permissions, select the command you want to configure from the list and add the rules for roles, members or channels as you like. Be sure to deny the default "everyone" role or "All channels" setting if you want to restrict the command only for the selected roles, members or channels.

![You can configure who can use a command by simply clicking on it](/.gitbook/assets/PermissionTutorialStep3.png)

## Default Overrides

Some commands have required permissions by default. For example, the [`/ban`](/moderation-commands/ban.md) command requires the Ban Members permission. This is a security measure in order to lock moderation commands from normal users. You can check the required permissions of each command by clicking it on the permission configuration menu or by visiting its documentation page. You can still override these default permissions by setting up command-specific permissions as explained above, this can be useful if you want for example allow some users to use the [`/temprole`](/role-management-commands/temprole.md) command without giving them the "Manage Roles" permission.

![Permission configuration menu of a command](/.gitbook/assets/PermissionTutorialStep4.png)

## Test your Permissions

Once you've set up the permissions, make sure the changes you've made are working as expected. You can use the ["View Server as Role"](https://support.discord.com/hc/en-us/articles/360055709773-View-as-Role-FAQ) feature to test the permissions of a specific role. To do this, on the server settings page, navigate to the Roles section, right-click on the role you want to test and click on "View Server as Role". You can even test the permissions with multiple roles by using the dropdown menu at the top of the screen.
