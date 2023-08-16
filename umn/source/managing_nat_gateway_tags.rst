:original_name: nat_tag_0000.html

.. _nat_tag_0000:

Managing NAT Gateway Tags
=========================

Scenarios
---------

A NAT gateway tag identifies the NAT gateway. Tags can be added to NAT gateways to facilitate NAT gateway identification and administration. You can add a tag to a NAT gateway when creating the NAT gateway. Alternatively, you can add a tag to a created NAT gateway on the NAT gateway details page. A maximum of ten tags can be added to each NAT gateway.

A tag consists of a key and value pair. :ref:`Table 1 <nat_tag_0000__ted9687ca14074ef785241145365a6175>` lists the tag key and value requirements.

.. _nat_tag_0000__ted9687ca14074ef785241145365a6175:

.. table:: **Table 1** Tag requirements

   +-----------------------------------+---------------------------------------------------------------------+
   | Parameter                         | Requirement                                                         |
   +===================================+=====================================================================+
   | Key                               | -  Cannot be left blank.                                            |
   |                                   | -  Must be unique for each NAT gateway.                             |
   |                                   | -  Can contain a maximum of 36 characters.                          |
   |                                   | -  Can contain only the following character types:                  |
   |                                   |                                                                     |
   |                                   |    -  Letters                                                       |
   |                                   |    -  Digits                                                        |
   |                                   |    -  Special characters, including hyphens (-) and underscores (_) |
   +-----------------------------------+---------------------------------------------------------------------+
   | Value                             | -  Can contain a maximum of 43 characters.                          |
   |                                   | -  Can contain only the following character types:                  |
   |                                   |                                                                     |
   |                                   |    -  Letters                                                       |
   |                                   |    -  Digits                                                        |
   |                                   |    -  Special characters, including hyphens (-) and underscores (_) |
   +-----------------------------------+---------------------------------------------------------------------+

Procedure
---------

**Search for public NAT gateways by tag key or tag value on the page listing the public NAT gateways.**

#. Log in to the management console.

#. Click **Service List** in the upper left corner. Under **Network**, select **NAT Gateway**.

#. In the upper right corner of the public NAT gateway list, click **Search by Tag**.

#. In the displayed area, enter the tag key and tag value of the public NAT gateway you are searching for. Both the tag key and value must be specified.

#. Click **+** to specify additional tag keys and values.

   You can add a maximum of ten tags to refine your search results. If you add more than one tag to search for public NAT gateways, the tags are automatically joined with AND.

#. Click **Search**.

   The system displays the public NAT gateways you are searching for based on the entered tag keys and tag values.

**Add, delete, edit, and view tags of a public NAT gateway on the Tags tab.**

#. Log in to the management console.

#. Click **Service List** in the upper left corner. Under **Network**, select **NAT Gateway**.

#. In the public NAT gateway list, locate the public NAT gateway whose tags you want to manage and click its name.

   The page showing details about the public NAT gateway is displayed.

4. Click the **Tags** tab and perform desired operations on tags.

   -  View a tag.

      On the **Tags** tab, you can view tag details of the current public NAT gateway, including the number of tags and the key and value of each tag.

   -  Add a tag.

      Click **Add Tag** in the upper left corner. In the displayed dialog box, enter the key and value of the tag to be added, and click **OK**.

      .. note::

         You can use the predefined tags as prompted to simplify tag adding operations. For details, see `Predefined Tags <https://docs.sc.otc.t-systems.com/usermanual/tms/en-us_topic_0101849262.html>`__.

   -  Modify a tag.

      Locate the row that contains the tag to be edited and click **Edit** in the **Operation** column. In the **Edit Tag** dialog box, change the tag value and click **OK**.

   -  Delete a tag.

      Locate the row that contains the tag to be deleted and click **Delete** in the **Operation** column. In the displayed **Delete Tag** dialog box, click **Yes**.
