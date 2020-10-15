=======================================
Single lidar data acquisition
=======================================

Use Livox Viewer to Collect Data
--------------------------------

Take Livox Mid-40 as an example:

**dependencies**：Ubuntu 16.04 or win10, Livox_Viewer(see driver for this part of the software installation :doc:`Driver <../data_summary/Livox_data_summary>`)

**Hardware part**：Livox-Mid 40, power adapter socket 2.0 or connection box, Ethernet cable, PC.

**Connection**：The physical connection is shown in the figure below

.. image:: ../image/one_lidar_connect.png

If you have any questions about the connection and IP configuration, please refer to the "Connection" section of the Livox Mid user manual on the Livox official website, and the link of the
`Livox Mid user manual <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/update/Livox%20Mid%20Series%20User%20Manual%20(EN).pdf>`_

Acquisition: After completing the hardware connection, open Livox Viewer, the download address is as follows:

`Livox Viewer 0.8.0 for Windows <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/update/Livox%20Viewer%200.8.0.7z>`_ 

`Livox Viewer 0.7.0 For Linux Ubuntu16.04_x64 <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/Livox%20Viewer/Livox_Viewr_For_Linux_Ubuntu16.04_x64_0.7.0.tar.gz>`_ 

After starting the terminal, go to the root directory of the unzipped folder and run the command './livox viewer.sh' to start

If the Lidar is correctly connected and the IP configuration is completed, the Livox Viewer interface is now shown as follows, and the model and 15-digit broadcast code of the connected Livox Lidar are displayed on the left.

.. image:: ../image/start_Viewer_and_link_Horizon.png

Click the button to start Lidar, and then click the play button to display the point cloud image collected by Lidar, as shown below:

.. image:: ../image/capture.png

After the acquisition is successful, you can click the record button on the toolbar to record the lvx format file, pause playback or click this button again to end the recording.

The toolbar contains multiple buttons to set the point cloud color scheme, point style size, frame integration duration and other functions. For details, please refer to the official website Livox Viewer User Manual. The link to Livox
`Livox Viewer User Manual <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/Livox%20Viewer/Livox%20Viewer%20User%20Manual.pdf>`_


The default format of Livox Viewer to record and save files is lvx. Select File->Save as in the menu to save the current point cloud as a csv or las file.


Collection Under ROS
-----------------------------

Take Livox Mid-40 as an example:

**dependencies**：ubuntu 16.04、ROS、Livox-SDK、Livox_ros_driver(see the driver for the detailed process of downloading and installing this part :doc:`Driver <../data_summary/Livox_data_summary>`)

**Hardware part**：Livox-Mid 40 × 1, power adapter 2.0 or connection box × 1, Ethernet cable (100M or Gigabit) × 1, PC × 1

**Connection**：The physical connection is shown in the figure below

.. image:: ../image/one_lidar_connect.png

If you have any questions about the connection and IP configuration, please refer to the "Connection" section of the Livox Mid User Manual on the Livox official website. 
`Livox Mid Manual <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/update/Livox%20Mid%20Series%20User%20Manual%20(EN).pdf>`_

**Point Cloud Collection:**：

-  Lvx:

First confirm that Livox-SDK has been cloned from Git

::

   $ git clone https://github.com/Livox-SDK/Livox-SDK.git


Complete the Lidar hardware and IP configuration part, and open a terminal window under the following file path:

::

   $ ../Livox_SDK/build/sample/lidar_lvx_file

Execute the following command to connect to Lidar and set the duration of the recorded point cloud data to 10s:

::
   
   $ ./lidar_lvx_sample -c "Lidar's Broadcast code" -t 10

.. image:: ../image/save_lvx_data_by_SDK_01.png


.. image:: ../image/save_lvx_data_by_SDK_02.png


After successful execution, a lvx file can be generated under the current path

.. image:: ../image/save_lvx_data_by_SDK_03.png

-  rosbag:

.. Note:: Since the Horizon integrates IMU, there are two topics when using this method to record Horizon lidar data: point cloud data in CustomMsg format and IMU data in sensor_msgs/Imu format.

1.1. After connecting the lidar, open the terminal to compile and update the current ROS package environment in the workspace where livox_ros_driver is located:

::

   $ catkin_make

   $ source ./devel/setup.sh

2.Use the ROS launch file to load the Livox ROS driver:

::

   $ roslaunch livox_ros_driver livox_lidar_rviz.launch

3.After starting rviz and displaying the lidar-screen, use the record command to record data:

::

   $ rosbag record -a
