
LuckPerms allows you to manage prefixes and suffixes for users. You can also
set prefixes for all users in a [group](./groups.md) - see the page for
[group prefixes and suffixes](./group-prefix.md).

> Note: you will need a plugin such as
  [TAB](https://modrinth.com/plugin/tab-was-taken)
  in order to display prefixes in chat and tablist.

## Prefix priority

- Each prefix and suffix has a *weight*, or *priority* - players and groups can
  have multiple prefixes and suffixes, and LuckPerms will use whatever prefix
  and suffix has the highest weight!

## Setting a prefix for a user

``` text
/lp user <player> meta setprefix <weight> <prefix>
```

For example, to give the user `Minecraft123` the `[Builder]` prefix with a
weight of 40, you would use:

``` text
/lp user Minecraft123 meta setprefix 40 "[Builder] "
```

The space after `[Builder]` is important here, as otherwise there would be no
gap between the prefix and the main name.

## Removing a prefix from a player

To remove a prefix, you remove the prefixes at a specific weight:

``` text
/lp user <player> meta removeprefix <weight>
```

For example, to remove prefixes from `Minecraft123` with a weight (priority) of
`40`:

``` text
/lp user Minecraft123 meta removeprefix 40
```

## Setting a prefix temporarily

Just like how you can temporarily add a user to a group, you can also set a
temporary prefix:

``` text
/lp user <player> meta settempprefix <weight> <prefix> <duration>
```

For example, to temporarily set the `[Helper] ` prefix for the `Minecraft123`
player at priority 60 for 3 days:

``` text
/lp user Minecraft123 meta settempprefix 60 "[Helper] " 3d
```