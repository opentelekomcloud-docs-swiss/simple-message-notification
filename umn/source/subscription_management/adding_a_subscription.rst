:original_name: smn_ug_0008.html

.. _smn_ug_0008:

Adding a Subscription
=====================

Scenarios
---------

To deliver messages published to a topic to endpoints, you must add the subscription endpoints to the topic. The endpoint can be a mail address, a mobile phone number, or an HTTP/HTTPS URL. After you add endpoints to the topic and the subscribers confirm the subscription, they are able to receive messages published to the topic.

You can add multiple subscriptions to each topic. This section describes how to add a subscription to a topic you created or a topic that you have permissions for and how to delete a subscription.


Adding a Subscription
---------------------

#. Log in to the management console.

#. Click |image1| on the upper left to select the desired region and project.

#. Under the **Application** service category, select **Simple Message Notification**.

   The SMN console is displayed.

#. In the navigation pane, choose **Subscriptions**.

#. On the **Subscriptions** page, click **Add Subscription**.

   The **Add Subscription** dialog box is displayed.


   .. figure:: /_static/images/en-us_image_0000001656296697.png
      :alt: **Figure 1** Add Subscription

      **Figure 1** Add Subscription

#. Specify the required subscription information.

   a. Click |image2| beside the **Topic Name** box to select a topic.
   b. Specify the subscription protocol and endpoints.

      .. table:: **Table 1** Parameter descriptions

         +-----------------------------------+------------------------------------------------------------------------------------------------------+
         | Parameter                         | Description                                                                                          |
         +===================================+======================================================================================================+
         | Topic Name                        | Name of the topic                                                                                    |
         +-----------------------------------+------------------------------------------------------------------------------------------------------+
         | Protocol                          | The following protocols are supported: SMS, Email, HTTP, and HTTPS.                                  |
         +-----------------------------------+------------------------------------------------------------------------------------------------------+
         | Endpoint                          | Subscription endpoint. You can enter up to 10 SMS, email, HTTP or HTTPS endpoints, one in each line. |
         |                                   |                                                                                                      |
         |                                   | -  **SMS**: Enter one or more valid phone numbers.                                                   |
         |                                   |                                                                                                      |
         |                                   |    The phone number is preceded by a plus sign (+) and the country code.                             |
         |                                   |                                                                                                      |
         |                                   |    Example:                                                                                          |
         |                                   |                                                                                                      |
         |                                   |    **+4900000000**                                                                                   |
         |                                   |                                                                                                      |
         |                                   |    **+4900000001**                                                                                   |
         |                                   |                                                                                                      |
         |                                   |    **+4900000002**                                                                                   |
         |                                   |                                                                                                      |
         |                                   |    **+4900000003**                                                                                   |
         |                                   |                                                                                                      |
         |                                   | -  **Email**: Enter one or more valid email addresses.                                               |
         |                                   |                                                                                                      |
         |                                   |    Example:                                                                                          |
         |                                   |                                                                                                      |
         |                                   |    **username@example.com**                                                                          |
         |                                   |                                                                                                      |
         |                                   |    **username2@example.com**                                                                         |
         |                                   |                                                                                                      |
         |                                   | -  **HTTP**: Enter one or more public network URLs.                                                  |
         |                                   |                                                                                                      |
         |                                   |    Example:                                                                                          |
         |                                   |                                                                                                      |
         |                                   |    **http://example.com/notification/action**                                                        |
         |                                   |                                                                                                      |
         |                                   | -  **HTTPS**: Enter one or more public network URLs.                                                 |
         |                                   |                                                                                                      |
         |                                   |    Example:                                                                                          |
         |                                   |                                                                                                      |
         |                                   |    **https://example.com/notification/action**                                                       |
         +-----------------------------------+------------------------------------------------------------------------------------------------------+

#. Click **OK**.

   The subscription you added is displayed in the subscription list.

   .. note::

      -  To prevent malicious users from attacking subscription endpoints, SMN limits the number of confirmation messages that can be sent to an endpoint within a specified period of time. For details, see :ref:`Traffic Control over Subscription Confirmation <smn_ug_a4000>`.
      -  SMN does not check whether subscription endpoints exist when you add subscriptions. However, subscribers will not receive notification messages until they confirm their subscriptions.
      -  After you add a subscription, SMN sends a confirmation message to the subscription endpoint. You can confirm the subscription within 48 hours through the confirmation link via your mobile phone, mailbox, or other endpoints.

.. |image1| image:: /_static/images/en-us_image_0000001656576717.png
.. |image2| image:: /_static/images/en-us_image_0000001607256696.png
