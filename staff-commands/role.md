# Role

### **Description**

This command is used to add a role to an user. If they already have the role, it will be removed.

If the user specified in the command is not in the server, a persistency will be created so that the role is added as soon as they join. Using this command again will remove the role from their persistency.

### **Required arguments**

* `user` - The user you want to toggle the role from
* `role` - The role you want to toggle from the user

### **Usage**

```
m:role <user> <role>
/role <user> <role>
```

### **Aliases**

None

### **Required permission**

This command's level is 50 by default.\
The bot needs **Read Messages, Send Messages **permissions in order to be able to execute this command.
