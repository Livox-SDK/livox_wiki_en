==============================================
Summary of Official Open Source Materials
==============================================

Drive
--------------

Livox SDK
~~~~~~~~~~~~~~~~~~~~~~

Livox SDK is a software development kit designed for all products under Livox. It is developed based on the C/C++ language, follows the Livox SDK communication protocol, and provides users with an easy-to-use C language style interface. Through the Livox SDK, users can quickly connect to Livox products and receive point cloud data. See  `Livox SDK <https://github.com/Livox-SDK/Livox-SDK>`_ for details and installation.

Livox ROS Driver
~~~~~~~~~~~~~~~~~~~~~~

Livox ROS driver is a brand new ROS package, specifically used to connect LiDAR products produced by Lavo. The driver can run under the ubuntu14.04/16.04/18.04 operating system with ROS environment (indigo, kinetic, melodic) installed. After testing, the hardware platforms that can run the Lanwo ROS driver include: intel x86 mainstream cpu platform, and some ARM64 hardware platforms (eg, nvida TX2/Xavier, etc.). See `Livox ROS Driver <https://github.com/Livox-SDK/livox_ros_driver>`_

Livox Apollo Driver
~~~~~~~~~~~~~~~~~~~~~~

The Apollo driver is used to convert the original data file scanned by Livox_Lidar into a standard point cloud format file and write it into the point cloud channel. For details and installation see  `Livox Apollo Driver <https://github.com/Livox-SDK/livox_apollo_driver>`_

Tools
--------------

Livox Viewer
~~~~~~~~~~~~~~~~~~~~~~

Livox Viewer is a software designed specifically for Livox lidar and Livox Hub, which can be used to display the point cloud data of all lidars connected to the computer in real time. Through Livox Viewer, users can easily view, record and store point cloud data for later use. Detailed instructions can be found in the Livox Viewer manual on Livox official website. The download address is as follows:

`Livox Viewer 0.7.0 (64bit) - Windows <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/Livox%20Viewer/Livox%20Viewer%200.7.0.zip>`_

`Livox Viewer 0.7.0(64bit) - Ubuntu 16.04 <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/Livox%20Viewer/Livox_Viewr_For_Linux_Ubuntu16.04_x64_0.7.0.tar.gz>`_

Open Source Algorithm
----------------------------

Livox Horizon LOAM
~~~~~~~~~~~~~~~~~~~~~~

Livox Horizon Loam is a robust, low-equivalent, real-time odometer and drawing software package developed for Livox Lidar. The software package is mainly designed for low-speed scenes (about 5km/h) and solves many key problems such as feature extraction and selection under limited field of view and motion distortion compensation. For details see: 
`Livox Horizon Loam <https://github.com/Livox-SDK/livox_horizon_loam>`_

Livox Horizon Calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Livox-Horizon-based calibration steps for Horizon-Horizon/Horizon-Tele. For details see:
`LOAM Horizon Calibration <https://github.com/Livox-SDK/livox_calibration>`_

livox scanner
~~~~~~~~~~~~~~~~~~~~~~

livox scanner is a 3D scanning solution, which mainly includes a Mid-40 lidar, Manifold 2 computing platform, and a GM6020 motor with encoder. The LiDAR and the motor are installed on the top of the tripod. The Mid-40 will rotate around the Z axis to scan different areas in the space, and the point cloud data will be fused with the motor angle to obtain a 3D image in the space. The system construction process and detailed code can be found here:
`livox scanner <https://github.com/Livox-SDK/livox_scanner>`_

livox high precision mapping
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This solution uses Mid-40 lidar sensor with a detection distance of 260m, accuracy of 2cm, and non-repetitive scanning mode, combined with the high-precision position and attitude data provided by the APX-15 inertial navigation module, to achieve real-time high-precision mapping function. For details, see:
`livox high precision mapping <https://github.com/Livox-SDK/livox_high_precision_mapping>`_

livox camera lidar calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This solution provides a method to manually calibrate the external parameters between Livox lidar and camera, which has been verified on Mid-40, Horizon and Tele-15. It contains code for calculating internal camera parameters, obtaining calibration data, optimizing external parameters and lidar camera fusion applications. In this scheme, the corners of the calibration board are used as the calibration targets. Due to the non-repetitive scanning feature of Livox lidar, the density of the point cloud is relatively high, and it is easier to find the accurate position of the corners in the lidar point cloud. The calibration and fusion of camera lidar can also get good results. For details see: 
`livox camera lidar calibration <https://github.com/Livox-SDK/livox_camera_lidar_calibration>`_

Horizon Highway SLAM
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Horizon is a high-performance lidar independently developed by Livox for L3 and L4 autonomous driving. Horizon Highway SLAM is a stable, low-drift and real-time SLAM software package developed based on Horizon for high-speed sports scenes. The algorithm is suitable for speed scenes of 0~80km/h, and solves the technical problems of feature extraction in extremely narrow FOV, motion distortion compensation and multi-sensor fusion to avoid scene degradation. For details see:
`Horizon Highway SLAM <https://github.com/Livox-SDK/horizon_highway_slam>`_

Livox-Relocalization
~~~~~~~~~~~~~~~~~~~~~~

Livox-Relocalization is a relocation software package for Livox Lidar developed by Livox. It can help users load the map collected with Mid-40 and use the map to relocate the lidar location information. For details see:
`Livox-Relocalization <https://github.com/Livox-SDK/livox_relocalization>`_


Documentation and Manuals
--------------------------------

Livox Viewer User Manual
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Download link:
`Livox Viewer <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/Livox%20Viewer/Livox%20Viewer%20User%20Manual.pdf>`_

Extension cord adapter box installation model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Download link:
`model <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/extend_coupler_asm.stp>`_

Livox point cloud characteristics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Download link:
`cloud characteristics <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/Point%20cloud%20characteristics.pdf>`_

Livox Avia
~~~~~~~~~~~~~~~~~~~~~~

-  Livox Avia doc link: `Livox Avia doc <https://github.com/Livox-SDK/livox_wiki_en/raw/master/source/doc/Livox_Avia_doc.pdf>`_


Livox Horizon
~~~~~~~~~~~~~~~~~~~~~~

-  Horizon user manual download link: `Livox Horizon User Manuel <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/update/Livox%20Horizon%20User%20Manual%20(EN).pdf>`_

-  Horizon Quick Start Guide download link: `Livox Horizon Quick Start Guide <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/assets/horizon/Livox%20Horizon%20Quick%20Start%20Guide.pdf>`_

-  Livox Horizon doc link: `Livox Horizon doc <https://github.com/Livox-SDK/livox_wiki_en/raw/master/source/doc/Livox_Horizon_doc.pdf>`_

Livox Mid
~~~~~~~~~~~~~~~~~~~~~~

-  Livox Series User Manual v1.0 download link : `Livox Mid Series User Manual v1.2 <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/update/Livox%20Mid%20Series%20User%20Manual%20(EN).pdf>`_

-  Livox Mid-40 Quick Start Guide v1.4 download link : `Livox Mid-40 Quick Start Guide v1.4 multi <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/20190530/Livox%20Mid-40%20Quick%20Start%20Guide%20multi%20v1.4.pdf>`_

-  Livox Mid-100 Quick Start Guide v1.4 download link: `Livox Mid-100 Quick Start Guide v1.4 multi <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/20190530/Livox%20Mid-100%20Quick%20Start%20Guide%20multi%20v1.4.pdf>`_

-  Mid-40 3D Model and FOV Shape download link:  `MID-40 3D Model and FOV Shape <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/MID-40%203D%20Model%20and%20FOV%20Shape.zip>`_

-  Mid-100 3D Model and FOV Shape download link: `MID-100 3D Model and FOV Shape <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/MID-100%203D%20Model%20and%20FOV%20Shape.zip>`_

-  Livox Mid-70 doc link: `Livox Mid-70 doc <https://github.com/Livox-SDK/livox_wiki_en/raw/master/source/doc/Livox_Mid-70_doc.pdf>`_

Livox Tele-15
~~~~~~~~~~~~~~~~~~~~~~

-  Tele-15 User Manual download link:  `Tele-15 User Manual <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/TELE15/Livox%20tele-15%20user%20manual%20v1.0.pdf>`_

-  Tele-15 Quick Start Guide download link:  `Tele-15 Quick Start Guide <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/TELE15/Livox%20Tele-15%20%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8%E6%8C%87%E5%8D%97.pdf>`_

-  Tele-15 3D Model and FOV Shape download link: `Tele-15 3D Model and FOV Shape <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/Tele-15_shell_FOV_3D.stp>`_

-  Tele-15 W/O Dissipation Module 3D Model download link: `Tele-15 W/O Dissipation Module 3D Model <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/Tele-15_withou_self_dissipation_module.stp>`_

-  Livox Tele-15 doc link: `Livox Tele-15 doc <https://github.com/Livox-SDK/livox_wiki_en/raw/master/source/doc/Livox_Tele_doc.pdf>`_

Livox Hub
~~~~~~~~~~~~~~~~~~~~~~

-  Livox Hub User Manual v1.2 download link: `Livox Hub User Manual v1.2 <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/20191128/Livox%20Hub%20Series%20User%20Manual%2020191018.pdf>`_

-  Livox Hub Quick Start Guide v1.0 download link： `Livox Hub Quick Start Guide <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/20190318/Livox%20Hub%20Quick%20Start%20Guide%20v1.0.pdf>`_

-  Livox Hub 3D model download link： `Livox Hub 3D model <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/20190318/Livox%20Hub%203D%20Model.zip>`_

Point Cloud Data
--------------------------

Livox Horizon point cloud data
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Data package 1 download link： `Livox Horizon Point Cloud Data 1 <https://terra-1-g.djicdn.com/65c028cd298f4669a7f0e40e50ba1131/Download/Horizon_%E9%81%93%E8%B7%AF%E5%9C%BA%E6%99%AF%E7%82%B9%E4%BA%91%E6%95%B0%E6%8D%AE_%E5%AE%98%E7%BD%91.lvx>`_

-  Data package 2 download link： `Livox Horizon Point Cloud Data 2 <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/20200107/Sample%20Point%20Cloud%20of%20Horizon.zip>`_ 

Livox Mid-100 Point Cloud Data
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Data package 1 download link: `Livox Mid-100 Point Cloud Data 1 <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/Livox%20Mid-100%20Point%20Cloud%20Data%201.zip>`_

-  Data package 2 download link: `Livox Mid-100 Point Cloud Data 2 <https://www.livoxtech.com/3296f540ecf5458a8829e01cf429798e/downloads/Livox%20Mid-100%20Point%20Cloud%20Data%202.zip>`_


Livox Vehicle Platform
----------------------------

-  Vehicle Platform for Livox lidar 

.. image:: ../image/vehicle_platform.png

download link: `Vehicle Platform DOC <https://github.com/Livox-SDK/livox_wiki_en/tree/master/source/data>`_

