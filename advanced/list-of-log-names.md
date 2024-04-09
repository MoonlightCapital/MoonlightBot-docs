---
description: On this page all the available logs are listed
---

# List of log names

Logs, categorized by what they do are listed here, and are **case sensitive**. Individual logs are written in _UPPER\_CASE_, while category names (which can be used in place of individual log names, see [_**configuring channels**_](../management-commands/config.md)) are _Capitalized_. Each one of them is separated by categories in the lists below. If you want to log everything, use an asterisk to include all things that can be logged, including ones that will be introduced in future updates.

{% hint style="warning" %}
Some logs require the bot to have the "View Audit Log" permission enabled.
{% endhint %}

## Moderation

This category is used for actions by moderators or ones that moderators could use. Most of them are fired when a command is run unless they start with AUDIT_, which uses the values in the server's audit log. In that case, actions that are done with or without using the bot are logged.

| Name              | Emitted when     |
| ----------------- | ---------------- |
| BAN               | A user gets banned |
| INFRACTION_DELETE | A moderator removes an infraction|
| KICK              | A user gets kicked |
| MUTE              | A user gets muted |
| PAUSE_ROLE_ADD    | A role gets temporarily removed |
| PAUSE_ROLE_EXTEND | A role's length of time to be removed gets adjusted |
| PAUSE_ROLE_REMOVE | A role gets added back |
| REASON_UPDATE     | A reason for an infraction gets updated |
| ROLE_ADD          | A role gets added |
| ROLE_REMOVE       | A role gets removed|
| SELFROLE_ADD      | A user adds a self-assignable role (see [Selfrole](../role-management-commands/selfrole.md)) |
| SELFROLE_REMOVE   | A user removes a user-assignable role  |
| SOFTBAN           | A user gets soft-banned |
| TEMPBAN_EXTEND    | A temporary ban gets extended |
| TEMPBAN_REMOVE    | A temporary ban gets removed |
| TEMPMUTE_EXTEND   | A temporary mute gets extended |
| TEMPMUTE_REMOVE   | A temporary ban gets removed |
| TEMPROLE_ADD      | A temporary role gets added |
| TEMPROLE_EXTEND   | The length of a temporary role gets extended |
| TEMPROLE_REMOVE   | A temporary role gets removed |
| TIMEOUT           | A user gets timed out |
| TIMEOUT_REMOVE    | A time out gets removed |
| UNBAN             | A user gets unbanned |
| UNMUTE            | A user gets unmuted |
| WARNING           | A user receives a warning |

## Members

This category is for when someone leaves or joins the server.

| Name      | Emitted when     |
| --------- | ---------------- |
| USER_JOIN | Someone joins |
| USER_LEFT | Someone leaves |

## Messages

This category is for things having to do with messages.

| Name                | Emitted when     |
| ------------------- | ---------------- |
| CHANNEL_CLEAN       | A moderator cleans all the messages from a channel (which creates a file with the deleted messages) |
| MESSAGE_BULK_DELETE | A moderator bulk deletes a set of messages |
| MESSAGE_DELETE      | A message is deleted |
| MESSAGE_EDIT        | A user edits a message |
| MESSAGE_PIN_ADD     | A message gets pinned |
| MESSAGE_PIN_REMOVE  | A message gets unpinned |

## Debug

{% hint style="info" %}
This category is for debugging purposes. Logs in this category are meant to aid in fixing errors that may prevent the bot from functioning correctly.

{% endhint %}

| Name                | Emitted when     |
| ------------------- | ---------------- |
| REACTION_ROLE_DEBUG | A user triggers a reaction role, and something goes wtong |
