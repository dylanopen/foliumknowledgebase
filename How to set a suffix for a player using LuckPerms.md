
LuckPerms allows you to manage suffixes for users. You can also
set suffixes for all users in a [group](./groups.md) - see the page for
[group suffixes](./group-suffix.md).

> Note: you will need a plugin such as
  [TAB](https://modrinth.com/plugin/tab-was-taken)
  in order to display suffixes in chat and tablist.

## Suffix priority

- Each suffix has a *weight*, or *priority* - players and groups can have
  multiple suffixes, and LuckPerms will use whatever suffix has the highest
  weight!

## Setting a suffix for a user

``` text
/lp user <player> meta setsuffix <weight> <suffix>
```

For example, to give the user `Minecraft123` the `[Builder]` suffix with a
weight of 40, you would use:

``` text
/lp user Minecraft123 meta setsuffix 40 " [Builder]"
```

The space before `[Builder]` is important here, as otherwise there would be no
gap between the username and the suffix.

## Removing a suffix from a player

To remove a suffix, you remove the suffixes at a specific weight:

``` text
/lp user <player> meta removesuffix <weight>
```

For example, to remove suffixes from `Minecraft123` with a weight (priority) of
`40`:

``` text
/lp user Minecraft123 meta removesuffix 40
```

## Setting a suffix temporarily

Just like how you can temporarily add a user to a group, you can also set a
temporary suffix:

``` text
/lp user <player> meta settempsuffix <weight> <suffix> <duration>
```

For example, to temporarily set the `[Helper] ` suffix for the `Minecraft123`
player at priority 60 for 3 days:

``` text
/lp user Minecraft123 meta settempsuffix 60 "[Helper] " 3d
```