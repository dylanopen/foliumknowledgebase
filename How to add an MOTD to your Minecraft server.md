
If you would like to change your server's MOTD (message of the day) from the default of `A Minecraft Server`, you can do that in two ways.

## Method 1: through the Configs tab

1. Log in to your server panel and choose your server you want to edit.
2. Make sure your server is offline (stop it if it is running).
3. Go to the `Configuration -> Configs` tab.
4. Select `server.properties` from the file drop-down if it is not already selected.
5. Search for 'motd' in the search bar.
6. Change the field under `MOTD` to whatever you would like.
7. Click `Save Changes` and start your server. The MOTD should now be changed.

## Method 2: directly editing server.properties

8. Log in to your server panel and choose your server you want to edit.
9. Make sure your server is offline (stop it if it is running).
10. Go to the `Files` tab.
11. Open `server.properties`.
12. Find the field called `motd`.
13. Change it from its default value of `A Minecraft Server` to whatever you want the MOTD to be.
14. Save the file and start the server. The MOTD should now be changed.

## Proxy servers and MOTD plugins

Proxy servers and some plugins which alter the MOTD provide their own way of changing the MOTD. This is not currently covered in this article.

## Styled MOTDs using the built-in MOTD creator

Folium provides a useful tool to generate styled MOTDs, including colors, bold text, and more.

You can find it under `Minecraft -> Utilities -> Server Customization -> MOTD Creator`. When you have finished editing, copy and paste the text from the field titled `FOR SERVER.PROPERTIES`, and paste it into your configuration using one of the two methods above.
