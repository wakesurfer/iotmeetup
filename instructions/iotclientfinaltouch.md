## The Final Touch ##

Now lets add some nice to haves to the client.

1. Obviously a "thing on the internet" that only sends one set of information and then needs to be restarted is not very useful. So lets introduce a loop that keeps the data flowing from the client.
Find the following block of code in iotclient.c.
```
/* get device handle */
if (iotcs_get_virtual_device_handle(iotcs_get_endpoint_id(), device_model_handle, &device_handle) != IOTCS_RESULT_OK) {
  fprintf(stderr,"iotcs_get_device_handle method failed\n");
  return IOTCS_RESULT_FAIL;
}
```
Then insert the following after the previous block of code.
```
/* Main loop - Read the sensor and send the attributes to IOT */
while(1) {
```
We then need to close the while loop after the attributes are updated and we can do the next iteration. Locate the following block of code.
```
// We are done. IOT can sync the virtual device
iotcs_virtual_device_finish_update(device_handle);
```
Now insert the following after the block of code above to close the while loop. We also call a sleep function to avoid overloading the DHT22 sensor.
```
  // Sleep 20 secs
  sleep(20);
}
```
Time to test your improved client. You know the drill by now. To end the test simply press ctrl-C.

2. Now we're rockin'. Lets start the client in the background so it will not be interrupted if our terminal session is disconnected.
```
nohup sh run_iotclient.sh 2>&1 log &
```

To check that the client is well and alive.
```
ps -ef | grep iotclient
```
You will get something that looks like
```
pi       16626  4215  0 17:16 pts/0    00:00:00 sh run_iotclient.sh log
pi       16627 16626  4 17:16 pts/0    00:00:00 ./iotclient.out ./AAAAAAQB7RGB-A5.conf Password1 test
pi       16631  4215  0 17:16 pts/0    00:00:00 grep --color=auto iotclient
```
If you want to stop your client you need to kill the process like this.
```
kill -9 <pid>
```
The pid in the above example is 16627. So it would be.
```
kill -9 16627
```
You can also check the log file to see what client is doing.
```
grep temperature log
```
or to "follow" the clients log do
```
tail -f log
```

3. Finally, why not start the client when the Raspberry boots? Then you can just plugin the power and your "appliance" will start its measurements and report to the IoT Cloud Service.
Edit the file */etc/rc.local*
```
sudo nano /etc/rc.local
```
and add the following code.
```
sh /home/pi/iotcs/posix/bin/run_iotclient.sh > /home/pi/iotcs/posix/bin/$(date +%Y\:%m\:%d-%H\:%M\:%S)-run.log 2>&1 &
```
Ok, now reboot the RPi to test. Remember you can check on the process with *ps -ef ...* as you did earlier.
You can also monitor the messages from your client in the IoT Servers Dashboards.

Congratulations! You've completed the Basic Tutorial. Now we have some suggestions for those that like challenges.

### [The Challenges](thechallenges.md) ###
