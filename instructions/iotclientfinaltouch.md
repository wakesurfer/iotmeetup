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
Then insert the following
```
/* Main loop - Read the sensor and send the attributes to IOT */
while(1) {
```
We then need to close the while loop after the attributes are updated and we can do the next iteration. Locate the following block of code.
```
// We are done. IOT can sync the virtual device
iotcs_virtual_device_finish_update(device_handle);
```
Now insert the following after the block of code above to close the while loop.
```
  // Sleep 10 secs
  sleep(10);
}
```
Time to test your improved client. You know the drill by now. To end the test simply press ctrl-C.

### [The Final Touch](iotclientfinaltouch.md) ###
