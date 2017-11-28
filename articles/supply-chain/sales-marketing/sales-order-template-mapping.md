---
title: "Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations"
description: "Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales. 

## <a name="template-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations:

- **Heiti sniðmáts í Gagnaflutningi** 

    - Sölupantanir (Sales við Fin and Ops)
    
- **Heiti verksins í gagnaflutningsverki**

    - OrderHeader
    - OrderLine

Samstillingarverk er nauðsynlegt fyrir samstillingu hausa sölureiknings og lína:

- Vörur (Fin og Ops til Sales )
- Reikningar (Sales við Fin and Ops) (ef notað)
- Tengiliðir við viðskiptavini (Sales við Fin and Ops) (ef notað)

## <a name="entity-set"></a>Einingastamstæða

| Finance and Operations |    Common Data Service (CDS)         |     Sölur      |
|------------------------|----------------|----------------|
| Hausar CDS-sölupöntunar| SalesOrder     | SalesOrders |
| CDS sölupöntunarlínur  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Einingaflæði

Sölupantanir eru búnar til í Finance and Operations og samstilltar við Sales.

Síur í sniðmáti tryggja að aðeins viðeigandi sölupantanir séu innifaldar í samstillingu:

- Bæði pöntun og innheimta viðskiptavinar á sölupöntun sem á uppruna sinn í Sales verða teknar með í samstillingu. Í Finance and Operations er reitirnir **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** notaðir til að rekja samstillingu í gagnaeiningum.

- **Sölupöntun** í Finance and Operations verður að staðfesta. Aðeins staðfestar sölupantanir eða sölupantanir með hærri vinnslustöðu, til dæmis, Sent eða Reikningsfært, eru samstilltar við Sales.

- Eftir að sölupöntun er búin til eða henni breytt verður að keyra runuvinnsluna **Reikna heildarsölu** í Finance and Operations. Aðeins sölupantanir með reiknaðar samtölur verða samstilltar við CDS og Sales.

> [!NOTE]
> Skattur tengdur gjöldum á **Sölupöntunarhaus** er ekki tekinn með í samstillingu úr Finance and Operations í Sales. Þetta er vegna þess að Sales styður ekki skattupplýsingar á hausstiginu. Skattur sem tengist gjöldum á línustigi er innifalinn.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Nýjum reitum er bætt við eininguna **Pöntun** og birtir á síðunni:

- **Er viðhaldið utanfrá** - Stillt á **Já** þegar pöntunin er úr Finance and Operations.

- **Vinnslustaða** - Notuð til að sýna vinnslustöðu pantanar í Finance and Operations. Gildi eru:

    - Í gangi
    - Staðfest
    - Fylgiseðill
    - Reikningsfært
    - Tekið til
    - Tínt að hluta
    - Tekið til að hluta
    - Sent
    - Afhent að hluta
    - Reikningsfært að hluta
    - Afturkallað

Stillingin **Er aðens með utanaðkomandi vörur** er notuð í öðrum sviðsmyndum sölupantana (úr Sales í Finance and Operation samstillingu) til að halda utan um það hvort sölupöntun sé eingöngu með **Vörur sem viðhaldið er utanfrá**, en í því tilfelli er vörum viðhaldið í Finance and Operations. Þetta tryggir að þú reynir ekki að samstilla sölupöntunarlínur með vörum sem eru óþekktar Finance and Operations.
 
**Stofna reikning**, **Hætta við pöntun**, **Endurreikna**, **Sækja vörur** og **Leita að aðsetri** hnapparnir á síðunni **Sölupöntun** eru ufaldir fyrir pantanir sem er viðhaldið utan frá þar sem reikningar verða stofnaðir í Finance and Operations og samstilltir við Sales. Ekki er hægt að breyta pöntunarsíðunni þar sem upplýsingar um sölupantanir verða samstilltar úr Finance and Operations.
 
**Staða sölupöntunar** verður áfram virk til að tryggja að gjöld úr Finance and Operations geti flætt í **Sölupöntun** í Sales. Þessu er stjórnað með því að stilla sjálfgefið **Statecode [Status]** á **Virkt** í gagnasamþættingarferlinu.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning 

Fyrir samstillingu sölupantana er mikilvægt að uppfæra kerfin með eftirfarandi stillingum:

### <a name="setup-in-sales"></a>Uppsetning í Sales

- Gakktu úr skugga um að heimildir fyrir teymi sem notandinn (úr Sales **Tenging**) er úthlutaður á. Ef þú ert að nota sýnigögn hefur notandinn venjulega aðgang að stjórnendum en ekki teyminu. Án þessa færð þú villu sem um að aðalsteymi vanti þegar þú keyrir verkefnið úr Gagnasamþáttara. 

    - Undir **Stillingar** > **Öryggi** > **Teymi**, velurðu viðkomandi teymi, smellir á **Stjórna hlutverkum** og velur hlutverk með viðkomandi heimildum, t.d. kerfisstjóri.

- Undir **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales**, skal tryggja að **Nota reikningskerfi verðs** er stillt á **Já**. 

- Farðu í **Stillingar**  >  **Stjórnun**  >  **Kerfisstillingar**  >  **Sales** og gakktu úr skugga um að reiturinn **Útreikningsaðferð afsláttar** sé stilltur á **Línatriði**. 

### <a name="setup-in-finance-and-operations"></a>Uppsetning Finance and Operations

Stilltu **Sala og markaðssetning** > **Reglubundin verkefni** > **Reikna út samtölu sölupantana** til að keyra sem runuvinnsla þar sem **Reikna út samtölu sölupantana** er stillt á **Já**. Þetta er mikilvægt vegna þess að aðeins sölupantanir með samtölum verða samstilltar við CDS og Sales. Tíðni runuvinnslunnar ætti að vera í samræmi við tíðni samstillingu sölupöntunar.

### <a name="setup-in-the-data-integration-project"></a>Setja upp gagnasamþættingarverk

#### <a name="salesheader-task"></a>SalesHeader verkefni

- Uppfæra vörpun fyrir **CDS Organization ID í uppruna** > **CDS**.

    - Sjálfgefið sniðmátsgildi fyrir **Account_Organization_OrganizationId** er ORG001.
    - Sjálfgefið sniðmátsgildi fyrir **InvoiceAccount_Organization_OrganizationId** er ORG001.
    - Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er ORG001.

- Gakktu úr skugga um að nauðsynleg vörpun sé til staðar í **Uppruna** > **CDS fyrir InvoiceCountryRegionId í BillingAddress_Country** og fyrir **DeliveryCountryRegionId í DeliveryAddress_Country**.

    - Sniðmátsgildi er **ValueMap** með vörpun á fjölda landa.

- **Verðlisti** er nauðsynlegur til að búa til pantanir í Sales. Uppfæra **ValueMap** in **CDS** > **Áfangastaður** fyrir **pricelevelid.name [Price List Name]** í **Verðlisti** sem er notaður í Sales eftir gjaldmiðli. Þú getur annað hvort notað sjálfgefinn **verðlista** fyrir einn gjaldmiðil eða **ValueMap** ef **Verðlisti** er í mörgum gjaldmiðlum.
    
    - Sjálfgefið sniðmátsgildi fyrir **pricelevelid.name [Price List Name]** er CRM Service USA (dæmi). 

#### <a name="salesline-task"></a>SalesLine verkefni

- Uppfæra vörpun fyrir **CDS Organization ID í uppruna** > **CDS**. 
    
    - Sjálfgefið sniðmátsgildi fyrir **SalesOrder_Organization_OrganizationId** er ORG001.
    - Sjálfgefið sniðmátsgildi fyrir **Product_Organization_OrganizationId** er ORG001.

- Gakktu úr skugga um að nauðsynleg vörpun sé til staðar í **Uppruna** > **CDS** fyrir **DeliveryCountryRegionId** í **DeliveryAddress_Country**.

    - Sniðmátsgildi er **ValueMap** með vörpun á fjölda landa.
    
- Gakktu úr skugga um að nauðsynlegt **ValueMap** fyrir **SalesUnitSymbol** í Finance and Operations sé til staðar í **Uppruni** > **CDS vörpun**.

    - Sniðmátsgildi með **ValueMap** er skilgreint **SalesUnitSymbol í Quantity_UOM**.

## <a name="template-mapping-in-data-integrator"></a>Sniðmátsvörpun í gagnasamþáttara

> [!NOTE]
> Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.

Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.

### <a name="orderheader"></a>OrderHeader

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-order-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-order-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Tengd efnisatriði

[Samstilla afurðir úr Finance and Operations í afurðir í Sales](products-template-mapping.md)

[Samstilla lykla úr Sales við viðskiptavini í Finance and Operations](accounts-template-mapping.md)

[Samstilla tengiliði úr Sales við tengiliði eða viðskiptavini í Finance and Operations](contacts-template-mapping.md)

[Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations](sales-quotation-template-mapping.md)

[Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations](sales-invoice-template-mapping.md)


