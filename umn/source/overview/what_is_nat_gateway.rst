:original_name: en-us_topic_0086739762.html

.. _en-us_topic_0086739762:

What Is NAT Gateway?
====================

Public NAT gateways are used to provide NAT.

Public NAT Gateways
-------------------

A public NAT gateway enables cloud and on-premises servers in a private subnet to access the Internet or provide services accessible from the Internet. Cloud servers are ECSs in a VPC. On-premises servers are servers in on-premises data centers that connect to a VPC through Direct Connect or Virtual Private Network (VPN). A public NAT gateway supports up to 20 Gbit/s of bandwidth.

Public NAT gateways offer source NAT (SNAT) and destination NAT (DNAT).

-  SNAT translates private IP addresses into elastic IP addresses (EIPs), allowing traffic from a private network to go out to the Internet.

   :ref:`Figure 1 <en-us_topic_0086739762__fig198671834111614>` shows how an SNAT rule works.

   .. _en-us_topic_0086739762__fig198671834111614:

   .. figure:: /_static/images/en-us_image_0000001362369170.png
      :alt: **Figure 1** NAT gateway with an SNAT rule

      **Figure 1** NAT gateway with an SNAT rule

-  DNAT enables multiple servers within an AZ or across multiple AZs in a VPC to share EIPs to provide services accessible from the Internet. With an EIP, a NAT gateway forwards the Internet requests from only a specific port and over a specific protocol to a specific port of a server, or it can forward all requests to the server regardless of which port they originated on.

   :ref:`Figure 2 <en-us_topic_0086739762__fig19521019227>` shows how a DNAT rule works.

   .. _en-us_topic_0086739762__fig19521019227:

   .. figure:: /_static/images/en-us_image_0000001412979853.png
      :alt: **Figure 2** NAT gateway with a DNAT rule

      **Figure 2** NAT gateway with a DNAT rule

How Do I Access the NAT Gateway Service?
----------------------------------------

You can access the NAT Gateway service through the management console or using HTTPS-based APIs.

-  Management console

   Log in to the management console and choose **NAT Gateway** from the service list to perform operations on the NAT gateway.

-  APIs

   Use APIs if you need to integrate NAT Gateway into your own system solution. For details, see the `NAT Gateway API Reference <https://docs.sc.otc.t-systems.com/api/nat/nat_api_0047.html>`__.
