The hms_code in the communication protocol is the diagnostic code of Avia2, which is pushed actively by the device. It is used to notify some special situations or help users quickly troubleshoot equipment failures.

.. _Composition format Avia2:

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

+---------+----------------+--------------------------------------------------------------------------------------------------------------+
| value   | level          | description                                                                                                  |
+=========+================+==============================================================================================================+
| 0x01    | Info           | Notification during normal work                                                                              |
+---------+----------------+--------------------------------------------------------------------------------------------------------------+
| 0x02    | Warning        | There might be problems, which will influence the normal work, please troubleshoot in time                   |
+---------+----------------+--------------------------------------------------------------------------------------------------------------+
| 0x03    | Error          | Device works in abnormal situation, please check the problem in time; long-term operation in this state may  |
|         |                | cause permanent unrecoverable damage                                                                         |
+---------+----------------+--------------------------------------------------------------------------------------------------------------+
| 0x04    | fatal          | Serious abnormal happened, there might be physically unrecoverable risk, the device will stop working now    |
+---------+----------------+--------------------------------------------------------------------------------------------------------------+


Parsing example
~~~~~~~~~~~~~~~~~~~~~~

For example, an HMS code: 0x01060002, refer to :ref:`Composition format<Composition format Avia2>`,
the abnormal ID is 0x0106, and the abnormal level is 0x02(Warning).

Refer to below HMS code table, the code represents "Fan speed may be abnormal", the abnormal level is warning,
and the suggested action is "Please check the fan status".

Diagnostic codes table
~~~~~~~~~~~~~~~~~~~~~~

==================  ================== ============================================================================= ==============================================================================================================
abnormal ID         abnormal level     abnormal description                                                          suggested solution
------------------  ------------------ ----------------------------------------------------------------------------- --------------------------------------------------------------------------------------------------------------
0x0106              warning            Fan speed may be abnormal                                                     Please check the fan status
0x0210              warning            Scan module speed is switching                                                Please wait for the speed to be stable
0x0211-0x021B       fatal              Scan module is abnormal                                                       Please wait, if it lasts too long, please try restarting the device to restore
0x0310-0x0312       warning            Internal module over-temperature                                              Please check the heat dissipation condition of the device
0x0313              warning            Ranging module optical power margin warning, please pay attention to eye      Please wait, if it lasts too long, please try restarting the device to restore
                                       safety
0x0314              fatal              Ranging module optical power margin abnormal, please pay attention to eye     Please try restarting to restore
                                       safety
0x0315              warning            Ranging module may be abnormal                                                Please try restarting to restore, or contact Livox technical support
0x0316              warning            Test environment detection warning                                            Please check whether there are highly reflective or fully reflective objects in the scene and remove them in
                                                                                                                     time, otherwise the device may be damaged
0x0317-0x0318       fatal              Test environment detection error                                              Please check whether there are highly reflective or fully reflective objects in the scene and remove them,
                                                                                                                     then restart the device to restore, otherwise the device may be damaged
0x0402              warning            PTP time synchronization stopped, or time gap is too big                      Please check whether the PTP clock source is working normally
0x0403              warning            The version of PTP is 1588-v2.1, device does not support this version         Please replace with 1588-v2.0 version for synchronization
0x0404              warning            PPS synchronization abnormal                                                  Please check the PPS and GPS signal
0x0407              warning            GPS time synchronization fails because of missing GPS signal                  Please check the GPS signal
0x0408              warning            GPS time synchronization fails because of missing PPS signal                  Please check the PPS signal
0x0409              warning            GPS signal is abnormal                                                        Please check the GPS signal source
0x040A              warning            Multiple time synchronization signals exist at the same time, synchronization Please check the network topology, use only one synchronization method alone
                                       may have problems
==================  ================== ============================================================================= ==============================================================================================================
