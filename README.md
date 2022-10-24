# Charlotte
Raspberry Pi based automatic software for cave surveing

## Origin of the name
Caving
HAcky
Rangefinder
Lidar
Open-source
Topographic
Tool
Embedded

The name reflects its core feature: it's a topographic tool for caves, like the famous DistoX, but it's hacky and cheap because it is built with a RaspberryPi computer and hobby electronics components.

The logo is inspired by the Charlotte cake:
Charlotte Cake IMG
Its classic cilindrical shape reflects the shape of the prototipe of this device. Also, there's a joke because this device is built on a Raspberry Pi, which sounds similar to "raspberry pie", and the Charlotte is a cake you can make also with wild berries (like raspberries).

## Safety notes
The default WiFi zone is Italy (Europe), so it's using a 2.4GHz radio signal.
The laser in the rangefinder is a <1mW laser, so it's not dangerous for human eyes. Please do not keep it pointed to cave animals, since they don't have protection against light radiation.

## Security notes
The default user for remote access over SSH is **pi** and the password is **raspberry**. It's important to change the password, using the command
`passwd`
otherwise the device will be vulnerable when connected to a network. In a cave it's not a big deal, but if you connect the raspberry to a network it must be something you trust until you change the default password.
The ethernet port connects automatically to any network with DHCP, so it can be used to update your Charlotte.
The WiFi device is always turned off at boot, and you need to enable it manually from the Mode tab of Charlotte interface. The WiFi cannot be used to connect to an existing network: it's instead automatically used to build an Access Point to wich you can connect using another device. This means you already need physical access the the device to be able to get remote control and access to the files.

## Install
The easiest way to get Charlotte ready to work is to download the image for a RaspberryPi from our website (TODO), and write it on a new SD card (minimum requirement: 16GB).

## Update
To update Charlotte, you first need to connect the device to a network using the ethernet cable. To update, you need to open a terminal (ssh connection) and run the following commands:
```
cd /home/pi/charlotte
git pull
./install.sh
```
Sooner or later there will be an update button on the GUI, but it's not a priority.

