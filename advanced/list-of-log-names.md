---
description: In this page all the available logs are listed
---

# List of log names

## Categories

{% hint style="warning" %}
Log names are **case sensitive**. Individual logs are written in _UPPER\_CASE_, while category names are _Capitalized_
{% endhint %}

{% hint style="info" %}
If you want everything to be logged, use `*` as name. This will also include logs that will be introduced **after** you set it.
{% endhint %}

### Moderation

| Type               | Description                                               |
| ------------------ | --------------------------------------------------------- |
| BAN                | Emitted when an user is banned                            |
| UNBAN              | Emitted when an user is unbanned                          |
| MUTE               | Emitted when an user is muted                             |
| UNMUTE             | Emitted when an user is unmuted                           |
| KICK               | Emitted when an user is kicked                            |
| WARNING            | Emitted when an user is warned                            |
| SOFTBAN            | Emitted when an user is softbanned                        |
| TEMPBAN\_ADD       | Emitted when an user is tempbanned                        |
| TEMPMUTE\_ADD      | Emitted when an user is tempmuted                         |
| TEMPROLE\_ADD      | Emitted when a temprole is added to an user               |
| REASON\_UPDATE     | Emitted when the reason of an infraction is changed       |
| TEMPROLE\_EXTEND   | Emitted when a temprole is extended                       |
| TEMPMUTE\_EXTEND   | Emitted when a tempmute is extended                       |
| TEMPBAN\_EXTEND    | Emitted when a tempban is extended                        |
| TEMPROLE\_REMOVE   | Emitted when a temprole is removed/has expired            |
| TEMPMUTE\_REMOVE   | Emitted when a tempmute is removed/has expired            |
| TEMPBAN\_REMOVE    | Emitted when a tempban is removed/has expired             |
| AUDIT\_KICK        | Emitted when a user is kicked but not by the bot          |
| AUDIT\_BAN\_ADD    | Emitted when a user is banned, but not by the bot         |
| ROLE\_ADD          | Emitted when a role is added through the `role` command   |
| ROLE\_REMOVE       | Emitted when a role is removed through the `role` command |
| SELFROLE\_ADD      | Emitted when a selfrole is added                          |
| SELFROLE\_REMOVE   | Emitted when a selfrole is removed                        |
| RAID\_CLEANUP      | Emitted when a raid is cleaned up                         |
| INFRACTION\_DELETE | Emitted when an infraction is deleted                     |

### Messages

| Type                 | Description                               |
| -------------------- | ----------------------------------------- |
| CHANNEL\_CLEAN       | Emitted when a channel is cleaned         |
| MESSAGE\_DELETE      | Emitted when a message is deleted         |
| MESSAGE\_EDIT        | Emitted when a message is edited          |
| MESSAGE\_PIN\_ADD    | Emitted when a message is pinned          |
| MESSAGE\_PIN\_REMOVE | Emitted when a pinned message is unpinned |

### Members

| Type       | Description                            |
| ---------- | -------------------------------------- |
| USER\_JOIN | Emitted when an user joins the server  |
| USER\_LEFT | Emitted when an user leaves the server |

### Debug

{% hint style="info" %}
This category is for debugging purposes. Logs in this category are meant to aid in fixing errors that may prevent the bot for functioning correctly
{% endhint %}

| Type                    | Description                              |
| ----------------------- | ---------------------------------------- |
| REACTION\_ROLE_\__DEBUG | Debug for reaction roles related actions |
