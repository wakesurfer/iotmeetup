## Registering a Single Device ##

To communicate with Oracle Internet of Things Cloud Service, every device that is connected to Oracle Internet of Things Cloud Service must be registered and then activated. 

Full official tutorial can be found [here](https://docs.oracle.com/en/cloud/paas/iot-cloud/iotgs/registering-your-devices.html "Registering Your Devices").

To register your RaspberryPi:

1. Open the Management Console. Click the **Menu** (Menu icon) , click **Devices**.
2. Click **Registration**.
3. Click **Register Single Device**.
4. Complete the optional and mandatory fields.
  * **Note:** If you leave the Activation Secret field blank, a value is auto-generated and displayed when the device registration is confirmed. You can enter your own Activation Secret value. Any additional information, such as Name, Description, and Metadata are optional, but can be useful as search criteria when managing your registered devices.
5. Click **Register**.
6. Enter a password in the **File Protection Password** field to encrypt the provisioning file that contains the configuration and credentials to activate your device.
Enter the password again in the **Confirm Password** field.
7. Click **Download Provisioning File** to download the provisioning file to your computer.
The provisioning file is required to run your client.
8. Click **Finish**.
9. Click Management .
  * The registered device is listed in the Management pane with a State value of Registered and Type value of Unknown.

You have now successfully registered your RaspberryPi as a device in the IoT Cloud Service! Time for the next step!

### [Configure your device to connect to the IoT Cloud Service server](configure.md) ###
