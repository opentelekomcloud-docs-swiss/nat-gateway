:original_name: nat_pro_0002.html

.. _nat_pro_0002:

Scenarios
=========

Public NAT Gateway
------------------

-  **Allowing a private network to access the Internet using SNAT**

   If your servers in a VPC need to access the Internet, you can configure SNAT rules to let these servers use one or more EIPs to access the Internet without exposing their private IP addresses. You can configure only one SNAT rule for each subnet in a VPC, and select one or more EIPs for each SNAT rule. Public NAT Gateway provides different numbers of connections, and you can create multiple SNAT rules to meet your service requirements.

   :ref:`Figure 1 <nat_pro_0002__fig136410435334>` shows how servers in a VPC access the Internet using SNAT.

   .. _nat_pro_0002__fig136410435334:

   .. figure:: /_static/images/en-us_image_0000001385259272.png
      :alt: **Figure 1** Using SNAT to enable servers in a VPC to access the Internet

      **Figure 1** Using SNAT to enable servers in a VPC to access the Internet

-  **Allowing Internet users to access a service in a private network using DNAT**

   DNAT rules enable servers in a VPC to provide services accessible from the Internet.

   After receiving requests from a specific port over a specific protocol, the public NAT gateway can forward the requests to a specific port of a server through port mapping. The public NAT gateway can also forward all requests destined for an EIP to a specific server through IP address mapping.

   One DNAT rule can be configured for each server. If there are multiple servers, you can create multiple DNAT rules to map one or more EIPs to the private IP addresses of these servers.

   :ref:`Figure 2 <nat_pro_0002__fig423465393415>` shows how servers (ECSs or ) in a VPC provide services accessible from the Internet using DNAT.

   .. _nat_pro_0002__fig423465393415:

   .. figure:: /_static/images/en-us_image_0000001435778377.png
      :alt: **Figure 2** Using DNAT to enable servers in a VPC to provide services accessible from the Internet

      **Figure 2** Using DNAT to enable servers in a VPC to provide services accessible from the Internet

-  **Allowing servers in an on-premises data center to access the Internet or be accessible from the Internet**

   In certain Internet, gaming, e-commerce, and financial scenarios, a large number of servers in a private cloud are connected to a VPC through Direct Connect or VPN. If such servers need secure, high-speed Internet access or need to provide services accessible from the Internet, you can deploy a NAT gateway and configure SNAT and DNAT rules to meet their requirements.

   :ref:`Figure 3 <nat_pro_0002__fig1264218457350>` shows how to use SNAT and DNAT to provide high-speed Internet access or provide services accessible from the Internet.

   .. _nat_pro_0002__fig1264218457350:

   .. figure:: /_static/images/en-us_image_0000001385738376.png
      :alt: **Figure 3** Using SNAT and DNAT to enable high-speed communication with the Internet

      **Figure 3** Using SNAT and DNAT to enable high-speed communication with the Internet
