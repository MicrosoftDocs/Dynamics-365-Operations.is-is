---
title: "Samstilla hausa og línur sölutilboðs beint úr Sales við Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur sölutilboðs beint úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 97536c27dea113cc3c019473f22d1925e7617f8f
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Samstilla hausa og línur sölutilboðs beint úr Sales við Finance and Operations

[!include [banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur sölutilboðs beint úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 Data samþættingu](/common-data-service/entity-reference/dynamics-365-integration).

## <a name="template-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla sölutilboðshausa og línur beint úr Sales í Finance and Operations:

- **Heiti sniðmátsins í gagnaflutningi:** Sölutilboð (Sales í Fin and Ops) - beint
- **Heiti verksins í gagnasamþættingarverki:**

    - QuoteHeader
    - QuoteLine

Eftirfarandi samstillingarverk eru nauðsynleg áður en samstilling úr sölutilboðshausum og línum getur átt sér stað:

- Vörur (Fin og Ops til Sales) - bein
- Reikningar (Sales við Fin and Ops) - Beint (ef notað)
- Tengiliðir við viðskiptavini (Sales við Fin og Ops) - Beint (ef notað)

## <a name="entity-set"></a>Einingastamstæða

| Sölur        | Finance and Operations     |
|--------------|----------------------------|
| Tilvitnanir       | CDS-sölutilboðshaus |
| QuoteDetails | CDS-sölutilboðslínur  |

## <a name="entity-flow"></a>Einingaflæði

Sölutilboð eru stofnuð í Sales og samstillt í Finance and Operations.

Sölutilboð úr Sales eru aðeins samstillt ef eftirfarandi skilyrði eru uppfyllt:

- Öllum tilboðsvörum á sölutilboðinu eru viðhaldið ytra.
- Eftir að þú smellir á **Virkja tilboð** er sölutilboðið virk.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

**Er aðens með utanaðkomandi vörur** reitnum hefur verið bætt við **Tilboð** til að fylgjast stöðugt með því hvort sölutilboð samanstanda aðeins af utanaðkomandi vörum. Ef sölutilboð inniheldur aðeins afurðir sem unnið er með utan frá, er afurðunum stýrt í Finance and Operations. Þetta tryggir að þú reynir ekki að virkja og samstilla sölutilboðslínur með vörum sem eru óþekktar Finance and Operations.

Allar tilboðsvörur á sölutilboðinu eru uppfærðar með **Er aðeins með utanaðkomandi vörur** upplýsingar í sölutilboðshausnum. Þessar upplýsingar finnast í **Tilboð er aðeins með utanaðkomandi vörur** reitnum á einingunni **QuoteDetails**.

Hægt er að bæta við afslætti við tilboðsvöruna og hann verður samstilltur við Finance and Operations. Reitirnir **Afsláttur**, **Gjöld** og **Skattur** á hausnum er stjórnað af uppsetningu í Finance and Operations. Eins og er, styður þessi uppsetning ekki samþættingarvörpun. Í núverandi hönnun er reitunum **Verð**, **Afsláttur**, **Gjöld** og **skattur** viðhaldið í Finance and Operations.

I Sales gerir lausnin það að verkum að eftirfarandi reitir eru ritvarðir, þar sem gildin eru ekki samstillt við Finance and Operations.

- Reitir með lesaðgangi í sölutilboðshaus: **Afsláttur %**, **Afsláttur** og **Flutningsupphæð**
- Reitir aðeins með lesaðgangi á tilboðsvörum: **Skattur**

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en sölutilboð eru samstillt er mikilvægt að eftirfarandi stillingar séu uppfærðar.

### <a name="setup-in-sales"></a>Uppsetning í Sales

- Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á. Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki. Ef teymið hefur ekki stjórnendaaðgang þegar þú keyri verkefnið úr gagnasamþáttara færðu villuskilaboð sem segir að aðalteymi vantar.

    Til að setja upp heimildir fyrir teymið ferðu í **Stillingar** &gt; **Öryggi** &gt; **Teymi** og velur teymið. Veldu **Stjórna hlutverkum** og svo hltuverk með viðkomandi heimildir, svo sem **Kerfisstjóri**.

- Farið í **Stillingar**&gt;**Stjórnun**&gt;**Kerfisstillingar**&gt;**Sales** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:

    - **Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.
    - **Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.

### <a name="setup-in-the-data-integration-project"></a>Setja upp gagnasamþættingarverk

#### <a name="quoteheader"></a>QuoteHeader

- Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Shipto\_land** í **DeliveryAddressCountryRegionISOCode**. Í gildisvörpuninni er hægt að skilgreina sjálfgefið gildi sem er notað ef gildið er autt. Slepptu aðeins vinstri hliðinni og settu hægri hliðina í viðkomandi land eða svæði. Á þennan hátt þarf ekki að slá inn landið eða svæði fyrir innlendar pantanir.

    Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð og þegar autt gildi jafngildir gildini **US**.

#### <a name="quoteline"></a>QuoteLine

- Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** sé til staðar í Finance and Operations.
- Gangið úr skugga um að nauðsynelgar einingar séu skilgreindar í Sales.

    Sniðmátsgildi með gildisvörpun er skilgreint fyrir **oumid.name** í **SalesUnitSymbol**.

- Valfrjálst: Hægt er að bæta við eftirfarandi vörpun til að tryggja að sölutilboðslínur séu fluttar inn í Finance and Operations ef engar sjálfgefnar upplýsingar eru frá viðskiptavinum eða vörunni:

    - **SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations. Það eru engin sjálfgefin sniðmátsgildi fyrir **SiteId**.
    - **WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations. Það er engin sjálfgefin sniðmátsgildi fyrir **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Sniðmátsvörpun í gagnasamþáttara

> [!NOTE]
> - Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations. Eins og er, styður þessi uppsetning ekki samþættingarvörpun. Í núverandi hönnun eru reitirnir **Verð**, **Afsláttur**, **Gjöld** og **Skattur** meðhöndlaðir af Finance and Operations.
> - Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.

Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.

### <a name="quoteheader"></a>QuoteHeader

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Tengd efnisatriði

[Prospect to cash](prospect-to-cash.md)


