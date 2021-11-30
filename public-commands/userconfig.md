# Userconfig

{% hint style="warning" %}
This command is available in version `2.5.0` and above.
{% endhint %}

The userconfig command works in the same exact way as [config](../admin-commands/config/), except it modifies some settings for the user who uses it. See the config page for details on syntax.

### Main options

| Name               | Description                                     | Type    | Default | Notes                                                                                                                                                        |
| ------------------ | ----------------------------------------------- | ------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|  voteNotifications | Whether to receive reminders when to vote again | boolean | true    | If you disable this after voting again, you may still receive a few reminders, as this only stops the creation of new reminders instead of stopping delivery |
| showInLeaderboard  | Shows you in the top 5 voters leaderboard       | boolean | true    |                                                                                                                                                              |
