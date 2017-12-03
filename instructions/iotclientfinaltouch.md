## The Final Touch ##

Now lets add some nice to haves to the client.

1. Obviously a "thing on the internet" that only sends one set of information and then needs to be retarted is not very useful. So lets introduce a loop that keeps the data flowing from the client. Insert the following after the call to *iotcs_get_virtual_device_handle()*.
```
  /* Main loop - Read the sensor and send attributes to IOT */
	while(1)
	{
```
We need to close the while loop after the attributes are updated and we can do the next iteration. Locate the following block of code.
```
// We are done. IOT can sync the virtual device
iotcs_virtual_device_finish_update(device_handle);
```
Now insert the following after the block of code above to close the while loop.
```
}
```



### [The Final Touch](iotclientfinaltouch.md) ###
