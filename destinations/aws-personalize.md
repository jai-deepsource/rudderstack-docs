---
description: Step-by-step guide to set up AWS Personalize as a destination in RudderStack.
---

# AWS Personalize

[Amazon Personalize](https://aws.amazon.com/personalize/), also called as AWS Personalize, is a machine learning service by Amazon. It enables you to create high-quality content recommendations, personalized product and marketing promotions, and much more. With Amazon Personalize, you can boost your customer engagement and overall business revenue in no time at all. 

RudderStack allows you to configure Amazon Personalize as a destination to which you can send your event data seamlessly, for personalized recommendation and effective product marketing.

## **Getting Started**

In order to enable dumping data to Amazon Personalize, you will first need to add it as a destination to the source from which you are sending event data. Once the destination is enabled, events from RudderStack will start to flow to Amazon Personalize. 

Before configuring your source and destination on the RudderStack app, please check whether the platform you are working on is supported by Amazon Personalize. Refer to the table below:

| **Connection Mode** | **Web** | **Mobile** | **Server** |
| :--- | :--- | :--- | :--- |
| **Device mode** | - | - | - |
| **Cloud mode** | **Supported** | **Supported** | **Supported** |

{% hint style="info" %}
 To know more about the difference between Cloud mode and Device mode in RudderStack, read the [RudderStack connection modes](https://docs.rudderstack.com/get-started/rudderstack-connection-modes) guide.
{% endhint %}

Once you have confirmed that the platform supports sending events to Amazon Personalize, perform the steps below:

* Run the script by following the instructions included in the [readme.md](https://github.com/rudderlabs/rudder-transformer/tree/destination_personalize/v0/personalize/scripts) to generate a tracking ID. 

{% hint style="success" %}
Keep this tracking ID handy as it is used later to configure AWS Personalize as a destination.
{% endhint %}

* Next, go to the [RudderStack dashboard](https://app.rudderlabs.com/), and choose a source to which you would like to add Amazon Personalize as a destination.

{% hint style="info" %}
Please follow our [Adding a Source and Destination](https://docs.rudderstack.com/getting-started/adding-source-and-destination-rudderstack) guide to know how to add a source in RudderStack.
{% endhint %}

* Select the destination as **AWS Personalize**. Give your destination a name and then click on **Next**. You should then see the following screen:

![](../.gitbook/assets/image%20%2831%29.png)

* Next, in the **Settings** section, ****fill all the fields with the relevant information and click **Next.** A brief description of each of these fields is mentioned below:
  * **Connection Credentials**
    * **Access Key ID**: The access key ID of your AWS account goes here.
    * **Secret Access Key**: Enter the secret access key of your AWS account.
    * **Region**: Please enter the region associated with your AWS account here.
  * **Information on Dataset Group**

    * **TrackingId**: Enter the tracking ID that you generated in the first step 
    * **Type Of Event**: Enter the type of event you want to send for this destination.

  * **Map all the fields**: In this section, enter the **Schema Field** you have used to create the schema in AWS Personalize \(for e.g. `USER_ID`, `TIMESTAMP`, `ITEM_ID`, etc.\). Also, enter the corresponding **Mapped Field** from which the value will be taken from your event payload.

## Contact Us

If you come across any issues while configuring AWS Personalize as a destination with RudderStack, please feel free to [contact us](mailto:%20docs@rudderstack.com). You can also start a conversation on our [Slack](https://resources.rudderstack.com/join-rudderstack-slack) channel; we will be happy to talk to you!

