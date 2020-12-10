===========================================================================
Multi-lidars data collection (using Livox Hub)
===========================================================================

Connection and Configuration
--------------------------

Take a Livox Mid-40 and a Livox Horizon as an example:

**dependencies:**：ubuntu 16.04、ROS、Livox-SDK、Livox ROS driver（see the driver for the detailed process of downloading and installing of this part :doc:`驱动 <../data_summary>`）

**Hardware part:**：Livox Mid-40 × 1, Livox Horizon × 1, Livox Hub × 1, Gigabit Ethernet cable × 1, Livox Hub power cord × 1, Livox lidar battery × 1, PC × 1.

**synchronization:**：For time stamp synchronization between multiple livox LiDARs, please refer to:  `Timestamp Synchronization <https://github.com/Livox-SDK/Livox-SDK/wiki/livox-device-time-synchronization-manual>`_

**Wiring and IP configuration:**：Livox Hub uses UDP communication protocol for data communication through Ethernet, and supports two types of IP address configuration: static IP address and dynamic IP address. The factory default is to use Dynamic Host Configuration Protocol (DHCP) to assign IP addresses. According to different IP address settings, the physical connection is slightly different.

-  When using a static IP address to connect, the physical connection is as shown in the figure below:

.. image:: ../image/static_ip.png

-  When a dynamic IP address is used for connection, the physical connection is shown below:

.. image:: ../image/dynamic_ip.png

Livox Hub uses Dynamic Host Configuration Protocol (DHCP) to assign IP addresses by default when it leaves the factory. If you want to use static IP to connect, you need to connect to a router for settings. The steps are as follows:

1.Connect the Livox Hub, Livox Lidar, PC and power supply through the router according to the dynamic IP address connection method as above figure.

2.Run Livox Viewer on the computer and click to open the device manager. Select Livox Hub and click to open the device properties page. Set the IP address of Livox Hub as a static IP address in the device properties page. Note that the static IP address of Livox Hub should be set to 192.168.1.X (where X is any number between 2 and 233).

3.After setting up, disconnect all connections to Livox Hub.

4.If Livox Hub is in static IP mode, the computer should also be set to static IP mode (if the computer uses dynamic IP mode, Livox Hub may not be found). The static IP address of the computer should be set to 192.168.1.X (where X is any number between 2 and 233), and it cannot be the same as the IP address of the connected Livox Hub.

If you have any questions about the connection and IP configuration of the Hub, please refer to the "Connection" section of the "Livox Hub User Manual v1.2" on the Livox official website. The download link is as follows: `Livox Hub manuel v1.2 <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/20191128/Livox%20Hub%20Series%20User%20Manual%2020191018.pdf>`_

This example uses static IP configuration, as shown in the following figure:

.. image:: ../image/static_IP_config.rst

Up to 9 Livox Lidars can be connected to the Livox Hub at the same time. In this example, a Livox Horizon and a Livox Mid-40 are connected. If you want to collect more Lidars at the same time, you can connect directly.

Collection Under ROS
------------------------------------------

After the connection is successful, compile in the local ws_livox path:

::
   
   catkin_make

Update the current ROS package environment:

::

   source ./devel/setup.bash``

Use the ROS launch file to load the LIvox ros driver

::
   
   roslaunch livox_ros_driver livox_hub_rviz.launch``

All launch files in the Livox driver are located under the path:
"ws\_livox/src/livox\_ros\_driver/launch".Different launch files have different configuration parameter values. Different launch files can be started according to different usage scenarios （detailed launch configuration can be found in the description section of `Livox ROS Driver github <https://github.com/Livox-SDK/livox_ros_driver>`_ 4.1 launch configuration file）

The livox_hub_rviz.launch will automatically connect to the Livox Hub device, publish pointcloud2 format point cloud data, and automatically load rviz to display real-time point cloud data, as shown in the following figure:

.. image:: ../image/ros_hub_scanning.png

The red part of the point cloud is the image scanned by Livox Horizon, and the purple part is the image scanned by Livox Mid-40

Use Livox Viewer to Collect Data
------------------------------------------

After the connection is successful, open a terminal in the Livox Viewer folder and run the following command to open the Livox Viewer program:

::
   
   ./livox_viewer.sh

.. |Viewer_manager| image:: ../image/devices_manager.png


Click |Viewer_manager| to Open the device manager and select Livox Hub. The IP address of Livox Hub may not match the IP address of the PC when connecting for the first time. If you have configured the Livox Hub and PC with static IP according to the above steps, you can click Network Adapter—refresh Adapter on the toolbar to refresh the configuration.

Open the Hub button and click play to display the real-time scan data of multiple lidars, as shown in the figure below:

.. image:: ../image/two_lidar_scanning.png

The yellow part of the point cloud is the data scanned by Livox Horizon, and the blue part of the point cloud is the data scanned by Livox Mid-40.

Similar to single lidar data recording, you can click the record button on the toolbar to record the lvx format file, pause playback or click this button again to end the recording.