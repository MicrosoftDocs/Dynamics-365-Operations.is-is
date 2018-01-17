---
title: "Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations"
description: "Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla hausa og línur sölureiknings úr Sales við Finance and Operations

- **Heiti sniðmátsins í Gagnaflutningi** 

     - Sölureikningar (Fin og Ops til Sales)

- **Heiti verksins í gagnasamþættingarverki**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Samstillingarverk sem er nauðsynlegt fyrir samstillingu hausa sölureiknings og lína:
-   Vörur (Fin og Ops til Sales )
-   Reikningar (Sales við Fin and Ops) (ef notað)
-   Tengiliðir (Sales við Fin and Ops) (ef notað)
-   Sölupöntunarhaus og -línur (Fin og Ops við Sales)

## <a name="entity-set"></a>Einingastamstæða

| Finance and Operations                               | Common Data Service (CDS)              | Sölur          |
|------------------------------------------------------|------------------|----------------|
| Sölureikningshausar viðskiptavinar sem unnið er með utan frá | SalesInvoice     | Reikningar       |
| Sölureikningslínur viðskiptavinar sem unnið er með utan frá   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Einingaflæði

Sölureikningar eru búnir til í Finance and Operations og samstilltir við Sales.

> [!NOTE]
> Skattur tengdur gjöldum á **Sölureikningshaus** er ekki tekinn með í samstillingu úr Finance and Operations í Sales. Þetta er vegna þess að Sales styður ekki skattupplýsingar á hausstiginu. Skattur sem tengist gjöldum á línustigi er innifalinn.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

-  **Reikningsnúmerareitur** er bætt við eininguna **Reikningur** og birtur á síðunni.
 
-  Hnappurinn **Stofna reikning** á **Sölupöntun** síðunni er falinn vegna þess að reikningar verða búnir til í Finance and Operations og samstilltir við Sales. Ekki er hægt að breyta siðunni **Reikningur** vegna þess að reikningar verða samstilltir úr Finance and Operations.
 
-  **Staða sölupöntunar** breytist sjálfkrafa í **Reikningsfært** þegar tengdur reikningur úr Finance and Operations hefur verið samstilltur við Sales. Einnig var eiganda sölupöntunar sem reikningurinn var búinn til úr úthlutað sem eiganda reikningsins. Þetta gefur eiganda sölurekningsins færi á á skoða reikninginn.
 
## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Fyrir samstillingu sölureikninga er mikilvægt að uppfæra kerfin með eftirfarandi stillingum:

### <a name="setup-in-sales"></a>Uppsetning í Sales

- Undir **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales**, skal tryggja að **Nota reikningskerfi verðs** er stillt á **Já**. 

- Farðu í **Stillingar**  >  **Stjórnun**  >  **Kerfisstillingar**  >  **Sales** og gakktu úr skugga um að reiturinn **Útreikningsaðferð afsláttar** sé stilltur á **Línatriði**. 

### <a name="setup-in-the-data-integration-project"></a>Setja upp gagnasamþættingarverk

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader task

- Uppfæra vörpun fyrir **CDS Organization ID** í **Uppruni** > **CDS**. 

    -  Sjálfgefið sniðmátsgildi fyrir **SalesOrder_Organization_OrganizationId** er ORG001.
    -  Sjálfgefið sniðmátsgildi fyrir **Account_Organization_OrganizationId** er ORG001.
    -  Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er ORG001.

- Gakktu úr skugga um að nauðsynleg kortlagning sé fyrir hendi í **Uppruni** > **CDS fyrir InvoiceCountryRegionId** í **BillingAddress_Country**.

    -  Sniðmátsgildi er **ValueMap** með vörpun á fjölda landa.

- **Verðskrá** er nauðsynleg til að búa til reikninga í Sales. Uppfærið **ValueMap** í **CDS** > **Áfangastaður fyrir pricelevelid.name [Price List Name]** í **Verðlisti** notaður í Sales eftir gjaldmiðli. Þú getur annað hvort notað sjálfgefinn **verðlista** fyrir einn gjaldmiðil eða **ValueMap** ef **Verðlisti** er í mörgum gjaldmiðlum.

    -  Sniðmátsgildi fyrir **pricelevelid.name [Price List Name]** er **ValueMap** byggt á **Gjaldmiðill**.
    -  usd: CRM Service USA (dæmi). 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine verkefni

- Gakktu úr skugga um að nauðsynleg vörpun sé til staðar í **Uppruni** > **CDS fyrir mælieiningu**.

- Gakktu úr skugga um að nauðsynlegt **ValueMap** fyrir **SalesUnitSymbol** í Finance and Operations sé til staðar í **Uppruni** > **CDS vörpun**. 
    
    - Sniðmátsgildi með **ValueMap** er skilgreint **SalesUnitSymbol í Quantity_UOM**.
    
-  Uppfæra vörpun fyrir **CDS Organization ID í uppruna** > **CDS**. 

    -  Sjálfgefið sniðmátsgildi fyrir **SalesInvoicer_Organization_OrganizationId** er ORG001.
    -  Sjálfgefið sniðmátsgildi fyrir **Product_Organization_OrganizationId** er ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Sniðmátsvörpun í Gagnasamþáttara

> [!NOTE]
> **Greiðsluskilmálar**, **Farmskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefinni vörpun. Vörpun þessara reita krefst þess að gildisvörpun sé sett upp, sem gildir sérstaklega fyrir gögnin í fyrirtækinu sem verið er að samstilla eininguna fyrir.

Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Tengd efnisatriði

[Samstilla afurðir úr Finance and Operations í afurðir í Sales](products-template-mapping.md)

[Samstilla lykla úr Sales við viðskiptavini í Finance and Operations](accounts-template-mapping.md)

[Samstilla tengiliði úr Sales við tengiliði eða viðskiptavini í Finance and Operations](contacts-template-mapping.md)

[Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations](sales-quotation-template-mapping.md)

[Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations](sales-order-template-mapping.md)


