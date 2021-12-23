# Infractions

### **Description**

This command is used to manage infractions, both show and delete them. It is broken down into multiple Slash Commands, all of which begin with `/infractions `

### **Subcommands**

#### **Summary**

Shows a brief list of infractions an user has, grouped by type. The only required argument is the user you want information on.

#### Detailed

Shows detailed information on a specific infraction. The only required argument is the infraction ID.

#### Archive

DMs you a file containing a list of infractions of the server. The only required argument is the format of the file (see below for a list of formats).

#### Delete

Deletes an infraction. The only required argument is the infraction ID. An optional reason for deleting the infraction can be put afterwards, and will be reflected in the log.

{% hint style="info" %}
Only the responsible moderator can delete their infraction. The server owner can delete any infraction on their server.
{% endhint %}

#### List

This option shows a list of infraction, provided certain parameters to restrict the search.

The arguments are to be put in a `filter:value` mode. Multiple filters can be used together, and must be chained with a `;`. If multiple filters are provided, they will be chained with a logical AND.

Valid filters are: `user`, `moderator`, `type`, `reason`, `partialreason`.

So for example, an execution like this:

```
/infractions list user:314110696071888896;type:warning
```

Will list all infractions issued to the user `314110696071888896` and of type `warning`.

If the output is too long, it will be sent as file, pretty much like the `archive` option. You can specify the format as specified below in the flags.

{% hint style="info" %}
User and moderator options only support user IDs. You risk of getting no results otherwise.
{% endhint %}

#### Search

This is pretty much like `list`, but you can get even higher precision and without filters. You can freely input anything. Check [here](https://fusejs.io/examples.html#extended-search) to see how special characters affect your search.

### Options

* `format=<format>` Selects the format for the `list` and `archive` options. Replace `<format>` with your desired format.

### **Usage**

```
/infractions summary <user>

/infractions list <query> [case-insensitive] [format]

/infractions search <query> [format]

/infractions detailed <id>

/infractions archive [format]

/infractions delete <id> [...reason]
```

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages, Embed Links, Attach Files** permissions in order to be able to execute this command.

### List of available export formats

`txt`, `csv`, `json`, `html`
