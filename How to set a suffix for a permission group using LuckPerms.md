
LuckPerms allows you to manage prefixes and suffixes for groups. You can also
set suffixes for specific players - see this page for more info:
[player suffixes](./player-suffix.md).

> Note: you will need a plugin such as
  [TAB](https://modrinth.com/plugin/tab-was-taken)
  in order to display suffixes in chat and tablist.

## Suffix priority

- Each suffix and suffix has a *weight*, or *priority* - players and groups can
  have multiple suffixes and suffixes, and LuckPerms will use whatever suffix
  and suffix has the highest weight!

## Setting a suffix for a group

``` text
/lp group <group> meta setsuffix <weight> <suffix>
```

For example, to give the group `Moderator` the `[Mod]` suffix with a
weight of 40, you would use:

``` text
/lp group Moderator meta setsuffix 40 " [Mod]"
```

The space after `[Mod]` is important here, as otherwise there would be no
gap between the suffix and the main name.

## Removing a suffix from a group

To remove a suffix, you remove the suffixes at a specific weight:

``` text
/lp group <group> meta removesuffix <weight>
```

For example, to remove suffixes from `Moderator` with a weight (priority) of
`40`:

``` text
/lp group Moderator meta removesuffix 40
```

## Setting a suffix temporarily

Just like how you can temporarily add a group to a group, you can also set a
temporary suffix:

``` text
/lp group <group> meta settempsuffix <weight> <suffix> <duration>
```

For example, to temporarily set the ` [Moderator]` suffix for the `Moderator`
group at priority 60 for 3 days:

``` text
/lp group Moderator meta settempsuffix 60 " [Moderator]" 3d
```