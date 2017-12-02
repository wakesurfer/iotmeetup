## Setup the Raspberry for IoT use! ##

Most of the configuration of the Raspberry is **already done** but we will revisit the different parts that are important if you would like to configure your own RPi.

These are the basic steps needed:

0. Setup WIFI connections. Instructions [here](https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md).

1. Creating a Bootable Image for the Raspberry. We are using the Raspbian Jessie Image.

2. Setting up the Raspberry to Allow SSH Connections

3. Connecting to the Raspberry
    1. Using SSH or Putty, **this is the option we are using**. We will post a list with the ip addresses for all the Raspberries to the Git repo at the start of the Meetup.
    2. Using a USB/TTY Cable

4. Optional. Setting the Raspberry Pi for a GUI Login. This is useful if you have an HDMI monitor and an external USB keyboard to use.

5. Optional. Setting a Static IP Address for the Raspberry. If you are on your own network and have control over address allocations.

The tool used for many of these steps is

`raspi-config`

The official setup instructions can be found [here](http://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/iot/RaspberryPiSetup/RaspberryPiSetup.html#section1).

On to some sensor work.

### [Sharpen your senses and Test your sensor](dhtsensor.md) ###
