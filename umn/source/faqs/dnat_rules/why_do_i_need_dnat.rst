:original_name: nat_faq_0006.html

.. _nat_faq_0006:

Why Do I Need DNAT?
===================

In a public NAT gateway, DNAT enables servers in a VPC to share an EIP to provide services accessible from the Internet. With an EIP, a public NAT gateway forwards the Internet requests from only a specific port and over a specific protocol to a specific port of a server, or it can forward all requests to the server regardless of which port they originated on. For details, see :ref:`Adding a DNAT Rule <en-us_topic_0127489530>`.
