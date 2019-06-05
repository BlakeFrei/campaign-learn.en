---
title: How to set up recurring and continuous email campaigns
seo-title: How to set up recurring and continuous email campaigns
description: This tutorial explains how to set up a recurring and a continuous delivery and the differences between the two approaches.  
seo-description: "After completing this module, you will be able to: - create a recurring delivery - create a continuous delivery - configure a scheduler activity - configure an incremental query - know the difference between tracking a recurring delivery vs. a continuous delivery"
uuid: 100d138d-f615-4f4d-afbd-b79aec9890f6
products: SG_CAMPAIGN/CLASSIC
discoiquuid: 3551093f-c8c4-4861-9561-ff33489da2fe
index: y
internal: n
snippet: y
---

# How to set up recurring and continuous email campaigns

This tutorial explains how to set up a recurring and a continuous delivery and the differences between the two approaches.  

## Recurring and Continuous Delivery Tracking {#recurring-and-continuous-delivery-tracking}

The recurring and continuous deliveries differ in the way contact data is managed:

* The **continuous delivery** lets you add new recipients to an existing delivery and avoids you having to create a new delivery each time a new recipient is added. You can update the creative directly in the campaign workflow and it will update the template in the delivery template Resource folder.  
  
  A continuous delivery will create a SINGLE delivery and delivery logs (broadLog) and tracking logs that reference that one delivery are added each time it executes.

![](assets/delivery_continuous.jpg)

* A **recurring delivery **will create a new delivery instance each time it executes. For example, if the workflow is scheduled to run once a week, that would result in 52 Deliveries after one year. This also means that the broadlog and tracking logs will be separated by each delivery instance.

![](assets/delivery_recurring.jpg)

## How to set up a recurring delivery {#how-to-set-up-a-recurring-delivery}

This video explains how to configure a recurring delivery and a scheduler activity.

>[!VIDEO](https://video.tv.adobe.com/v/25040?quality=12)

## How to set up a continuous delivery {#how-to-set-up-a-continuous-delivery}

This video shows how to configure a continuous delivery with an incremental query.

##

>[!VIDEO](https://video.tv.adobe.com/v/25039?quality=12)

## Additional Resources

-  [Sending a recurring birthday email](https://docs.campaign.adobe.com/doc/AC/en/WKF_Use_cases_Sending_a_recurring_birthday_email.html)