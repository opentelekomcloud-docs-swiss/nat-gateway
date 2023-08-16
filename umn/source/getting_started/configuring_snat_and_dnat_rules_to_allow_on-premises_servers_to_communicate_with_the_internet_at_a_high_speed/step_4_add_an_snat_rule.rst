:original_name: nat_qs_0017.html

.. _nat_qs_0017:

Step 4: Add an SNAT Rule
========================

Scenarios
---------

After a public NAT gateway is created, you can add SNAT rules for it. With SNAT rules, servers that are connected to a VPC using Direct Connect can access the Internet by sharing an EIP.

Each SNAT rule is configured for only one CIDR block. If servers that are connected to a VPC using Direct Connect are in multiple CIDR blocks, you can create multiple SNAT rules to allow the servers to share EIPs.

Prerequisites
-------------

There is a public NAT gateway available.

Procedure
---------

#. Log in to the management console.

2. Click **Service List** in the upper left corner. Under **Network**, select **NAT Gateway**.

   The **Public NAT Gateway** page is displayed.

3. On the displayed page, click the name of the public NAT gateway that you want to add an SNAT rule for.

4. On the **SNAT Rules** tab, click **Add SNAT Rule**.

5. Configure the required parameters. For details, see :ref:`Table 1 <nat_qs_0017__table4272024117597>`.

   .. _nat_qs_0017__table4272024117597:

   .. table:: **Table 1** Parameter descriptions

      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                             |
      +===================================+=========================================================================================================================================================================================================================================+
      | Scenario                          | Select **Direct Connect** if servers in your data center need to access the Internet.                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                         |
      |                                   | The servers in your data center that are connected to a VPC through Direct Connect can use the SNAT rule to access the Internet.                                                                                                        |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | CIDR Block                        | A CIDR block of an on-premises data center connected to the cloud through a Direct Connect connection. Local servers whose IP addresses belong to this CIDR block can access the Internet using the SNAT rule.                          |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | EIP                               | The EIP used for accessing the Internet                                                                                                                                                                                                 |
      |                                   |                                                                                                                                                                                                                                         |
      |                                   | You can select an EIP that either has not been bound, has been bound to a DNAT rule with **Port Type** set to **Specific port** of the current public NAT gateway, or has been bound to an SNAT rule of the current public NAT gateway. |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

6. Click **OK**.

7. View details in the SNAT rule list.

   If **Status** of the SNAT rule is **Running**, the SNAT rule has been created.

   .. note::

      -  You can add multiple SNAT rules for a public NAT gateway to suite your service requirements.
      -  Each VPC can only have one NAT gateway.
      -  Only one SNAT rule can be added for each VPC subnet.
