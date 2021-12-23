# Create-muterole

### **Description**

This command is used to create a mute role and setup channel permissions. This can be either a new role, or an existing role if provided as argument.

### **Required arguments**

None

### **Optional arguments**

An existing role name can be specified to apply permissions to. If none is specified, a new role is created for this purpose.

### **Usage**

```
/create-muterole [role]
```

### **Required permissions**

This command's level is 100 by default.\
The bot needs **Read Messages, Send Messages, Manage Roles** permissions in order to be able to execute this command. It additionally requires permission to **Read Messages** and **Manage Permissions** in the channels where you want the mute to be effective in.
