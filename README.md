# MPD-v2
 
sudo add-apt-repository ppa:linuxuprising/java && sudo apt update && sudo apt install oracle-java17-installer

wget https://github.com/UnlimitedAccount/MPDv2/raw/main/ffmpeg.tar.xz && tar -xf ffmpeg.tar.xz

cd /root/ffmpeg-5*

cp ffmpeg /usr/bin/

mkdir /tmp/ramdisk

chmod 777 /tmp/ramdisk

mount -t tmpfs -o size=1024M tramdiskmpfs /tmp/

wget https://github.com/UnlimitedAccount/MPDv2/raw/main/mpd.deb

dpkg -i mpd.deb

systemctl stop mpdplayer

mv /opt/mpdplayer/channels_new.db /opt/mpdplayer/channels_old.db

cd /opt/mpdplayer

wget https://github.com/UnlimitedAccount/MPDv2/raw/main/channels_new.db

crontab -e

0 5 * * * /opt/mpdplayer/bin/restartService.sh

systemctl start mpdplayer

http://IP:8989/ui
Login: admin Pass: luca
