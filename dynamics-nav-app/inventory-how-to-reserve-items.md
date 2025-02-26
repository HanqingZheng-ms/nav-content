---
    title: How to Reserve Items 
    description: You can reserve items for sales orders, purchase orders, and production orders. You can reserve items on inventory or inbound on open document lines.
    
    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 08/14/2017
    ms.author: edupont

---
# How to: Reserve Items
You can reserve items for sales orders, purchase orders, service orders, assembly orders, and production orders. You can reserve items on inventory or inbound on open document or journal lines. You perform the work in the **Reservation** window.

Each line in the **Reservation** window, which you open to reserve items, displays information about one type of line (sales, purchase, journal) or inventory entry. The lines describe how many items are available to be reserved from each type of line or entry.

## To reserve items for sales
The following describes how to reserve items from a sales order. The steps are similar for purchase, service, and assembly orders.  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.  
2.  On a sales order, on the **Lines** FastTab, choose the **Reserve** action. The **Reservation** window opens.  
3. Select the line that you want to reserve the items from.  
4. Choose one of the following actions.  

    |**Function**|**Description**|
    |------------------|---------------------|  
    |**Auto Reserve**|To automatically reserve items in the **Reservation** window.|  
    |**Reserve from Current Line**|To reserve the items from the document on the line you have selected.|  
    |**Cancel Reservation from Current Line**|To cancel reservation of the items from the document on the line you have selected.|

> [!NOTE]  
>  If item tracking lines exist for the sales order, the reservation system will take you through special steps. For more information, see the "To reserve a specific serial or lot number" section.  

## To reserve an item for a production order line  
You can reserve items for production orders. You have to distinguish between production order lines, meaning the parent item, and production order components.

In the following procedure, a firm planned production order is used.   
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.  
2. Open the firm planned production order you want to reserve parent items for.  
3. Select the relevant production order line.  
4. On the **Lines** FastTab, choose the **Reserve** action.
5. In the **Reservation** window, select the **Sales Line, Order** line, and then choose the **Reserve from Current Line** action.  

The quantity you entered in the firm planned production order line is now reserved.

## To reserve items for production order components  
You can reserve items for production orders. You have to distinguish between production order lines, meaning the parent item, and production order components.

In the following procedure, a firm planned production order is used.    
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.  
2. Open the firm planned production order you want to reserve component items for.  
3. Select the relevant production order line.  
4. On the **Lines** FastTab, choose **Line**, and then choose **Components**.  
5. Select the relevant component line.  
6. Choose On the **Lines** FastTab, choose the **Reserve** action.  
7. In the **Reservation** window, select a line, and then choose the **Reserve from Current Line** action.  

The quantity you entered in the firm planned production component line is now reserved.

## To change a reservation  
Sometimes, you may want to change an item reservation.   
1. From the document line that you have reserved from, on the **Lines** FastTab, choose the **Reserve** action.  
2. In the **Reservation** window, choose the **Reservation Entries** action.
3. The **Reservation Entries** window, update the **Quantity** field on the line you want to change.
4. Confirm the subsequent message, by choosing the **OK** button.

## To cancel a reservation  
Sometimes, you may want to cancel an item reservation.   
1. From the document line that you want to cancel a reservation from, on the **Lines** FastTab, choose the **Reserve** action.  
2. In the **Reservation** window, choose **Reservation Entries** action.  
3.  In the **Reservation Entries** window, choose the **Cancel Reservation** action.  
4.  Confirm the subsequent message, by choosing the **OK** button.  

## To reserve a specific serial or lot number  
From outbound documents for item-tracked items, such as sales orders or production component lists, you can reserve specific serial or lot numbers. This may be relevant, for example, if you need production components from a specific lot to ensure consistency with earlier production batches, or because a customer has requested a specific serial number. For more information, see [How to: Work with Serial and Lot Numbers](inventory-how-work-item-tracking.md).

This is referred to as a specific reservation, because you reserve from the quantity of  Item X that belongs to Lot X. If you simply reserve from quantities of Item X, then it is a normal, non-specific, reservation. For more information, see [Design Details - Item Tracking and Reservations](design-details-item-tracking-and-reservations.md).

The following procedure is based on a sales order.    
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.  
2. Create a sales order line for an item-tracked item.  
3. Assign serial and lot numbers to the sales order line. For more information, see [How to: Work with Serial and Lot Numbers](inventory-how-work-item-tracking.md).
4. On the sales order line, choose the **Reserve** action.  
5. Choose the **Yes** button to reserve specific serial or lot numbers.  
6. In the   **Item Tracking List** window, select the serial and lot number combination that you have just assigned.  
7. Choose the **OK** button to open the **Reservation** window showing only supply with the specified item tracking number. If there are any non-specific reservations on any of the item tracking numbers that you have specified for this line, you are informed of the quantity that has already been reserved.  
8. Choose either the **Auto Reserve** or the **Reserve from Current Line** action to create the reservation on the specific item tracking numbers.

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Inventory](inventory-manage-inventory.md)  
[Design Details: Reservation, Order Tracking, and Action Messaging](design-details-reservation-order-tracking-and-action-messaging.md)  
[Design Details - Item Tracking and Reservations](design-details-item-tracking-and-reservations.md)  
[How to: Work with Serial and Lot Numbers](inventory-how-work-item-tracking.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
