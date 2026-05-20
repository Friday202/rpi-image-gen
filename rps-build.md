# This is rps build
To build the image: 

``
cd /home/rps/rpi-image-gen/
./rpi-image-gen build -S ./examples/rpskiosk/ -c kiosk.yaml
``

# To flash the image on sd card 
``
sudo umount /dev/sdb1 /dev/sdb2
sudo dd if=/home/rps/rpi-image-gen/work/image-mykioskimage/mykioskimage.img of=/dev/sdb bs=4M status=progress conv=fsync
sync
``