---
description: On this page all the available logs are listed
---

# List of log names

Logs, categorized by what they do are listed here, and are **case sensitive**. Individual logs are written in _UPPER\_CASE_, while category names(which can be used in place of individual log names, see [configuring channels](../admin-commands/config/configuring-channels.md)) are _Capitalized_. Each one of them is separated by categories in the lists below. If you want to log everything, use an asterisk to include all things that can be logged, including ones that will be introduced in future updates.

{% hint style="warning" %}
Some logs require the bot to have the "View Audit Logs" permission enabled.
{% endhint %}

## Moderation

This category is used for actions by moderators or ones that moderators could use. Most of them are fired when a command is run unless they start with AUDIT_. In that case, actions that are done with or without using the bot are logged.

| Name              | Emitted when     |
| ----------------- | ---------------- |
| BAN               | Someone gets banned |
| INFRACTION_DELETE | Someone removes an infraction|
| KICK              | Someone gets kicked |
| MUTE              | Someone gets muted |
| PAUSE_ROLE_ADD    | An expiring role gets added  |
| PAUSE_ROLE_EXTEND | A role expiration date gets extended |
| PAUSE_ROLE_REMOVE | A role gets temporarily removed |
| REASON_UPDATE     | A reason for an infraction gets updated |
| ROLE_ADD          | Someone adds a role |
| ROLE_REMOVE       | Someone removes a role|
| SELFROLE_ADD      | Someone adds a user-assignable role |
| SELFROLE_REMOVE   | Someone removes a user-assignable role  |
| SOFTBAN           | Someone gets soft-banned |
| TEMPBAN_EXTEND    | Someone's temporary ban gets extended |
| TEMPBAN_REMOVE    | Someone's temporary ban gets removed |
| TEMPMUTE_EXTEND   | Someone's temporary mute gets extended |
| TEMPMUTE_REMOVE   | Someone's temporary ban gets removed |
| TEMPROLE_ADD      | A temporary role gets added |
| TEMPROLE_EXTEND   | The length of a temporary role gets extended |
| TEMPROLE_REMOVE   | A temporary role gets removed |
| TIMEOUT           | Someone gets timed out |
| TIMEOUT_REMOVE    | Someone's time out gets removed |
| UNBAN             | Someone gets unbanned |
| UNMUTE            | Someone gets unmuted |
| WARNING           | Someone receives a warning |

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
| CHANNEL_CLEAN       | Someone cleans all the messages from a channel |
| MESSAGE_BULK_DELETE | Someone bulk deletes a set of messages |
| MESSAGE_DELETE      | Anyone deletes a message |
| MESSAGE_EDIT        | Anyone edits a message |
| MESSAGE_PIN_ADD     | A message gets pinned |
| MESSAGE_PIN_REMOVE  | A message gets unpinned |

## Debug

{% hint style="info" %}
This category is for debugging purposes. Logs in this category are meant to aid in fixing errors that may prevent the bot from functioning correctly.

{% endhint %}

| Name                | Emitted when     |
| ------------------- | ---------------- |
| REACTION_ROLE_DEBUG | Someone uses a reaction role |
