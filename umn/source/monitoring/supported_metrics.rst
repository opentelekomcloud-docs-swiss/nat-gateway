:original_name: nat_ces_0002.html

.. _nat_ces_0002:

Supported Metrics
=================

Description
-----------

This section describes metrics reported by NAT Gateway to Cloud Eye as well as their namespaces, monitoring metrics, and dimensions. You can use the management console or the APIs provided by Cloud Eye to query the metrics generated for NAT Gateway.

Namespace
---------

SYS.NAT

Metrics
-------

.. table:: **Table 1** Public NAT gateway metrics

   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | Metric ID                | Name                     | Description                                                                                                                                           | Value Range | Monitored Object   | Monitoring Period (Raw Data) |
   +==========================+==========================+=======================================================================================================================================================+=============+====================+==============================+
   | snat_connection          | SNAT Connections         | Number of SNAT connections of the NAT gateway                                                                                                         | >= 0        | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: Count                                                                                                                                           |             |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | inbound_bandwidth        | Inbound Bandwidth        | Inbound bandwidth of servers using the SNAT function                                                                                                  | >= 0        | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: bit/s                                                                                                                                           | bits/s      |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | outbound_bandwidth       | Outbound Bandwidth       | Outbound bandwidth of servers using the SNAT function                                                                                                 | >= 0        | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: bit/s                                                                                                                                           | bits/s      |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | inbound_pps              | Inbound PPS              | Inbound PPS of servers using the SNAT function                                                                                                        | >= 0        | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: Count                                                                                                                                           |             |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | outbound_pps             | Outbound PPS             | Outbound PPS of servers using the SNAT function                                                                                                       | >= 0        | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: Count                                                                                                                                           |             |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | inbound_traffic          | Inbound Traffic          | Inbound traffic of servers using the SNAT function                                                                                                    | >= 0 bytes  | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: byte                                                                                                                                            |             |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | outbound_traffic         | Outbound Traffic         | Outbound traffic of servers using the SNAT function                                                                                                   | >= 0 bytes  | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: byte                                                                                                                                            |             |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | snat_connection_ratio    | SNAT Connection Usage    | SNAT connection usage of the NAT gateway                                                                                                              | >= 0        | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | The maximum number of connections is the number of connections allowed by a NAT gateway type. .                                                       |             |                    |                              |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: Percent                                                                                                                                         |             |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | inbound_bandwidth_ratio  | Inbound Bandwidth Usage  | Inbound bandwidth usage of servers using the SNAT function. The maximum bandwidth supported by a NAT gateway is 20 Gbit/s.                            | >= 0        | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: Percent                                                                                                                                         |             |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+
   | outbound_bandwidth_ratio | Outbound Bandwidth Usage | Outbound bandwidth usage of servers using the SNAT function                                                                                           | >= 0        | Public NAT gateway | 1 minute                     |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | The maximum bandwidth supported by a NAT gateway is 20 Gbit/s. Outbound bandwidth usage = Used bandwidth/Maximum bandwidth of the NAT gateway x 100%. |             |                    |                              |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | Unit: Percent                                                                                                                                         |             |                    |                              |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          | .. note::                                                                                                                                             |             |                    |                              |
   |                          |                          |                                                                                                                                                       |             |                    |                              |
   |                          |                          |    This metric is used to monitor the performance of NAT gateways instead of the EIP bandwidth.                                                       |             |                    |                              |
   +--------------------------+--------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-------------+--------------------+------------------------------+

Dimensions
----------

============== =====================
Key            Value
============== =====================
nat_gateway_id Public NAT gateway ID
============== =====================
