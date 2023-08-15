:original_name: nat_qs_0011.html

.. _nat_qs_0011:

Step 4: Test the Connection
===========================

Scenarios
---------

After you add a DNAT rule, you can perform the following steps to verify the connection:

#. Verify that the DNAT rule has been added for the public NAT gateway.
#. Check whether ECS 01 on the private network can be accessed by ECS 02 on the public network through the NAT gateway (EIP 120.46.131.153 bound to the DNAT rule).

Prerequisites
-------------

A DNAT rule has been added.

Verifying that the DNAT Rule Has Been Added
-------------------------------------------

#. Log in to the management console.

#. Click **Service List** in the upper left corner. Under **Network**, select **NAT Gateway**.

#. On the displayed page, click the name of the target public NAT gateway.

#. In the **DNAT Rules** tab, view details about the DNAT rule and check whether the DNAT rule has been created.

   If **Status** of the DNAT rule is **Running**, the DNAT rule has been created.

Verifying that Servers in a VPC Can Be Accessed from the Internet Through a NAT Gateway
---------------------------------------------------------------------------------------

#. Log in to the management console.

#. Hover on |image1| in the upper left corner to display **Service List** and choose **Computing** > **Elastic Cloud Server**.

#. Log in to ECS 02 with an EIP bound.

#. On ECS 02, ping the EIP (120.46.131.153) to check whether ECS 01 on the private network can be accessed by ECS 02 on the public network through the NAT gateway.


   .. figure:: /_static/images/en-us_image_0000001178838178.png
      :alt: **Figure 1** Failed to access the Internet

      **Figure 1** Failed to access the Internet

.. |image1| image:: /_static/images/en-us_image_0000001223839393.png
