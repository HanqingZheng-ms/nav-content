---
    title: How to Export Payments Using EZAG
    description: You can generate a file for electronic payment using the Elektronischer Zahlungsauftrag (EZAG) method, and export it for the bank to use for the payments.

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
# How to: Export Payments Using EZAG
You can generate a file for electronic payment using the Elektronischer Zahlungsauftrag (EZAG) method, and export it for the bank to use for the payments.  

## To export payments using EZAG  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.  
2.  In the **Batch Name** field, select the journal batch name.  
3.  Choose the **Generate EZAG File** action.  
4.  In the **EZAG File** batch job, on the **Options** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Debit to bank**|Specify the code of the bank to be charged.|  
    |**Combined payment for vendor**|Specify if the payment lines that have the same vendor, currency, bank, and debit bank in the generated EZAG file will be combined.|  
    |**Shipment with disk**|Specify if the EZAG file will be saved to a disk so that you can deliver it to the bank.|  

5.  Choose the **OK** button. The EZAG file is generated.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Swiss Electronic Payments Using DTA](swiss-electronic-payments-using-dta.md)   
 [How to: Suggest DTA Payment for Vendors](how-to-suggest-dta-payment-for-vendors.md)   
 [How to: Verify a List of Vendors for DTA Payments](how-to-verify-a-list-of-vendors-for-dta-payments.md)   
 [How to: Submit DTA Payments](how-to-submit-dta-payments.md) 
