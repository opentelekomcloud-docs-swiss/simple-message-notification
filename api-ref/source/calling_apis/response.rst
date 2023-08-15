:original_name: smn_api_35000.html

.. _smn_api_35000:

Response
========

Status Code
-----------

After sending a request, you will receive a response, including a status code, response header, and response body.

A status code is a group of digits, ranging from 1xx to 5xx. It indicates the status of a request. For more information, see :ref:`Returned Value <smn_api_63002>`.

For example, if status code **200** is returned for calling the API used to obtain a VPC list, the request is successful.

Response Header
---------------

Similar to a request, a response also has a header, for example, **Content-Type**.

:ref:`Figure 1 <smn_api_35000__en-us_topic_0170210614_en-us_topic_0170195383_fig4865141011511>` shows the response header fields for the API used to obtain a VPC list.

.. _smn_api_35000__en-us_topic_0170210614_en-us_topic_0170195383_fig4865141011511:

.. figure:: /_static/images/en-us_image_0170196244.png
   :alt: **Figure 1** Header fields of the response to the request for obtaining a VPC list

   **Figure 1** Header fields of the response to the request for obtaining a VPC list

(Optional) Response Body
------------------------

The body of a response is often returned in structured format as specified in the **Content-Type** header field. The response body transfers content except the response header.

The following shows the response body for the API used to obtain a VPC list. In the response body, the VPC named **vpc-test** is displayed.

.. code-block::

   {
       "vpcs": [
           {
               "id": "7e1a7e70-3f3e-4581-955e-26a4848d8f31",
               "name": "vpc-test",
               "description": "",
               "cidr": "192.168.0.0/16",
               "status": "OK",
               "routes": [],
               "enterprise_project_id": "0"
           }
       ]
   }

If an error occurs during API calling, an error code and a message will be displayed. The following shows an error response body.

.. code-block::

   {
       "code": "VPC.0002",
       "message": "Available zone Name is null."
   }

In the response body, **error_code** is an error code, and **error_msg** provides information about the error.
