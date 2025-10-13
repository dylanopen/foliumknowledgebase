
The `view-distance` of your server determines the maximum render distance players can use. It is a **limit** to how high players can set their render distance while on your server.

## Method 1: using the `Config` tab

1. Stop your server if it is not already offline.
2. Go to the `Configuration -> Configs` tab.
3. Select `server.properties` from the file dropdown by the search bar.
4. Find or search for the `view` config option.
5. Change the value from its default `10` to the value you have chosen (see the `Recommended view distance` section below).
6. Click the blue `Save` button at the top right.
7. Start your server.

## Method 2: editing `server.properties`

This method does exactly the same thing, but more directly.

1. Stop your server if it isn't already stopped.
2. Go to the `Files` tab.
3. Click on the `server.properties` file.
4. Find the `view-distance=10` line, and change it to your view distance of choice (see the `recommended view distance` section below).
5. Click the `SAVE CONTENT` button to save your file.
6. Start your server.

## Recommended view distance

The view distance you choose will be greatly affected by:
- the number of players on your server
- your server's plan (how much RAM you have)
- how important having a high view distance is to you and your players

Having a high view distance does not usually affect your server's `TPS` and `MSPT` (see [What is TPS on my Minecraft server?](https://billing/foliumhosting.net/knowledgebase/PLEASE/INSERT/LINK/HERE)). However, it **does** increase the RAM usage of your server.

An SMP-style server with a view distance of `24`, for example, will generally use around `1GB` of RAM per player, while the same server with a view distance of just `10` may only use around `200MB` of RAM per player (5x less).

If you have a server plan of 8GB or more and are just playing your server with a few friends, you can increase the render distance to whatever you think is necessary, but for a larger server or if you have less RAM allocated to your server, you should use a lower view distance.
