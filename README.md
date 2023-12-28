# ACC_RemoteServer_GUI

## Content
[Install](#install)
[Issues](#issues)
[UserGuide](#guide)

<picture>
  <center>
  <source media="(prefers-color-scheme: dark)" srcset="img/Screenshot%202023-12-18%20113509.png">
  <source media="(prefers-color-scheme: light)" srcset="img/Screenshot%202023-12-18%20113509.png">
  <img alt="ACC RSGUI ScreenShot">
  </center>
</picture>

ACC RSGUI (ACC Remote Server GUI) aims to help server managers easily edit and configure server setups. The GUI contains all the main elements used when configuring a server but avoids issues that can crop up with editing JSON files.

The app will notify users of updates as they are released. Push the update button when it appears to update and restart the app. Saved profiles should not be affected.

# INSTALL
ACC RS GUI uses <a href = "https://github.com/clowd/Clowd.Squirrel" target= "_blank">Clowd Squirrel</a> to create and manage app installs and updates. ACC RS GUI will create a desktop shortcut and install local app files in  ..\AppData\Local\ACC_RS_GUI. Latest updates from <a href = "https://github.com/mog456/ACC-RSGUI-Releases/releases" target="_blank"> https://github.com/mog456/ACC-RSGUI-Releases/releases</a> will be noted by the app and the user will be notified with a restart button after the update is complete.

On running  the app, a directory structure will be created in Documents/ACC RS GUI Settings. This dir contains all server configs, last session data and ACC server JSON files.

# ISSUES
1. <b>THIS IS A BETA RELEASE!</b> Before running any uploads to your server I would suggest to make a backup of the current server/cfg folder so it can be replaced if anything goes wrong. This is now in testing so any probs let me know and I can propbaly adapt the existing functionality and release an update.
2. There are currently <b>NO WARNINGS</b> when uploading/downloading files - so once you push the buttons data WILL be overwritten.
3. On boot the app will search for any previous use sessions and attempt to load the corresponding data. This is not functional atm on boot and needs the user to press the 'LOAD' button (on the 'Local Files') section in order to properly populate the Weather/Advanced tabs data.
4. Did I mention this is a beta release? Good.
5. Any bugs/issues can be reported <a href="https://github.com/mog456/ACC-RSGUI-Releases/issues" target = _blank>here</a>

# GUIDE
## Main Tab
main settings and connect/save options

### FIRST BOOT
On first boot no info will be available. Enter your credentials and click 'Download' button on remote files area. This will attempt to make a copy of the active (/cfg) folder on your server. If connection is successful a new profile (named 'serverName') will be available in subsequent sessions.

<b>Check the Weather and Avanced tabs - if no data os present there may have been a connection error. Check the black ops console (can be scrolled up) for reported connection issues.</b>

#### REMOTE FILES
SFTP and connection info are in the form 123.456.789.101:12345 - this is based specifically on GTX gaming servers. If your server is different and you cannot connect let me know and I'll add required formatting.
As a guide SFTP info is formatted 123.456.789.101:SFTP_Port_Number.

Download button will test credentials then download and OVERWRITE any local files that exist. Will also create a new User Profile per server connection that will be available via the LOCAL FILES/Available Profiles drop down. This action will create a new local dir (if it doesn't exist) containing a copy of all JSONs in yourServer/cfg.

Upload button will OVERWRITE ALL configuration files in yourServer/cfg directory with your edited (local) settings.

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

## ACC Server Wiki
Contains all info from the ACC Server Config Wiki page



