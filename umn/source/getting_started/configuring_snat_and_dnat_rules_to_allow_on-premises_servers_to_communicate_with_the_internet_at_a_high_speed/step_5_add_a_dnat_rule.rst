:original_name: nat_qs_0018.html

.. _nat_qs_0018:

Step 5: Add a DNAT Rule
=======================

Scenarios
---------

After a public NAT gateway is created, you can add DNAT rules to allow servers in your on-premises data center to provide services accessible from the Internet.

You can configure a DNAT rule for each port on a server. If there are multiple servers, you can create multiple DNAT rules to allow servers to share EIPs.

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

#. Configure the required parameters. For details, see :ref:`Table 1 <nat_qs_0018__table30787259144637>`.

   .. _nat_qs_0018__table30787259144637:

   .. table:: **Table 1** Parameter descriptions

      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                |
      +===================================+============================================================================================================================================================================================================================================================+
      | Scenario                          | Select **Direct Connect** if servers in your data center need to access the Internet.                                                                                                                                                                      |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | Servers in your data center that connected to a VPC using Direct Connect can use the DNAT rule to provide services accessible from the Internet.                                                                                                           |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Port Type                         | The port type                                                                                                                                                                                                                                              |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | -  **All ports**: This is effectively like having a regular EIP bound to your servers. All requests received by the gateway will be forwarded to your servers, regardless of what port or protocol was used.                                               |
      |                                   | -  **Specific port**: The public NAT gateway forwards requests to your servers only from the outside port and to the inside port configured here, and only if they use the right protocol.                                                                 |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Protocol                          | The protocol can be TCP or UDP.                                                                                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | This parameter is available if you select **Specific port** for **Port Type**. If you select **All ports**, this parameter is **All** by default.                                                                                                          |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | EIP                               | The EIP that will be used by the server to provide services accessible from the Internet                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | You can select an EIP that either has not been bound, has been bound to a DNAT rule with **Port Type** set to **Specific port** of the current public NAT gateway, or has been bound to an SNAT rule of the current public NAT gateway.                    |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Outside Port                      | The port of the EIP                                                                                                                                                                                                                                        |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | This parameter is only available if you select **Specific port** for **Port Type**.                                                                                                                                                                        |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | Range: 1 to 65535                                                                                                                                                                                                                                          |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | You can only enter a specific port number, for example, 80.                                                                                                                                                                                                |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Private IP Address                | The IP address of the server in your on-premises data center or your private IP address                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | This IP address is used by local servers that are connected to a VPC through Direct Connect to provide services accessible from the Internet through DNAT. Configure the port of **Private IP Address** if you select **Specific port** for **Port Type**. |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | This IP address is used by the server to provide services through DNAT.                                                                                                                                                                                    |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Inside Port                       | The port of the server that uses the DNAT rule to provide services accessible from the Internet                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | This parameter is only available if you select **Specific port** for **Port Type**.                                                                                                                                                                        |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | Range: 1 to 65535                                                                                                                                                                                                                                          |
      |                                   |                                                                                                                                                                                                                                                            |
      |                                   | You can only enter a specific port number, for example, 80.                                                                                                                                                                                                |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK**.

.. important::

   After you add a DNAT rule, add rules to the security group associated with the servers to allow inbound or outbound traffic. Otherwise, the DNAT rule does not take effect.
