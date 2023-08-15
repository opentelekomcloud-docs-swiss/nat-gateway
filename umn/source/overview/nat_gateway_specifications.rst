:original_name: en-us_topic_0086739763.html

.. _en-us_topic_0086739763:

NAT Gateway Specifications
==========================

The NAT gateway performance is determined by the maximum number of SNAT connections supported.

Public NAT Gateway
------------------

An SNAT connection consists of a source IP address, source port, destination IP address, destination port, and a transport layer protocol. The source IP address is the EIP, and the source port is the EIP port. An SNAT connection uniquely identifies a session.

Throughput is the total bandwidth of all EIPs in DNAT rules. For example, a public NAT gateway has two DNAT rules. The EIP bandwidth in the first DNAT rule is 10 Mbit/s, and that in the second DNAT rule is 5 Mbit/s. The throughput of the public NAT gateway will be 15 Mbit/s.

Select a public NAT gateway based on your service requirements. :ref:`Table 1 <en-us_topic_0086739763__table39923257151849>` lists the public NAT gateway specifications.

.. _en-us_topic_0086739763__table39923257151849:

.. table:: **Table 1** Public NAT gateway specifications

   ============== ================================== =========
   Specifications Maximum Number of SNAT Connections Bandwidth
   ============== ================================== =========
   Small          10,000                             20 Gbit/s
   Medium         50,000                             20 Gbit/s
   Large          200,000                            20 Gbit/s
   Extra-large    1,000,000                          20 Gbit/s
   ============== ================================== =========
