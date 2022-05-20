---
    title: Digipoort Overview
    description: In the Netherlands, you use Digipoort (government electronic post office) to make periodic electronic filings for VAT declarations and ICP reports in EU sales list submissions.

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
# Digipoort Overview
In the Netherlands, you use Digipoort to make periodic electronic filings for VAT declarations and ICP reports in EU sales list submissions. Digipoort is the electronic post office provided by the Dutch government for companies. It provides the common infrastructure for the communication of information between companies and the government, including VAT declarations. The reports are in XBRL format.  

[!INCLUDE[navnow](../../includes/navnow_md.md)] installer installs the .dll to the following location: c:Program Files (x86)Microsoft Dynamics NAV&lt;<version&gt;>RoleTailored ClientAdd-insMicrosoft.Dynamics.NL.Digipoortservice.dll.  

The Digipoort channel replaces the BAPI method for making submissions.  

## Certificate Storage  
In order to communicate electronically using Digipoort with the Dutch government, you will need two certificates (PKIoverheid). You will need a private certificate for the company as well as a public certificate from the website of the Dutch tax authorities. need a private certificate for the company as well as a public certificate from the Dutch authorities. You can get more specific information from the website of the Dutch tax authority. For more information, see the Dutch Tax Administration website[Logius](https://aansluiten.procesinfrastructuur.nl/site/en/).  

You will have to import the certificates that you receive into the Windows Certificate store. This is a change from prior releases, in which you stored your certificates in [!INCLUDE[navnow](../../includes/navnow_md.md)].  

## See Also
[Dynamics 365 Business Central](/dynamics365/business-central/)  
[How to: Set Up Certificates for use with Digipoort](how-to-set-up-certificates-for-use-with-digipoort.md)
