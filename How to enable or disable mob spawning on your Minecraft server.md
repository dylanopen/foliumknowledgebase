
The `spawn-monsters` field in `server.properties` determines whether mobs can spawn on your server.

> This can also be configured in-game using the `/gamerule` command. With gamerules, you also can separate some mobs from this - for example, disable only phantoms with the `doInsomnia` gamerule.

## Method 1: using the `Config` tab

1. Stop your server if it is not already offline.
2. Go to the `Configuration -> Configs` tab.
3. Select `server.properties` from the file dropdown by the search bar.
4. Find or search for the `monsters` config option.
5. Change the value from its default `true` to `false`.
6. Click the blue `Save` button at the top right.
7. Start your server.

## Method 2: editing `server.properties`

This method does exactly the same thing, but more directly.

1. Stop your server if it isn't already stopped.
2. Go to the `Files` tab.
3. Click on the `server.properties` file.
4. Find the `spawn-monsters=true` line, and change it to `spawn-monsters=false`.
5. Click the `SAVE CONTENT` button to save your file.
6. Start your server.

## Method 3: using a gamerule

This is the recommended way of disabling mob spawning.

### Toggle general mob spawning

Run either of these commands in-game (if running through console, do not add the leading `/`):

```
/gamerule doMobSpawning false
/gamerule doMobSpawning true
```

### Toggle phantom spawning

Run either of these commands in-game (if running through console, do not add the leading `/`):

```
/gamerule doInsomnia false
/gamerule doInsomnia true
```

### Toggle pillager patrol spawning

Run either of these commands in-game (if running through console, do not add the leading `/`):

```
/gamerule doPatrolSpawning false
/gamerule doPatrolSpawning true
```
