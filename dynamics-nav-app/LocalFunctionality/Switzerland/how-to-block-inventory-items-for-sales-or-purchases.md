---
    title: How to Block Inventory Items for Sales or Purchases
    description: In [!INCLUDE[navnow](../../includes/navnow_md.md)], an item can be marked as blocked for sales, blocked for purchase, or blocked for all purposes.

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
# How to: Block Inventory Items for Sales or Purchases
In [!INCLUDE[navnow](../../includes/navnow_md.md)], an item can be marked as blocked for sales, blocked for purchase, or blocked for all purposes.  

The following table illustrates what occurs when items are blocked.  

|Item marked as|Result|  
|--------------------|------------|  
|**Sale blocked**|You cannot use the item in a sales document or in a sales item journal.|  
|**Purchase blocked**|You cannot use the item in a purchase document, in a purchase item journal, or in purchase planning processes.|  
|**Blocked**|You cannot use the item for any item transaction. For more information about blocking an item for all purposes, see Item Card.|  

## To block inventory items for sales  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.  
2.  Select the item that you want to block, and then choose the **Edit** action.  
3.  To block the selected item for sales transactions, on the **Invoicing** FastTab, select the **Sale blocked** check box.  
4.  Choose the **OK** button.  

## To block inventory items for purchase  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.  
2.  Select the item that you want to block, and then choose the **Edit** action.  
3.  To block an item for purchase transactions, on the **Replenishment** FastTab, select the **Purchase blocked** check box.  
4.  Choose the **OK** button.  

You will receive an error message if you try to do the following:  

- Enter sales lines and purchase lines in sales documents and purchase documents for blocked items. For more information, see the Sales Line table and the Purchase Line table.  
- Create new lines in an item journal for blocked items. For more information, see the Item Journal window.  
- Post item transactions for blocked items.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Swiss Inventory Management](swiss-inventory-management.md)   
 [How to: Block Shipment for Negative Inventory](how-to-block-shipment-for-negative-inventory.md)   
 [How to: Copy Existing Items to New Items](how-to-copy-existing-items-to-new-items.md)   
 [How to: Deactivate Item Cost Tracking](how-to-deactivate-item-cost-tracking.md)
