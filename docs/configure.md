# Configuring MoonlightBot

?> This guide assumes you're using the standard MoonlightBot. If you're using another version, change the prefix accordingly

You can change every bit of MoonlightBot's configuration with the `m:set` command. Here's a detailed guide on how to use it.

## Editing a role

`m:set role <role ID> <option> [...data]`

### Available options

  #### level
  Assigns the level of the role. It must be a number between 0 and the user's power level.

  Usage: `m:set role <role ID> level <level>`

  #### selfAssignable
  Sets if the role can be assigned by users to themselves. If the role is already set to self-assignable, it will not be self-assignable anymore.

  Usage: `m:set role <role ID> selfAssignable`

  #### selfAssignableDuration
  If a role is self-assignable, you can set a timer for the role to be automatically removed.

  Usage: `m:set role <role ID> selfAssignableDuration <timer>`
