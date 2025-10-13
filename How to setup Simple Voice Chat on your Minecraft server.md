
## Video guide

https://youtu.be/w9khzbE-m7s

## Installing the plugin or mod

1. Go to the `Minecraft -> Plugins` or `Minecraft -> Mods` tab on your server, depending on if you run a modded or plugin-based server software.
2. Search for `Simple Voice Chat`. It should be one of the top results.
3. Install the version that corresponds to your server version. This is not necessarily the pre-selected version.
4. Start / restart your server to generate the required configuration.

## Allocating a port

1. Go to the `Network -> Ports` tab.
2. Click the `Create Allocation` button.
3. Copy the port number it just created.

## Configuring voice chat

1. Open the `voicechat-server.properties` file. This is either in the `plugins/voicechat` folder or the `config/voicechat` folder, depending on whether you installed the plugin or modded version of Simple Voice Chat.
2. Change the `port=24454` line to be `port=PORTNUM`, where `PORTNUM` is the port number you copied in the last stage.
3. Change any other configuration settings you want to.
4. Save the file.
5. Restart your server and Simple Voice Chat should be working! Make sure to install the client-side mod if you haven't already.

## Permissions

If you are using a plugin like Luckperms, you may need to give permission for your players to use Simple Voice Chat.

You need to give the `default` group these permissions:
- `voicechat.listen`
- `voicechat.speak`
- `voicechat.groups`

In luckperms, you would run these three commands:

```
/lp group default permission set voicechat.listen
/lp group default permission set voicechat.speak
/lp group default permission set voicechat.groups
```
