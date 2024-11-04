# Server
Server Name
```
HK-TH  ARMA 3 Server  By. ToRTonight #1
```
Server Admins
```
"76561198196638689","76561199101845342"
```
MOTD
```
"Welcome to Arma 3","HK-TH  ARMA 3 Server  By. ToRTonight #1"
```
Client File Patching Exceptions
```
"76561198196638689","76561199101845342"
```
Headless Client IPs
```
"127.0.0.1","138.19.83.118"
```
Local Headless Client IPs
```
"127.0.0.1","192.168.0.148"
```
Additional Server Startup Parameters
```
-filePatching -noLogs
```
Enable UPnP
```
On
```
# Gameplay
![Screenshot](https://github.com/user-attachments/assets/5e91a2cb-7893-4d59-9fa9-d354f2d1e449)

# Miscellaneous
Log Time Stamp Format
```
Short
```
Run Script On User Connected
```
['onUserConnected',_this] call QS_fnc_serverEventHandler
```
Run Script On User Disconnected
```
['onUserDisconnected',_this] call QS_fnc_serverEventHandler
```
Run Script On Double ID Detected
```
['doubleIdDetected',_this] call QS_fnc_serverEventHandler
```
Run Script On User Kicked
```
['onUserKicked',_this] call QS_fnc_serverEventHandler
```
Run Script On Unsigned Data
```
['onUnsignedData',_this] call QS_fnc_serverEventHandler;
```
Run Script On Hacked Data
```
['onHackedData',_this] call QS_fnc_serverEventHandler;
```
Run Script On Different Data
```
['onDifferentData',_this] call QS_fnc_serverEventHandler;
```
