# role

This command allows you to assign or remove a role from a user.

## Required permissions

MoonlightBot requires the following permissions to successfully execute this command:

* Manage Roles

By default, a user is required to have the following permissions to use this command:

* Manage Roles

For more information on editing permission requirements for specific users/roles, refer to
the [permissions tutorial](<linkToPermissionsTutorial>)

## Syntax

```text
/role <user> <role> [reason]
```

### Options

* `user`: The user to assign/remove the role to/from. You can mention the user or use their ID to specify the user.
* `role`: The role to assign/remove from the user. You can mention the role or use its ID to specify the role.
* `reason`: The reason for assigning/removing the role from the user. This is an optional parameter, which can be used
  for moderation.

## Logs

* `ROLE_ADD`: This log is triggered when a role is assigned to a user.
  It will log the user, the role, the responsible moderator, and the reason for the role assignment.
* `ROLE_REMOVE`: This log is triggered when a role is removed from a user.
  It will log the user, the role, the responsible moderator, and the reason for the role removal.

For more information on setting up those logs, refer to the [log setup tutorial](<linkToLogTutorial>)