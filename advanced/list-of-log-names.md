---

description: On this page all the available logs are listed

---

# List Of Log Names

Logs, categorized by what they do are listed here, and are **case sensitive**. Individual logs are written in _UPPER\_CASE_, while category names (which can be used in place of individual log names, see [_**configuring channels**_](../management-commands/config.md)) are _Capitalized_. Each one of them is separated by categories in the lists below. If you want to log everything, use an asterisk to include all things that can be logged, including ones that will be introduced in future updates. All logs require the bot to have permission to view and send messages in the logging channel. It must also be able to send embeds and files there,and some logs require the bot to have the "View Audit Log" permission enabled.

## Moderation

This category is to log actions taken by moderators. Most of them are triggered by using bot commands, but those starting with `AUDIT_` will read the data from Discord's audit log providing MoonlightBot has permission to do so.

| Name              | Emitted when     |
| ----------------- | ---------------- |
| BAN               | A user [gets banned](../moderation-commands/ban.md) |
| INFRACTION_DELETE | A moderator [deletes an infraction](../moderation-commands/infractions.md)|
| KICK              | A user [gets kicked](../moderation-commands/kick.md) |
| MUTE              | A user [gets muted](../moderation-commands/mute.md) |
| PAUSE_ROLE_ADD    | A role [gets temporarily removed](../role-management-commands/pause-role.md) |
| PAUSE_ROLE_EXTEND | A role's length of time to be removed gets adjusted |
| PAUSE_ROLE_REMOVE | A role gets added back |
| REASON_UPDATE     | A [reason for an infraction](../moderation-commands/infractions.md#reason ) gets updated |
| ROLE_ADD          | A [role](../role-management-commands/role.md) gets added |
| ROLE_REMOVE       | A role gets removed|
| SELFROLE_ADD      | A user adds a [self-assignable role](../role-management-commands/selfrole.md) to themselves |
| SELFROLE_REMOVE   | A user removes a self-assignable role from themselves  |
| SOFTBAN           | A user gets [soft-banned](../moderation-commands/softban.md) |
| TEMPBAN_EXTEND    | A [temporary ban](../moderation-commands/tempban.md) gets extended |
| TEMPBAN_REMOVE    | A temporary ban gets removed |
| TEMPMUTE_EXTEND   | A [temporary mute](../moderation-commands/tempmute.md) gets extended |
| TEMPMUTE_REMOVE   | A temporary ban gets removed |
| TEMPROLE_ADD      | A [temporary role](../role-management-commands/temprole.md) gets added |
| TEMPROLE_EXTEND   | The length of a temporary role gets extended |
| TEMPROLE_REMOVE   | A temporary role gets removed |
| TIMEOUT           | A user gets [timed out](../moderation-commands/timeout.md) |
| TIMEOUT_REMOVE    | A time out gets removed |
| UNBAN             | A user gets [unbanned](../moderation-commands/unban.md) |
| UNMUTE            | A user gets [unmuted](../moderation-commands/unmute.md) |
| WARNING           | A user [receives a warning](../moderation-commands/warn.md) |

## Members

This category is for actions relating to members interacting with the server.

| Name      | Emitted when     |
| --------- | ---------------- |
| USER_JOIN | Someone joins |
| USER_LEFT | Someone leaves |

## Messages

This category is for things having to do with messages.

| Name                | Emitted when     |
| ------------------- | ---------------- |
| CHANNEL_CLEAN       | Messages get [cleaned](../moderation-commands/clean.md) from a channel. Includes a file with a backup of the deleted messages |
| MESSAGE_BULK_DELETE | A moderator bulk deletes a set of messages |
| MESSAGE_DELETE      | A message is deleted |
| MESSAGE_EDIT        | A message gets edited |
| MESSAGE_PIN_ADD     | A message gets pinned |
| MESSAGE_PIN_REMOVE  | A message gets unpinned |

## Debug

{% hint style="info" %}
This category is for debugging purposes. Logs in this category are meant to aid in fixing errors that may prevent the bot from functioning correctly.

{% endhint %}

| Name                | Emitted when     |
| ------------------- | ---------------- |
| REACTION_ROLE_DEBUG | An error occurs in the process of triggering a [reaction role.](/start-up/setting-up-reaction-roles.md) |  
