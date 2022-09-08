---
    title: How to Suggest DTA Payment for Vendors
    description: You can suggest vendor payments using the payment journal, and transfer the overdue invoices into the journal for individual vendors. You can also examine each vendor for open credit memos or open payments, and build a list of vendors for DatenTrägerAustausch (DTA) processing.

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
# How to: Suggest DTA Payment for Vendors
You can suggest vendor payments using the payment journal, and transfer the overdue invoices into the journal for individual vendors. You can also examine each vendor for open credit memos or open payments, and build a list of vendors for DatenTrägerAustausch (DTA) processing. For more information, see [How to: Verify a List of Vendors for DTA Payments](how-to-verify-a-list-of-vendors-for-dta-payments.md).  

During the batch processing of DTA payment suggestions, the foreign currency (FCY) amount is converted to local currency (LCY) at the current rate for FCY payments, and transferred into the payment journal. For more information, see the **Payment Journal** window. In the case of a bank debit, the LCY amount is overwritten with the debited LCY amount, and the exchange rate—or exchange factor—is calculated.

## To suggest DTA payment for vendors  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.  
2.  In the **Batch Name** field, select the required journal batch.  
3.  Select the required payment line, and then choose the **DTA Suggest Vendor Payment** action.  
4.  In the **DTA Suggest Vendor Payments** window, on the **Options** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Posting Date**|Specify the credit date for the payment. This date is useful in determining whether a payment discount has been provided.|  
    |**Due Date from**|Specify the starting date for the open invoices to be included in the payment suggestion.|  
    |**Due Date to**|Specify the ending date for the open invoices to be included in the payment suggestion.|  
    |**Process Cash Discounts**|Specify if the cash discount payments outside the due date range will be considered for the payment suggestion.|  
    |**Cash Disc. Date from**|Specify the starting date for the cash discount. The open entries with cash discount dates within this date range are included in the payment suggestion.|  
    |**Cash Disc. Date to**|Specify the ending date for the cash discount. The open entries with cash discount dates within this date range are included in the payment suggestion.|  
    |**Available Amount (LCY)**|Enter the maximum value of the sum of all payments.|  
    |**First Doc. No.**|Specify the payment suggestion document number. This number is assigned according to the number series for the current log.|  
    |**Debit to Bank**|Select the code of the bank that will receive the debit. The bank must be activated for DTA.|  
    |**Auto. Debit Bank**|Specify if the bank will be debited automatically, depending on the currency code.|  

5.  Choose the **OK** button.  

During processing, each vendor is checked for open credit memos or open payments, and a message displays at the end of the process. All of the related lines are transferred to the payment journal. The related vendor ledger entries are marked with **DTA** to prevent transfer of duplicate entries to the payment journal. You can view, check, and modify the suggested payments, and you can decide whether to reduce the payments by the credit memo amounts, or to apply the open credit memos and open invoices.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Swiss Electronic Payments Using DTA](swiss-electronic-payments-using-dta.md)   
 [How to: Verify a List of Vendors for DTA Payments](how-to-verify-a-list-of-vendors-for-dta-payments.md)   
 [How to: Submit DTA Payments](how-to-submit-dta-payments.md)   
 [How to: Export Payments Using EZAG](how-to-export-payments-using-ezag.md)   
 [Making Payments](../../payables-make-payments.md)
