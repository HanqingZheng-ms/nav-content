---
    title: How to Fiscally Close Years
    description: When a fiscal year is complete, you must fiscally close the periods that it comprises to make sure that no more general ledger entries can be posted.

    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/21/2020
    ms.author: edupont

---
# How to: Fiscally Close Years
When a fiscal year is complete, you must fiscally close the periods that it comprises to make sure that no more general ledger entries can be posted.  

Before fiscal closing is allowed the following must be done:  

- The fiscal year has been closed first. For more information, see [How to: Close Years](how-to-close-years.md).  
- All journal lines that are not posted and all simulation entries for the year are either posted or deleted before the year is fiscally closed.
- All closing entries are up-to-date.  

## To fiscally close years  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the relevant link.  
2.  On the **Navigate** tab, in the **Fiscal Closing** group, choose the **Fiscally Close Year** check box.  

    If more than one fiscal year is not fiscally closed, the earliest one should be fiscally closed. A message appears that identifies the year that should be closed and explains the consequences of closing it.  

3.  To fiscally close the year, choose the **Yes** button.  

When the fiscal year is fiscally closed, the **Fiscally Closed** field for all the periods in the year is selected. The fiscally closed year cannot be opened again, and you cannot clear the **Fiscally Closed** field.  

General journal entries can still be posted as long as the **Allow posting from** and **Allow posting to** fields in the posting setup for the relevant users are within the posting date of the entry. Once posted, this will be tagged as prior-year entry on the general ledger entries.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[How to: Close Years](how-to-close-years.md)   
 [Year End Processes Overview](year-end-processes-overview.md)   
 [How to: Post the Year-End Closing Entry](how-to-post-the-year-end-closing-entry.md)   
 [Closing Years and Periods](../../year-close-years-periods.md)  
