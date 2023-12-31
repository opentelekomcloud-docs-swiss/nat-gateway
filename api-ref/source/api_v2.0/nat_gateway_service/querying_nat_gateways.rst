:original_name: nat_api_0002.html

.. _nat_api_0002:

Querying NAT Gateways
=====================

Function
--------

This API is used to query NAT gateways. Unless otherwise specified, exact match is applied.

URI
---

GET /v2.0/nat_gateways

.. note::

   You can type the question mark (?) and ampersand (&) at the end of the URI to define multiple search criteria. All optional parameters can be filtered. For details, see the example request.

.. table:: **Table 1** Parameter description

   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter           | Mandatory       | Type            | Description                                                                                                                                       |
   +=====================+=================+=================+===================================================================================================================================================+
   | id                  | No              | String          | Specifies the NAT gateway ID.                                                                                                                     |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | limit               | No              | Integer         | Specifies the number of records on each page.                                                                                                     |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | tenant_id           | No              | String          | Specifies the project ID.                                                                                                                         |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | name                | No              | String(64)      | Specifies the NAT gateway name.                                                                                                                   |
   |                     |                 |                 |                                                                                                                                                   |
   |                     |                 |                 | The name can contain only digits, letters, underscores (_), and hyphens (-).                                                                      |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | description         | No              | String(255)     | Provides supplementary information about the NAT gateway.                                                                                         |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | spec                | No              | String          | Specifies the NAT gateway type.                                                                                                                   |
   |                     |                 |                 |                                                                                                                                                   |
   |                     |                 |                 | The type can be:                                                                                                                                  |
   |                     |                 |                 |                                                                                                                                                   |
   |                     |                 |                 | -  **1**: small type, which supports up to 10,000 SNAT connections.                                                                               |
   |                     |                 |                 | -  **2**: medium type, which supports up to 50,000 SNAT connections.                                                                              |
   |                     |                 |                 | -  **3**: large type, which supports up to 200,000 SNAT connections.                                                                              |
   |                     |                 |                 | -  **4**: extra-large type, which supports up to 1,000,000 SNAT connections.                                                                      |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | router_id           | No              | String          | Specifies the router ID.                                                                                                                          |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | internal_network_id | No              | String          | Specifies the network ID of the downstream interface (the next hop of the DVR) of the NAT gateway.                                                |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | status              | No              | String          | -  Specifies the NAT gateway status.                                                                                                              |
   |                     |                 |                 | -  For details about all its values, see :ref:`Table 1 <nat_api_0042__table1390614366107>`.                                                       |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | admin_state_up      | No              | Boolean         | -  Specifies whether the NAT gateway is up or down.                                                                                               |
   |                     |                 |                 | -  The state can be:                                                                                                                              |
   |                     |                 |                 |                                                                                                                                                   |
   |                     |                 |                 |    -  **true**: The NAT gateway is up.                                                                                                            |
   |                     |                 |                 |    -  **false**: The NAT gateway is down.                                                                                                         |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | created_at          | No              | String          | Specifies when the NAT gateway is created (UTC time). Its value rounds to 6 decimal places for seconds. The format is yyyy-mm-dd hh:mm:ss.ffffff. |
   +---------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------+

Request
-------

None

Response
--------

:ref:`Table 2 <nat_api_0002__table8843312114313>` lists response parameters.

.. _nat_api_0002__table8843312114313:

.. table:: **Table 2** Response parameter

   +--------------+---------------------+--------------------------------------------------------------------------------------------------------+
   | Parameter    | Type                | Description                                                                                            |
   +==============+=====================+========================================================================================================+
   | nat_gateways | List (NAT gateways) | Specifies the NAT gateway objects. For details, see :ref:`Table 3 <nat_api_0002__table1810691174217>`. |
   +--------------+---------------------+--------------------------------------------------------------------------------------------------------+

.. _nat_api_0002__table1810691174217:

.. table:: **Table 3** Description of the **nat_gateway** field

   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                                                                                                       |
   +=======================+=======================+===================================================================================================================================================+
   | id                    | String                | Specifies the NAT gateway ID.                                                                                                                     |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | tenant_id             | String                | Specifies the project ID.                                                                                                                         |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | name                  | String(64)            | Specifies the NAT gateway name.                                                                                                                   |
   |                       |                       |                                                                                                                                                   |
   |                       |                       | The name can contain only digits, letters, underscores (_), and hyphens (-).                                                                      |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | description           | String(255)           | Provides supplementary information about the NAT gateway.                                                                                         |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | spec                  | String                | Specifies the NAT gateway type.                                                                                                                   |
   |                       |                       |                                                                                                                                                   |
   |                       |                       | The type can be:                                                                                                                                  |
   |                       |                       |                                                                                                                                                   |
   |                       |                       | -  **1**: small type, which supports up to 10,000 SNAT connections.                                                                               |
   |                       |                       | -  **2**: medium type, which supports up to 50,000 SNAT connections.                                                                              |
   |                       |                       | -  **3**: large type, which supports up to 200,000 SNAT connections.                                                                              |
   |                       |                       | -  **4**: extra-large type, which supports up to 1,000,000 SNAT connections.                                                                      |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | router_id             | String                | Specifies the router ID.                                                                                                                          |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | internal_network_id   | String                | Specifies the network ID of the downstream interface (the next hop of the DVR) of the NAT gateway.                                                |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | status                | String                | -  Specifies the NAT gateway status.                                                                                                              |
   |                       |                       | -  For details about all its values, see :ref:`Table 1 <nat_api_0042__table1390614366107>`.                                                       |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | admin_state_up        | Boolean               | -  Specifies whether the NAT gateway is up or down.                                                                                               |
   |                       |                       | -  The state can be:                                                                                                                              |
   |                       |                       |                                                                                                                                                   |
   |                       |                       |    -  **true**: The NAT gateway is up.                                                                                                            |
   |                       |                       |    -  **false**: The NAT gateway is down.                                                                                                         |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
   | created_at            | String                | Specifies when the NAT gateway is created (UTC time). Its value rounds to 6 decimal places for seconds. The format is yyyy-mm-dd hh:mm:ss.ffffff. |
   +-----------------------+-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+

Examples
--------

-  Example request

   .. code-block:: text

      GET https://{Endpoint}/v2.0/nat_gateways?limit=10

-  Example response

   .. code-block::

      {
           "nat_gateways": [
               {
                   "router_id": "b1d81744-5165-48b8-916e-e56626feb88f",
                   "status": "ACTIVE",
                   "description": "",
                   "admin_state_up": true,
                   "tenant_id": "27e25061336f4af590faeabeb7fcd9a3",
                   "created_at": "2017-11-15 14:50:39.505112",
                   "spec": "2",
                   "internal_network_id": "5930796a-6026-4d8b-8790-6c6bfc9f87e8",
                   "id": "a253be25-ae7c-4013-978b-3c0785eccd63",
                   "name": "wj3"
               },
               {
                   "router_id": "305dc52f-13dd-429b-a2d4-444a1039ba0b",
                   "status": "ACTIVE",
                   "description": "",
                   "admin_state_up": true,
                   "tenant_id": "27e25061336f4af590faeabeb7fcd9a3",
                   "created_at": "2017-11-17 07:41:07.538062",
                   "spec": "2",
                   "internal_network_id": "fc09463b-4ef8-4c7a-93c8-92d9ca6daf9d",
                   "id": "e824f1b4-4290-4ebc-8322-cfff370dbd1e",
                   "name": "lyl001"
              }
          ]
      }

Status Code
-----------

See :ref:`Status Codes <nat_api_0038>`.
