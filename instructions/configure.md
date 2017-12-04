# Part 2: Configure and test the Raspberry #

## Configure your device ##

Almost done! It's finally time to put everything together on your RaspberryPi and set up the connection. If you have your own device, please see **[Raspberry Setup](raspberrysetup.md)** for information on how to set up your device.

(Full official tutorial for developing your device software can be found [here](https://docs.oracle.com/en/cloud/paas/iot-cloud/iotgs/developing-device-software-using-client-software-libraries1.html "Developing Device Software Using the Client Software Libraries"), or follow this [QuickStart tutorial](http://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/iot/IoT%20Quick%20Start%20CPOSIX/IoTQuickStartCPOSIX.html "POSIX Application on a Raspberry Pi").)

To make things easier, we have prepared some sample code which you can download directly to the Raspberry using Git.

1. Find the **IP-address** of your RaspberryPi. If you are using one of the provided ones, they are clearly marked with an alias (Ripan, Viggen, Ugglan...), making them earier to identify. We have provided the IP-addresses on papers next to them. Note the IP-adress. If you have your own device, locate one of the screens .
2. Optional. If you are familiar with Git, it is a good idea to now **create your own repository** with the code and files needed, starting by cloning `https://github.com/DiscoTechOracle/iotmeetup-code`.
3. Now, **SSH to your device**. If you are on a windows computer, we suggest using Putty. Use the provided credentials for the borrowed RaspberryPis.
4. You now want to copy your downloaded **provisioning file** to the Raspberry, to your home directory (/home/pi). Add it to your repository, or we suggest using FileZilla/sftp/similar. 
5. To get the sample code: Clone the github repository by entering : `git clone https://github.com/DiscoTechOracle/iotmeetup-code.git iotcs`, replace with your own repository if you have one.
6. Open **esensor.c**. At the top you will find variables for the URN, provisioning file and the password. Enter your own according to your notes. **Save**/**Upload new version**.
7. Compile the c program you created in the previous step.  
   `gcc -g -I../include -I../lib/arm -o ./hello_world_sample.out ./esensor.c -Wl,-Bstatic -L../lib/arm -ldeviceclient -Wl,-Bdynamic -lssl -lcrypto -lm -lrt -lpthread`
8. Verify that your program was successfully compiled by checking that the directory where your C program resides also contains the file esensor.out
9. Copy the provisioning file that was downloaded when you registered the device into that directory.


You have now successfully registered your RaspberryPi as a device in the IoT Cloud Service! 
On to some sensor work.

### Sharpen your senses and [Test your sensor](dhtsensor.md) ###
