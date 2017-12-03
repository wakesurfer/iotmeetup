## Test the client ##

1. To test the app we need to again build it with **build_iotclient.sh**. But remember to first update the code on the client by doing a git pull.
```
git pull
sh build_iotclient.sh
```
Now run the client.
```
sh run_iotclient.sh
```
Hopefully you will see some measurements from the sensor which will be sent to the IOT Server. The URL of the server is located in the conf file that you provide as an input parameter (in the shell script) to the iotclient app.

2. To see what happens on the other side lets login to the IoT Server @ https://oc-129-150-123-79.compute.oraclecloud.com/ui/

3. On the dashboard click into the IoT Application that you previously created for your team.

Now I'm sure you would like to add some features that would make this code more useful in production scenario.

### [The Final Touch](iotclientfinaltouch.md) ###
