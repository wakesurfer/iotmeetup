## Test the client ##

1. To test the client we need to again build it with **build_iotclient.sh**. But remember to first update the code on the client by doing a git pull/use FileZilla.
```
git pull
sh build_iotclient.sh
```
Now run the client.
```
sh run_iotclient.sh
```
Whoa that's a lot of diagnostic info! To only see our own printf's, redirect stdout to a log file. This is the reason for the unconventional logging to stderr in case you where wondering.
```
sh run_iotclient.sh 1> log
```

Hopefully you will see some measurements from the sensor which will be sent to the IOT Server. The URL of the server is located in the conf file that you provide as an input parameter (in the shell script) to the iotclient app.

2. To see what happens on the other side lets login to the IoT Server @ https://oc-129-150-123-79.compute.oraclecloud.com/ui/
The credentials will be provided at the event.

3. On the dashboard click into the IoT Application that you previously created for your team.

Now I'm sure you would like to add some features that would make this code even more useful!

### [The Final Touch](iotclientfinaltouch.md) ###
