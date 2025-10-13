
If you disable the nether dimension in your server, players can still build nether portals, but the nether portal animation will just play constantly without the player entering the nether.

## Method 1: using the Configs tab

1. Log in to your server panel and choose your server you want to edit.
2. Make sure your server is offline (stop it if it is running).
3. Go to the `Configuration -> Configs` tab.
4. Select `paper-global.yml` from the file drop-down if it is not already selected.
5. Search for 'nether' in the search bar.
6. Change the field under `ENABLE NETHER` to off (false).
7. Click `Save Changes` and start your server. The nether should now be disabled.

## Method 2: manually editing paper-global.yml

1. Log in to your server panel and choose your server you want to edit.
2. Make sure your server is offline (stop it if it is running).
3. Go to the `Files` tab.
4. Open `paper-global.yml`.
5. Find the field called `enable-nether`.
6. Change its value to `false`.
7. Save the file and start the server. The nether should now be disabled.
