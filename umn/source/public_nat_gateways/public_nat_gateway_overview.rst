:original_name: nat_publicnat_0001.html

.. _nat_publicnat_0001:

Public NAT Gateway Overview
===========================

Public NAT gateways provide network address translation with 20 Gbit/s of bandwidth for ECSs in a VPC, or servers in on-premises data centers that connect to a VPC through Direct Connect or VPN, allowing these servers to share EIPs to access the Internet or provide services accessible from the Internet.

The process of using a public NAT gateway is as follows:


.. figure:: /_static/images/en-us_image_0260279602.png
   :alt: **Figure 1** Process of using a public NAT gateway

   **Figure 1** Process of using a public NAT gateway

.. note::

   An SNAT rule and a DNAT rule cannot share the same EIP. Therefore, if you need to create an SNAT rule and a DNAT rule separately, assign two EIPs.
