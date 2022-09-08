---
    title: How to Download CODA Files from an Isabel Server
    description: CODA files can be downloaded manually or in attended mode.

    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 07/01/2017
    ms.author: edupont

---
# How to: Download CODA Files from an Isabel Server
CODA files can be downloaded manually or in attended mode.  

To manually download CODA files, log  on to the Isabel server and select the files that you want to download. The downloaded files can then be imported from the **Bank Account** table. For more information, see [How to: Import CODA Statements](how-to-import-coda-statements.md).  

## To download CODA files in attended mode  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **IBS Logs**, and then choose the related link.  
2.  Choose the **Download** action.  
3.  In the **IBS Download Request Options** window, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**From Date**|Specify the start date of the download.|  
    |**To Date**|Specify the end date of the download.|  
    |**File Format**|Select **Coda** as the file format.|  
    |**File Status**|Select the file status of the download. File statuses include **Not Downloaded**, **Downloaded**, and **All**. Typically you will select **Not Downloaded**, because you are downloading the CODA files that have not been downloaded to your system.|  

4.  Choose the **OK** button.  

    > [!NOTE]  
    >  You cannot delete any files from the Isabel server by using the **IBS Download Request Options** window. You must manually delete the files by logging on to the Isabel server.  

     After the CODA files have been downloaded, the **Process Status** field will display **Created** in the **IBS Logs** window. You can log on to the Isabel server to manually retrieve the files. For more information, see [How to: Import CODA Statements](how-to-import-coda-statements.md).  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Belgium Local Functionality](belgium-local-functionality.md)
