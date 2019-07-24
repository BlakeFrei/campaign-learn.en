---
title: Configure and run workflow with API activity
seo-title: Configure and run workflow with API activity
description: The External API activity allows easy data ingress and egress with REST API systems for batch and blast workflows. 
seo-description: The External API activity allows easy data ingress and egress with REST API systems for batch and blast workflows. 
feature: Data Management
topics: Workflows   
kt: KT-2764
doc-type: feature video
activity: use
team: TM
---

# Configure and run workflow with API activity (beta)

The External API activity allows easy data ingress and egress with REST API systems for batch and blast workflows. 

The External API activity is meant for realtime fetching of campaign wide data (latest set of offers, latest scores etc.) not for retrieving specific information for each profile.  It enables a connection to Adobe I/O Runtime and similar systems (Azure Functions, AWS Lambda) from the workflow

Example use cases:

* Getting the latest game-day lineup for a sports event to personalize content
* Getting the latest set of offers
* Connecting to a coupon generation system
* Checking the weather in local regions and using it to personalize content (each zip code used could potentially retrieve its own local temperature
  
  >[!VIDEO](https://video.tv.adobe.com/v/28200/?quality=12)
  *External API Activity (min 04:12)*
