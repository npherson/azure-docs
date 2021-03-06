---
title: Monitor messages in B2B transactions - Azure Logic Apps | Microsoft Docs
description: Monitor and track messages during B2B communication between processes and apps using Logic Apps in your Integration Account.
author: padmavc
manager: anneta
editor: ''
services: logic-apps
documentationcenter: ''

ms.assetid: bb7d9432-b697-44db-aa88-bd16ddfad23f
ms.service: logic-apps
ms.workload: integration
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 10/21/2016
ms.author: padmavc

---
# Monitor B2B messages
B2B communication involves message exchanges between two running business processes or applications. The relationship defines an agreement between business processes. Once the communication has been established, there needs to be a way to monitor if the communication is working as expected.  Message tracking has been implemented for the B2B protocols: AS2, X12, and EDIFACT.  You can configure your Integration Account to use Diagnostics for richer details and debugging

## Prerequisites
* An Azure account; you can create a [free account](https://azure.microsoft.com/free)
* An Integration Account; you can create an [Integration Account](logic-apps-enterprise-integration-create-integration-account.md)
* A Logic App; you can create a [Logic App](logic-apps-create-a-logic-app.md) and [enable logging](logic-apps-monitor-your-logic-apps.md)

## Enable logging for an integration account
You can enable logging for an integration account either with **Azure portal** or with **Monitor**

### Enable logging with Azure portal

1. Select **integration account** and select **diagnostics logs** 
![select integration account](media/logic-apps-monitor-b2b-message/pic5.png)  

2. Select your **Subscription** and **Resource Group**, **Integration Account** from Resource Type and select your **Integration Account** from Resource drop-down to enable diagnostics.  Click **Turn on Diagnostics** to enable diagnostics for the selected Integration Account               
![select Integration Account](media/logic-apps-monitor-b2b-message/pic2.png) 

3. Select status **ON**       
![Turn diagnostics on](media/logic-apps-monitor-b2b-message/pic3.png) 

4. Select **Send to Log Analytics** and configure Log Analytics to emit data               
![Turn diagnostics on](media/logic-apps-monitor-b2b-message/pic4.png)

### Enable logging with Monitor

1. Select **Monitor** and click **Diagnostics logs**   
![select Monitor](media/logic-apps-monitor-b2b-message/pic1.png)

2. Select your **Subscription** and **Resource Group**, **Integration Account** from Resource Type and select your **Integration Account** from Resource drop-down to enable diagnostics.  Click **Turn on Diagnostics** to enable diagnostics for the selected Integration Account               
![select Integration Account](media/logic-apps-monitor-b2b-message/pic2.png)

3. Select status **ON**       
![Turn diagnostics on](media/logic-apps-monitor-b2b-message/pic3.png) 

4. Select **Send to Log Analytics** and configure Log Analytics to emit data 
![Turn diagnostics on](media/logic-apps-monitor-b2b-message/pic4.png)

## Extending your solutions
In addition to the **Log Analytics**, you can configure your Integration Account and [Logic Apps](./logic-apps-monitor-your-logic-apps.md) to an Event Hub or Storage Account         
![Azure Diagnostics settings](./media/logic-apps-monitor-your-logic-apps/diagnostics.png)


You can use this telemetry from the Event Hub or Storage into other services like [Azure Stream Analytics](https://azure.microsoft.com/services/stream-analytics/), and [Power BI](https://powerbi.com) to have real-time monitoring of your integration workflows.

## Supported Tracking Schema
We are supporting following tracking schema types.  All of them has fixed schemas except Custom type.

* [Custom Tracking Schema](logic-apps-track-integration-account-custom-tracking-schema.md)   
* [AS2 Tracking Schema](logic-apps-track-integration-account-as2-tracking-schemas.md)   
* [X12 Tracking Schema](logic-apps-track-integration-account-x12-tracking-schema.md)  

## Next steps
[Tracking B2B messages in OMS Portal](logic-apps-track-b2b-messages-omsportal.md "Tracking B2B messages")   
[Learn more about the Enterprise Integration Pack](logic-apps-enterprise-integration-overview.md "Learn about Enterprise Integration Pack") 

