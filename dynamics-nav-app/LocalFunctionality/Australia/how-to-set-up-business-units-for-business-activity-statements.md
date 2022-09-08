---
    title: How to Set Up Business Units for Business Activity Statements
    description: In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can consolidate the financial statements of various companies into one financial statement.

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
# How to: Set Up Business Units for Business Activity Statements
In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can consolidate the financial statements of various companies into one financial statement.  

You must set up a consolidation company to perform the consolidation. In this company, the total amounts for all accounts in the group, from both the parent company and subsidiaries are added together. You must also indicate the general ledger accounts in the consolidated company to which the total should be transferred.  

You can use the **BAS Business Units** window to set up the following:  

- Parent company  
- Subsidiaries  
- Affiliates  

You must set up information in the **General Ledger Setup** window before you can set up business units.  

## To set up general ledger for a business activity statement  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.  
2.  Fill in the required fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**BAS to be Lodged as a Group**|Select if you are logging a business activity statement for a group of companies.|  
    |**BAS Group Company**|Select if this company is the main company in the group of companies for which you are lodging a group business activity statement.|  

3.  Choose the **OK** button.  

## To set a business unit for a business activity statement  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **BAS Business Units**, and then choose the related link.  
2.  Fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Company Name**|Specify the name of the company which will be added to the group company's business activity statement.|  
    |**Document No.**|Specify the BAS document number that has to be consolidated. This field is associated with the **BAS Version** field.|  
    |**BAS Version**|Specify the BAS version number in which the transaction was included. This field is associated with the **Document No.** field.|  

3.  Choose the **OK** button.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Business Activity Statements](business-activity-statements.md)   
 [How to: Set Up Business Activity Statements](how-to-set-up-business-activity-statements.md)
