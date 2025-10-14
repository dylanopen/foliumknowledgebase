
## What do the different difficulties do?

- **Peaceful** - no hostile mobs spawn, you do not lose hunger bars, faster regeneration, among other things.
- **Easy** - the next easiest difficulty, where mobs do spawn but deal less damage than in harder difficulties: you cannot die from hunger, among other things.
- **Normal** - a difficulty that is more difficult than easy, but less difficult than hard difficulty.
- **Hard** - the hardest difficulty (with the exception of hardcore mode) - 

## Method 1: the /difficulty command

Run this command in-game:

```
/difficulty <DIFFICULTY>
```

Or this command through console:

```
difficulty <DIFFICULTY>
```

Where `<DIFFICULTY>` is one of the following:

- `peaceful`
- `easy`
- `normal`
- `hard`

> Note that, while this method usually works, sometimes the difficulty can be reset after a server restart. If this happens, use `Method 2` or `Method 3` below.

## Method 2: using the Configs tab

1. Log in to your server panel and choose your server you want to edit.
2. Make sure your server is offline (stop it if it is running).
3. Go to the `Configuration -> Configs` tab.
4. Select `server.properties` from the file drop-down if it is not already selected.
5. Search for 'difficulty' in the search bar.
6. Change the field under `DIFFICULTY` to the option of your choice.
7. Click `Save Changes` and start your server. The max players should now be updated.

## Method 3: manually editing server.properties

1. Log in to your server panel and choose your server you want to edit.
2. Make sure your server is offline (stop it if it is running).
3. Go to the `Files` tab.
4. Open `server.properties`.
5. Find the field called `max-players`.
6. Change it from its default value of `20` to whatever you want the max players to be. It must be a positive whole number (integer).
7. Save the file and start the server. The maximum players should now be changed.
