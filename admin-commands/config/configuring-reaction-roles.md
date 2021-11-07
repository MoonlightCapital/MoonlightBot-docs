# Configuring reaction roles

To start configuring reaction roles, enter a group name.

{% hint style="info" %}
You must have already created a group before editing its settings. Please refer to [Setting up reaction roles](../../start-up/setting-up-reaction-roles.md) for a guide.
{% endhint %}

| Name           | Description                                                             | Type     | Default | Notes                                                                                                                             |
| -------------- | ----------------------------------------------------------------------- | -------- | ------- | --------------------------------------------------------------------------------------------------------------------------------- |
| JoinOnly       | If set, this only allows users to join roles but not leave them         | Boolean  | false   | If this and leaveOnly are set, both will take effect. If you don't want roles to be assigned, consider freezing the group instead |
| LeaveOnly      | If set, this only allows users to leave roles but not join them         | Boolean  | false   | If this and joinOnly are set, both will take effect. If you don't want roles to be assigned, consider freezing the group instead  |
| Reverse        | Inverts the actions performed when the reaction is added/removed        | Boolean  | False   | Available on version `2.17.0` onwards                                                                                             |
| MaxRoles       | The maximum amount of roles from an user can have simultaneously        | Number   | 0       | If set to 0, no limit will be enforced                                                                                            |
| DmNotification | Whether to send notifications through direct messages to users          | Boolean  | true    | An user can turn this off for themselves with the `userconfig` command                                                            |
| Freeze         | "freezes" the group, meaning users will not be able to interact with it | Boolean  | false   | Attempts to use this group will still be logged in the debug log                                                                  |
| Duration       | Duration for the roles, starts when it's joined                         | Duration | 0       | If set to 0, no timer will be created                                                                                             |
