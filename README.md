# ArmA3-Server-on-Linux
[link](https://community.bistudio.com/wiki/Arma_3:_Dedicated_Server#Instructions_.28Linux_o.2Fs.29)
# Installation (with root)
```bash
apt-get update && apt-get upgrade
apt-get install lib32stdc++6
apt-get install screen
```
```bash
mkdir /home/ArmA3
cd /home/ArmA3
mkdir steam
mkdir server
cd steam
```
- 1.Download the SteamCMD executable.
```bash
wget http://media.steampowered.com/client/steamcmd_linux.tar.gz
```
or
```bash
wget https://github.com/tortonight/ArmA3-Server-on-Linux/raw/main/steamcmd_linux.tar.gz
```
- 2.Extract the contents to the directory.
```bash
tar -xvzf steamcmd_linux.tar.gz
```
- 3.Remove the tar file.
```bash
rm -f steamcmd_linux.tar.gz
```
-  4.Run and update SteamCMD.
```bash
./steamcmd.sh
```
```bash
login <USER> <PASS> (Steam ID)
force_install_dir ../server
app_update 233780 validate
app_update 233780 -beta creatordlc validate //[DLCs]
exit
```
Once it finishes downloading, you can close SteamCMD by typing in exit. Since we now have the Arma 3 server downloaded, we can now start it by changing to the arma3 directory.
```bash
cd ../server
```
... and then starting a new screen to start the server, where armaserver is the screen name.
```bash
screen -S armaserver
```
Run the Arma 3 server. Additional launch parameters can be found on the Bohemia Interactive Wiki.
```bash
./arma3server
./arma3server_x64 -ip=0.0.0.0 -port=2302 -profiles=./serverprofile -bepath=./battleye -cfg=basic.cfg -config=server.cfg -mod= -serverMod=@Apex -filePatching -noLogs
```
You can also return to the main screen by hitting Ctrl + A, then D. If you wish to return to the server console, you can do so by using the command below (where "armaserver" is your screen name).
```bash
screen -r armaserver
```
Kill detached screen session [closed]
```bash
screen -list
kill [NUMBER] (Detached)
```
You can close your Arma 3 server at any time by hitting Ctrl + C in the Arma 3 Server console.
# Firewall Rules (UFW)

If UFW is enabled, you may have to add a few new rules. This can easily be done with the following commands:
```bash
sudo ufw allow from 81.0.236.111 to any port 2344 proto tcp
sudo ufw allow from 81.0.236.111 to any port 2344 proto udp
sudo ufw allow from 81.0.236.111 to any port 2345 proto tcp
sudo ufw allow proto udp to any port 2302:2305
```



