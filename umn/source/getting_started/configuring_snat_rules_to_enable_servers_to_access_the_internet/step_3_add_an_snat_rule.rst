:original_name: nat_qs_0004.html

.. _nat_qs_0004:

Step 3: Add an SNAT Rule
========================

Scenarios
---------

To enable your servers in a specific subnet to access the Internet by sharing the same EIP, add SNAT rules after you create a public NAT gateway.

Each SNAT rule is configured for only one subnet or CIDR block. If there are multiple subnets or CIDR blocks in a VPC, you can add multiple SNAT rules to allow multiple servers to share EIPs.

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

#. Configure the required parameters. :ref:`Table 1 <nat_qs_0004__table1966804261617>` describes the parameters.

   .. _nat_qs_0004__table1966804261617:

   .. table:: **Table 1** Parameter descriptions

      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                             |
      +===================================+=========================================================================================================================================================================================================================================+
      | Scenario                          | Select **VPC** if your servers in a VPC will use the SNAT rule to access the Internet.                                                                                                                                                  |
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
