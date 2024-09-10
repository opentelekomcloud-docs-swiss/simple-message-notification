:original_name: en-us_topic_0043961401.html

.. _en-us_topic_0043961401:

Creating a Topic
================

Scenarios
---------

A topic is a specified event to publish messages and subscribe to notifications. It serves as a message sending channel, where publishers and subscribers can interact with each other.


Creating a Topic
----------------

#. Log in to the management console.

#. Click |image1| on the upper left to select the desired region and project.

#. Under the **Application** service category, select **Simple Message Notification**.

   The SMN console is displayed.

#. In the navigation pane on the left, choose **Topics**.

   The **Topics** page is displayed.

#. In the upper right corner, click **Create Topic**.


   .. figure:: /_static/images/en-us_image_0000001656336945.png
      :alt: **Figure 1** Create Topic

      **Figure 1** Create Topic

#. Enter a topic name and display name.

   .. _en-us_topic_0043961401__en-us_topic_0043394871_table9567729153632:

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

.. |image1| image:: /_static/images/en-us_image_0000001607216700.png
