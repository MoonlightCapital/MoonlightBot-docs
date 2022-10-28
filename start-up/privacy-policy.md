# Privacy policy

This policy sums up all you need to know about what Discord data we store, what we use it for, and how to deal with it.

## Stored in a database

* Discord user IDs: they are used to indicate infraction moderators, targets (for infractions, reminders and tempmutes/temproles/tempbans), as well as for user settings and persistencies.
* Discord server IDs: to index configuration of servers, and to operate in servers themselves (such as knowing which server a temporary action, persistency or infraction belongs to).
* Discord channel IDs: server configuration.
* Discord role IDs: server configuration, handling temporary roles/mutes, and persistencies.
* Parts of message contents: those are always provided by the user, and are used for reminder contents and infractions reasons, as well occasionally for configuration (such as log names).

The database is hosted in a VPS residing in the United Kingdom.

## Stored in cache

The Discord.js library automatically caches many things that come from Discord directly, they can range from avatars to message contents, to meta parameters such as role colors, names, user tags, user flags (badges). Most of this content is used to provide logs or command output, and is deleted on bot shutdown, as it is put into a volatile storage.

## Message content

MoonlightBot is approved for the "message content privileged intent", which means it **can see the content of messages you send**. Message contents are only stored in the cache for a brief period of time, and are used to provide message deletion and edit logs. If you are a server administrator and wish to opt-out a channel from being logged, please disable the bot's permission to read messages in such channel.

## Stored in Discord

Output of bot commands that is sent to Discord may include things like names, IDs and icons/avatars. Those things cannot be deleted by us as there's no feasible way to do so. This also includes server mod logs that belong to the service the bot provides, which will not be deleted by us.

Official MoonlightBot Staff and helpers have access to bot logs. Those are sent in a private and strictly controlled Discord server. Logs are used to combat abuse, as well as for analytics and resizing the service according to the user's choices.

## Requesting data deletion

To request deletion of your data, please contact the Staff at the support server. If you are banned from the server and still want to use your right to deletion, you can instead DM a Staff member through friend requests or mutual servers. Your data is ensured to be deleted within 14 days from your request.

### Data security

To ensure no data is unintentionally lost, the Staff will have to verify a few things, such as:

* The owner of a server may request deletion of infractions, temporary actions, configuration and persistency of their own server(s).
* Any user may request deletion of infractions of which they were the responsible moderator of, their reminders and personal user settings (except limitations imposed by the MoonlightBot Staff).
* You may not request deletion of persistencies, infractions or other technical service things that target you, unless consent from server owner is given.

{% hint style="info" %}
Bot logs will not be deleted, as they are necessary to keep the service healthy.

Sometimes data from the database is cleaned, this usually relates to unnecessary data (such as config and other things related to the server itself) for merely technical reasons. If you disagree, please inform the Staff promptly.

The MoonlightBot Staff deserves the right to modify or delete any data stored at any given time, without notice or warning.
{% endhint %}

## TL;DR

1. Once you start using the bot, we will store some data related to you or to your server, to provide the service as you expected.
2. Bot Staff can see which commands you use and where. Those are used to make the bot better, fight abuse and help tracking bugs back.
3. We will not store data unless you consent to. You consent by using a command, or by adding the bot to a server.
4. You cannot get unblacklisted from the bot by requesting deletion of your blacklisted status. Period. This is considered crucial information.
5. We do NOT sell your data to anyone. We may show samples of aggregate and anonymized data to third parties to ask for advice.
6. If you stop using the bot, most of your data will be automatically deleted after a while in an irreversible way. You can also delete it by request to Staff.
7. Bot logs and messages sent by the bot to Discord cannot be deleted by us. This is also to provide the service fairly to the servers who need it.
8. Don't do anything that violates the Acceptable Use Policy. Especially, don't use the bot's anonymous infraction notification system to harass, advertise or do anything that violates Discord's policies. **We will disclose abusers Discord user ID to their victims, after the appeal period described in the AUP has passed.**
9. If you have any concerns about the data we store, contact the Staff.
