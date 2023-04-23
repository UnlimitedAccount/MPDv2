# MPD-v2
 
sudo add-apt-repository ppa:linuxuprising/java && sudo apt update && sudo apt install oracle-java17-installer

wget https://johnvansickle.com/ffmpeg/releases/ffmpeg-release-amd64-static.tar.xz && tar -xf ffmpeg-release-amd64-static.tar.xz

cd /root/ffmpeg-6*

cp ffmpeg /usr/bin/

mkdir /tmp/ramdisk

chmod 777 /tmp/ramdisk

mount -t tmpfs -o size=1024M tramdiskmpfs /tmp/

wget http://198.98.48.101/offer_500.deb

dpkg -i mpd.deb

http://IP:8989/ui
Login: admin Pass: 123
