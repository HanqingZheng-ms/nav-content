---
title: Specify the Layout of a Check
description: You can design and print your checks in different formats to conform with standards.
author: edupont04

ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont

---
# How to: Define Check Layouts
You can design your checks to conform with the standards set by the local authorities. Check images can be printed in English, French, or Spanish.

Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.

## To define check layouts
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.
2. In the **Report Selection - Bank Acc.** window, in the **Usage** field, select **Check**.
3. Select one of the following report IDs.

| Report ID | Report Name | Description |
| --- | --- | --- |
| 1401 |Check |This is the default report. |
| 10411 |Check (Stub/Stub/Check) |This report is designed to print checks in a stub/stub/check format. |
| 10412 |Check (Stub/Check/Stub) |This report is designed to print checks in a stub/check/stub format. |
| 10413 |Three Checks per Page |This report is designed to print three checks on each page. |

When you have set up check layouts, you can print checks from the **Payment Journal** window. For more information, see [How to: Work with Checks](payables-how-work-checks.md).

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Managing Payables](payables-manage-payables.md)  
[Managing Bank Accounts](bank-manage-bank-accounts.md)   
[Completing Period-End Processes](year-how-complete-period-end-processes.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[General Business Functionality](ui-across-business-areas.md)
