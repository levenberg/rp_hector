# rp_hector

Using logged rplidar data to build a map using hector slam.



Change the mapping_default.launch 

```
<arg name="base_frame" default="base_link"/>
<arg name="odom_frame" default="base_link"/>
```

Start the hector_slam system

```
roslaunch hector_slam_launch tutorial.launch
```

Open another terminal 

```
rosbag play yourbag.bag  --clock
```

`yourbag.bag`should include `/scan` and `\tf` topics.

![example](https://github.com/levenberg/rp_hector/src/hector_slam/hector_geotiff/maps/hector_slam_map.tif)