---
    title: Swiss Electronic Payments
    description: Swiss enhancements allow you to send invoices to customers electronically. The invoices are presented and paid directly using the customer's online banking software.

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
# Swiss Electronic Payments
[!INCLUDE[navnow](../../includes/navnow_md.md)] allows you to send invoices to customers electronically. The invoices are presented and paid directly using the customer's online banking software.  

## Electronic Payment Methods  
You can make electronic payments using the following methods:  

- DatenTrägerAustausch (DTA)  
- Elektronischer Zahlungsauftrag (EZAG)  
- Einzahlungsschein mit Referenznummer (ESR)  
- Lastschrift Verfahren (LSV+)  
- SEPA credit transfers  

## DTA and EZAG  
The DTA electronic payment method is a universal service adopted by Swiss banks to settle payments electronically in DTA format using standardized payment records. This method is based on data carriers and data transfer. The specifications are coordinated by Swiss Interbank Clearing (SIC). For more information, see [Swiss Electronic Payments Using DTA](swiss-electronic-payments-using-dta.md).  

EZAG is the electronic payment method of Swiss PostFinance, and requires a giro account. You can create and send orders for vendor payments in DTA bank format or PostFinance EZAG format.  

## ESR  
ESR is an electronic debtor service that uses payment slips to collect money. It is the standard electronic payment system created by Swiss Post. You can print ESR payment slips as invoice attachments, calculate ESR reference numbers, and import ESR files that have payment information from banks. For more information, see [Swiss Electronic Payments Using ESR](how-to-print-esr-invoices.md). You can also make ESR and ESR+ payments using the bank’s version of this payment method, which is named Bank-ESR (BESR).  

## LSV+  
LSV+ is a direct debit service that is used for processing payments. Companies can release customer payments directly from the customer's bank using direct debit. You can request and collect customer payments using direct debit in the LSV+ bank format, or in the DebitDirect PostFinance format. For more information, see [Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md).  

## SEPA Credit Transfers  
To export payments according to the SEPA standard, you must use a bank account. To make sure that the related general ledger entries are consistent with those generated for local Swiss payment methods (see above), the value in the **Bank Acc. Posting Group** field in the **Bank Account Card** window must point to the relevant general ledger account. For more information about how to export SEPA payments, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](../../finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[How to: Import Swiss Bank Clearing Numbers](how-to-import-swiss-bank-clearing-numbers.md)   
 [Swiss Electronic Payments Using DTA](swiss-electronic-payments-using-dta.md)   
 [Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md)   
 [How to: Print ESR Invoices](how-to-print-esr-invoices.md)   
 [Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md)   
 [Switzerland Local Functionality](switzerland-local-functionality.md)  '
 [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](../../finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
 [Making Payments](../../payables-make-payments.md)
