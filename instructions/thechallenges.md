## The Challenges ##

Now on to some interesting challenges. Here we will not guide like in the tutorials. If you complete 3 of these then you will get a permanent place in the IoT Gurus Hall of Fame on our Meetup.com site!

1. You remember that sometimes the DHT22 sensor fails to provide measurements? Now this is a perfect place to use IoT Alerts! Enhance your iotclient.c code to send alerts to the server when the DHT22 fails to return any temperature and humidity values.

2. Even though doing real coding is awesome, sometimes you need to quickly create some devices with sensors where the hardware has not even been built yet. The answer to this is Simulators. Try to build a simulator and use it in the IoT Server.
[Link to Simulator docs](https://docs.oracle.com/en/cloud/paas/iot-cloud/iotgs/using-iot-device-simulator.html)

3. Build a Python client that does something similar to the C client in the tutorial or something totally different, it is up to you to dazzle us! Here we need to explore the [IoT REST APIs](https://docs.oracle.com/en/cloud/paas/iot-cloud/iotrq/toc.htm "REST API for Oracle Internet of Things Cloud Service") of the IoT Server since there are no client libraries for Python. You might involve the DHT22 sensor or just send some sample data to the server.

4. Ask the Meetup leaders to get to try another type of sensor, the *DS18B20* and connect it to the Raspberry. Then try to use it with the iotclient.c code or your own code. This will involve understanding the 1-Wire protocol used by these sensors. This is uncharted territory so only for the real techies!

5. Of course you brought your own Raspberry to the event! Now it is time to replicate what we have done but without the added help of templates and crutches!

6. More of a front-end person? Use the [IoT REST APIs](https://docs.oracle.com/en/cloud/paas/iot-cloud/iotrq/toc.htm "REST API for Oracle Internet of Things Cloud Service") and why not create your own monitoring-website for your team?

Hint hint, nudge nudge: for some of the challenges you can find excellent help by searching Github for examples.

### [Back to the start](../README.md) ###
