---
title: AEM Platform Configurations
seo-title: AEM Platform Configurations
description: The page describes AEM Platform Configurations
seo-description: The page describes AEM Platform Configurations
---
# AEM Platform Configurations  {#platform-configurations}

Follow the sections below to set up AEM platform configurations to get started with AEM Screens.

## Server Configurations {#server-configurations}

To set up server configurations, refer to [Server Configurations](https://helpx.adobe.com/experience-manager/6-5/screens/using/configuring-screens-introduction.html#ServerConfiguration)  to set it up.

## Author-Publish {#author-publish}

To set up author-publish, refer to [Configuring Author and Publish in AEM Screens](https://helpx.adobe.com/experience-manager/6-5/screens/using/author-and-publish.html)

>[!NOTE]
>
> If there is only one author and one publish you only need to follow the steps under **Setting up Replication Agents on Author** in [Configuring Author and Publish in AEM Screens](https://helpx.adobe.com/experience-manager/6-5/screens/using/author-and-publish.html) page.


## Dispatcher Configurations {#dispatcher-configurations}

Dispatcher is Adobe Experience Manager's caching and/or load balancing tool. Using AEM's Dispatcher also helps to protect your AEM server from attack. Therefore, you can increase the security of your AEM instance by using the Dispatcher in conjunction with an enterprise-class web server.

Refer to **[Dispatcher Configurations for AEM Screens](https://helpx.adobe.com/experience-manager/6-5/screens/using/dispatcher-configurations-aem-screens.html)** that highlights guidelines for configuring dispatcher for an AEM Screens project.

## Installing FFMpeg {#installing-ffmpeg}

Install FFMpeg following the steps for the appropriate OS (usually RHEL):

1. If installing by enabling EPEL and RPMFusion, you can install all the gstreamer codecs to broaden support for FFmpeg conversions
1. If the AAC codec is marked as experimental, ffmpeg conversions will fail. To avoid this add -strict -2 to the video profiles (/etc/dam/video in AEM 6.3 and moved to /libs/settings/dam/video in AEM 6.4)
   >[!NOTE]
   >
   > Please note that -strict -2 needs to be the last parameters in the list of parameters. Additionally in AEM 6.4 you need to copy the nodes under */libs/settings/dam/video* to */conf/global/settings/dam/video* as mentioned in [Video Renditions](https://helpx.adobe.com/experience-manager/6-5/screens/using/generating-renditions.html).
1. Verify that video conversions are happening and that renditions are being created.

## Passsword Restrictions {#password-restrictions}

The password policy of AEM needs to be disabled on the AMS instance. This can be alternately configured in the web console using the Screens device service *com.adobe.cq.screens.device.impl.DeviceService*
Refer to **Password Restrictions** section in[Configuring Author and Publish in AEM Screens](https://helpx.adobe.com/experience-manager/6-5/screens/using/author-and-publish.html)

## Setting up ACLs {#setting-up-acls}

Setting up ACLs explains how to segregate projects so that each individual or team handles their own project.

As an AEM administrator, you want ensure that team members of a project do not interfere with other projects and each of the users are assigned sepecific roles as per project requirements.

Refer  to [Setting up ACLs](https://helpx.adobe.com/experience-manager/6-5/screens/using/setting-up-acls.html) for more details.