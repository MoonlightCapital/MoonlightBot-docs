# premium

This command allows you to learn about [MoonlightBot Premium](/support/premium.md) subscriptions and manage your subscription status.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

*No specific permissions required*

By default, a user is required to have the following permissions to use this command:

*No specific permissions required*

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## info

This subcommand shows information about Premium subscriptions. Depending on your situation, it will display one of the following:

* **You are not a subscriber**: The command will display an interactive panel with tier selection buttons to switch between the various tiers, the list of benefits for the selected tier, and at the bottom buttons explaining how to obtain that tier. You can also ask to be automatically reminded once you are eligible for a selected [volunteer position](/support/volunteering.md) if a tier can be obtained that way.
* **You have a Premium subscription enabled:** You will see all the information about your subscription, such as the expiration date, which and how many servers you represent, and how your subscription was obtained.
* **You use a command in a server with Premium enabled:** The command will tell you who the representative of the server is. Only on the MoonlightBot Premium instance.

{% hint style="info" %}
The overview shown to non-subscribers was completely remade in version 4.8.0, currently available on [MoonlightBot beta](/support/beta.md).
{% endhint %}

```text
/premium info
```

*This subcommand does not have any options*

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## enable

This subcommand allows a new [Patreon subscriber](https://www.patreon.com/MoonlightCapital) to enable their subscription themselves, without waiting for Staff. To successfully enable your subscription, all of the following conditions must be met:

* You must be a member of the [support server](https://discord.gg/hNQWVVC).
* Your Discord account must be [connected on Patreon's site](https://support.patreon.com/hc/en-us/articles/212052266-Getting-Discord-access).
* Your Patreon account must not have already been used to enable a subscription for a different Discord account.
* You must have an actual active (paid) pledge to one of the [tiers](/support/premium.md#tiers) on Patreon.
* Your latest Patreon payment must have gone through during the current month.

If you change your pledge for extra server slots, run the command again to update your allowance.

After enabling your subscription, if you are on the Advanced tier or higher, you can add the Premium bot to your server. For instructions, see the [activation guide](/support/premium.md#activation).

{% hint style="info" %}
This subcommand was introduced in version 4.8.0, currently available on [MoonlightBot beta](/support/beta.md).
{% endhint %}

```text
/premium enable
```

*This subcommand does not have any options*

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md).

## Logs

*This command does not trigger any log events*

For more information on setting up those logs, refer to the [log setup tutorial](/README.md#logging)
