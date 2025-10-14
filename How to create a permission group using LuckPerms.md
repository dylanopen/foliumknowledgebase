
A group in LuckPerms allows you to create a 'rank' or 'role' for **multiple players to have**. It avoids you having to manually manage the permissions for each individual player - just create a group and give each player that group.

## Creating a group

You can create a group using this command:

```text
/lp creategroup <groupName>
```

## Deleting a group

To delete a group, use:

```text
/lp deletegroup <group>
```

## List all groups

```text
/lp listgroups
```

## Adding a player to a group

```text
/lp user <player> parent add <group>
```

Note that we use `parent add` here instead of `parent set`: that's because you usually want to keep somebody's existing groups, but just add another. If you want to delete all groups from a player and just have the new one, use `parent set` instead.

## Group inheritance

If you want one group to take all permissions from another (and then possibly add some) run this command:

```text
/lp group <group> parent set <parentGroup>
```

For example, to make the `admin` group inherit from the `moderator` group:

```text
/lp group admin parent set moderator
```

> You should **always** inherit from at least one group (which itself will inherit from the `default` group). If a group doesn't have a logical parent, you should instead make it inherit from the `default` group.

## Setting group weight

Each group has a weight. When LuckPerms decides what permission it has, it will prioritise the permissions of higher-weighted groups.

For example, if the `moderator` group specifically _prevents access_ to the `/tp` command but the `admin` group allows it, if `admin` has a higher weight, then players with `admin` will have that permission, as `admin` takes priority over `moderator`.

You can set a group's weight like this:

```text
/lp group <group> setweight <weight>
```

... where `<weight>` is a number.

## LuckPerms group permissions

You can set permissions for either a group or an individual player.

Permissions determine which commands a player has access to. There are generally separate permissions for each command, giving you a lot of control over what commands they can access.

> Note: it's usually better to add permissions to groups rather than players, but if you only want to give a permission to a single person, you _can_ just use [player permissions](https://dylanopen.github.io/serverbook/luckperms/player-permissions.html)

> Note: to set a permission for all players, you should set permissions for the `default` group.

## Giving a permission to a group

To give a permission to a group, use this command:

```text
/lp group <group> permission set <permission> true
```

You don't actually need to add the `true` at the end, so this would also be fine:

```text
/lp group <group> permission set <permission>
```

For example, we could give permission to the `/tp` command to a group called `Moderator` like this:

```text
/lp group Moderator permission set minecraft.command.teleport true
```

## Removing a permission from a group

To remove a permission from a group, use this command:

```text
/lp group <group> permission unset <permission>
```

Using our example above, we can remove the teleport permission from `Moderator` like this:

```text
/lp group Moderator permission unset minecraft.command.teleport
```

## Explicit `false` permissions

Some commands are available to everyone by default, even if they are not an operator.

For example, the `/plugins` command is available to everyone by default on Bukkit servers, but you might not want this.

To explicitly block a command, use:

```text
/lp group <group> permission set <permission> false
```

For example, to block `Moderator` from using `/plugins`, you can use:

```text
/lp group Moderator permission set bukkit.command.plugins false
```

## Getting information about permissions

If you want to know what permissions a group has, use this command:

```text
/lp group <group> info
```

For example, to check all of `Moderator`'s permissions, type:

```text
/lp group Moderator info
```

## Setting permissions temporarily

You can set a permission for a group, but only for a certain amount of time, using this syntax:

```text
/lp group <group> permission settemp <permission> <true/false> <duration>
```

For example, to give `Moderator` permission to use the `/ban` command but _only for two days_:

```text
/lp group Moderator permission settemp minecraft.command.ban true 2d
```

Or, to prevent them from using the `/tell` command for 5 minutes:

```text
/lp group Moderator permission settemp minecraft.command.tell false 5m
```

## *Un*setting permissions temporarily

You can temporarily remove a permission for a group (for only a certain amount of time) using this syntax:

```text
/lp group <group> permission unsettemp <permission> <duration>
```

For example, to remove `Moderator`s' permission to use the `/ban` command but _only for two hours_:

```text
/lp group Moderator permission unsettemp minecraft.command.ban 2h
```
