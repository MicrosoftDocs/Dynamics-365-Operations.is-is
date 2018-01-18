---
title: "Samstilla sölutilboðshausa og línur úr Sales í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla sölutilboðshausa og línur úr Microsoft Dynamics 365 for Sales í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Samstilla sölutilboðshausa og línur úr Sales í Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration). 

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla sölutilboðshausa og línur úr Microsoft Dynamics 365 for Sales (Sales) í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations). 

## <a name="template-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla sölutilboðshausa og línur úr Sales í Finance and Operations:

- **Nafn sniðmáts:** Sölutilboð (Sales í Fin and Ops)
- **Heiti verkefnanna í verkinu:**

    - QuoteHeader
    - QuoteLine

Eftirfarandi samstillingarverk eru nauðsynleg áður en samstilling úr sölutilboðshausum og línum getur átt sér stað:

- Vörur (Fin og Ops til Sales )
- Reikningar (Sales við Fin and Ops) (ef notað)
- Tengiliðir við viðskiptavini (Sales við Fin and Ops) (ef notað)

## <a name="entity-set"></a>Einingastamstæða

| Sölur        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Tilvitnanir       | Tilboð     | Sölutilboðshausar   |
| QuoteDetails | QuotationLine | CDS-sölutilboðslínur |

## <a name="entity-flow"></a>Einingaflæði

Sölutilboð eru stofnuð í Sales og samstillt í Finance and Operations.

Sölutilboð úr Sales eru aðeins samstillt ef eftirfarandi skilyrði eru uppfyllt:

- Unnið er með allar afurðir í sölutilboðslínum utan frá.
- Sölutilboðið er virkt eða virkjað.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Reitnum **Hefur aðeins afurðir sem unnið er með utan frá** hefur verið bætt við sölutilboðseininguna til að fylgjast með því hvort sölutilboð samanstendur eingöngu af afurðum sem unnið er með utan frá. Ef sölutilboð inniheldur aðeins afurðir sem unnið er með utan frá, er afurðunum stýrt í Finance and Operations. Þessi hegðun hjálpar til við að tryggja að þú reynir ekki að samstilla sölutilboðslínur við vörur sem eru óþekktar í Finance and Operations.

Allar afurðir og línur í tilboðinu eru uppfærðar með upplýsingunum í **Hefur aðeins afurðir sem unnið er með utan frá** úr tilboðshaus. Þessar upplýsingar má finna í reitnum **Tilboðið hefur aðeins afurðir sem unnið er með utan frá** á tilboðslínueiningu.

Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations. Þessi uppsetning styður ekki samþættingarvörpun eins og er. Í núverandi hönnun er reitunum **Verð**, **Afsláttur**, **Gjöld** og **Skattur** stýrt og meðhöndlaðir af Finance and Operations.

I Sales gerir lausnin það að verkum að eftirfarandi reitir eru ritvarðir, þar sem gildin eru ekki samstillt við Finance and Operations.

- **Ritvarðir reitir í sölutilboðshaus:** Afsláttur % Afsláttur, Fraktupphæð
- **Ritvarðir reitir í sölutilboðslínum:** Skattur

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Fyrir samstillingu sölupantana er mikilvægt að uppfæra kerfin með eftirfarandi stillingum:

### <a name="setup-in-sales"></a>Uppsetning í Sales

- Farðu í **Stillingar** &gt; **Stjórnun** &gt; **Kerfisstillingar** &gt; **Sales** og gakktu úr skugga um að reiturinn **Reikningsaðferð reikningsafsláttar** sé stilltur á **Á einingu**. Þessi stilling hjálpar til við að tryggja að línuafsláttur vöru í Sales sé sá sami og stillingarnar í Finance and Operations. Að öðrum kosti er afslátturinn ekki réttur í Finance and Operations, þar sem Finance and Operations les afsláttinn á hverja einingu þrátt fyrir að hann sé á hverja línu í Sales.

### <a name="setup-in-finance-and-operations"></a>Uppsetning Finance and Operations

- Farðu í **Viðskiptakröfur** &gt; **Uppsetning** &gt; **Færibreytur viðskiptakrafna**. Í flipanum **Númeraröð** skaltu velja númeraröðina fyrir sölutilboðið og smelltu svo á **Skoða upplýsingar**. Því næst, undir **Almenn uppsetning**, stilltu reitinn **Handvirkt** á **Já**.
- Farðu í **Viðskiptakröfur** &gt; **Uppsetning** &gt; **Færibreytur viðskiptakröfu**. Því næst, í flipanum **Sendingar**, stilltu reitinn **Stýring afhendingardagsetninga** á **Ekkert**. Þessi stilling hjálpar til við að koma í veg fyrir að samstilling bregðist fyrir sölutilboð.

### <a name="setup-in-the-data-integration-project"></a>Setja upp gagnasamþættingarverk

#### <a name="quoteheader"></a>QuoteHeader

- Reiturinn **Umbeðin afhendingardagsetning** er nauðsynlegur í Finance and Operations og samstilling gengur ekki eftir ef reiturinn er auður. Til að koma í veg fyrir þetta vandamál, ef reiturinn er auður, er sjálfgefin dagsetning sótt í **Uppruni &gt; CDS**. Dagsetningin skal uppfærð í æskilegt gildi. Sem stendur er ekki hægt að færa inn gildi eins og **Í dag** til að standa fyrir daginn í dag. Það verður að færa inn tiltekna dagsetningu. Gildi sniðmátsgildsins fyrir **Umbeðna afhendingardagsetningu** er **1/1/2020**.
- Reiturinn **Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations. Til að koma í veg fyrir samstillingarvillur, er hægt að tilgreina sjálfgefið gildi sem er notað ef reiturinn er hafður auður í Sales. Þetta sjálfgefna gildi er einnig gagnlegt vegna þess að þú þarft ekki að færa handvirkt inn gildi í reitinn **Landsvæði** fyrir staðbundin aðsetur. Það er ekkert sjálfgefið sniðmátsgildi fyrir **DeliveryAddressCountryRegionISOCode**.
- Uppfærðu vörpunina fyrir **CDS-fyrirtækjaauðkenni** í **Uppruni &gt; CDS** þannig að hún samsvari **CDS-fyrirtæki** í fyrirtækiseiningunni:

    - Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er **ORG001**.
    - Sjálfgefið sniðmátsgildi fyrir **Account_Organization_OrganizationId** er **ORG001**.
    - Sjálfgefið sniðmátsgildi fyrir **InvoiceAccount_OrganizationId** er **ORG001**.

#### <a name="quoteline"></a>QuoteLine

- Uppfærðu vörpunina fyrir **CDS-fyrirtækjaauðkenni** í **Uppruni &gt; CDS** þannig að hún samsvari **CDS-fyrirtæki** í fyrirtækiseiningunni:

    - Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er **ORG001**.
    - Sjálfgefið sniðmátsgildi fyrir **Product_Organization_Organization_OrganizationId** er **ORG001**.
    - Sjálfgefið sniðmátsgildi fyrir **Quotation_Organization_Organization_OrganizationId** er **ORG001**.

- Reiturinn **Umbeðin afhendingardagsetning** er nauðsynlegur í Finance and Operations og samstilling gengur ekki eftir ef reiturinn er auður. Til að koma í veg fyrir þetta vandamál, ef reiturinn er auður, er sjálfgefin dagsetning sótt í **Uppruni &gt; CDS**. Dagsetningin skal uppfærð í æskilegt gildi. Sem stendur er ekki hægt að færa inn gildi eins og **Í dag** til að standa fyrir daginn í dag. Það verður að færa inn tiltekna dagsetningu. Gildi sniðmátsgildsins fyrir **Umbeðna afhendingardagsetningu** er **1/1/2020**.
- Hægt er að bæta við eftirfarandi vörpunum úr **CDS &gt; Viðtökustaður** til að hjálpa til við að tryggja að sölutilboðslínur séu fluttar inn í Finance and Operations ef það eru engar sjálfgefnar upplýsingar, hvorki frá viðskiptavini né afurð:

    - **SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations. Það eru engin sjálfgefin sniðmátsgildi fyrir **SiteId**.
    - **WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations. Það er engin sjálfgefin sniðmátsgildi fyrir **WarehouseId**.

- Gakktu úr skugga um að nauðsynleg gildisvörpun fyrir sölu á mælieiningu (UOM) í Finance and Operations sé til í vörpuninni **CDS &gt; Viðtökustaður** fyrir **Magn_Mælieiningu** í **SALESUNITSYMBOL**.

## <a name="template-mapping-in-data-integrator"></a>Sniðmátsvörpun í gagnasamþáttara

> [!NOTE]
> - Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations. Þessi uppsetning styður ekki samþættingarvörpun eins og er. Í núverandi hönnun eru reitirnir **Verð**, **Afsláttur**, **Gjöld** og **Skattur** meðhöndlaðir af Finance and Operations.
> - Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.

Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.

### <a name="quoteheader"></a>QuoteHeader

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Tengd efnisatriði

[Samstilla afurðir úr Finance and Operations í afurðir í Sales](products-template-mapping.md)

[Samstilla lykla úr Sales við viðskiptavini í Finance and Operations](accounts-template-mapping.md)

[Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations](contacts-template-mapping.md)



