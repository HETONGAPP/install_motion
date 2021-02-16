# install_motion

sudo apt-get update
sudo apt-get upgrade
sudo apt-get install rpi-update
sudo rpi-update
sudo reboot

cd ~/
mkdir mmal
cd mmal

sudo apt-get install motion libjpeg62

wget https://www.dropbox.com/s/6ruqgv1h65zufr6/motion-mmal-lowflyerUK-20151114.tar.gz
tar -zxvf motion-mmal-lowflyerUK-20151114.tar.gz

width=667
height=375
target_dir=/home/pi/mmal/video_dump
logfile=/home/pi/mmal/motion.log
stream_maxrate=5
framerate=5
output_pictures=off

motion -n -c motion-mmalcam.conf
