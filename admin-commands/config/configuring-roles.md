# Configuring roles

To start configuring a role, enter its name, mention or ID.

{% hint style="info" %}
To edit the role, you must have an higher role than that, and it must have a lower level than yours. The server owner can edit any role.
{% endhint %}

| Name                   | Description                                                                                                                         | Type     | Default | Notes                                                                                                            |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | -------- | ------- | ---------------------------------------------------------------------------------------------------------------- |
| Level                  | The level of the role                                                                                                               | Number   | 0       | Must be between 0 and 100 (included). Must also be lower than your level                                         |
| SelfAssignable         | Whether users can assign themselves this role with the `selfrole` command                                                           | Boolean  | false   |                                                                                                                  |
| SelfAssignableDuration | Determines the duration of the selfrole                                                                                             | Duration | 0       | Optional; selfAssignable must be true for this to work. If this is set to 0, the role won't expire automatically |
| SelfAssignableMaxTimes | Determines how many times a single user can assign themselves this role (this includes both `selfrole` command and reaction roles)  | Number   | 0       | Can be between 0 and 100. If set to 0, there will be no limit                                                    |
| JoinAssignable         | Whether this role is added to an user when they join the server                                                                     | Boolean  | false   |                                                                                                                  |
| JoinAssignableDuration | Determines how long will the role be removed after it's added on join                                                               | Duration | 0       | Optional; joinAssignable must be true for this to work. If this is set to 0, the role won't expire automatically |
| Persistent             | Whether this role will be added again if an user who precedently had it left and rejoined the server                                | Boolean  | false   |                                                                                                                  |
