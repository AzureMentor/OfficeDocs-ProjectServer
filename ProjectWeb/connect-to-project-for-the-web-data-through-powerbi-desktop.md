---
title: 'Connect to Project for the web data through Power BI Desktop'
description: 'Connect to Project for the web data through Power BI Desktop'
author: efrene
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 10/29/2019
audience: admin
ms.topic: article
ms.service: project-web
search.appverid: PJO150
localization_priority: Normal

---
# Connect to Project for the web data through Power BI Desktop


## Get started 
You first need to do the following:

- Download [Power BI Desktop](https://go.microsoft.com/fwlink/?LinkID=521662), then run the installer to get **Power BI Desktop** on your computer.
- Download the [Project for the web Power BI template](https://aka.ms/ProjectReports) to your computer.

## Launch and configure the Power BI Desktop template file
1. Click on the Project for the web Power BI template file to open it in Power BI Desktop.
2. In the **Enter Parameters** screen, in the **CDS URL** field, type the URL of your Dynamics 365 Common Data Service (CDS) default instance you are using for Project for the web, and then click **Load**.<br/>
![Default CDS environment](media/Parameter.png)
3.  Power BI Desktop will prompt you to authenticate with your Office 365 account. Select **Organizational account** and then click **Sign In**.</br>
![Default CDS environment](media/OrgSignin.png)
4.  A message will display telling you that your data is loading. Depending on the number of projects, tasks, and resources in your system, this may take some time. 


### How to determine your CDS URL

 Project for the web data is stored in the Dynamics 365 Common Data Service (CDS). You need to enter the URL of your default CDS instance that you are using, and it needs to be in the following format: 

https://<spam><spam>(environment_name).(region).dynamics<spam><spam>.com

For example:
https://<spam><spam>orgde6d15d8.crm.dynamics<spam><spam>.com

The following will tell you how to find the *environment_name* and the *region* values of the URL.

**To determine the Default CDS environment name value of the URL**:

1. While logged into Office 365, go to this site:  https://<spam><spam>web.powerapps<spam><spam>.com
2. On the PowerApps page, note the value in the **Environments** section.  In the image below, the default CDS environment value is **orgde6d15d8**.

    ![Default CDS environment](media/PowerAppsPage.png)

**To determine the region value of the URL**:

The region value will usually be associated to the data center that is close to you geographically. The following list shows the region values associated with regional data centers.

|||
|:-----|:-----|
|**Region** <br/> |**Value** <br/> |
|North America   <br/> |crm <br/> |
|South America <br/> |crm2  <br/> |
|Canada   <br/> |crm3 <br/> |
|Europe, Middle East and Africa (EMEA)  <br/> |crm4<br/> |
|Asia Pacific Area (APAC)  <br/> |crm5 <br/> |
|Oceania   <br/> |crm6 <br/> |
|Japan   <br/> |crm7 <br/> |
|India  <br/> |crm8 <br/> |
|North America 2   <br/> |crm9 <br/> |
|United Kingdom   <br/> |crm11 <br/> |
|France  <br/> |crm12 <br/> |

If you are not sure, check with your Office 365 administrator and have them check for the value in the [Power Platform Admin Center](https://docs.microsoft.com/power-platform/admin/admin-guide).

![PowerPlatform Admin Center](media/PowerPlatformAdminCenter.png)

## After connecting to your data

After Power BI Desktop retrieves the data, the visualizations in each report page will load and display the data.  

> [!Note]
> You need to have read permissions at the business-unit level to the CDS entities to which the report connects to have a portfolio-level view of the data.  


From the Power BI Desktop, we recommend [publishing the report to a shared workspace](https://docs.microsoft.com/power-bi/desktop-upload-desktop-files), and then [configure scheduled refresh of the data to keep your dataset up to date](https://docs.microsoft.com/power-bi/refresh-scheduled-refresh).

## See also

[Compose HTTP requests and handle errors](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/compose-http-requests-handle-errors#web-api-url-and-versions).   

  






