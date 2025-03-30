# AAE6102-Laboratory
Change the initialized position and base station position in **rtklib.h**

```
/** Whampoa data, evaluation for GPS solutions (dynamic, loop) **/
#define ref_lon    114.190305193         /* Yixin: reference longitude */
#define ref_lat    22.301575393        /* Yixin: reference latitude */
#define ref_alt    5.4704              /* Yixin: reference altitude */

#define station_x     -2421567.8916       /* Yixin: pose x of base station */
#define station_y     5384910.5631        /* Yixin: pose y of base station */
#define station_z     2404264.3943        /* Yixin: pose z of station */

#define start_gps_sec 453618 /* Yixin: Time of Whampoa 2021-05-21 6:00:00 */
#define end_gps_sec 457218  /*Yixin: Time of Whampoa 2021-05-21 7:00:00 */
```

The pesudorange- doppler fusion with FGO method has a rosbuster solution in urban canyons, where the 
