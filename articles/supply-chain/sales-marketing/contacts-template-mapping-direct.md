---
title: Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla einingar tengiliðar (tengiliða) og tengiliðar (viðskiptavina) úr Dynamics 365 Sales við Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 57a9c2a860e99855e841f0f4276ba2f92767c2b1
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062516"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management

[!include [banner](../includes/banner.md)]



> [!NOTE]
> Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Microsoft Dataverse fyrir forrit](/powerapps/administrator/data-integrator).

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla töflur tengiliðs (tengiliða) og tengiliðar (viðskiptavina) beint úr Dynamics 365 Sales við Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales. Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.

[![Gagnaflæði í Prospect to cash.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla tengiliðatöflur (Tengiliðir) í Sales í tengiliðatölfur (Viðskiptavinir) í Supply Chain Management.

- **Heiti sniðmátanna í gagnasamþættingu**

    - Tengiliðir (Sales til Supply Chain Management) - Bein
    - Tengiliðir við viðskiptavin (Sales til Supply Chain Management) - Beint

- **Heiti verksins í gagnasamþættingarverki**

    - Tengiliðir
    - ContactToCustomer

Eftirfarandi samstilliningarverkefni er nauðsynlegt til að samstiling Tengiliðar geti farið fram: Lyklar (Sales við Supply Chain Management)

## <a name="entity-sets"></a>Einingastamstæður

| Sala    | Birgðakeðjustjórnun |
|----------|------------------------|
| Tengiliðir | Dataverse-tengiliðir           |
| Tengiliðir | Viðskiptavinir V2           |

## <a name="entity-flow"></a>Einingaflæði

Tengiliðum er stjórnað í Sales og þeir samstilltir við Supply Chain Management.

Tengiliður í Sales getur orðið tengiliður eða viðskiptavinur í Supply Chain Management. Til að ákvarða hvort tengiliður í Sales eigi að samstilla við Supply Chain Management sem tengilið eða viðskiptamann, lítur kerfið á eftirfarandi eiginleika tengiliðarins í Sales:

- **Samstilling við viðskiptavin í Supply Chain Management:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Já**
- **Samstilling við tengilið í Supply Chain Management:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Nei** og **Fyrirtæki** (yfirreikningur/tengiliður) vísar í reikning (ekki tengilið)

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Nýjum **Er virkur viðskiptavinur** dálki hefur verið bætt við tengiliðinn. Dálkurinn er notaður til að aðgreina tengiliði sem hafa sölustarfsemi og tengiliði sem hafa ekki sölustarfsemi. **Er virkur viðskiptavinur** er stillt á **Já** aðeins fyrir tengiliði sem hafa tengd tilboð, pantanir eða reikninga. Aðeins þeir tengiliðir eru samstilltir við Supply Chain Management sem viðskiptavinir.

Nýjum **IsCompanyAnAccount** dálki hefur verið bætt við tengiliðinn. Dálkurinn gefur til kynna hvort tengiliður er tengdur við fyrirtæki (yfirreikning/tengilið) af gerðinni **Reikningur**. Þessar upplýsingar eru notaðar til að auðkenna tengiliði sem ætti að samstilla við Supply Chain Management sem tengiliði.

Nýjum **Númer tengiliðs** dálki hefur verið bætt við tengiliðinn til að hjálpa við að tryggja einkvæman lykil fyrir samþættinguna. Þegar nýr tengiliður er búinn til er sjálfkrafa myndað **Númer tengiliðs** gildi með því að nota númeraröð. Gildið samanstendur af **CON**, því næst hækkandi talnaröð og svo sex stafa viðskeyti. Hér er dæmi: **CON-01000-BVRCPS**

Þegar samþættingarlausn fyrir Sales er beitt stillir uppfærsluforskrift dálkinn **Númer tengiliðs** fyrir fyrirliggjandi tengiliði með því að nota númeraröðina sem áður var getið. Uppfærsluforskriftin stillir einnig **Er virkur viðskiptavinur** dálkinn á **Já** fyrir alla tengiliði með söluaðgerðir.

## <a name="in-supply-chain-management"></a>Í Supply Chain Management

Tengiliðir eru merktir með eiginleikanum **IsContactPersonExternallyMaintained**. Þessi eign gefur til kynna að unnið sé með tilteknum tengilið utan frá. Í því tilfelli er utanaðkomandi tengiliðum viðhaldið í Sales.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="contact-to-customer"></a>Tengiliður í viðskiptavin

- **Viðskiptavinahópur** er krafist í Supply Chain Management. Til að forðast samstillingarvillur er hægt að tilgreina sjálfgildi í vörpun. Sjálfgefið gildi er síðan notað ef dálkurinn er hafður auður í Sales.

    Sjálfgefið sniðmátsgildi er **10**.

- Með því að bæta við eftirfarandi vörpunum er hægt að hjálpa til við að minnka fjölda handvirkra uppfærslna sem eru nauðsynlegar í Supply Chain Management. Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.

    - **SiteId** – Einnig er hægt að tilgreina sjálfgefið svæði vara í Supply Chain Management. Svæði er nauðsynlegt til að búa til tilboð og sölupöntunum í Supply Chain Management.

        Sniðmátsgildi fyrir **SiteId** er ekki skilgreint.

    - **WarehouseId** – Einnig er hægt að tilgreina sjálfgefið vöruhús vara í Supply Chain Management. Vöruhús er nauðsynlegt til að búa til tilboð og sölupöntunum í Supply Chain Management.

        Sniðmátsgildi fyrir **WarehouseId** er ekki skilgreint.

    - **LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Supply Chain Management.
    
        Sjálfgefið sniðmátsgildi er **en-us**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. 

> [!NOTE]
> Vörpunin sýnir hvaða dálkupplýsingar verða samstilltar úr Sales í Supply Chain Management.

### <a name="contact-to-contact-example"></a>Dæmi um tengilið í tengilið

![Sniðmátsvörpun tengiliðar í tengilið í gagnasamþættingu.](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer-example"></a>Dæmi um tengilið í viðskiptavin

![Sniðmátsvörpun tengiliðar í viðskiptavin í gagnasamþættingu.](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Tengd efnisatriði

[Viðfang til sjóðstreymis](prospect-to-cash.md)

[Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management](accounts-template-mapping-direct.md)

[Samstilla vörur beint úr Sales við viðskiptavini í Supply Chain Management við vörur í Sales](products-template-mapping-direct.md)

[Samstilling sölupantana beint á milli Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Samstilla hausa og línur sölureiknings beint úr Supply Chain Management í Sales](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]