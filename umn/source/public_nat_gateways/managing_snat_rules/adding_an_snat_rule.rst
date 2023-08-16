:original_name: en-us_topic_0127489529.html

.. _en-us_topic_0127489529:

Adding an SNAT Rule
===================

Scenarios
---------

After the public NAT gateway is created, add SNAT rules, so that servers in a VPC subnet or servers that are connected to a VPC through Direct Connect can access the Internet by sharing an EIP.

Each SNAT rule is configured for only one subnet. If there are multiple subnets in a VPC, you can create multiple SNAT rules to allow them to share EIPs.

Prerequisites
-------------

There is a public NAT gateway available.

Procedure
---------

#. Log in to the management console.

#. Click **Service List** in the upper left corner. Under **Network**, select **NAT Gateway**.

   The **Public NAT Gateway** page is displayed.

#. On the displayed page, click the name of the public NAT gateway that you want to add an SNAT rule for.

#. On the **SNAT Rules** tab, click **Add SNAT Rule**.

#. Configure the required parameters. For details, see :ref:`Table 1 <en-us_topic_0127489529__en-us_topic_0127293981_table4272024117597>`.

   .. _en-us_topic_0127489529__en-us_topic_0127293981_table4272024117597:

   .. table:: **Table 1** Parameter descriptions

      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                             |
      +===================================+=========================================================================================================================================================================================================================================+
      | Scenario                          | The scenarios where the SNAT rule is used                                                                                                                                                                                               |
      |                                   |                                                                                                                                                                                                                                         |
      |                                   | Select **VPC** if your servers in a VPC need to access the Internet.                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                                         |
      |                                   | Select **Direct Connect** if the servers that are connected to a VPC through Direct Connect or VPN in your data center need to access the Internet.                                                                                     |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Subnet                            | The subnet in which servers can use the SNAT rule to access the Internet                                                                                                                                                                |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | EIP                               | The EIP used for accessing the Internet                                                                                                                                                                                                 |
      |                                   |                                                                                                                                                                                                                                         |
      |                                   | You can select an EIP that either has not been bound, has been bound to a DNAT rule with **Port Type** set to **Specific port** of the current public NAT gateway, or has been bound to an SNAT rule of the current public NAT gateway. |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK**.

   .. note::

      -  You can add multiple SNAT rules for a public NAT gateway to suite your service requirements.
      -  Each VPC can only have one NAT gateway.
      -  Only one SNAT rule can be added for each VPC subnet.
