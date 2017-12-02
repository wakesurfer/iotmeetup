## Test your sensor ##

For this client we are using an Adafruit sensor DHT22. This is a popular device that is reasonably accurate for a low price. You can find som information on these devices [here](https://learn.adafruit.com/dht/overview#)

Now we need to test that our sensor is actually working. To make this really simple we have provided a test client.

1. In the bin directory there is a file **sensor_test.c**. Compile this code with the provided shell script
**build_sensor_test.sh**

2. Then run the test with
**./sensor_test.out**
If everything works you will get the current temperature and humidity.

3. You might notice that sometimes the sensor does not return a proper value. Since they are low cost this is ok. But we need to handle that in the client code. More in that later.

You have now successfully tested your DHT sensor! Time for the next step!

### [Building the IoT client](iotclient.md) ###
