# Ninja-Live-Scoreboard
Written by Rylen W. Garlitz - 2023

FinishLynx live scoreboard interface for MeetPro2 Live Results


## Installation: 
1. Download repo. 
2. Edit the `config.json` file with your information prior to starting the listener. 
  - Replace the `company` tag with the name of your timing company. Don't use any spaces. e.g. `elitetiming`, `halfmiletiming`, `ninjatiming` are all acceptable.
  - Replace the `uid` tag with the UID assigned to you.
  - Replace the `directory` tag with your 'MeetPro2 Report Templates' folder found in your 'Documents' folder.
    - **WIN10** : Shift + Right-Click and select "Copy as path" 
    - **WIN11** : Right-Click and select "Copy as path" 
    - The `directory` path should resemble the following: `"C:/Users/User/Documents/MeetPro2 Report Templates"`

3. Right click on the `.exe` file and create a shortcut to place on your Desktop or somewhere easily accessible. 

## Scoreboard FinishLynx Settings:
The two files 'NinjaLive-Clock' and 'NinjaLive-Results' need to be placed into you main Lynx directory, `C:\Lynx`, so FinishLynx can access those files on startup. 

1. Create two scoreboard using the following settings: 

- Clock/Time: NinjaLive-Clock.lss | Network (Connect) | Port: `43000` | IP Address: Selected in the listener.
- Results: NinjaLive-Results.lss | Network (Connect) | Port: `43001` | IP Address: Same as Clock.

2. In the Lynx Hidden Settings [Shift + Ctrl click on File|Options]
  - Change Scoreboards/Port Buffer to `32768`

## When Transmitting Data to the Scoreboard: 
1. Run the listener PRIOR to starting MeetPro2. 
2. Enter the Event Code into the text field. (Event codes are arbitary and can be any alphanumeric code you would like to identify your meet with. Good practice is to include the date and name of the event such as `040423ucfrelays`. Multiple events **CAN NOT** have the same event code. If your company is running multiple events at different venues, all codes must be unique. 
3. Select the Network which you want to start the server on. Make sure you are choosing the same LAN that your FinishLynx computer is on. 
4. Click the green `Start` Button at the bottom of the window.
5. Upload Results, Startlist, etc. through 'Upload to Web' in MeetPro2. 
- To use the Live Scoreboard make sure that 'Continuous Updating' is selected in the 'Report Settings' of MeetPro2. 

Clock and Result data will populate the Log window throughout the event as new information is sent to the scoreboard. **DO NOT** close the listener windows. 

If the internet connection drops, the program will attempt to re-connect automatically upon a successful connection.

If the listener is unable to reconnect (usually around 20sec), you will receive an error in the black command window. Stop and restart the listner when you have reconnected your computer to the internet.
