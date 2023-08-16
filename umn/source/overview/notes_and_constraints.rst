:original_name: en-us_topic_0086739750.html

.. _en-us_topic_0086739750:

Notes and Constraints
=====================

Public NAT Gateway
------------------

When using a public NAT gateway:

-  Multiple rules for one public NAT gateway can use the same EIP, but the rules for different NAT gateways must use different EIPs.
-  Each VPC can only have one NAT gateway.
-  Only one SNAT rule can be added for each VPC subnet.
-  SNAT and DNAT rules cannot use the same EIP.
-  DNAT rules cannot map virtual IP addresses to EIPs.
-  If both an EIP and a public NAT gateway are configured for a server, data will be forwarded through the EIP.
-  If the rule is used in the Direct Connect scenario, the custom CIDR block must be a CIDR block of a Direct Connect connection and cannot overlap with the NAT gateway's VPC subnets.
-  Only one DNAT rule can be configured for each port on a server. One port can be mapped to only one EIP.
-  Up to 200 DNAT rules can be added to a public NAT gateway. The number of SNAT rules that can be added to a public NAT gateway is not limited.
