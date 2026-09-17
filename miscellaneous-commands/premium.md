# premium

This command allows you to manage your [Premium](/support/premium.md) subscription or links to the documentation page if you are not a subscriber.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

*No specific permissions required*

By default, a user is required to have the following permissions to use this command:

*No specific permissions required*

For more information on editing permission requirements for specific users/roles, refer to the [permissions tutorial](/start-up/permission-tutorial.md)

## info

This subcommand shows comprehensive information about Premium subscriptions. If you are not a subscriber, it displays a brief description, a banner for each tier, benefits explained, and buttons to switch between tiers. Each tier also includes buttons explaining all methods of obtaining a subscription of that tier, and a button to check eligibility for volunteer positions.
If you are a subscription holder, it shows info about your subscription or tells you who the representative is if your server has a premium subscription.

```text
/premium info
```

*This subcommand does not have any options*

### Required permissions

MoonlightBot requires the following permissions to successfully execute this subcommand:

*No specific permissions required*

## enable

This subcommand allows a new Patreon subscriber to automatically enable their own subscription without waiting for a Staff member to manually allow it, getting all the data needed directly from the Patreon API. If you are already subscribed but adjusted your pledge for extra slots, using this command again will adjust your allowance accordingly.

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
