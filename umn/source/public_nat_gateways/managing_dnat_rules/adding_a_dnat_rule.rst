:original_name: en-us_topic_0127489530.html

.. _en-us_topic_0127489530:

Adding a DNAT Rule
==================

Scenarios
---------

After a public NAT gateway is created, you can add DNAT rules to allow servers in your VPC to provide services accessible from the Internet.

You can configure only one DNAT rule for each port on a server. One port can be mapped to only one EIP. If multiple servers need to provide services accessible from the Internet, create multiple DNAT rules.

Prerequisites
-------------

There is a public NAT gateway available.

Procedure
---------

#. Log in to the management console.

#. Click **Service List** in the upper left corner. Under **Network**, select **NAT Gateway**.

   The **Public NAT Gateway** page is displayed.

#. On the displayed page, click the name of the public NAT gateway that you want to add a DNAT rule for.

#. On the public NAT gateway details page, click the **DNAT Rules** tab.

#. Click **Add DNAT Rule**.

#. Configure the required parameters. For details, see :ref:`Table 1 <en-us_topic_0127489530__en-us_topic_0127293986_table30787259144637>`.

   .. _en-us_topic_0127489530__en-us_topic_0127293986_table30787259144637:

   .. table:: **Table 1** Parameter descriptions

      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                                                            |
      +===================================+========================================================================================================================================================================================================================================================================================================+
      | Scenario                          | Select **VPC** if your servers in a VPC will use the DNAT rule to share the same EIP to provide services accessible from the Internet.                                                                                                                                                                 |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | **Direct Connect**: Select this scenario if servers in an on-premises data center connected to a VPC through Direct Connect will use the DNAT rule to provide services accessible from the Internet.                                                                                                   |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Port Type                         | The port type                                                                                                                                                                                                                                                                                          |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | -  **All ports**: This is effectively like having a regular EIP bound to your servers. All requests received by the gateway will be forwarded to your servers, regardless of what port or protocol was used.                                                                                           |
      |                                   | -  **Specific port**: The public NAT gateway forwards requests to your servers only from the outside port and to the inside port configured here, and only if they use the right protocol.                                                                                                             |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Protocol                          | The protocol can be TCP or UDP.                                                                                                                                                                                                                                                                        |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | This parameter is available if you select **Specific port** for **Port Type**. If you select **All ports**, this parameter is **All** by default.                                                                                                                                                      |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | EIP                               | The EIP that will be used by the server to provide services accessible from the Internet                                                                                                                                                                                                               |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | You can select an EIP that either has not been bound, has been bound to a DNAT rule with **Port Type** set to **Specific port** of the current public NAT gateway, or has been bound to an SNAT rule of the current public NAT gateway.                                                                |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Outside Port                      | The port of the EIP                                                                                                                                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | This parameter is only available if you select **Specific port** for **Port Type**. Range: 1 to 65535                                                                                                                                                                                                  |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | You can only enter a specific port number, for example, 80.                                                                                                                                                                                                                                            |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Private IP Address                | -  In a VPC scenario, set this parameter to the IP address of the server in a VPC. This IP address is used by the server to provide services accessible from the Internet through DNAT.                                                                                                                |
      |                                   | -  In a Direct Connect scenario, set this parameter to IP address of the server in your on-premises data center or your private IP address. This IP address is used by local servers that are connected to a VPC through Direct Connect to provide services accessible from the Internet through DNAT. |
      |                                   | -  Configure the port of **Private IP Address** if you select **Specific port** for **Port Type**.                                                                                                                                                                                                     |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Inside Port                       | The port of the server that uses the DNAT rule to provide services accessible from the Internet                                                                                                                                                                                                        |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | This parameter is only available if you select **Specific port** for **Port Type**.                                                                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | Range: 1 to 65535                                                                                                                                                                                                                                                                                      |
      |                                   |                                                                                                                                                                                                                                                                                                        |
      |                                   | You can only enter a specific port number, for example, 80.                                                                                                                                                                                                                                            |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK**.

   Once the rule is created, its status changes to **Running**.

.. important::

   After you add a DNAT rule, add rules to the security group associated with the servers to allow inbound or outbound traffic. Otherwise, the DNAT rule does not take effect.
