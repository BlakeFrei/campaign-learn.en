---
title: In-App Messaging Tutorial
seo-title: In-App Messaging Tutorial
description: In-App Messaging  allows you to present the user with contextually relevant In-App messages in response to a customer's real-time behavior within the mobile application.
seo-description: In-App Messaging  allows you to present the user with contextually relevant In-App messages in response to a customer's real-time behavior within the mobile application.
uuid: 50a13c41-88ad-43c4-8c42-d941bca2bf0a
products: SG_CAMPAIGN/STANDARD
discoiquuid: a3c10847-6163-4915-aae5-6200cd0474e5
targetaudience: target-audience new;target-audience ongoing
index: y
internal: n
snippet: y
---

# In-App Messaging Tutorial{#in-app-messaging-tutorial}

## General Overview {#general-overview}

In-App Messaging is a channel that allows you to display a message when the user is active within the mobile application. This channel requires mobile applications to be integrated with Adobe Experience Platform SDK.

This tutorial will explain the steps required to set up the mobile properties, the launch extension for the In-App Messaging channel, as well as how to prepare, customize, and send In-App Messages in Adobe Campaign Standard.

## Prerequisites {#prerequisites}

1. Make sure you can access the **In-App** channel. If you cannot access these channels, contact your account team.  
1. Verify that your **user** has the necessary **permissions** in Adobe Campaign Standard and Launch.

    1. In Adobe Campaign Standard, ensure that the IMS user is part of the Standard User and Administrator groups.  
       This step allows the user to log in to Adobe Campaign Standard, navigate to the Experience Platform SDK mobile app page, and view the mobile app properties that you created in Launch.
    1. In Launch, ensure that your IMS user is part of a Launch product profile.  
       This step allows the user to log in to Launch to create and view the properties. For more information about product profiles in Launch, see [Create your product profile](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile). In the product profile, there should be no permissions set on the company or the properties, but the user should be able to still log in.

1. In **Adobe Launch:**

    1. create the mobile application by creating a mobile property and instrument your mobile app with Experience Platform SDK.
    1. Install the **Adobe Campaign Standard** extension for your mobile application

For more on extensions, refer to the [Configure Campaign Standard Extension in Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) in Adobe Launch documentation.

## Configuring a mobile application using Adobe Experience Platform SDK {#configuring-a-mobile-application-using-adobe-experience-platform-sdk}

To send In-App messages (and push notifications) with an Experience Cloud SDK application, a mobile app has to be set up in Adobe Experience Platform Launch and be configured in Adobe Campaign.

The video below demonstrate the required steps to configure a mobile app in Launch:

>[!VIDEO](https://video.tv.adobe.com/v/26224?quality=12)

>[!NOTE]
>See [Configuring your application in Launch](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#ConfiguringyourapplicationinLaunch) for the detailed documentation and the code templates used in the video.


## Configuring Events {#configuring-events}

When configuring an In-App message you need to define which user initiated action will trigger the message to be displayed. These actions are called events. Three categories of events are available: Mobile Application events, Life Cycle events, and Analytics events.

### 1. Mobile Application Events {#mobile-application-events}

Mobile Application events are custom events that are implemented in your mobile application.

Examples are:

* A customer has viewed an item
* A customer adds an item to the cart
* Cart abandonment
* A customer has purchased something

You will need to configure these events in Adobe Campaign. The video below describes how to do this.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)
*In-App channel-specific application configuration in Adobe Campaign*

### 2. Life Cycle Events  {#life-cycle-events}

Lifecycle events are out-of-the-box events. The following events are available:

* launched
* upgraded
* crashed

An example use case could be a message introducing new features after an upgrade, or an event promotion.

>[!NOTE]
>
>The Lifecycle module needs to be configured in the mobile application. Please see here for more information on [how to add Lifecycle to your app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

### 3. Analytics Events {#analytics-events}

The following three categories are supported depending on what is instrumented in your mobile app:

* Adobe Analytics
* Context data 
* View state.

>[!NOTE]
>
>Analytics events require an Adobe Analytics licence. Once you have the [Analytics extension configured](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) and have added [Analytics to your App](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), these events become available in the In-App configuration in ACS.

## Create, manage, and publish In-App messages {#create-manage-and-publish-in-app-messages}

With this channel, you will have the option to target your users through different delivery templates

### 1. Broadcast In-App message (Target all users of a mobile app) {#broadcast-in-app-message-target-all-users-of-a-mobile-app}

To Broadcast to all users of your mobile app whether or not Campaign has their profile information, you will need to use the **Target all users of a mobile app template.**

Some of the pertinent use cases in this category are - mobile app tutorials to first time app launchers or announcements for new feature releases.

>[!VIDEO](https://video.tv.adobe.com/v/26199?quality=12)
*Create a Broadcast In-App message using an SDKV5 Mobile property*

### 2. Target all users based on their mobile app profile {#target-all-users-based-on-their-mobile-app-profile}

Target all known and/or unknown users (those who have browsed the app in an anonymous mode) with message personalized with user attributes obtained from m This delivery template is geared towards a mixed user base of some known and some anonymous profiles. So, the personalization strategy is based on what you have learnt about the users from their interaction with the device (e.g. target all users who have who have launched their App more than 5 times in last one week).

### 3. Target users based on their Campaign profile {#target-users-based-on-their-campaign-profile}

Target known mobile app users (those who have logged into the app with PII) with message personalized with CRM profile attributes available in Campaign. This template is most useful to support cross-channel orchestration use cases, where you have already targeted users on other channels like Email or Push and based on their response, you want to engage them with an in-app message.

>[!VIDEO](https://video.tv.adobe.com/v/26200?quality=12)

*Create an In-App message using a Campaign profile template*

## Creating a In-App delivery within a workflow {#creating-a-in-app-delivery-within-a-workflow}

The In-App delivery activity is generally used to automate sending an In-App message to a target audience calculated in the same workflow.

The recipients are defined upstream of the activity in the same workflow, via targeting activities such as queries, intersections, etc.

The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can choose t to request a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.

>[!VIDEO](https://video.tv.adobe.com/v/26226?quality=12)

*Creating a In-App delivery within a workflow*

## In-App message reporting {#in-app-message-reporting}

You can review your In-app delivery related data either in the Delivery Summary by adding In-App specific metrics. Alternatively, you can use the out of the box [In-App Report](https://helpx.adobe.com/campaign/standard/reporting/using/in-app-report.html).

>[!VIDEO](https://video.tv.adobe.com/v/26412?quality=12)

*Introduction to In-App reporting*

## Additional Resources

* [In-App Report (documentation)](https://helpx.adobe.com/campaign/standard/reporting/using/in-app-report.html)
* [Set up a mobile property  (Adobe Launch documentation)](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configuring a mobile application using Adobe Experience Platform SDKs (documentation)](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html)
* [Preparing and sending an In-App message (documentation)](https://helpx.adobe.com/campaign/standard/channels/using/preparing-and-sending-an-in-app-message.html)
* [Customizing an In-App message (documentation)](https://helpx.adobe.com/campaign/standard/channels/using/customizing-an-in-app-message.html)
* [Sending an In-App message within a workflow  (documentation)](https://helpx.adobe.com/campaign/standard/automating/using/in-app-delivery.html)
* [Enable Lifecycle Metrics (documentation)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
