---
title: Data Service
seo-title: ACS Data Service
description: The ACS Data Service is a helper service that enables customer data to flow from ACS to the platform
seo-description: The ACS Data Service is a helper service that enables customer data to flow from ACS to the platform
uuid: add8c2b6-834b-4c3d-bcde-57c72e3ce0ae
products: SG_CAMPAIGN/STANDARD
discoiquuid: 591a564a-39df-4fcc-a412-0899ae24b7c3
targetaudience: target-audience new;target-audience ongoing
index: y
internal: y
snippet: y
---

# Data Service

The ACS Data Service is a helper service that enables customer data to flow from ACS to the platform.

Data Service enables Adobe Campaign Standard users to map custom resources and experience events residing in Campaign Standard to XDM schema and transmit data from Campaign Standard to Data platform. It transmits data natively collected in Campaign (touch points/Landing Pages, subscription / unsubscription etc.) to Platform . Both Batch as well as Streaming Data Transfer are covered. The service is Uni-Directional, from Campaign to Platform only.

The mapping feature is intended for data engineers who understand Adobe Campaign Standard resources and have an understanding of how customer's overall data schema should be inside Adobe Experience Platform.

## Understand OOTP Mapping in ACS Data Service

>[!VIDEO](https://video.tv.adobe.com/v/27304/?quality=12)
*This video gives an overview over the Data Service feature in ACS (09:35 min)*

>[!NOTE]
>
>The out-of-the-box transfer of subscription events is not supported. To transfer subscription events, you can create corresponding XDM and dataset on AEP, then configure a custom data mapping for these data.
>
>Existing experience events cannot be ingested into AEP, but ongoing generated experience events will be streamed to AEP.

## Mapping Custom Resources of the Data Types (integer, strings, etc.)

>[!VIDEO](https://video.tv.adobe.com/v/27231/?quality=12)
*This video explains how to map different data types between Adobe Campaign Standard (ACS) and Adobe Experience Platform (AEP) (6:01 min)*

## Adding Identity Namespaces in a Mapping

There are two ways to add identity namespaces, either in Adobe Experience Platform or directlt y in Adobe Campaign Standard. The video below desciribes both options. 

You can find more information in namespaces in the [documentation](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/identity_namespace_overview/identity_namespace_overview.md).

>[!NOTE]
>
>The Expression to define the primary identity of a namespace in ACS is:
>
>`/identityMap/your namespace code/0/id  (e.g.: /identityMap/Email/0/id)`

>[!VIDEO](https://video.tv.adobe.com/v/27360/?quality=12)
*This video describes the two ways to add identity name spaces (05:56 min)*

More information namespaces can be found in the [Identity namespace overview](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/identity_namespace_overview/identity_namespace_overview.md).

## How to Check the Status of Mapping and Use Edit/ Publish/ Save the Mapping, Introduce the Concept of Audit Fields

>[!VIDEO](https://video.tv.adobe.com/v/27266/?quality=12)
*This video describes the different mapping statuses (02:46 min)*


## How to Lookup the Status of a Job

>[!VIDEO](https://video.tv.adobe.com/v/27268/?quality=12)
*This video explains how to check if the data has been injested into the from ACS into AEP (04:11 min)*

## How to Ingest CDP as Part of Experience Events

>[!VIDEO](https://video.tv.adobe.com/v/27265/?quality=12)
*This video explains how experience events are mapped in AEP (06:25 min)*

## Mapping Seed Table Data

>[!VIDEO](https://video.tv.adobe.com/v/27264/?quality=12
*This video explains how to map you seed data / test profiles with the Adobe Experience Platform (AEP) (02:53 min)*

## Additional Resources

* [Understand data definition and flows to carry your local data onto the Adobe Experience Platform (documentation)](https://docs.adobe.com/content/help/en/campaign/prerelease/administration/about.html)
* [Identity namespace overview (documentation)](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/identity_namespace_overview/identity_namespace_overview.md)
  