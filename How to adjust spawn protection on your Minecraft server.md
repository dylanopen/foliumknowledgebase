
The spawn protection radius is the radius of the area around spawn that players cannot break or place blocks or interact with the world in any way. You may notice this when trying to break blocks nearby spawn: the block will regenerate and not drop.

Players with operator permissions (through the `/op` command) can bypass spawn protection limitations.

## Method 1: using the Configs tab

1. Log in to your server panel and choose your server you want to edit.
2. Make sure your server is offline (stop it if it is running).
3. Go to the `Configuration -> Configs` tab.
4. Select `server.properties` from the file drop-down if it is not already selected.
5. Search for 'spawn' in the search bar.
6. Change the field under `SPAWN PROTECTION` to any integer value you like.
7. Click `Save Changes` and start your server. The spawn protection radius should now be changed.

## Method 2: manually editing server.properties

1. Log in to your server panel and choose your server you want to edit.
2. Make sure your server is offline (stop it if it is running).
3. Go to the `Files` tab.
4. Open `server.properties`.
5. Find the field called `spawn-protection`.
6. Change it from its default value of `16` to whatever you want the spawn radius to be. It must be a whole number (integer).
7. Save the file and start the server. The spawn protection radius should now be changed.

## Disabling spawn protection

While it isn't technically possible to completely disable spawn protection, you can make it have a single block radius which effectively disables it.

To do that, set the `spawn-protection` field in `server.properties` (using either method described above) to `0`.
