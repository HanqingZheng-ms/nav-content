---
    title: Inventory Setup
    description: As part of inventory management, you can set up inventory to assign item charges on purchases from foreign countries/regions based on weight or volume, and to use the same column for original and corrective postings.

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
# Inventory Setup
As part of inventory management, you can set up inventory to:  

- Assign item charges on purchases from foreign countries/regions based on weight or volume.  
- Use the same column for original and corrective postings.  

## Item Charge Assignment in Purchase Documents  
In Russia, [!INCLUDE[navnow](../../includes/navnow_md.md)] can assign item charges on purchases from foreign countries/regions based on weight or volume. For each item, in the **Item Card** window, on the **Foreign Trade** FastTab, if the **Gross Weight Mandatory** and **Unit Volume Mandatory** check boxes are selected, you must fill in the **Gross Weight** and **Unit Volume** fields. When you suggest an item charge assignment on a purchase order, you must specify that the distribution principle, weight, and volume are added to the options to choose from. For more information, see [How to: Use Item Charges to Account for Additional Trade Costs](../../payables-how-assign-item-charges.md).

## Item Corrections  
You can set up inventory to use the same column for original and corrective postings. This is often referred to as *red storno*.  

You can use red storno posting to post corrections for the following inventory entries:  

- Corrective entries in the item journal.  
- Reversal of item documents such as item receipts and item shipments.  
- Posting item revaluation or item reclassification journals.  
- Periodic adjustments of item costs.  

For more information, see [How to: Post Red Storno Corrections](how-to-post-red-storno-corrections.md).  

### Adjusting Item Cost  
If you select the Enable Red Storno field in the **Inventory Setup** window, then negative deviations are posted according to red storno when you run the **Adjust Cost - Item Entries** batch job.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[Item Documents](item-documents.md)   
 [Item Obligatory Acts](item-obligatory-acts.md)   
 [How to: Post Red Storno Corrections](how-to-post-red-storno-corrections.md)   
 [How to: Use Item Charges to Account for Additional Trade Costs](../../payables-how-assign-item-charges.md)
