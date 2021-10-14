---
title: Samstilla hausa og línur sölutilboðs beint úr Sales í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur sölutilboða beint úr Dynamics 365 Sales við Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 46584f397e83bc68878ff5ef2848a251912811af
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566408"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Samstilla hausa og línur sölutilboðs beint úr Sales í Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur sölutilboða beint úr Dynamics 365 Sales við Dynamics 365 Supply Chain Management.

> [!NOTE]
> Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Microsoft Dataverse fyrir forrit](/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales. Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna fyrir reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.

[![Gagnaflæði í Prospect to cash.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla sölutilboðshausa og línur beint úr Sales í Supply Chain Management:

- **Heiti sniðmátsins í Gagnaflutningi:** Sölutilboð (Sales til Supply Chain Management) - beint
- **Heiti verksins í gagnasamþættingarverki:**

    - QuoteHeader
    - QuoteLine

Eftirfarandi samstillingarverk eru nauðsynleg áður en samstilling úr sölutilboðshausum og línum getur átt sér stað:

- Afurðir (Supply Chain Management itl Sales) - Beint
- Lyklar (Sales til Supply Chain Management) - Bein (ef notað)
- Tengiliðir við viðskiptavini (Sales til Supply Chain Management) - Beint (ef notað)

## <a name="entity-set"></a>Einingastamstæða

| Sala        | Birgðakeðjustjórnun     |
|--------------|----------------------------|
| Tilvitnanir       | Dataverse sölutilboðshaus |
| QuoteDetails | Dataverse sölutilboðslínur  |

## <a name="entity-flow"></a>Einingaflæði

Sölutilboð eru stofnuð í Sales og samstillt við Supply Chain Management.

Sölutilboð úr Sales eru aðeins samstillt ef eftirfarandi skilyrði eru uppfyllt:

- Öllum tilboðsvörum á sölutilboðinu eru viðhaldið ytra.
- Eftir að þú smellir á **Virkja tilboð** er sölutilboðið virk.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

**Er aðens með utanaðkomandi vörur** reitnum hefur verið bætt við **Tilboð** til að fylgjast stöðugt með því hvort sölutilboð samanstanda aðeins af utanaðkomandi vörum. Ef sölutilboð inniheldur aðeins afurðir sem unnið er með utan frá, er afurðunum stýrt í Supply Chain Management. Þetta tryggir að þú reynir ekki að virkja og samstilla sölutilboðslínur með vörum sem eru óþekktar Supply Chain Management.

Allar tilboðsvörur á sölutilboðinu eru uppfærðar með **Er aðeins með utanaðkomandi vörur** upplýsingar í sölutilboðshausnum. Þessar upplýsingar finnast í **Tilboð er aðeins með utanaðkomandi vörur** reitnum á einingunni **QuoteDetails**.

Hægt er að bæta við afslætti við tilboðsvöruna og hann verður samstilltur við Supply Chain Management. Reitirnir **Afsláttur**, **Gjöld** og **Skattur** á hausnum er stjórnað af uppsetningu í Supply Chain Management. Eins og er, styður þessi uppsetning ekki samþættingarvörpun. Í núverandi hönnun er reitunum **Verð**, **Afsláttur**, **Gjöld** og **skattur** viðhaldið í Supply Chain Management.

I Sales gerir lausnin það að verkum að eftirfarandi reitir eru ritvarðir, þar sem gildin eru ekki samstillt við Supply Chain Management:

- Reitir með lesaðgangi í sölutilboðshaus: **Afsláttur %**, **Afsláttur** og **Flutningsupphæð**
- Reitir aðeins með lesaðgangi á tilboðsvörum: **Skattur**

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en sölutilboð eru samstillt er mikilvægt að eftirfarandi stillingar séu uppfærðar.

### <a name="setup-in-sales"></a>Uppsetning í Sales

- Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á. Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki. Ef teymið hefur ekki stjórnendaaðgang þegar þú keyri verkefnið úr gagnasamþáttara færðu villuskilaboð sem segir að aðalteymi vantar.

    Til að setja upp heimildir fyrir teymið ferðu í **Stillingar** &gt; **Öryggi** &gt; **Teymi** og velur teymið. Veldu **Stjórna hlutverkum** og svo hltuverk með viðkomandi heimildir, svo sem **Kerfisstjóri**.

- Farið í **Stillingar** &gt; **Stjórnun** &gt; **Kerfisstillingar** &gt; **Sala** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:

    - **Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.
    - **Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.

### <a name="setup-in-the-data-integration-project"></a>Setja upp gagnasamþættingarverk

#### <a name="quoteheader"></a>QuoteHeader

- Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Shipto\_land** í **DeliveryAddressCountryRegionISOCode**. Í gildisvörpuninni er hægt að skilgreina sjálfgefið gildi sem er notað ef gildið er autt. Slepptu aðeins vinstri hliðinni og settu hægri hliðina í viðkomandi land eða svæði. Á þennan hátt þarf ekki að slá inn landið eða svæði fyrir innlendar pantanir.

    Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð og þegar autt gildi jafngildir gildini **US**.

#### <a name="quoteline"></a>QuoteLine

- Gangið úr skugga um að nauðsynleg gildisvörpun sé til staðar fyrir **SalesUnitSymbol** í Supply Chain Management.
- Gangið úr skugga um að nauðsynelgar einingar séu skilgreindar í Sales.

    Sniðmátsgildi með gildisvörpun er skilgreint fyrir **oumid.name** í **SalesUnitSymbol**.

- Valfrjálst: Hægt er að bæta við eftirfarandi vörpun til að tryggja að sölutilboðslínur séu fluttar inn í Supply Chain Management ef engar sjálfgefnar upplýsingar eru frá viðskiptavinum eða vörunni:

    - **SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Supply Chain Management. Það eru engin sjálfgefin sniðmátsgildi fyrir **SiteId**.
    - **WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Supply Chain Management. Það er engin sjálfgefin sniðmátsgildi fyrir **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Sniðmátsvörpun í gagnasamþáttara

> [!NOTE]
> - Reitirnir **Afsláttur**, **Gjöld** og **Skattur** er stjórnað af flókinni uppsetningu í Supply Chain Management. Eins og er, styður þessi uppsetning ekki samþættingarvörpun. Í núverandi hönnun eru reitirnir **Verð**, **Afsláttur**, **Gjöld** og **Skattur** meðhöndlaðir af Supply Chain Management.
> - Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.

Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.

### <a name="quoteheader"></a>QuoteHeader

![Sniðmátsvörpun í Gagnasamþáttara, QuoteHeader.](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Sniðmátsvörpun í Gagnasamþáttara, QuoteLine.](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Tengd efnisatriði

[Viðfang til sjóðstreymis](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]