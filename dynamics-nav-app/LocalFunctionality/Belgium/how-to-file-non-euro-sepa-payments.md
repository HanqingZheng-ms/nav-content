---
    title: How to File Non-Euro SEPA Payments
    description: In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can file non-euro SEPA payments with the bank. This is useful when you make payments to other countries/regions that do not use SEPA and for currencies other than the euro.

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
# How to: File Non-Euro SEPA Payments
In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can file non-euro SEPA payments with the bank. This is useful when you make payments to other countries that do not use SEPA and for currencies other than the euro.  

Before you can file a non-euro SEPA payment you must complete the following administration tasks:  

- Set up a new export protocol for a non-euro SEPA. For more information, see Export Protocol.  
- In the **Country/Region** table, clear the **SEPA Allowed** field for each country that belongs to the EEA zone.  
- Verify that the **Currency Euro** field in the **General Ledger Setup** table is not in euro currency.  
- Verify that the vendor’s **Preferred Bank Account** field in the **Vendor** table contains the IBAN and SWIFT code.  

## To file a non-euro SEPA payment  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **File Non Euro SEPA Payments**, and then choose the related link.  
2.  Fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Journal Template Name**|Specify the general journal template for the non-euro SEPA payment report.|  
    |**Journal Batch**|Specify the general journal batch for the non-euro SEPA payment report.|  
    |**Post General Journal Lines**|Specify if you want to transfer the payment lines to the general ledger.|  
    |**Include Dimensions**|Enter the dimensions that you want to include in the non-euro SEPA payment report. The option is only available if the **Summarize Gen. Jnl. Lines** field in the **Electronic Banking Setup** window is selected.|  
    |**Execution Date**|Enter an execution date if you want an execution date that differs from the posting date on the payment lines.|  
    |**File Name**|Enter the name of the file, including the drive and folder, to which you want to print the report.|  

3.  Choose the **OK** button.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[How to: File SEPA Payments](how-to-file-sepa-payments.md)   
 [How to: Activate SEPA Payments](how-to-activate-sepa-payments.md)   
 [SEPA Payments](sepa-payments.md)
