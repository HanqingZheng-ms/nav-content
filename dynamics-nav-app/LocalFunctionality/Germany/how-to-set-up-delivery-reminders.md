---
    title: How to Set Up Delivery Reminders (Germany)
    description: In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.

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
# How to: Set Up Delivery Reminders (Germany)
In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries. To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders in the **Purchases & Payables Setup** window.  

## To set up delivery reminders  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.  
2.  On the **General** FastTab, in the **Default Del. Rem. Date Field** field, specify one of the following options as described in the following table.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Requested Receipt Date**|To specify that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.|  
    |**Promised Receipt Date**|To specify that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.|  
    |**Expected Receipt Date**|To specify that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.|  

3.  On the **Numbering** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Delivery Reminder Nos.**|The number series code for delivery reminders.|  
    |**Issued Delivery Reminder Nos.**|The number series code for issued delivery reminders.|  

4.  Choose the **OK** button.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Delivery Reminders](delivery-reminders.md)   
 [How to: Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [How to: Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [How to: Create Delivery Reminders Manually](how-to-create-delivery-reminders-manually.md)
