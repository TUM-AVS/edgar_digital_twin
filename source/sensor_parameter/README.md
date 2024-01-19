# Overview
This section describes the sensor position paramters for our EDGAR research vehicle. The vehicle consists of multiple different sensors ranging from microphone, RADAR, LiDAR, Camera and dGPS. In the below picture, you see a qualitative picture of where the sensors are positioned
![EDGAR_Sensors](EDGAR_Sensor_Overview.png)

# URDF
Here, we describee the [edgar.urdf](edgar.urdf) of the EDGAR research vehicle. A URDF (Unified Robot Description Format) is a file used to represent the kinematic and dynamic description of a robot. It enables the modeling of robots using joints and links among other attributes.

The edgar.urdf is structured as follows:

1. Robot element:
	- The `robot` as the main container for the robot description

2. The link elements represent a rigid body in a robot model. In this particular case the links defined in the URDF are:

	Reference frames:

	- [base_link](edgar.urdf#L15)
	- [rear_axle_center_ground](edgar.urdf#L5)
	- [rack_rear_center](edgar.urdf#L16)
	- [rear_axle_center](edgar.urdf#L17)

	The respective sensors installed on EDGAR, i.e.:

	- [gnss_left](edgar.urdf#L19)
	- [imu](edgar.urdf#L22)
	- [lidar_ouster_left](edgar.urdf#L24)
	- [radar_front_left](edgar.urdf#L29)
	- [camera_sr_front_left](edgar.urdf#L36)
	- ...

	Links can also be visualized using geometric features. We use a [3d model](../3d_model/low_res/edgar.fbx) for EDGAR (see first section in the [edgar.urdf](edgar.urdf) file).  

3. The joint elements describe the relative transformation between two links with the origin being the relative position of the child link with respect to the parent link. All [joints](edgar.urdf#L73) in the EDGAR URDF are defined as fixed.

You can find an exemplary integration of the EDGAR URDF file and 3d model using the [edgar_state_publisher](../../tools/edgar_state_publisher).

For a more detailed tutorial on URDF please refer to http://wiki.ros.org/urdf/Tutorials.
