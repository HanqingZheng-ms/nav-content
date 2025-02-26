---
    title: Send Electronic Documents 
    description: learn how to send invoices electronically.
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 08/21/2017
    ms.author: edupont

---
# How to: Send Electronic Documents
The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers. A document exchange service provider dispatches electronic documents between trading partners. To provide support for other electronic document formats, you use the data exchange framework.  

 In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company. For more information, see [How to: Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).  

 To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile. First, you must set up various master data, such as company information, customers, items, and units of measure. These are used to identify the business partners and items when converting data in fields in [How to: Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### To send an electronic sales invoice  

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.  

2.  Create a new sales invoice.  

3.  When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.  

     If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.  

4.  In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.  

5.  In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.  

6.  In the **Format** field, choose **PEPPOL**.  

7.  Choose the **OK** button. The **Post and Send Confirmation** dialog box appears. **Electronic Document (PEPPOL)** is added to the **Send Document to** field.  

8.  Choose the **Yes** button.  

     The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.  

    > [!NOTE]  
    >  You can also send a posted sales invoice as an electronic document. The procedure is the same as described in this topic for non-posted sales documents. In the **Posted Sales Invoice** window, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document. For more information, see **Activity Log**.  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[How to: Invoice Sales](sales-how-invoice-sales.md)  
[How to: Set Up Document Sending Profiles](sales-how-setup-document-send-profiles.md)  
[How to: Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[How to: Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md)  
[How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md)  
[Exchanging Data Electronically](across-data-exchange.md)  
[General Business Functionality](ui-across-business-areas.md)  
