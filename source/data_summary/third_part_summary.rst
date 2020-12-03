========================================
Summary of Unofficial Open Source Materials
========================================

Paper
--------------

**Low-cost Retina-like Robotic Lidar Based on Incommensurable Scanning**

-  High performance lidars are essential in autonomous robots  such  as  self-driving  cars,  automated  ground  vehicles  and  intelligent machines. Traditional mechanical scanning lidars offer superior  performance  in  autonomous  vehicles,  but  the  potential  mass   application   is   limited   by   the   inherent   manufacturing difficulty.    We    propose    a    robotic    lidar    sensor    based    on    incommensurable   scanning   that allows   straightforward   mass   production and  adoption  in  autonomous  robots.  Some  unique  features  are  additionally  permitted  by  this  incommensurable  scanning. Similar to the fovea in human retina, this lidar features a  peaked  central  angular density,  enabling  in   applications  that prefers eye-like attention. The incommensurable scanning method of  this  lidar  could  also  provide  a  much higher  resolution  than  conventional lidars which is beneficial in robotic applications such as sensor calibration. Examples making use of these advantageous features are demonstrated.  

-  link:`Low-cost Retina-like Robotic Lidar Based on Incommensurable Scanning <https://128.84.21.199/abs/2006.11034>`_


**Loam_livox: A fast, robust, high-precision LiDAR odometry and mapping package for LiDARs of small FoV**

-  LiDAR odometry and mapping (LOAM) has been playing an important role in autonomous vehicles, due to its ability to simultaneously localize the robot's pose and build high-precision, high-resolution maps of the surrounding environment. This enables autonomous navigation and safe path planning of autonomous vehicles. In this paper, we present a robust, real-time LOAM algorithm for LiDARs with small FoV and irregular samplings. By taking effort on both front-end and back-end, we address several fundamental challenges arising from such LiDARs, and achieve better performance in both precision and efficiency compared to existing baselines. To share our findings and to make contributions to the community, we open source our codes on Github.

-  link：`Loam_livox: A fast, robust, high-precision LiDAR odometry and mapping package for LiDARs of small FoV <https://arxiv.org/abs/1909.06700>`_

-  code：`Github <https://github.com/Livox-SDK/livox_horizon_loam>`_

**A fast, complete, point cloud based loop closure for LiDAR odometry and mapping**

-  This paper presents a loop closure method tocorrect the long-term drift in LiDAR odometry and mapping(LOAM).Our proposed method computes the 2D histogram of keyframes,a local map patch, and uses the normalizedcross-correlation of the 2D histograms as the similarity metricbetween the current keyframe and those in the map. We showthat this method is fast,invariant to rotation,and producesreliable and accurate loop detection.The proposed method is implemented with careful engineering and integrated into the LOAM algorithm,forming a complete and practical systemready to use.To benefit the community by serving a benchmarkfor loop closure,the entire system is made open source on Github.

-  link：`A fast, complete, point cloud based loop closure for LiDAR odometry and mapping <https://arxiv.org/abs/1909.11811>`_

-  code：`Github <https://github.com/hku-mars/loam_livox>`_

**BALM: Bundle Adjustment for Lidar Mapping**

-  This paper proposes a framework for bundle adjustment (BA) on sparse lidar points and incorporate it to a lidar odometry and mapping (LOAM) to lower the drift

-  link：`BALM: Bundle Adjustment for Lidar Mapping <https://arxiv.org/abs/2010.08215>`_

-  code：`Github <https://github.com/hku-mars/BALM>`_

**A decentralized framework for simultaneous calibration, localization and mapping with multiple LiDARs**

-   This paper proposes a decentralized framework for simultaneous calibration, localization and mapping with multiple LiDARs.

-  link：`A decentralized framework for simultaneous calibration, localization and mapping with multiple LiDARs <https://arxiv.org/abs/2007.01483>`_

-  code：`Github <https://github.com/hku-mars/decentralized_loam>`_

