# ACC_RemoteServer_GUI

<picture>
  <center>
  <source media="(prefers-color-scheme: dark)" srcset="img/Screenshot%202023-12-18%20113509.png">
  <source media="(prefers-color-scheme: light)" srcset="img/Screenshot%202023-12-18%20113509.png">
  <img alt="ACC RSGUI ScreenShot">
  </center>
</picture>

ACC RSGUI (ACC Remote Server GUI) aims to help server managers easily edit and configure server setups. The GUI contains all the main elements used when concofiguring a server but avoids issues that can crop up with editing JSON files.

The app will notify users of updates as they are released. Push the update button when it appears to update and restart the app. Saved profiles should not be affected.

# GUIDE
## Main Tab
main settings and connect/save options
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
In development but functional in terms of setting weather conditions.

## Advanced Tab
Contains the other settings you're looking for...

## BOP tab
Empty, in development

## ACC Server Wiki
Contains all info from the ACC Server Config Wiki page



