
The `simulation-distance` of your server determines the radius of chunks around each player that 'tick'.

Increasing this will exponentially increase the number of chunks that tick, which will greatly increase your `MSPT` and possibly decrease your `TPS`, causing server lag.

> The default `simulation-distance` on Paper servers is set to `10`. You probably don't need to go higher than this.

## Method 1: using the `Config` tab

1. Stop your server if it is not already offline.
2. Go to the `Configuration -> Configs` tab.
3. Select `server.properties` from the file dropdown by the search bar.
4. Find or search for the `simulation` config option.
5. Change the value from its default `10` to the value you have chosen (see the `Recommended simulation distance` section below).
6. Click the blue `Save` button at the top right.
7. Start your server.

## Method 2: editing `server.properties`

This method does exactly the same thing, but more directly.

1. Stop your server if it isn't already stopped.
2. Go to the `Files` tab.
3. Click on the `server.properties` file.
4. Find the `simulation-distance=10` line, and change it to your simulation distance of choice (see the `recommended simulation distance` section below).
5. Click the `SAVE CONTENT` button to save your file.
6. Start your server.

## Recommended simulation distance

The simulation distance you choose will be greatly affected by:
- the number of players on your server
- how well optimised your server is
- how important having a high simulation distance is (e.g. are your players technical players who like to build farms that rely on 10-12 simulation distance?)

If you are just playing your server with a few friends, you can probably set the simulation distance to whatever you think is necessary, but for a larger server, you should use a lower simulation distance.
