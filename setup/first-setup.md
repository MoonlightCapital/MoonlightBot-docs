# First setup

## Branches
Currently, MoonlightBot is offered in three different branches, each different from the other. Said branches are:

- Stable (teal icon). This version has been fully tested against errors and is suitable for public use
- Beta (orange icon). This version has been showing to perform well in tests, but it may be a bit unstable in some cases. You can geat early access to new features in Beta.
- Preview (black icon). This is a bleeding edge version: It's only used in private volunteer tests, and it gets updates the quickest.

## Inviting the bots
Currently, Stable and Beta have been shut down until enough progress is made on the bot rewrite, which is happening in Preview.
As for preview, it's currently meant to be semi-public. If you'd like early feature access, please [Contact the developers](https://discord.gg/8376ZVg).

The bots won't conflict each other if they're in the same server, but they're also out of sync, which means infractions, config files and user data do not carry over from one bot to another.

## Server configuration
**Note: this system may receive breaking changes in the future**

After inviting the bot of the branch of your choice, you can set the features you want for your server. To do so, you have to create a JSON file with all the server configuration data. The command to upload the file is:
`p:config upload`, and add your JSON file as Discord attachment. If the upload is successful, the changes made to the server config will be live instantly.

For more specific information on various config features, please refer to the other docs of this folder.
