:original_name: en-us_topic_0044170767.html

.. _en-us_topic_0044170767:

Publishing a JSON Message
=========================

Scenarios
---------

In a JSON message, you can specify different message content for different protocols, including SMS, email, HTTP, and HTTPS.

Prerequisites
-------------

Subscribers in the topic must have confirmed the subscription, or they will not be able to receive any messages.

Procedure
---------

#. Log in to the management console.

#. Click |image1| on the upper left to select the desired region and project.

#. Under the **Application** service category, select **Simple Message Notification**.

   The SMN console is displayed.

#. In the navigation pane, choose **Topics**.

   The **Topics** page is displayed.

#. In the topic list, locate the topic that you need to publish a message to and click **Publish Message** in the **Operation** column.

#. Configure the required parameters.

   The topic name is provided by default and cannot be changed.

   Configure the required parameters based on :ref:`Table 1 <en-us_topic_0043961403__table616755201736>`.

   Select **JSON** for **Message Format**.

   Manually type the JSON message in the **Message** box or click **Generate JSON Message** to generate it automatically. The total size of a JSON message cannot exceed 256 KB.

   -  If you choose to manually type the JSON message, see :ref:`JSON Message Format <smn_ug_a1000>` for detailed requirements.
   -  If you choose to automatically generate the JSON message, proceed with steps :ref:`7 <en-us_topic_0044170767__li59465700211512>` through :ref:`10 <en-us_topic_0044170767__li3542952114596>`.

#. .. _en-us_topic_0044170767__li59465700211512:

   Click **Generate JSON Message**.

#. Enter your message content, for example **This is a default message.**, in the **Message** box and select the desired message protocols.

   The size of a JSON message varies depending on the protocol combinations. As you type in the message content, the system will calculate the number of bytes you have entered, the size of the JSON message, and how many bytes are left. The total size of a JSON message includes braces, quotation marks, spaces, line breaks, and message content. For details about how to calculate the size of a JSON message, see :ref:`Calculation on the Size of a JSON Message <smn_ug_a1000__section11977745123756>` in :ref:`JSON Message Format <smn_ug_a1000>`.


   .. figure:: /_static/images/en-us_image_0000001607216720.png
      :alt: **Figure 1** Generate JSON Message

      **Figure 1** Generate JSON Message

#. Click **OK**.


   .. figure:: /_static/images/en-us_image_0000001656336969.png
      :alt: **Figure 2** JSON message

      **Figure 2** JSON message

#. .. _en-us_topic_0044170767__li3542952114596:

   Modify the message content for each protocol so that different messages are sent to endpoints of different protocols. The system generates JSON-formatted content that includes a default message and content for each protocol. When SMN fails to match any specific message protocol, it sends the default message. For detailed, see :ref:`JSON Message Format <smn_ug_a1000>`.

#. Click **OK**.

   SMN delivers your message to all subscription endpoints. For details about the messages received by each endpoint, see :ref:`Messages Using Different Protocols <smn_ug_a3000>`.

.. |image1| image:: /_static/images/en-us_image_0000001607216700.png
