
This guide should help you decide which server software to choose when starting your own server.

## I care about preserving vanilla mechanics

If your players are technical players, or you just want more vanilla mechanics, you should install the `Fabric` server software and add [optimisation mods](https://gist.github.com/Obydux/55b967f5dcc00633fe895e5a473363d5).

## I want to run a modpack

Usually, you don't have a choice. Most modpacks are built for a specific server software.

If you have a choice, you should always choose to run a Fabric server over a Forge server.

## I want a server software with lots of ready-made admin tools

You should use a server software with support for **Bukkit plugins**. The most popular choice is [PaperMC](https://papermc.io).

Paper has thousands of community-made plugins which will make managing your Minecraft server much easier.

## I want the most optimised server software for small-medium player counts

Take a look at [Purpur](https://purpurmc.org). It's a drop-in replacement for Paper and adds lots of optimisation options.

You could also try LeafMC, though it will be much less stable and may break some game mechanics.

## I run a very large server where players are spread out

You could try [Folia](https://papermc.io/software/folia). It multithreads the game by splitting up the world into regions, which it runs in parallel.

You should be prepared to code some custom plugins if you decide to use Folia - there is a much smaller range of plugins which have Folia support compared to support for Paper or Purpur.
