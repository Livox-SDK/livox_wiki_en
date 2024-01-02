The HMS(health management system) codes in the communication protocols are the diagnostic codes of Mid360, which push periodically by the lidar. They are used to notify some special situations or help users check equipment failures.

.. _Composition format:

Composition format
~~~~~~~~~~~~~~~~~~~~~~
A complete HMS code is a 4 bytes(uint32) code.
It consists of an abnormal ID and abnormal level, which is shown below:

+---------------+---------+----------------+
| Byte[3:2]     | Byte[1] | Byte[0]        |
+===============+=========+================+
| Abnormal ID   | RSVD    | Abnormal level |
+---------------+---------+----------------+


In addition, an abnormal level is a value that is not equal to 0, the value is bigger, and the problem is more serious.
As is shown below: 

+---------+----------------+--------------------------------------------------------------------------------------------+
| value   | level          | description                                                                                |
+=========+================+============================================================================================+
| 0x01    | Info           | Notification during normal work                                                            |
+---------+----------------+--------------------------------------------------------------------------------------------+
| 0x02    | Warning        | There might be problems, which will influence the normal work                              |
+---------+----------------+--------------------------------------------------------------------------------------------+
| 0x03    | Error          | Device work in abnormal situation, please check the problem in time                        |
+---------+----------------+--------------------------------------------------------------------------------------------+
| 0x04    | fatal          | Serious abnormal happened, it might not be recovered, lidar will stop working now          |
+---------+----------------+--------------------------------------------------------------------------------------------+


Parsing example
~~~~~~~~~~~~~~~~~~~~~~

For example, an HMS code: 0x01020002, refer to :ref:`Composition format<Composition format>`,
the abnormal ID is 0x0102, and the abnormal level is 0x02(warning)。

Refer to below HMS code table, the code represents “environment temperature is slightly high”, the abnormal level is warning,
suggested action is “Please check the environment temperature and losing heat measures”。

Diagnostic codes table
~~~~~~~~~~~~~~~~~~~~~~

==================  ================== ============================================================================= ================================================================================                                       
abnormal ID         abnormal level     abnormal description                                                          suggested solution
------------------  ------------------ ----------------------------------------------------------------------------- --------------------------------------------------------------------------------                                         
0x0102              warning            Environment temperature is slightly high                                      Please check the environment temperature and losing heat measures
0x0103              warning            Environment temperature is relatively high                                    Please check the environment temperature and losing heat measures
0x0104              warning            The window is dirty, which will influence the reliability of the point cloud  Please clean the window
0x0105              warning            An error occurred during device upgrade process                               Please restart the upgrade process
0x0111              fatal              Abnormal temperature of internal components of the device                     Please check the environment temperature and losing heat measures
0x0112              fatal              Abnormal temperature of internal components of the device                     Please check the environment temperature and losing heat measures
0x0113              fatal              IMU stopped working                                                           Please try to restart the device to restore
0x0114              error              Environment temperature is high                                               Please check the environment temperature and losing heat measures
0x0115              fatal              Environment temperature beyond the limit, the device has stopped working      Please check the environment temperature and losing heat measures
0x0116              fatal              Abnormal external voltage                                                     Please check the external voltage
0x0117              fatal              Abnormal lidar parameters                                                     Please try to restart the device to restore
0x0201              warning            Scan module is heating                                                        Please wait for the scan module heating
0x0210-0x0219       error              Scan module is abnormal, the system is trying to recover                      Please wait, if it lasts too long, please try restarting the device to restore
0x0210-0x0219       fatal              Scan module is abnormal                                                       Please try to restart the device to restore
0x0401              warning            Communication link was linked down, now it is recovered                       Please check the communication link
0x0402              warning            PTP time synchronization stop or time gap is too big                          Please check the PTP time source
0x0403              warning            The version of PTP is 1588-v2.1, device don't support this version            Please replace 1588-v2.1 version with 1588.2.0 version
0x0404              warning            PPS time synchronization abnormal                                             Please check the PPS and GPS signal
0x0405              warning            There was an exception in time synchronization                                Please check the exception reason
0x0406              warning            Time synchronization accuracy is low                                          Please check the time source
0x0407              warning            PPS time synchronization fails because of loss of GPS signal                  Please check the GPS signal
0x0408              warning            PPS time synchronization fails because of loss of PPS signal                  Please check the PPS signal
0x0409              warning            GPS signal is abnormal                                                        Please check the GPS time source
0x040A              warning            The PTP and GPTP signals exist at the same time                               Please check the network topology, use PTP or GPTP alone to synchronize
==================  ================== ============================================================================= ================================================================================