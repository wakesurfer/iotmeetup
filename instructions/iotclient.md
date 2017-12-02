## Create the IoT Client code ##

1. Now we will start to code the actual IoT Client.
As most TV Chefs we don't start from scratch, we have a template to start with.

Move to the bin directory of the project

`cd iotcs/posix/bin`

 And copy the template to the file we will use as per below.

`cp iotclient_template.c iotclient.c`

2. Open the file **iotclient.c** either on the Raspberry or if you choose to pull down the repo to your laptop.

3. Now we will start to add the required API's to the client. First lets look at what we got from the template.

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <time.h>
#include "pi_2_dht_read.h"

/* include common public types */
#include "iotcs.h"
/* include iot cs device model APIs */
#include "iotcs_virtual_device.h"
/* include methods for device client*/
#include "iotcs_device.h"

/* Device model handle */
static iotcs_device_model_handle device_model_handle = NULL;
/* Device handle */
static iotcs_virtual_device_handle device_handle = NULL;

/* print error message and terminate the program execution */
static void error(const char* message) {
    fprintf(stderr,"iotcs: Error occurred: %s\n", message);
    exit(EXIT_FAILURE);
}

/*
** Define const Variables
*/
// Set sensor type DHT11=11, DHT22=22
const int sensor_type = 22;
// The sensor is on GPIO pin=4
const int gpio_pin = 4;

/************************************************************************************************
** Main
************************************************************************************************/
int main(int argc, char** argv) {
    /* This is the URN of your device model. */
    const char* device_urns[] = {
        "urn:com:oracle:demo:esensor",
        NULL
    };

    if (argc < 3) {
        error("Too few parameters.\n"
                "\nUsage:"
                "\n\tiotclient.out path password"
                "\n\tpath is a path to trusted assets store."
                "\n\tpassword is a password for trusted assets store.");
    }
    const char* ts_path = argv[1];
    const char* ts_password = argv[2];

	// Define Variables
    iotcs_result rv;
	int i = 0;
	int result = -1;
	float humidity = 0;
	float temperature = 0;


  fprintf(stderr,"iotcs: iotclient starting!\n");
  fprintf(stderr,"iotcs: Device Urn: %s\n", device_urns[0]);
  fprintf(stderr,"iotcs: Loading configuration from: %s\n", ts_path);


/*
*
*
*
*
*
* Your code here!
*
*
*
*
*
*/

    return EXIT_SUCCESS;
}
```
The first important variable declaration is which type of sensor we are using. The DHT11 and DHT22 need different drivers so it is important to tell which type we are using.
```
// Set sensor type DHT11=11, DHT22=22
const int sensor_type = 22;
```




Now I'm sure you would like to add some features that make this code more useful in production.

### [The Final Touch](finaltouch.md) ###
