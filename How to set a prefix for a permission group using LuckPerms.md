# Group prefixes

LuckPerms allows you to manage prefixes and suffixes for groups. You can also
set prefixes for specific players - see this page for more info:
[player prefixes](./player-prefix.md).

> Note: you will need a plugin such as
  [TAB](https://modrinth.com/plugin/tab-was-taken)
  in order to display prefixes in chat and tablist.

## Prefix priority

- Each prefix and suffix has a *weight*, or *priority* - groups and groups can
  have multiple prefixes and suffixes, and LuckPerms will use whatever prefix
  and suffix has the highest weight!

## Setting a prefix for a group

``` text
/lp group <group> meta setprefix <weight> <prefix>
```

For example, to give the group `Moderator` the `[Mod]` prefix with a
weight of 40, you would use:

``` text
/lp group Moderator meta setprefix 40 "[Mod] "
```

The space after `[Mod]` is important here, as otherwise there would be no
gap between the prefix and the main name.

## Removing a prefix from a group

To remove a prefix, you remove the prefixes at a specific weight:

``` text
/lp group <group> meta removeprefix <weight>
```

For example, to remove prefixes from `Moderator` with a weight (priority) of
`40`:

``` text
/lp group Moderator meta removeprefix 40
```

## Setting a prefix temporarily

Just like how you can temporarily add a group to a group, you can also set a
temporary prefix:

``` text
/lp group <group> meta settempprefix <weight> <prefix> <duration>
```

For example, to temporarily set the `[Moderator] ` prefix for the `Moderator`
group at priority 60 for 3 days:

``` text
/lp group Moderator meta settempprefix 60 "[Moderator] " 3d
```