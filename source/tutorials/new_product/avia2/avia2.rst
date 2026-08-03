=================
Avia2
=================

Communication Protocol
------------------------

.. toctree::

    livox_eth_protocol_avia2.md

Supported Time Synchronization Methods
------------------------------------------------

**GPS**\ : Second pulse + SDK protocol time data, see details: :ref:`GPS Time Synchronization <GPS Time Synchronization>`;

**NTP**\ : Network Time Protocol, see details: :ref:`NTP Time Synchronization <NTP Time Synchronization>`;

**PTP**\ : IEEE 1588v2.0 UDP/IP Network protocol synchronization, see details: :ref:`PTP Time Synchronization <PTP Time Synchronization>`;

**gPTP**: Automotive ethernet time synchronization protocol(2 layer), see details: :ref:`gPTP Time Synchronization <gPTP Time Synchronization>`;

**GPS**\ : Second pulse + GPRMC time data to form GPS time synchronization mode, see details: :ref:`GPS Time Synchronization <GPS Time Synchronization>`;

Notice:

* The time limit for GPS time synchronization is from 1/1/2000 to 31/12/2037
* PTP time synchronization does not support IEEE1588v2.1
* Not recommended for use in scenarios where IEEE1588v2.0 and gPTP coexist;

HMS Diagnostic Code Introduction
------------------------------------
.. toctree::

    hms_code_avia2.rst
