# Balena Cloud Direwolf Softmodem
Container for running [Direwolf](https://github.com/wb2osz/direwolf) soundcard softmodem on [BalenaCloud](https://www.balena.io/)

## Installation
1. Create BalenaCloud account
2. Create a new Application with a distinct name
3. Add a new device (Download and write provided image to SD card)
4. Install SDcard into Raspberry Pi and wait for it to appear under 'Devices'
5. Add Device Environmental Variables (See Variables section below)
6. Install [Balena-CLI](https://www.balena.io/docs/reference/balena-cli/) tools
7. Clone this project

    ``` git clone https://github.com/AllanGallop/Balena-Direwolf.git ```
8. Login to balena

    ``` balena login ```
9. Push project to application (name created in step 2)

    ``` balena push APPLICATION-NAME ```

10. Wait for build to complete
11. On Device summary page, open a terminal to device 'main'
12. Run ```alsamixer``` to adjust audio device levels
13. Run ```alsastore``` to save audio device levels

## Variables
The following 'Device Environmental Variables' can be used to configure a device from BalenaCloud, alternatively 'Application Environmental Variables' can be used to apply configuration options to all devices within a fleet

|  Variable |                       USE                      |
|:---------:|:----------------------------------------------:|
| CALLSIGN  | Your stations callsign (eg. MB7XXX-10)         |
| ADEVICE   | Device HW Identity (eg. rtlsdr, plughw:1,0)    |
| IGSERVER  | APRS Tier2 Server address (eg. euro.aprs.net)  |
| IGLOGIN   | APRS Login name and passcode (eg. MB7XXX 1234) |
| LONGITUDE | Longitude                                      |
| LATITUDE  | Latitude                                       |
| ALT       | Altitude (In Meters ASL)                       |
| SYMBOL    | APRS Symbol (eg. igate)                        |
| OVERLAY   | APRS Symbol Overlay (eg. S)                    |
| COMMENT   | APRS Comment (eg. Direwolf on BalenaCloud)     |