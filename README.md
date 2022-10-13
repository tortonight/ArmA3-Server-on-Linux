# ArmA3-Server-on-Linux
[link](https://community.bistudio.com/wiki/Arma_3:_Dedicated_Server#Instructions_.28Linux_o.2Fs.29)
# Installation
```
apt-get update && apt-get upgrade
apt-get install lib32stdc++6
apt-get install screen

cd /home/<USER>
mkdir steam
mkdir arma3
cd steam



    1.Download the SteamCMD executable.

    wget http://media.steampowered.com/client/steamcmd_linux.tar.gz
    or
    https://github.com/tortonight/ArmA3-Server-on-Linux/raw/main/steamcmd_linux.tar.gz

    2.Extract the contents to the directory.

    tar -xvzf steamcmd_linux.tar.gz

    3.Remove the tar file.

    rm -f steamcmd_linux.tar.gz

    4.Run and update SteamCMD.

    ./steamcmd.sh
    
login <USER> <PASS>
force_install_dir ../arma3
app_update 233780 validate
app_update 233780 -beta creatordlc validate //[DLCs]
exit
```
Once it finishes downloading, you can close SteamCMD by typing in exit. Since we now have the Arma 3 server downloaded, we can now start it by changing to the arma3 directory.
```
cd ../arma3
```
... and then starting a new screen to start the server, where armaserver is the screen name.
```
screen -S armaserver
```
Run the Arma 3 server. Additional launch parameters can be found on the Bohemia Interactive Wiki.
```
./arma3server
```
You can also return to the main screen by hitting Ctrl + A, then D. If you wish to return to the server console, you can do so by using the command below (where "armaserver" is your screen name).
```
screen -r armaserver
```
You can close your Arma 3 server at any time by hitting Ctrl + C in the Arma 3 Server console.
# Firewall Rules (UFW)

If UFW is enabled, you may have to add a few new rules. This can easily be done with the following commands:
```
sudo ufw allow from 81.0.236.111 to any port 2344 proto tcp
sudo ufw allow from 81.0.236.111 to any port 2344 proto udp
sudo ufw allow from 81.0.236.111 to any port 2345 proto tcp
sudo ufw allow proto udp to any port 2302:2305
```



