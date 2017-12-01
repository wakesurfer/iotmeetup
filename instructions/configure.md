## Configure your device ##

Almost done! It's finally time to put everything together on your RaspberryPi and set up the connection.

(Full official tutorial for developing your device software can be found [here](https://docs.oracle.com/en/cloud/paas/iot-cloud/iotgs/developing-device-software-using-client-software-libraries1.html "Developing Device Software Using the Client Software Libraries"), or follow this [QuickStart tutorial](http://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/iot/IoT%20Quick%20Start%20CPOSIX/IoTQuickStartCPOSIX.html "POSIX Application on a Raspberry Pi").)

To make things easier, we have prepared some sample code which you can download directly to the RaspberryPi using Git.

1. Find the **IP-address** of your RaspberryPi using **nmap** (for example: nmap -v -sn 192.168.1.0/24). If you are using one of the provided ones, they are clearly marked with an alias (Ripan, Viggen, Ugglan...), making them earier to identify. 
2. You now want to copy your downloaded **provisioning file** to the RaspberryPi, to the folder XXX. We suggest using FileZilla or sftp.  
2. SSH to your RaspberryPi. If you are on a windows computer, we suggest using Putty.
3. Navigate back to the folder XXX.
4. Clone the repository by entering : "git clone https://github.com/DiscoTechOracle/IoT-Meetup.git"
5.  


You have now successfully registered your RaspberryPi as a device in the IoT Cloud Service! Time for the next step!

### [Configure your device to connect to the IoT Cloud Service server](configure.md) ###
