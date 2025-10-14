
Using LuckPerms, you can set permissions for either a group or an individual player.

Permissions determine which commands a player has access to. There are generally separate permissions for each command, giving you a lot of control over what commands they can access.

> Note: it's usually better to add permissions to groups rather than players, but if you only want to give a permission to a single person, you _can_ just use player permissions.

## Adding a player to a group

```text
/lp user <player> parent add <group>
```

Note that we use `parent add` here instead of `parent set`: that's because you usually want to keep somebody's existing groups, but just add another. If you want to delete all groups from a player and just have the new one, use `parent set` instead.

## Adding a permission to a player

To add a permission from a player, use this command:

```text
/lp user <player> permission set <permission> true
```

Luckperms will infer you want to set the permission to `true`, so you don't have to type the true:

```
/lp user <player> permission set <permission>
```

Using our example above, we can give the teleport permission to user `Minecraft123` like this:

```text
/lp user Minecraft123 permission set minecraft.command.teleport
```

## Removing a permission from a player

To remove a permission from a player, use this command:

```text
/lp user <player> permission unset <permission>
```

Using our example above, we can remove the teleport permission from `Minecraft123` like this:

```text
/lp user Minecraft123 permission unset minecraft.command.teleport
```

## Explicit false player permissions

Some commands are available to everyone by default, even if they are not an operator. Or, you may wish to have a group which prevents access to a command that another group gives the player.

For example, the `/plugins` command is available to everyone by default on Bukkit servers, but you might not want this.

To explicitly block a command, use:

```text
/lp user <player> permission set <permission> false
```

For example, to block `Minecraft123` from using `/plugins`, you can use:

```text
/lp user Minecraft123 permission set bukkit.command.plugins false
```

## Querying player permissions

If you want to know what permissions a player has, use this command:

```text
/lp user <player> info
```

For example, to check all of `Minecraft123`'s permissions, type:

```text
/lp user Minecraft123 info
```

## Adding temporary permissions

You can set a permission for a player, but only for a certain amount of time, using this syntax:

```text
/lp user <player> permission settemp <permission> <true/false> <duration>
```

For example, to give `Minecraft123` permission to use the `/ban` command but _only for two days_:

```text
/lp user Minecraft123 permission settemp minecraft.command.ban true 2d
```

Or, to prevent them from using the `/tell` command for 5 minutes:

```text
/lp user Minecraft123 permission settemp minecraft.command.tell false 5m
```

## Removing permissions temporarily

You can temporarily remove a permission for a player (for only a certain amount of time) using this syntax:

```text
/lp user <player> permission unsettemp <permission> <duration>
```

For example, to remove `Minecraft123`'s permission to use the `/ban` command but _only for two hours_:

```text
/lp user Minecraft123 permission unsettemp minecraft.command.ban 2h
```
