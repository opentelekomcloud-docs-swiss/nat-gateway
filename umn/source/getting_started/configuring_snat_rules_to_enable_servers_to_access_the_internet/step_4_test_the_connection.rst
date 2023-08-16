:original_name: nat_qs_0005.html

.. _nat_qs_0005:

Step 4: Test the Connection
===========================

Scenarios
---------

After you add an SNAT rule, you can perform the following steps to verify the connection:

#. Verify that the SNAT rule has been added for the public NAT gateway.
#. Verify that servers that have no EIP bound can access the Internet through a NAT gateway.

Prerequisites
-------------

An SNAT rule has been added.

Verifying that the SNAT Rule Has Been Added
-------------------------------------------

#. Log in to the management console.

#. Click **Service List** in the upper left corner. Under **Network**, select **NAT Gateway**.

#. On the displayed page, click the name of the target public NAT gateway.

#. In the **SNAT Rules** tab, view details about the SNAT rule.

   If **Status** of the SNAT rule is **Running**, the SNAT rule has been created.

Verifying that Servers Can Access the Internet Through the NAT Gateway
----------------------------------------------------------------------

#. Log in to the management console.
#. Hover on |image1| in the upper left corner to display **Service List** and choose **Computing** > **Elastic Cloud Server**.
#. Log in to the server to be verified.
#. Verify that the server can access the Internet.

.. |image1| image:: /_static/images/en-us_image_0000001223710285.png
