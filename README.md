# ACC_RemoteServer_GUI

## Content
[Install](#install)
[Issues](#issues)
[UserGuide](#guide)
[TODO](#todo)

<picture>
  <center>
  <source media="(prefers-color-scheme: dark)" srcset="img/Screenshot%202023-12-18%20113509.png">
  <source media="(prefers-color-scheme: light)" srcset="img/Screenshot%202023-12-18%20113509.png">
  <img alt="ACC RSGUI ScreenShot">
  </center>
</picture>

ACC RSGUI (ACC Remote Server GUI) aims to help server managers easily edit and configure server setups. The GUI contains all the main elements used when configuring a server but avoids issues that can crop up with editing JSON files. The app will notify users of updates as they are released. Push the update button when it appears to update and restart the app. Saved profiles should not be affected.

# INSTALL
ACC RS GUI uses <a href = "https://github.com/clowd/Clowd.Squirrel" target= "_blank">Clowd Squirrel</a> to create and manage app installs and updates. ACC RS GUI will create a desktop shortcut and install local app files in  ..\AppData\Local\ACC_RS_GUI. Latest updates from <a href = "https://github.com/mog456/ACC-RSGUI-Releases/releases" target="_blank"> https://github.com/mog456/ACC-RSGUI-Releases/releases</a> will be installed silently and applied after restart.

On running  the app, a directory structure will be created in 'Documents/ACC RS GUI Settings'. This dir contains all server configs, last session data and ACC server JSON files.

# ISSUES
1. <b>THIS IS A BETA RELEASE!</b> Before running any uploads to your server I would suggest to make a backup of the current server/cfg folder so it can be replaced if anything goes wrong. This is now in testing so any probs let me know and I can propbaly adapt the existing functionality and release an update.
2. There are currently <b>NO WARNINGS</b> when uploading/downloading files - so once you push the buttons data WILL be overwritten.
3. On boot the app will search for any previous use sessions and attempt to load the corresponding data. This is not functional atm on boot and needs the user to press the 'LOAD' button (on the 'Local Files') section in order to properly populate the Weather/Advanced tabs data.
4. Did I mention this is a beta release? Good.
5. Any bugs/issues can be reported <a href="https://github.com/mog456/ACC-RSGUI-Releases/issues" target = _blank>here</a>

# GUIDE
## Main Tab
main settings and connect/save options

### QUICK START
1. On first boot 'Available Profiles' will be empty. Enter your credentials and click 'Connect' button. If connection is successful a new profile (named 'serverName') will be available in subsequent sessions.
2. Next try the 'Download' button. This will copy all the JSON files from your 'server/cfg' to '/Documents/ACC RS GUI Settings/yourServerName/cfg'. The app will then load the JSON data into the editor. Check 'Weather' and 'Advanced' tabs to make sure all data has populated (this is a known issue). If the fields have not completely populated try 'Load Profile' again from the main tab.
3. Edit the settings as needed
4. 'Save Profile' button will write all data to the LOCAL folder - Documents/ACC RS GUI Settings/yourServerName/cfg - it will not upload any content
5. 'Upload' button will OVERWRITE files on yourServer/cfg with the local settings (in the app). There will be no warning...(haven't done that yet)...it will not be televised....so make sure you've got a backup...
6. <b>You will have to restart your server from your host to apply the new config</b>.
7. On subsequent use (after first boot) your last session will load automatically. There is an issue here so you'll need to press the 'LOAD PROFILE' button again to make sure all fields are populated.
8. When updates are available you will be notified with a 'Restart Now' button. Updates are installed sliently and rebooting the app will apply any updates

### TROUBLESHOOTING
- Check the info panel on the right hand side of the main tab for error info. 
- Make sure your configurationINFO (USER,PASSWORD, ETC) are correct. Trying the 'CONNECT' button will give you an idea of any errors in connecting to your server. 
- Other issues contact me

#### REMOTE FILES
SFTP and connection info are in the form 123.456.789.101:12345 - this is based specifically on GTX gaming servers. If your server is different and you cannot connect let me know and I'll add required formatting.
As a guide SFTP info is formatted 123.456.789.101:SFTP_Port_Number.

Download button will test credentials then download and OVERWRITE any local files that exist. Will also create a new User Profile per server connection that will be available via the LOCAL FILES/Available Profiles drop down. This action will create a new local dir (if it doesn't exist) containing a copy of all JSONs in yourServer/cfg.

Upload button will OVERWRITE ALL configuration files in yourServer/cfg directory with your edited (local) settings. <b>You will have to restart your server from your host to apply the changes</b>.

#### LOCAL FILES
Load/save local configs from previous sessions. BUG NOTE - on load the app will TRY and load the last settings but you may need to hit the LOAD button again and check all fields (e.g. in Advanced) have beeen populated.

#### Console
Contains various messsages from the app. Can be used to troubleshoot. (currently in development).

#### BASIC SETTINGS 
The main thing to note here is the 'Enable' checkboxes for P/Q/R sessions. These checkboxes indicate whether or not the session will be included in the configuration.

## Weather Tab
Set weather conditions based on the ACC wiki

## Advanced Tab
Contains the other settings you're looking for...

## BOP tab
Empty, in development
</div>

<s>## ACC Server Wiki
Contains all info from the ACC Server Config Wiki page</s>

# TODO
- add weather profiles Load/Save
- add check for BOP updates from LFM



