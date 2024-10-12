---
description: On this page all the available logs are listed
---

# List of log names

Logs, categorized by what they do, are listed here and are **case sensitive**. Individual logs are written in _UPPER\_CASE_, while category names (which can be used in place of individual log names, see [configuring channels](../management-commands/config.md#channels)) are _Capitalized_. Each one of them is separated by categories in the lists below. To log all events, use an asterisk (`*`). All logs require the bot to have permission to view and send messages, embed links and attach files in the respective channels. Some logs require the bot to have the "View Audit Log" permission enabled at server level.

## Moderation

This category is to log actions taken by moderators. Most of them are triggered by using bot commands, but those starting with `AUDIT_` will read the data from Discord's audit log providing MoonlightBot has permission to do so.

| Name                | Emitted when                                                                                |
| ------------------- | ------------------------------------------------------------------------------------------- |
| BAN                 | A user [gets banned](../moderation-commands/ban.md)                                         |
| INFRACTION\_DELETE  | A moderator [deletes an infraction](../moderation-commands/infractions.md)                  |
| KICK                | A user [gets kicked](../moderation-commands/kick.md)                                        |
| MUTE                | A user [gets muted](../moderation-commands/mute.md)                                         |
| PAUSE\_ROLE\_ADD    | A role [gets temporarily removed](../role-management-commands/pause-role.md)                |
| PAUSE\_ROLE\_EXTEND | A role's length of time to be removed gets adjusted                                         |
| PAUSE\_ROLE\_REMOVE | A role gets added back                                                                      |
| REASON\_UPDATE      | A [reason for an infraction](../moderation-commands/infractions.md#reason) gets updated     |
| ROLE\_ADD           | A [role](../role-management-commands/role.md) gets added                                    |
| ROLE\_REMOVE        | A role gets removed                                                                         |
| SELFROLE\_ADD       | A user adds a [self-assignable role](../role-management-commands/selfrole.md) to themselves |
| SELFROLE\_REMOVE    | A user removes a self-assignable role from themselves                                       |
| SOFTBAN             | A user gets [soft-banned](../moderation-commands/softban.md)                                |
| TEMPBAN\_EXTEND     | A [temporary ban](../moderation-commands/tempban.md) gets extended                          |
| TEMPBAN\_REMOVE     | A temporary ban gets removed                                                                |
| TEMPMUTE\_EXTEND    | A [temporary mute](../moderation-commands/tempmute.md) gets extended                        |
| TEMPMUTE\_REMOVE    | A temporary ban gets removed                                                                |
| TEMPROLE\_ADD       | A [temporary role](../role-management-commands/temprole.md) gets added                      |
| TEMPROLE\_EXTEND    | The length of a temporary role gets extended                                                |
| TEMPROLE\_REMOVE    | A temporary role gets removed                                                               |
| TIMEOUT             | A user gets [timed out](../moderation-commands/timeout.md)                                  |
| TIMEOUT\_REMOVE     | A time out gets removed                                                                     |
| UNBAN               | A user gets [unbanned](../moderation-commands/unban.md)                                     |
| UNMUTE              | A user gets [unmuted](../moderation-commands/unmute.md)                                     |
| WARNING             | A user [receives a warning](../moderation-commands/warn.md)                                 |

## Members

This category is for actions relating to members interacting with the server.

| Name       | Emitted when   |
| ---------- | -------------- |
| USER\_JOIN | Someone joins  |
| USER\_LEFT | Someone leaves |

## Messages

This category is for things having to do with messages.

| Name                  | Emitted when                                                                                                                  |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| CHANNEL\_CLEAN        | Messages get [cleaned](../moderation-commands/clean.md) from a channel. Includes a file with a backup of the deleted messages |
| MESSAGE\_BULK\_DELETE | A moderator bulk deletes a set of messages                                                                                    |
| MESSAGE\_DELETE       | A message is deleted                                                                                                          |
| MESSAGE\_EDIT         | A message gets edited                                                                                                         |
| MESSAGE\_PIN\_ADD     | A message gets pinned                                                                                                         |
| MESSAGE\_PIN\_REMOVE  | A message gets unpinned                                                                                                       |

## Debug

{% hint style="info" %}
This category is for debugging purposes. Logs in this category are meant to aid in fixing errors that may prevent the bot from functioning correctly.
{% endhint %}

| Name                  | Emitted when                                                                                                |
| --------------------- | ----------------------------------------------------------------------------------------------------------- |
| REACTION\_ROLE\_DEBUG | An error occurs in the process of triggering a [reaction role](../get-started/setting-up-reaction-roles.md) |
