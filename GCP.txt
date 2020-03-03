#!/bin/bash
mount /dev/disk/by-id/google-minecraft-disk /home/minecraft
cd /home/minecraft
screen -d -m -S mcs java -Xmx1024M -Xms1024M -jar server.jar nogui
