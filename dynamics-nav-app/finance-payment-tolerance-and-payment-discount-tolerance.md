---
    title: Payment Tolerance and Payment Discount Tolerance 
    description: You can set up payment tolerance to close an invoice when the payment does not fully cover the amount on the invoice.
    
    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 08/10/2017
    ms.author: edupont

---
# How to: Work with Payment Tolerances and Payment Discount Tolerances
You can set up a payment tolerance to close an invoice when the payment does not fully cover the amount on the invoice. You can set up a payment discount tolerance to grant a payment discount after the payment discount date has passed.  

You can use payment tolerances so that every outstanding amount has a set maximum allowed payment tolerance. If the payment tolerance is met, then the payment amount is analyzed. If the payment amount is an underpayment, then the outstanding amount is fully closed by the underpayment. A detailed ledger entry is posted to the payment entry so that no remaining amount is left on the applied invoice entry. If the payment amount is an overpayment, then a new detailed ledger entry is posted to the payment entry so that no remaining amount is left on the payment entry.

You can use payment discount tolerances so that if you accept a payment discount after the payment discount date, then it is always posted to either the payment discount account or a payment tolerance account.

## Applying Payment Tolerance to Multiple Documents  
A single document has the same payment tolerance whether it is applied on its own or with other documents. Acceptance of a late payment discount when you are applying payment tolerance to multiple documents automatically occurs for each document where the following rule is true:  

*payment discount date < payment date on the selected entry <= payment tolerance date*  

This rule also applies to determine whether to display warnings when you apply payment tolerance to multiple documents. The payment discount tolerance warning is displayed for each entry that meets the date criteria. For more information, see the "Example 2 - Tolerance Calculations for Multiple Documents" section. 

You can choose to display a warning that is based on different tolerance situations.  

- The first warning is for the payment discount tolerance. You are informed that you can accept a late payment discount. You can then choose whether to accept tolerance on the discount date.  
- The second warning is for the payment tolerance. You are informed that all entries can be closed because the difference is in the sum of the maximum payment tolerance for the applied entries. You can then choose whether to accept tolerance on the payment amount.

For more information, see the "To enable or disable payment tolerance warning" section.     

## To set up tolerances  
Tolerance on days and amounts allows you to close an invoice even though the payment does not fully cover the amount on the invoice, whether this is because the due date for the payment discount has been exceeded, goods have been deducted or because of a minor error. This also applies to refunds and credit memos.  

To set up tolerance you have to set up various tolerance accounts, specify both payment discount tolerance and payment tolerance posting methods and then run the **Change Payment Tolerance** batch job.  
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Posting Setup**, and then choose the related link.  
2. In the **General Posting Setup** window, set up a debit and a credit sales payment tolerance account and a debit and a credit purchase payment tolerance account.  
3. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.    
4. In the **Customer Posting Groups** window, set up a debit and a credit payment tolerance account. For more information, see [Setting Up Posting Groups](finance-posting-groups.md).  
5. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Setup**, and then choose the related link.  
6. In the **Vendor Posting Groups** window, set up a debit and a credit payment tolerance account.  
7. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.  
8. Open the **General Ledger Setup** window.  
9. On the **Application** FastTab, fill in the **Pmt. Disc. Tolerance Posting**, **Payment Discount Grace Period** and **Payment Tolerance Posting** fields.   
10. Choose the **Change Payment Tolerance** action.
11. In the **Change Payment Tolerance** window, fill in the **Payment Tolerance %** and **Max Payment Tolerance Amount** fields, and then choose the **OK** button.

> [!IMPORTANT]  
>  You have now set up tolerance for local currency only. If you want [!INCLUDE[d365fin](includes/d365fin_md.md)] to handle tolerance on payments, credit memos, and refunds in a foreign currency, you must run the **Change Payment Tolerance** batch job with a value in the **Currency Code** field.  

> [!NOTE]  
>  If you want to get a payment tolerance warning every time that you post an application in the tolerance, you must activate the payment tolerance warning. For more information, see the "To enable or disable payment tolerance warning" section.  
>   
>  To deactivate tolerance for a customer or vendor, you must block tolerances on the relevant customer or vendor card. For more information, see the "To block payment tolerance for customers" section.  
>   
>  When you set up tolerance, [!INCLUDE[d365fin](includes/d365fin_md.md)] also checks if there are any open entries and calculates the tolerance for these entries.

## To enable or disable payment tolerance warnings
The payment tolerance warning appears when you post an application that has a balance in the allowed tolerance. You can then choose how you want to post and document the balance.    
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.  
2. In the **General Ledger Setup** window, on the **Application** FastTab, select the **Payment Tolerance Warning** check box to activate the warning. To deactivate the warning, clear the check box.  

> [!NOTE]  
>  The default option for the **Payment Tolerance Warning** window is **Leave the Balance as Remaining Amount**. The default option for the **Pmt. Disc. Tolerance Warning** window the is **Do Not Accept the Late Payment Discount**.

## To block payment tolerance for customers  
The default setting for payment tolerance is allowed. To disallow a certain customer or vendor payment tolerance you need to block tolerance on the respective customer or vendor card. The following describes how to do it for a customer. The steps are similar for a vendor.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer** or **Vendor**, and then choose the related link.  
2. On the **Payments** FastTab, select the **Block Payment Tolerance** check box.  

> [!NOTE]  
>  If the customer or vendor has open entries, you must first remove payment tolerance from entries that are currently open.

## Example 1 - Tolerance Calculations for a Single Document
The following are some example scenarios showing the expected tolerance calculations and postings occurring in different situations.  

The **G/L Setup** window contains the following setup:
- Payment Discount Grace Period: 5D  
- Max Payment Tolerance: 5  

Scenarios with alternative A or B represent the following:  

- **A** In this case, the payment discount tolerance warning has been turned off OR the user has the warning on and has selected to allow the late payment discount (Post the Balance as Payment Tolerance).  
- **B** In this case, the user has the warning on and has selected not to allow the late payment discount (Leave the Balance as Remaining Amount).  

|—|Inv.|Pmt. Disc.|Max<br /><br /> Pmt. Tol.|Pmt. Disc. Date|Pmt. Disc. Tol. Date|Payment Date|Pmt.|Tolerance Type|All Entries closed|Pmt. Disc. Tol. <br /> GL/CL|Pmt.<br /><br /> Tol.<br /><br /> G/L|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1,000|20|5|01/15/03|01/20/03|<=01/15/03|985|Pmt.Tol.|Yes|0|-5|  
|2|**1,000**|**20**|**5**|**01/15/03**|**01/20/03**|**<=01/15/03**|**980**|**None**|**Yes**|**0**|**0**|  
|3|1,000|20|5|01/15/03|c|<=01/15/03|975|Pmt.Tol.|Yes|0|5|  
|4A|1,000|20|5|01/15/03|01/20/03|01/16/03 01/20/03|1005|Pmt.Disc.Tol.|No, 25 on the Pmt.|20/-20|0|  
|5A|1,000|20|5|01/15/03|01/20/03|01/16/03 01/20/03|1000|Pmt.Disc.Tol.|No, 20 on the Pmt.|20/-20|0|  
|6A|1,000|20|5|01/15/03|01/20/03|01/16/03 01/20/03|995|Pmt.Disc.Tol.|No, 15 on the Pmt.|20/-20|0|  
|4B|1,000|20|5|01/15/03|01/20/03|01/16/03 01/20/03|1005|Pmt.Tol.|Yes|0|-5|  
|**5B**|**1,000**|**20**|**5**|**01/15/03**|**01/20/03**|**01/16/03 01/20/03**|**1000**|**None**|**Yes**|**0**|**0**|  
|6B|1,000|20|5|01/15/03|01/20/03|01/16/03 01/20/03|995|Pmt.Tol.|Yes|0|5|  
|7|1,000|20|5|01/15/03|01/20/03|01/16/03 01/20/03|985|Pmt.Disc.Tol. & Pmt.Tol.|Yes|20/-20|-5|  
|8|1,000|20|5|01/15/03|01/20/03|01/16/03 01/20/03|980|Pmt.Disc.Tol.|Yes|20/-20|0|  
|9|1,000|20|5|01/15/03|01/20/03|01/16/03 01/20/03|975|Pmt.Disc.Tol. & Pmt.Tol.|Yes|20/-20|5|  
|10|1,000|20|5|01/15/03|01/20/03|>01/20/03|1005|Pmt.Tol.|Yes|0|-5|  
|**11**|**1,000**|**20**|**5**|**01/15/03**|**01/20/03**|**>01/20/03**|**1000**|**None**|**Yes**|**0**|**0**|  
|12|1,000|20|5|01/15/03|01/20/03|>01/20/03|995|Pmt.Tol.|Yes|0|5|  
|13|1,000|20|5|01/15/03|01/20/03|>01/20/03|985|None|No, 15 on the invoice|0|0|  
|14|1,000|20|5|01/15/03|01/20/03|>01/20/03|980|None|No, 20 on the invoice|0|0|  
|15|1,000|20|5|01/15/03|01/20/03|>01/20/03|975|None|No, 25 on the invoice|0|0|  

### Payment Range Diagrams  
In relation to the scenario above, the diagrams of payment ranges are as follows:  

#### (1) Payment Date <=01/15/03 (Scenarios 1-3)  
Remaining Amount per  

Normal Application Rules  

![Single payment tolerance rules &#40;before 03&#47;15&#41;](media/singlePmtTolRules(Pre1503).gif "singlePmtTolRules(Pre1503)")  

(1) If payment falls in these ranges, all application entries can be closed with or without tolerance.  

(2) If payment falls in these ranges, all application entries cannot be closed even with tolerance.  

#### (2) Payment Date is between 01/16/03 and 01/20/03 (Scenarios 4-9)  
Remaining Amount per  

Normal Application Rules  

![Single payment tolerance rules &#40;grace period&#41;](media/singlePmtTolRules(GracePeriod).gif "singlePmtTolRules(GracePeriod)")  

(1) If payment falls in these ranges, all application entries can be closed with or without tolerance.  

(2) If payment falls in these ranges, all application entries cannot be closed even with tolerance.  

#### (3) Payment Date is after 01/20/03 (Scenarios 10-15)  
Remaining Amount per  

Normal Application Rules  

![Single payment tolerance rules &#40;before 01&#47;20&#41;](media/singlePmtTolRules(Post0120).gif "singlePmtTolRules(Post0120)")  

(1) If payment falls in these ranges, all application entries can be closed with or without tolerance.  

(2) If payment falls in these ranges, all application entries cannot be closed even with tolerance.  

## Example 2 - Tolerance Calculations for Multiple Documents
The following are some example scenarios showing the expected tolerance calculations and postings occurring in different situations. The examples are limited to being only those scenarios that result in all entries in the application being closed.  

The **G/L Setup** window contains the following setup:
- Payment Discount Grace Period 5D  
- Max Payment Tolerance 5  

Scenarios with alternative A, B, C, or D represent the following:  

- **A** In this case the payment discount tolerance warning has been turned off, OR the user has the warning on and has selected to allow the late payment discount (Post as Tolerance) in any invoice.  
- **B** In this case, the user has the warning on and has selected not to allow the late payment discount on any invoice.  
- **C** - In this case, the user has the warning on and has selected to allow the late payment discount on the first invoice but not the second.  
- **D** - In this case, the user has the warning on and has selected not to allow the late payment discount on the first invoice but allowed it on the second.  

|—|Inv.|Pmt Disc.|Max Pmt. Tol.|Pmt. Disc. Date|Pmt. Disc. Tol. Date|Payment Date|Pmt|Tolerance Type|All Entries closed|Pmt. Disc. Tol. <br /> GL/CL|Pmt. Tol.<br /><br /> G/L|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|<=01/15/03|1920|Pmt.Tol.|Yes|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**<=01/15/03**|**1910**|**None**|**Yes**|**0**<br /><br /> **0**|0 <br />0|  
|3|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|<=01/15/03|1900|Pmt.Tol.|Yes|0<br /><br /> 0|5 <br />5|  
|4B|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/16/03 01/17/03|1980|Pmt.Tol.|Yes|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/16/03 01/17/03**|**1970**|**None**|**Yes**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/16/03 01/17/03|1960|Pmt.Tol.|Yes|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/16/03 01/17/03|1920|Pmt.Disc.Tol. & Pmt.Tol.|Yes|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/16/03 01/17/03|1910|Pmt.Disc.Tol.|Yes|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/16/03 01/17/03|1900|Pmt.Disc.Tol. & Pmt.Tol.|Yes|60/60|5 <br />5|  
|10B|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|2010|Pmt.Tol.|Yes|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/18/03 01/20/03**|**2000**|**None**|**Yes**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1990|Pmt.Tol.|Yes|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1980|Pmt.Disc.Tol. & Pmt.Tol.|Yes|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1970|Pmt.Disc.Tol.|Yes|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1960|Pmt.Disc.Tol. & Pmt.Tol.|Yes|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1950|Pmt.Disc.Tol. & Pmt.Tol.|Yes|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1940|Pmt.Disc.Tol.|Yes|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1930|Pmt.Disc.Tol. & Pmt.Tol.|Yes|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1920|Pmt.Disc.Tol. & Pmt.Tol.|Yes|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1910|Pmt.Disc.Tol.|Yes|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/18/03 01/20/03|1900|Pmt.Disc.Tol. & Pmt.Tol.|Yes|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/21/03 01/22/03|2010|Pmt.Tol.|Yes|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/21/03 01/22/03**|**2000**|**None**|**Yes**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/21/03 01/22/03|1990|Pmt.Tol.|Yes|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/21/03 01/22/03|1980|Pmt.Disc.Tol. & Pmt.Tol.|Yes|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/21/03 01/22/03|1970|Pmt.Disc.Tol.|Yes|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|01/21/03 01/22/03|1960|Pmt.Disc.Tol. & Pmt.Tol.|Yes|0/0<br /><br /> 30/30|5 <br />5|  
|28|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|>01/22/03|2010|Pmt.Tol.|Yes|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**>01/22/03**|**2000**|**None**|**Yes**|**0**|**0**|  
|30|1,000 <br />1,000|60 <br />30|5 <br />5|01/15/03 <br />01/17/03|01/20/03 <br />01/22/03|>01/22/03|1990|Pmt.Tol.|Yes|0|5|  

### Payment Range Diagrams  
In relation to the scenario above, the diagrams of payment ranges are as follows:  

#### (1) Payment Date <=01/15/03 (Scenarios 1-3)  
Remaining Amount per  

Normal Application Rules  

![Multiple payment tolerance rules &#40;before 03&#47;15&#41;](media/multiplePmtTolRules(Pre1503).gif "multiplePmtTolRules(Pre1503)")  

(1) If payment falls in these ranges, all application entries can be closed with or without tolerance.  

(2) If payment falls in these ranges, all application entries cannot be closed even with tolerance.  

#### (2) Payment Date is between 01/16/03 and 01/17/03 (Scenarios 4-9)  
Remaining Amount per  

Normal Application Rules  

![Multiple payment tolerance rules &#40;grace period&#41;](media/multiplePmtTolRules(GracePeriodInv1).gif "multiplePmtTolRules(GracePeriodInv1)")  

(1) If payment falls in these ranges, all application entries can be closed with or without tolerance.  

(2) If payment falls in these ranges, all application entries cannot be closed even with tolerance.  

#### (3) Payment Date is between 01/18/03 and 01/20/03 (Scenarios 10-21)  
Remaining Amount per  

Normal Application Rules  

![Multiple payment tolerance rules &#40;grace period&#41;](media/multiplePmtTolRules(GracePeriodInv1-2).gif "multiplePmtTolRules(GracePeriodInv1-2)")  

(1) If payment falls in these ranges, all application entries can be closed with or without tolerance.  

(2) If payment falls in these ranges, all application entries cannot be closed even with tolerance.  

#### (4) Payment Date is between 01/21/03 and 01/22/03 (Scenarios 22-27)  
Remaining Amount per  

Normal Application Rules  

![Multiple payment tolerance rules &#40;grace period&#41;](media/multiplePmtTolRules(GracePeriodInv2).gif "multiplePmtTolRules(GracePeriodInv2)")  

(1) If payment falls in these ranges, all application entries can be closed with or without tolerance.  

(2) If payment falls in these ranges, all application entries cannot be closed even with tolerance.  

#### (5) Payment Date is after 01/22/03 (Scenarios 28-30)  
Remaining Amount per  

Normal Application Rules  

![Multiple payment tolerance rules &#40;after 01&#47;22&#41;](media/multiplePmtTolRules(Post0122).gif "multiplePmtTolRules(Post0122)")  

(1) If payment falls in these ranges, all application entries can be closed with or without tolerance.  

(2) If payment falls in these ranges, all application entries cannot be closed even with tolerance.

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Finance](finance.md)  
[Setting Up Finance](finance-setup-finance.md)  
[Managing Receivables](receivables-manage-receivables.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
