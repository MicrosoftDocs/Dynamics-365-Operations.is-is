---
title: Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla einingar tengiliðar (tengiliða) og tengiliðar (viðskiptavina) úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fbc75702c9db1e877addc4605dcb444c344dfa5c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742448"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla einingar tengiliðar (tengiliða) og tengiliðar (viðskiptavina) beint úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales. Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Finance and Operations og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.

[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla Tengilið (Tengiliðir) einingar í Sales við Tengilið (Viðskiptavinir) einingar í Finance and Operations:

- **Heiti sniðmátsins í Gagnaflutningi:**

    - Tengiliðir (Sales við Fin and Ops) - beint
    - Tengiliðir við Viðskiptavin (Sales við Fin and Ops) - beint

- **Heiti verksins í gagnasamþættingarverki:**

    - Tengiliðir
    - ContactToCustomer

Eftirfarandi samstilliningarverkefni er nauðsynlegt til að samstiling Tengiliðar geti farið fram: Lyklar (Sales við Fin and Ops)

## <a name="entity-sets"></a>Einingastamstæður

| Sölur    | Finance and Operations |
|----------|------------------------|
| Tengiliðir | Tengiliðir fyrir skuldatryggingu           |
| Tengiliðir | Viðskiptavinir V2           |

## <a name="entity-flow"></a>Einingaflæði

Tengiliðum er stýrt í Sales og þeir samstilltir við Finance and Operations.

Tengiliður í Sales getur orðið tengiliður eða viðskiptavinur í Finance and Operations. Til að ákvarða hvort tengiliður í Sales eigi að samstilla við Finance and Operations sem tengilið eða viðskiptamann, lítur kerfið á eftirfarandi eiginleika tengiliðarins í Sales:

- **Samstilling við viðskiptavin í Finance and Operations:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Já**
- **Samstilling við tengilið í Finance and Operations:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Nei** og **Fyrirtæki** (yfirreikningur/tengiliður) vísar í reikning (ekki tengilið)

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Nýjum **Er virkur viðskiptavinur** reit hefur verið bætt við tengiliðinn. Reiturinn er notaður til að aðgreina tengiliði sem hafa sölustarfsemi og tengiliði sem hafa ekki sölustarfsemi. **Er virkur viðskiptavinur** er stillt á **Já** aðeins fyrir tengiliði sem hafa tengd tilboð, pantanir eða reikninga. Aðeins þeir tengiliðir eru samstilltir við Finance and Operations sem viðskiptavinir.

Nýjum **IsCompanyAnAccount** reit hefur verið bætt við tengiliðinn. Reiturinn gefur til kynna hvort tengiliður er tengdur við fyrirtæki (yfirreikning/tengilið) af gerðinni **Reikningur**. Þessar upplýsingar eru notaðar til að auðkenna tengiliði sem ætti að samstilla við Finance and Operations sem tengiliði.

Nýjum **Númer tengiliðs** reit hefur verið bætt við tengiliðinn til að hjálpa við að tryggja einkvæman lykil fyrir samþættinguna. Þegar nýr tengiliður er búinn til er sjálfkrafa myndað **Númer tengiliðs** gildi með því að nota númeraröð. Gildið samanstendur af **CON**, því næst hækkandi talnaröð og svo sex stafa viðskeyti. Hér er dæmi: **CON-01000-BVRCPS**

Þegar samþættingarlausn fyrir Sales er beitt stillir uppfærsluforskrift **Númer tengiliðs** fyrir fyrirliggjandi tengiliði með því að nota númeraröðina sem áður var getið. Uppfærsluforskriftin stillir einnig **Er virkur viðskiptavinur** reitinn á **Já** fyrir alla tengiliði með söluaðgerðir.

## <a name="in-finance-and-operations"></a>Í Finance and Operations

Tengiliðir eru merktir með eiginleikanum **IsContactPersonExternallyMaintained**. Þessi eign gefur til kynna að unnið sé með tilteknum tengilið utan frá. Í því tilfelli er utanaðkomandi tengiliðum viðhaldið í Sales.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="contact-to-customer"></a>Tengiliður í viðskiptavin

- **CustomerGroup** er nauðsynlegt í Finance and Operations. Til að forðast samstillingarvillur er hægt að tilgreina sjálfgildi í vörpun. Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales.

    Sjálfgefið sniðmátsgildi er **10**.

- Með því að bæta við eftirfarandi vörpunum er hægt að hjálpa til við að minnka fjölda handvirkra uppfærslna sem eru nauðsynlegar í Finance and Operations. Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.

    - **SiteId** – Einnig er hægt að tilgreina sjálfgefið svæði vara í Finance and Operations. Svæði er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations.

        Sniðmátsgildi fyrir **SiteId** er ekki skilgreint.

    - **WarehouseId** – Einnig er hægt að tilgreina sjálfgefið vöruhús vara í Finance and Operations. Vöruhús er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations.

        Sniðmátsgildi fyrir **WarehouseId** er ekki skilgreint.

    - **LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations.
    
        Sjálfgefið sniðmátsgildi er **en-us**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. 

> [!NOTE]
> Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar ´ru Sales í Finance and Operations.

### <a name="contact-to-contact"></a>Tengiliður í tengilið

![Sniðmátsvörpun í Gagnasamþáttara](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Tengiliður í viðskiptavin

![Sniðmátsvörpun í Gagnasamþáttara](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Tengd efnisatriði

[Prospect to cash](prospect-to-cash.md)

[Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations](accounts-template-mapping-direct.md)

[Samstilla vörur beint úr Finance and Operations við vörur í Sales](products-template-mapping-direct.md)

[Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations](sales-order-template-mapping-direct-two-ways.md)

[Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations](sales-invoice-template-mapping-direct.md)


