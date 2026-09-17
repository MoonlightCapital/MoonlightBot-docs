# premium

This command allows you to learn about [Premium](/support/premium.md) subscriptions and manage your own.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

*No specific permissions required*

By default, a user is required to have the following permissions to use this command:

*No specific permissions required*

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## info

This subcommand shows information about Premium subscriptions, depending on your situation:

* If you are **not a subscriber**, it shows an overview of Premium: a brief description, then a banner and the list of benefits for each tier, with buttons to switch between tiers (each tier includes all the benefits of the lower ones). At the bottom, buttons explain every method of obtaining a subscription of that tier. If you haven't been using MoonlightBot for long enough to be eligible for a [volunteer position](/support/volunteering.md), you can also ask to be reminded once you become eligible
* If your **server has a Premium subscription**, it tells you who the representative is
* If you are a **subscription holder** yourself, it shows information about your subscription

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

This subcommand allows a new [Patreon](https://www.patreon.com/MoonlightCapital) subscriber to enable their subscription on their own, without waiting for a Staff member to do it manually: all the needed data is fetched directly from the Patreon API. You can run it anywhere, as long as you are a member of the [support server](https://discord.gg/hNQWVVC). If you are already subscribed and later adjust your pledge to add extra server slots, run this command again to update your allowance accordingly.

Once enabled, subscribers of the Advanced tier or higher can add the MoonlightBot Premium instance to their servers, as described in the [activation guide](/support/premium.md#activation).

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
