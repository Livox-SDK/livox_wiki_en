========================================
Summary of Unofficial Open Source Materials
========================================

Paper
--------------


**Low-cost Retina-like Robotic Lidar Based on Incommensurable Scanning**

-  Abstract： High performance lidars are essential in autonomous robots  such  as  self-driving  cars,  automated  ground  vehicles  and  intelligent machines. Traditional mechanical scanning lidars offer superior  performance  in  autonomous  vehicles,  but  the  potential  mass   application   is   limited   by   the   inherent   manufacturing difficulty.    We    propose    a    robotic    lidar    sensor    based    on    incommensurable   scanning   that allows   straightforward   mass   production and  adoption  in  autonomous  robots.  Some  unique  features  are  additionally  permitted  by  this  incommensurable  scanning. Similar to the fovea in human retina, this lidar features a  peaked  central  angular density,  enabling  in   applications  that prefers eye-like attention. The incommensurable scanning method of  this  lidar  could  also  provide  a  much higher  resolution  than  conventional lidars which is beneficial in robotic applications such as sensor calibration. Examples making use of these advantageous features are demonstrated.  

-  link:`Low-cost Retina-like Robotic Lidar Based on Incommensurable Scanning <https://128.84.21.199/abs/2006.11034>`_


**Loam_livox: A fast, robust, high-precision LiDAR odometry and mapping package for LiDARs of small FoV**

-  Abstract：LiDAR odometry and mapping (LOAM) has been playing an important role in autonomous vehicles, due to its ability to simultaneously localize the robot's pose and build high-precision, high-resolution maps of the surrounding environment. This enables autonomous navigation and safe path planning of autonomous vehicles. In this paper, we present a robust, real-time LOAM algorithm for LiDARs with small FoV and irregular samplings. By taking effort on both front-end and back-end, we address several fundamental challenges arising from such LiDARs, and achieve better performance in both precision and efficiency compared to existing baselines. To share our findings and to make contributions to the community, we open source our codes on Github.

-  link：`Loam_livox: A fast, robust, high-precision LiDAR odometry and mapping package for LiDARs of small FoV <https://arxiv.org/abs/1909.06700>`_

-  code：`Github <https://github.com/Livox-SDK/livox_horizon_loam>`_


**CamVox: A Low-cost and Accurate Lidar-assisted Visual SLAM System**

-   Abstract：Combining lidar in camera-based simultaneous localization and mapping (SLAM) is an effective method in improving overall accuracy, especially at a large scale outdoor scenario. Recent development of low-cost lidars (e.g. Livox lidar) enable us to explore such SLAM systems with lower budget and higher performance. In this paper we propose CamVox by adapting Livox lidars into visual SLAM (ORB-SLAM2) by exploring the lidars' unique features. Based on the non-repeating nature of Livox lidars, we propose an automatic lidar-camera calibration method that will work in uncontrolled scenes. The long depth detection range also benefit a more efficient mapping. Comparison of CamVox with visual SLAM (VINS-mono) and lidar SLAM (LOAM) are evaluated on the same dataset to demonstrate the performance. We open sourced our hardware, code and dataset on GitHub. 

-  link:`CamVox: A Low-cost and Accurate Lidar-assisted Visual SLAM System <https://arxiv.org/abs/2011.11357>`_

-  code：`Github <https://github.com/ISEE-Technology/CamVox>`_


**A fast, complete, point cloud based loop closure for LiDAR odometry and mapping**

-  Abstract：This paper presents a loop closure method tocorrect the long-term drift in LiDAR odometry and mapping(LOAM).Our proposed method computes the 2D histogram of keyframes,a local map patch, and uses the normalizedcross-correlation of the 2D histograms as the similarity metricbetween the current keyframe and those in the map. We showthat this method is fast,invariant to rotation,and producesreliable and accurate loop detection.The proposed method is implemented with careful engineering and integrated into the LOAM algorithm,forming a complete and practical systemready to use.To benefit the community by serving a benchmarkfor loop closure,the entire system is made open source on Github.

-  link：`A fast, complete, point cloud based loop closure for LiDAR odometry and mapping <https://arxiv.org/abs/1909.11811>`_

-  code：`Github <https://github.com/hku-mars/loam_livox>`_

**BALM: Bundle Adjustment for Lidar Mapping**

-  Abstract：We propose a framework for bundle adjustment (BA) on sparse lidar points and incorporate it to a lidar odometry and mapping (LOAM) to lower the drift. A local BA on a sliding window of keyframes has been widely used in visual SLAM and has proved to be very effective in lowering the drift. But in lidar mapping, BA method is hardly used because the sparse feature points (e.g., edge and plane) in a lidar point-cloud make the exact feature matching impossible. Our method is to enforce feature points lie on the same edge or plane by minimizing the eigenvalue of the covariance matrix. To speedup the optimization, we derive the analytical derivatives, up to second order, in closed form. Moreoever, we propose a novel adaptive voxelization method to search feature correspondence efficiently. The proposed formulations are incorporated into a LOAM back-end for map refinement. Results show that, although as a back-end, the local BA can be solved very efficiently, even in real-time at 10Hz when optimizing 20 scans of point-cloud. The local BA also considerably lowers the LOAM drift. Our implementation of the BA optimization and LOAM are open-sourced to benefit the community. 

-  link：`BALM: Bundle Adjustment for Lidar Mapping <https://arxiv.org/abs/2010.08215>`_

-  code：`Github <https://github.com/hku-mars/BALM>`_

**A decentralized framework for simultaneous calibration, localization and mapping with multiple LiDARs**

-   Abstract：LiDAR is playing a more and more essential role in autonomous driving vehicles for objection detection, self localization and mapping. A single LiDAR frequently suffers from hardware failure (e.g., temporary loss of connection) due to the harsh vehicle environment (e.g., temperature, vibration, etc.), or performance degradation due to the lack of sufficient geometry features, especially for solid-state LiDARs with small field of view (FoV). To improve the system robustness and performance in self-localization and mapping, we develop a decentralized framework for simultaneous calibration, localization and mapping with multiple LiDARs. Our proposed framework is based on an extended Kalman filter (EKF), but is specially formulated for decentralized implementation. Such an implementation could potentially distribute the intensive computation among smaller computing devices or resources dedicated for each LiDAR and remove the single point of failure problem. Then this decentralized formulation is implemented on an unmanned ground vehicle (UGV) carrying 5 low-cost LiDARs and moving at 1.3m/s in urban environments. Experiment results show that the proposed method can successfully and simultaneously estimate the vehicle state (i.e., pose and velocity) and all LiDAR extrinsic parameters. The localization accuracy is up to 0.2% on the two datasets we collected. To share our findings and to make contributions to the community, meanwhile enable the readers to verify our work.

-  link：`A decentralized framework for simultaneous calibration, localization and mapping with multiple LiDARs <https://arxiv.org/abs/2007.01483>`_

-  code：`Github <https://github.com/hku-mars/decentralized_loam>`_


**Initial Investigation of a Low-Cost Automotive LIDAR System**

-   Abstract：This investigation focuses on the performance assessment of a low-cost automotive LIDAR, the Livox Mid-40 series. The work aims to examine the qualities of the sensor in terms of ranging, repeatability and accuracy. Towards these aims a series of experiments were carried out based on previous research of low-cost sensor accuracy, LIDAR accuracy investigation and TLS calibration experiments. The Livox Mid-40 series offers the advantage of a long-range detection beyond 200 m at a remarkably low cost. The preliminary results of the tests for this sensor indicate that it can be used for reality capture purposes such as to obtain coarse as-built plans and volume calculations to mention a few. Close-range experiments were conducted in an indoor laboratory setting. Long-range experiments were performed outdoors towards a building façade. Reference values in both setups were provided with a Leica RTC 360 terrestrial LIDAR system. In the close-range experiments a cross section of the point cloud shows a significant level of noise in the acquired data. At a stand-off distance of 5 m the length measurement tests reveal deviations of up to 11 mm to the reference values. Range measurement was tested up to 130 meters and shows ranging deviations of up to 25 millimetres. The authors recommend further investigation of the issues in radiometric behaviour and material reflectivity. Also, more knowledge about the internal components is needed to understand the causes of the concentric ripple effect observed at close ranges. Another aspect that should be considered is the use of targets and their design as the non-standard scan pattern prevents automated detection with standard commercial software.

-  link：`Initial Investigation of a Low-Cost Automotive LIDAR System <https://discovery.ucl.ac.uk/id/eprint/10087172>`_


**Towards high-performance solid-state-lidar-inertial odometry and mapping**

-   Abstract：We present a novel tightly-coupled LiDAR-inertial odometry and mapping scheme for both solid-state and mechanical LiDARs. As frontend, a feature-based lightweight LiDAR odometry provides fast motion estimates for adaptive keyframe selection. As backend, a hierarchical keyframe-based sliding window optimization is performed through marginalization for directly fusing IMU and LiDAR measurements. For the Livox Horizon, a newly released solid-state LiDAR, a novel feature extraction method is proposed to handle its irregular scan pattern during preprocessing. LiLi-OM (Livox LiDAR-inertial odometry and mapping) is real-time capable and achieves superior accuracy over state-of-the-art systems for both LiDAR types on public data sets of mechanical LiDARs and in experiments using the Livox Horizon. Source code and recorded experimental data sets are available on Github. 

-  link：`Towards High-Performance Solid-State-LiDAR-Inertial Odometry and Mapping <https://arxiv.org/abs/2010.13150>`_

-  code：`Github <https://github.com/KIT-ISAS/lili-om>`_


**Accuracy Assessment and Calibration of Low-Cost Autonomous LIDAR Sensors**

-   Abstract：A number of low-cost, small form factor, high resolution lidar sensors have recently been commercialized in an effort to fill thegrowing needs for lidar sensors on autonomous vehicles. These lidar sensors often report performance as range precision and angularaccuracy, which are insufficient to characterize the overall quality of the point clouds returned by these sensors. Herein, a detailedgeometric accuracy analysis of two representative autonomous sensors, the Ouster OSI-64 and the Livox Mid-40, is presented. Thescanners were analyzed through a rigorous least squares adjustment of data from the two sensors using planar surface constraints.The analysis attempts to elucidate the overall point cloud accuracy and presence of systematic errors for the sensors over medium (<40 m) ranges.

-  link：`Accuracy Assessment and Calibration of Low-Cost Autonomous LIDAR Sensors <https://search.proquest.com/openview/6f17add1979112225261ab18249b02af/1?pq-origsite=gscholar&cbl=2037674>`_



**UAV LiDAR Point Cloud Segmentation of A Stack Interchange with Deep Neural Networks**

-  Abstract：Stack interchanges are essential components of transportation systems. Mobile laser scanning (MLS) systemshave been widely used in road infrastructure mapping, but accu-rate mapping of complicated multi-layer stack interchanges arestill challenging. This study examined the point clouds collectedby a new Unmanned Aerial Vehicle (UAV) Light Detection andRanging (LiDAR) system to perform the semantic segmentationtask  of  a  stack  interchange.  An  end-to-end  supervised  3D  deeplearning  framework  was  proposed  to  classify  the  point  clouds.The  proposed  method  has  proven  to  capture  3D  features  incomplicated interchange scenarios with stacked convolution andthe result achieved over 93% classification accuracy. In addition,the   new   low-cost   semi-solid-state   LiDAR   sensor   Livox   Mid-40  featuring  a  incommensurable  rosette  scanning  pattern  hasdemonstrated  its  potential  in  high-definition  urban  mapping.

-  link：`UAV LiDAR Point Cloud Segmentation of A Stack Interchange with Deep Neural Networks <https://arxiv.org/abs/2010.11106>`_


**FAST-LIO: A Fast, Robust LiDAR-inertial Odometry Package by Tightly-Coupled Iterated Kalman Filter**

-  Abstract： This paper presents a computationally efficient and robust LiDAR-inertial odometry framework. We fuse LiDAR feature points with IMU data using a tightly-coupled iterated extended Kalman filter to allow robust navigation in fast-motion, noisy or cluttered environments where degeneration occurs. To lower the computation load in the presence of large number of measurements, we present a new formula to compute the Kalman gain. The new formula has computation load depending on the state dimension instead of the measurement dimension. The proposed method and its implementation are tested in various indoor and outdoor environments. In all tests, our method produces reliable navigation results in real-time: running on a quadrotor onboard computer, it fuses more than 1,200 effective feature points in a scan and completes all iterations of an iEKF step within 25 ms. Our codes are open-sourced online. 

-  link：`FAST-LIO: A Fast, Robust LiDAR-inertial Odometry Package by Tightly-Coupled Iterated Kalman Filter <https://arxiv.org/abs/2010.08196>`_

-  code：`Github <https://github.com/hku-mars/FAST_LIO>`_



**VIO-UWB-Based Collaborative Localization and Dense Scene Reconstruction within Heterogeneous Multi-Robot Systems**

-  Abstract： Effective collaboration in multi-robot systems requires accurate and robust estimation of relative localization: from cooperative manipulation to collaborative sensing, and including cooperative exploration or cooperative transportation. This paper introduces a novel approach to collaborative localization for dense scene reconstruction in heterogeneous multi-robot systems comprising ground robots and micro-aerial vehicles (MAVs). We solve the problem of full relative pose estimation without sliding time windows by relying on UWB-based ranging and Visual Inertial Odometry (VIO)-based egomotion estimation for localization, while exploiting lidars onboard the ground robots for full relative pose estimation in a single reference frame. During operation, the rigidity eigenvalue provides feedback to the system. To tackle the challenge of path planning and obstacle avoidance of MAVs in GNSS-denied environments, we maintain line-of-sight between ground robots and MAVs. Because lidars capable of dense reconstruction have limited FoV, this introduces new constraints to the system. Therefore, we propose a novel formulation with a variant of the Dubins multiple traveling salesman problem with neighborhoods (DMTSPN) where we include constraints related to the limited FoV of the ground robots. Our approach is validated with simulations and experiments with real robots for the different parts of the system. 

-  link：`VIO-UWB-Based Collaborative Localization and Dense Scene Reconstruction within Heterogeneous Multi-Robot Systems <https://arxiv.org/abs/2011.00830>`_

-  code：`Github <https://github.com/TIERS>`_


**A Survey of Simultaneous Localization and Mapping with an Envision in 6G Wireless Networks**

-   Abstract： Simultaneous Localization and Mapping (SLAM) achieves the purpose of simultaneous positioning and map construction based on self-perception. The paper makes an overview in SLAM including Lidar SLAM, visual SLAM, and their fusion. For Lidar or visual SLAM, the survey illustrates the basic type and product of sensors, open source system in sort and history, deep learning embedded, the challenge and future. Additionally, visual inertial odometry is supplemented. For Lidar and visual fused SLAM, the paper highlights the multi-sensors calibration, the fusion in hardware, data, task layer. The open question and forward thinking with an envision in 6G wireless networks end the paper. The contributions of this paper can be summarized as follows: the paper provides a high quality and full-scale overview in SLAM. It's very friendly for new researchers to hold the development of SLAM and learn it very obviously. Also, the paper can be considered as a dictionary for experienced researchers to search and find new interesting orientation.  

-  link：`A Survey of Simultaneous Localization and Mapping with an Envision in 6G Wireless Networks <https://arxiv.org/abs/1909.05214>`_


**Review on 3D Lidar Localization for Autonomous Driving Cars**

-  Abstract： LiDAR sensors are becoming one of the most essential sensors in achieving full autonomy for self driving cars. LiDARs are able to produce rich, dense and precise spatial data, which can tremendously help in localizing and tracking a moving vehicle. In this paper, we review the latest finding in 3D LiDAR localization for autonomous driving cars, and analyse the results obtained by each method, in an effort to guide the research community towards the path that seems to be the most promising.   

-  link：`Review on 3D Lidar Localization for Autonomous Driving Cars <https://arxiv.org/abs/2006.00648>`_


**ACSC: Automatic Calibration for Non-repetitive Scanning Solid-State LiDAR and Camera Systems**

-  Abstract： Recently, the rapid development of Solid-State LiDAR (SSL) enables low-cost and efficient obtainment of 3D point clouds from the environment, which has inspired a large quantity of studies and applications. However, the non-uniformity of its scanning pattern, and the inconsistency of the ranging error distribution bring challenges to its calibration task. In this paper, we proposed a fully automatic calibration method for the non-repetitive scanning SSL and camera systems. First, a temporal-spatial-based geometric feature refinement method is presented, to extract effective features from SSL point clouds; then, the 3D corners of the calibration target (a printed checkerboard) are estimated with the reflectance distribution of points. Based on the above, a target-based extrinsic calibration method is finally proposed. We evaluate the proposed method on different types of LiDAR and camera sensor combinations in real conditions, and achieve accuracy and robustness calibration results. The code is available at this https URL.   

-  link：`ACSC: Automatic Calibration for Non-repetitive Scanning Solid-State LiDAR and Camera Systems <https://arxiv.org/abs/2011.08516>`_

-  code：`Github <https://github.com/HViktorTsoi/ACSC>`_


**Autonomous Dam Surveillance Robot System Based on Multi-Sensor Fusion**

-  Abstract： Dams are important engineering facilities in the water conservancy industry. They have many functions, such as flood control, electric power generation, irrigation, water supply, shipping, etc. Therefore, their long-term safety is crucial to operational stability. Because of the complexity of the dam environment, robots with various kinds of sensors are a good choice to replace humans to perform a surveillance job. In this paper, an autonomous system design is proposed for dam ground surveillance robots, which includes general solution, electromechanical layout, sensors scheme, and navigation method. A strong and agile skid-steered mobile robot body platform is designed and created, which can be controlled accurately based on an MCU and an onboard IMU. A novel low-cost LiDAR is adopted for odometry estimation. To realize more robust localization results, two Kalman filter loops are used with the robot kinematic model to fuse wheel encoder, IMU, LiDAR odometry, and a low-cost GNSS receiver data. Besides, a recognition network based on YOLO v3 is deployed to realize real-time recognition of cracks and people during surveillance. As a system, by connecting the robot, the cloud server and the users with IOT technology, the proposed solution could be more robust and practical.    

-  link：`Autonomous Dam Surveillance Robot System Based on Multi-Sensor Fusion <https://www.mdpi.com/1424-8220/20/4/1097/htm>`_
