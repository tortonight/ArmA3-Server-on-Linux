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




