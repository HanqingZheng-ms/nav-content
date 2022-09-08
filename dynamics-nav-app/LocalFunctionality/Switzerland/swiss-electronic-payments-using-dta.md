---
    title: Swiss Electronic Payments Using DTA
    description: In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can make electronic payments for invoices using the DatenTrägerAustausch (DTA) electronic payment method. Swiss banks use the DTA electronic payment method to settle payments efficiently using standardized payment records.

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
# Swiss Electronic Payments Using DTA
In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can make electronic payments for invoices using the DatenTrägerAustausch (DTA) electronic payment method. Swiss banks use the DTA electronic payment method to settle payments efficiently using standardized payment records. This method is based on data carriers and data transfer. This electronic service allows you to convert payments electronically in DTA format, and then submit them to your bank for payment.  

> [!NOTE]  
>  Before you use the DTA electronic payment method, you must define the DTA settings for making electronic payments in the DTA setup. For more information, see the DTA Setup table.  

With DTA electronic payments, you can do the following:  

- Generate vendor payments by processing the automatic DTA payment. For more information, see [How to: Suggest DTA Payment for Vendors](how-to-suggest-dta-payment-for-vendors.md).  

- Verify the list of vendors and payment information. For more information, see [How to: Verify a List of Vendors for DTA Payments](how-to-verify-a-list-of-vendors-for-dta-payments.md).  

- Submit the DTA file to the bank electronically, where vendor payments are released in a few hours. For more information, see [How to: Submit DTA Payments](how-to-submit-dta-payments.md). After this has been done, the payment journal can be posted.  

In the payment journal, you can have the DTA payments suggested based on posted invoices. The suggested payments contain vendor and external document number information, and can be modified. For more information, see [How to: Suggest DTA Payment for Vendors](how-to-suggest-dta-payment-for-vendors.md) and the DTA Payment Journal window.  

When you want to pay a vendor by using DTA, you generate a DTA file, which contains data from the payment journal line and the general journal line. Optionally, the DTA file can combine several payments to the vendor. The DTA file also contains posting text.  

> [!NOTE]  
>  If you combine payments to the vendor, the posting text must include the document numbers of the invoices. Also, if the length of the document number is longer than 50 characters, the word "etc." will be added to the field.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Swiss Electronic Payments](swiss-electronic-payments.md)   
 [How to: Suggest DTA Payment for Vendors](how-to-suggest-dta-payment-for-vendors.md)   
 [How to: Verify a List of Vendors for DTA Payments](how-to-verify-a-list-of-vendors-for-dta-payments.md)   
 [How to: Submit DTA Payments](how-to-submit-dta-payments.md)   
 [How to: Export Payments Using EZAG](how-to-export-payments-using-ezag.md)   
 [Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md)   
 [Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md)  
 [Making Payments](../../payables-make-payments.md) 
