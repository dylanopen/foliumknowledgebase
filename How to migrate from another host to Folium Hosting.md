
If you have previously hosted your server with another server hosting company, you can easily import all your files to your new Folium server.

## Method 1: using the Importer tab

Requirements:

- You still have your previous hosting plan active
- You have access to SFTP details from your old hosting company

Steps:
1. Find the SFTP details from your old server host. This should include a host name, port, username and password.
2. Stop your old server, as it could interfere with server files during the migration.
3. Log in to your Folium panel and choose the server you want to migrate **to**.
4. Go to the `Configuration -> Importer` tab.
5. Enter the SFTP details from step `1`. Make sure that the hostname does **not** contain a port (i.e. no colon and number at the end).
6. Click `Test` to make sure Folium can make the connection.
7. Once the `Import` button is no longer grayed-out, click it.
8. If your **new** server does not have any important information on it, selecting the `Wipe Server Files` option can help avoid file conflict issues.
9. Click on `Import` and wait for the transfer to complete.

> You won't be able to access any of the panel's features until the transfer is complete.

## Method 2: using SFTP with a local copy

This method is slower as it is dependent on your internet speed, but it will work with any host, even if you don't have access to an SFTP server.

Steps:
1. Download the server files from your old host, to your local computer. The easiest way to do this is usually to:
	1. Make a backup of your server.
	2. Download that backup (as an archive file).
	3. Extract that archive to a folder using tools such as 7-zip.
2. Launch an SFTP client such as [Filezilla](https://filezilla-project.org/) and connect to your Folium panel, using the SFTP details found in the `Environment -> Settings` tab.
3. Delete all files from your Folium server. **Make sure there is nothing important there first**.
4. Find the local folder of the server files, and go into this folder. You should see a list of all the files and folders from your old server - including a `server.jar` file, a `world` folder, `logs`, etc.
5. Select **all** of these files and folders instead of uploading the entire folder.
6. Once all files are selected, click the `Upload` button with your SFTP client. This may require right clicking on on of the files selected to find the upload button.
7. This can take some time, but once done, all your server files should be visible on your Folium panel and you should be able to start your server!

## Server software jar file

On some hosts, the default server software file may not be called `server.jar`. In that case you have two options:
- Rename your server software `jar` to `server.jar`.
- Change the `.jar` file that Folium starts in the `Environment -> Startup` tab.

### Renaming `server.jar`

To rename the server software file to `server.jar`, simply find the server software file in the `Files` tab, then right click the file or click the three dots next to the file. Finally, click `Rename` and type `server.jar` (case-sensitive) in the file name field.

### Changing the jar that Folium starts

1. Go to the `Environment -> Startup` tab.
2. Find the box titled `SERVER JAR FILE`.
3. Write the name of your server jar file in the field.

