---
    title: How to Set Up VAT Ledgers
    description: VAT ledgers are used to store details about VAT in transactions that involve goods and services in Russia or goods imported into Russia. You can create and store different kinds of VAT ledgers.

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
# How to: Set Up VAT Ledgers
VAT ledgers are used to store details about VAT in transactions that involve goods and services in Russia or goods imported into Russia. You can create and store different kinds of VAT ledgers. For example, you can create VAT ledgers for:  

- Sales to different groups of customers.  
- Sales amount differences and prepayments.  
- Purchases from different vendor groups.  

To use VAT ledgers, you must specify the relevant number series.  

## To set up VAT ledgers  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.  
2.  In the **General Ledger Setup** window, on the **Numbering** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**VAT Purch. Ledger No. Series**|Specifies the number series that you want to use for VAT ledgers for purchase documents.|  
    |**VAT Sales Ledger No. Series**|Specifies the number series that you want to use for VAT ledgers for sales documents.|  

     You must ensure that vendor purchase documents cannot be posted without stating the invoice date and number.  

3.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.  
4.  In the **Vendor Posting Groups** window, for the relevant posting groups, select the **VAT Invoice Mandatory** field.  

    Next, you must set up VAT posting. For each VAT posting setup you must specify if entries that use the setup must be included in VAT ledgers.  
5.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Posting Setup**, and then choose the related link.  
6.  In the **VAT Posting Setup** window, for each VAT posting setup, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Not Include into VAT Ledger**|Specifies if entries that use the setup must be included in VAT ledgers. For more information, see Not Include into VAT Ledger.|  
    |**VAT Exempt**|Specifies if entries that use this posting setup are VAT exempt. For more information, see VAT Exempt.|  

Now, you can create VAT ledgers for purchases and sales.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[How to: Report VAT to Tax Authorities](../../finance-how-report-vat.md)  
 [How to: Register VAT on Purchase Orders](how-to-register-vat-on-purchase-orders.md)   
 [How to: Prepare VAT Entries for Posting](how-to-prepare-vat-entries-for-posting.md)   
 [How to: Create VAT Ledgers](how-to-create-vat-ledgers.md)   
 [How to: Create Additional Sheets](how-to-create-additional-sheets.md)
