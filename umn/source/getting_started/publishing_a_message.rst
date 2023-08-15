:original_name: smn_ug_0004.html

.. _smn_ug_0004:

Publishing a Message
====================

After you learn the basic concepts in SMN, you can start to create a topic, add subscriptions to the topic, and publish messages on the SMN console or by calling RESTful APIs provided by SMN.

:ref:`Figure 1 <smn_ug_0004__fig208091627152213>` shows the process to publish a message.

.. _smn_ug_0004__fig208091627152213:

.. figure:: /_static/images/en-us_image_0000001616672638.png
   :alt: **Figure 1** Process of publishing a message

   **Figure 1** Process of publishing a message

Scenarios
---------

To send similar messages repeatedly, create a message template which contains fixed and changeable content. Every time you send messages using the template, you only have to replace changeable content. For example, your organization holds expositions regularly and needs to notify relevant people of the time, you can create a message template containing date variables and other fixed content.

Step 1. Create a Topic
----------------------

#. Log in to the management console.

#. Click |image1| on the upper left to select the desired region and project.

#. Under the **Application** service category, select **Simple Message Notification**.

   The SMN console is displayed.

#. In the navigation pane on the left, choose **Topics**.

   The **Topics** page is displayed.

#. In the upper right corner, click **Create Topic**.


   .. figure:: /_static/images/en-us_image_0000001656336945.png
      :alt: **Figure 2** Create Topic

      **Figure 2** Create Topic

#. Enter a topic name and display name.

   .. table:: **Table 1** Parameter descriptions

      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                     |
      +===================================+=================================================================================================================================================================================================+
      | Topic Name                        | Topic name, which:                                                                                                                                                                              |
      |                                   |                                                                                                                                                                                                 |
      |                                   | -  Contains only letters, digits, hyphens (-), and underscores (_), and must start with a letter or digit.                                                                                      |
      |                                   | -  Contains 1 to 255 characters.                                                                                                                                                                |
      |                                   | -  Must be unique and cannot be modified once the topic is created.                                                                                                                             |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Display Name                      | Message sender name, which can contain up to 192 characters                                                                                                                                     |
      |                                   |                                                                                                                                                                                                 |
      |                                   | .. note::                                                                                                                                                                                       |
      |                                   |                                                                                                                                                                                                 |
      |                                   |    After you specify a display name, the sender in email messages will be presented as *Display name*\ **<username@example.com>**. Otherwise, the sender will be **username@example.com**.      |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Tag                               | A tag is a key-value pair. Tags identify cloud resources so that you can easily categorize and search for your resources.                                                                       |
      |                                   |                                                                                                                                                                                                 |
      |                                   | -  A key can contain up to 36 characters. A value can contain up to 43 characters. Both **Key** and **Value** can contain only digits, letters, hyphens (-), at signs (@), and underscores (_). |
      |                                   | -  You can add up to 10 tags for each topic.                                                                                                                                                    |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK.**

   The topic you created is displayed in the topic list. The system generates a topic URN, which is the unique resource identifier of the topic and cannot be changed.

#. Click the name of the topic to view its details (including the topic URN and display name), tags, and subscriptions.

Step 2. Add a Subscription
--------------------------

#. Log in to the management console.

#. Click |image2| on the upper left to select the desired region and project.

#. Under the **Application** service category, select **Simple Message Notification**.

   The SMN console is displayed.

#. In the navigation pane, choose **Subscriptions**.

#. On the **Subscriptions** page, click **Add Subscription**.

   The **Add Subscription** dialog box is displayed.


   .. figure:: /_static/images/en-us_image_0000001656296697.png
      :alt: **Figure 3** Add Subscription

      **Figure 3** Add Subscription

#. Specify the required subscription information.

   a. Click |image3| beside the **Topic Name** box to select a topic.
   b. Specify the subscription protocol and endpoints.

      .. table:: **Table 2** Parameter descriptions

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
         |                                   |    +4900000000                                                                                       |
         |                                   |                                                                                                      |
         |                                   |    +4900000001                                                                                       |
         |                                   |                                                                                                      |
         |                                   |    +4900000002                                                                                       |
         |                                   |                                                                                                      |
         |                                   |    +4900000003                                                                                       |
         |                                   |                                                                                                      |
         |                                   | -  **Email**: Enter one or more valid email addresses.                                               |
         |                                   |                                                                                                      |
         |                                   |    Example:                                                                                          |
         |                                   |                                                                                                      |
         |                                   |    username@example.com                                                                              |
         |                                   |                                                                                                      |
         |                                   |    username2@example.com                                                                             |
         |                                   |                                                                                                      |
         |                                   | -  **HTTP**: Enter one or more public network URLs.                                                  |
         |                                   |                                                                                                      |
         |                                   |    Example:                                                                                          |
         |                                   |                                                                                                      |
         |                                   |    http://example.com/notification/action                                                            |
         |                                   |                                                                                                      |
         |                                   | -  **HTTPS**: Enter one or more public network URLs.                                                 |
         |                                   |                                                                                                      |
         |                                   |    Example:                                                                                          |
         |                                   |                                                                                                      |
         |                                   |    https://example.com/notification/action                                                           |
         +-----------------------------------+------------------------------------------------------------------------------------------------------+

#. Click **OK**.

   The subscription you added is displayed in the subscription list.

   .. note::

      -  To prevent malicious users from attacking subscription endpoints, SMN limits the number of confirmation messages that can be sent to an endpoint within a specified period of time. For details, see :ref:`Traffic Control over Subscription Confirmation <smn_ug_a4000>`.
      -  SMN does not check whether subscription endpoints exist when you add subscriptions. However, subscribers will not receive notification messages until they confirm their subscriptions.
      -  After you add a subscription, SMN sends a confirmation message to the subscription endpoint. The message contains a link for confirming the subscription. The subscription confirmation link is valid within 48 hours. Confirm the subscription on your mobile phone, mailbox, or other endpoints in time.

Step 3. Create a Message Template
---------------------------------

#. Log in to the management console.

#. Click |image4| on the upper left to select the desired region and project.

#. Under the **Application** service category, select **Simple Message Notification**.

   The SMN console is displayed.

#. In the navigation pane, choose **Message Templates**.

#. On the **Message Templates** page, click **Create Message Template**.

   The **Create Message Template** dialog box is displayed.


   .. figure:: /_static/images/en-us_image_0000001606936996.png
      :alt: **Figure 4** Create Message Template

      **Figure 4** Create Message Template

#. Specify the template name, protocol, and content.

   .. table:: **Table 3** Parameters required for creating a message template

      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                                                                                                    |
      +===================================+================================================================================================================================================================================================================================================================================================================================================+
      | Template Name                     | Template name, which:                                                                                                                                                                                                                                                                                                                          |
      |                                   |                                                                                                                                                                                                                                                                                                                                                |
      |                                   | -  Contains only letters, digits, hyphens (-), and underscores (_), and must start with a letter or digit.                                                                                                                                                                                                                                     |
      |                                   | -  Can contain 1 to 64 bytes.                                                                                                                                                                                                                                                                                                                  |
      |                                   | -  Cannot be modified once the template is created.                                                                                                                                                                                                                                                                                            |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Protocol                          | Endpoint protocol of the template, which cannot be changed once the template is created                                                                                                                                                                                                                                                        |
      |                                   |                                                                                                                                                                                                                                                                                                                                                |
      |                                   | The protocol can be **Default**, **SMS**, **HTTP**, **HTTPS**, or **Email**.                                                                                                                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                                                                                                                                |
      |                                   | If you do not specify a protocol, **Default** is used.                                                                                                                                                                                                                                                                                         |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Content                           | Template content                                                                                                                                                                                                                                                                                                                               |
      |                                   |                                                                                                                                                                                                                                                                                                                                                |
      |                                   | You can use variables as the placeholders to create a template. Before you send messages using the template, SMN replaces the variables with the message content you specify. A variable can contain up to 21 characters and must start with a letter or digit. It can contain letters, digits, hyphens (-), underscores (_), and periods (.). |
      |                                   |                                                                                                                                                                                                                                                                                                                                                |
      |                                   | The message template must meet the following requirements:                                                                                                                                                                                                                                                                                     |
      |                                   |                                                                                                                                                                                                                                                                                                                                                |
      |                                   | -  The template supports plain text only.                                                                                                                                                                                                                                                                                                      |
      |                                   | -  The template content cannot be left blank and cannot exceed 256 KB.                                                                                                                                                                                                                                                                         |
      |                                   |                                                                                                                                                                                                                                                                                                                                                |
      |                                   | -  The template can contain up to 256 variables in total, but that includes redundant variables. For unique variables, there can be no more than 90.                                                                                                                                                                                           |
      |                                   | -  When you send messages using a template, the message content you specify for each variable cannot exceed 1 KB.                                                                                                                                                                                                                              |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   For example, the template information is as follows:

   -  **Template Name**: **tem_001**

   -  **Protocol**: **Default**

   -  **Content**: **The Arts and Crafts Exposition will be held from {startdate} through {enddate}. We sincerely invite you to join us.**


      .. figure:: /_static/images/en-us_image_0000001664792529.png
         :alt: **Figure 5** Create Message Template

         **Figure 5** Create Message Template

#. Click **OK**.

   The template you created is displayed in the template list.

Step 4. Publish a Template Message
----------------------------------

#. Log in to the management console.

#. Click |image5| on the upper left to select the desired region and project.

#. Under the **Application** service category, select **Simple Message Notification**.

   The SMN console is displayed.

#. In the navigation pane on the left, choose **Topics**.

   The **Topics** page is displayed.

#. In the topic list, locate the topic that you need to publish a message to and click **Publish Message** in the **Operation** column.

#. Configure the required parameters.

   The topic name is provided by default and cannot be changed.

   Select **Template** for **Message Type**. Then, manually type the template content in the **Message** box or click **Generate Template Message** to generate it automatically. The template message content cannot exceed 256 KB.

   -  If you choose to manually type the template message, see :ref:`Template Message Format <smn_ug_a2000>` for detailed requirements.
   -  If you choose to automatically generate the template message, proceed with steps :ref:`7 <smn_ug_0004__en-us_topic_0044170770_li37303092212221>` to :ref:`10 <smn_ug_0004__en-us_topic_0044170770_li3929025721230>`.

#. .. _smn_ug_0004__en-us_topic_0044170770_li37303092212221:

   Click **Generate Template Message**.

#. Select a template name, for example, **tem_001**, and enter values for the variables.

   The system replaces the variables with the message content you specified. The protocols configured in the template will be displayed after the tags. In this example, only the default protocol is specified in **tem_001**. Therefore, all confirmed subscribers in the topic will receive the message content in the default template.


   .. figure:: /_static/images/en-us_image_0000001607216728.png
      :alt: **Figure 6** Generate Template Message

      **Figure 6** Generate Template Message

#. Click the **Preview** tab to preview the template message.

   In this example, the message generated is "The Arts and Crafts Exposition will be held from February 10 through February 21. We sincerely invite you to join us."


   .. figure:: /_static/images/en-us_image_0000001606777232.png
      :alt: **Figure 7** Previewing the template message

      **Figure 7** Previewing the template message

#. .. _smn_ug_0004__en-us_topic_0044170770_li3929025721230:

   Click **OK**.

   The message that is generated contains the template name and variables.


   .. figure:: /_static/images/en-us_image_0000001656456921.png
      :alt: **Figure 8** Template message example

      **Figure 8** Template message example

#. Click **OK**.

   SMN delivers your message to all subscription endpoints. For details about messages for different protocols, see :ref:`Messages Using Different Protocols <smn_ug_a3000>`.

Step 5. Receive a Template Message
----------------------------------

Subscription endpoints of different protocols receive different messages.

-  Email

   Subscription endpoints are email addresses.

   Email messages contain the message content and a link to unsubscribe.


   .. figure:: /_static/images/en-us_image_0000001606777308.png
      :alt: **Figure 9** Email message

      **Figure 9** Email message

-  HTTP or HTTPS

   Subscription endpoints are public network URLs. For details, see :ref:`HTTP/HTTPS Messages <smn_ug_0031>`.

-  SMS

   Subscription endpoints are phone numbers.

   SMS messages contain only the message content.

.. |image1| image:: /_static/images/en-us_image_0000001607216700.png
.. |image2| image:: /_static/images/en-us_image_0000001656576717.png
.. |image3| image:: /_static/images/en-us_image_0000001607256696.png
.. |image4| image:: /_static/images/en-us_image_0000001656576665.png
.. |image5| image:: /_static/images/en-us_image_0000001656456929.png
