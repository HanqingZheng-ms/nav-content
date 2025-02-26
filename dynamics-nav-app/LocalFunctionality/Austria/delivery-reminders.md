---
    title: Delivery Reminders in Austria
    description: In Austria, delivery reminders are used to track overdue vendor shipments, and to remind vendors about overdue deliveries. 

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
# Delivery Reminders in Austria
Delivery reminders are used to track overdue vendor shipments, and to remind vendors about overdue deliveries. To create delivery reminders, you must set up the following:  

- Delivery reminder terms  

    Delivery reminder terms are identified by a code that must be assigned to vendors. To use more than one combination of settings, you must set up a code for each setting separately. You can set up any number of delivery reminder terms.  

- Delivery reminder levels  

    For every delivery reminder term, you must set up delivery reminder levels. These levels determine how often delivery reminders can be created for a specific term. Level 1 is the first delivery reminder that you create for an overdue delivery. Level 2 is the second delivery reminder, and so on. When delivery reminders are created, the number of reminders that were created previously is considered, and the current number is used to apply terms.  

- Delivery reminder texts messages  

    You must set up delivery reminder text messages for every delivery reminder level. There are two types of delivery reminder text messages: beginning and ending. The beginning text message is printed under the header section, before the list of entries that are marked for reminder. The ending text message is printed after this list.  

For more information, see [How to: Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md).  

After you have set up the delivery terms, you must assign the delivery reminder term codes to vendors. For more information, see [How to: Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md).  

You can create delivery reminders manually or automatically. You can use the **Create Delivery Reminder** batch job to create delivery reminders automatically. This batch job allows you to select the purchase orders for which delivery reminders must be created. For more information, see [How to: Generate Delivery Reminders](how-to-issue-delivery-reminders.md).  

You can also track documents in relation to purchase order lines and sales order lines.  

[!INCLUDE[navnow](../../includes/navnow_md.md)] provides the following reports:  

- **Issued Delivery Reminder** - To view the delivery reminders for vendors.  
- **Delivery Reminder - Test** - To verify the delivery reminders before you issue them.  

For more information, see [How to: Print Test Reports for Delivery Reminders](how-to-print-test-reports-for-delivery-reminders.md).  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[How to: Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md)   
 [How to: Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [How to: Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [How to: Generate Delivery Reminders](how-to-generate-delivery-reminders.md)   
 [How to: Create Delivery Reminders Manually](how-to-create-delivery-reminders-manually.md)   
 [How to: Issue Delivery Reminders](how-to-issue-delivery-reminders.md)   
 [How to: Print Test Reports for Delivery Reminders](how-to-print-test-reports-for-delivery-reminders.md)
