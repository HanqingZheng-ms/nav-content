---
    title: Swiss Inventory Management
    description: Swiss enhancements include special inventory management features.

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
# Swiss Inventory Management
[!INCLUDE[navnow](../../includes/navnow_md.md)] includes Swiss enhancements to inventory management. This includes the following:  

- Detailed reporting.  For more information, see the Inventory - Sales Statistics report and the Inventory - List report.  
- The ability to track an invoice with multiple shipments.  
- Including an item card location code as the default location code for sales lines and item journals. For more information, see [How to: Set Up Locations](../../inventory-how-setup-locations.md). 

## Managing Item Details  
Companies can have different warehouses for different product categories. In such cases, you must use the default location code retrieved from the item card. When you define a location code for an item, it is transferred to the sales lines and item journals as a default item location code. For more information, see the Sales Line and the Item Journal Line table.  

You can provide an item description with up to 50 characters, and a tariff number with up to 15 characters. For more information, see the Item Card window.  

Additional information, such as customer number, ship-to address code, and customer sales person code, is stored in item ledger entries. This information helps you to create customized reporting criteria, such as revenue per customer, and item or sales provisions for sales people. For more information, see the Item Ledger Entry table.  

## Invoices with Multiple Shipments  
If multiple shipments have been posted for a customer, then you can create a combined invoice with the **Get Shipment Lines** function. For more information, see the Get Shipment Lines window. When you use this function, the text created on the invoice lines includes information about the shipment number and the shipment date. For example, the text could appear as Shipment No. 102040 of 25.01.01. This allows you to easily track invoices with multiple shipments.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[How to: Block Shipment for Negative Inventory](how-to-block-shipment-for-negative-inventory.md)   
 [How to: Block Inventory Items for Sales or Purchases](how-to-block-inventory-items-for-sales-or-purchases.md)   
 [How to: Copy Existing Items to New Items](how-to-copy-existing-items-to-new-items.md)   
 [How to: Deactivate Item Cost Tracking](how-to-deactivate-item-cost-tracking.md)   
 [Switzerland Local Functionality](switzerland-local-functionality.md)   
 [How to: Set Up Locations](../../inventory-how-setup-locations.md)
