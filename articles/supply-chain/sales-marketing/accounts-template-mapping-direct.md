---
title: Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla reikninga úr Dynamics 365 Sales í Supply Chain Management.
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
ms.openlocfilehash: f6f5662427be92ad57def2af772dd69abd575b81
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566504"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Microsoft Dataverse fyrir forrit](/powerapps/administrator/data-integrator).

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla reikninga beint úr Dynamics 365 Sales í Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales.  Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.

[![Gagnaflæði í Prospect to cash.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla lykla frá Sales til Supply Chain Management:

- **Heiti sniðmátsins í gagnaflutningi:** Reikningar (Sales í Fin and Ops) - beint
- **Heiti verksins í verkefninu:** Reikningar - Viðskiptamenn

Ekki þarf að samstilla áður en samstilling Reiknings/Viðskiptamanns á sér stað.

## <a name="entity-set"></a>Einingastamstæða

| Sala    | Birgðakeðjustjórnun |
|----------|------------------------|
| Lyklar | Viðskiptavinir V2           |

## <a name="entity-flow"></a>Einingaflæði

Lyklum er stjórnað í Sales og þeir samstilltir við Supply Chain Management sem viðskiptamenn. **Er viðhaldið utanfrá** eignin á þessum viðskiptamönnum er stillt á **Yes** til að rekja viðskiptamenn sem eiga uppruna sinn í Sales. Við reikningsfærslu eru þessar upplýsingar notaðar til að sía reikninga sem eru samstilltir við Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Dálkurinn **Lykilnúmer** er í boði á síðunni **Lykill**. Það er einkvæmur lykill til að styðja við samþættingu. Eiginleiki raunlykils fyrir lausnina Tengslastjórnun (CRM) kann að hafa áhrif á viðskiptavini sem hafa þegar notað **Lykilnúmer** dálkinn en notað ekki einkvæm **Lykilnúmer** gildi fyrir hvern lykil. Eins og er styður samþættingarlausin ekki slík tilfelli.

Þegar nýr lykill er stofnaður, og ef **Lykilnúmersgildi** er ekki þegar til, er það sjálfkrafa búið til með talnaröð. Gildið samanstendur af **ACC**, því næst hækkandi talnaröð og svo sex stafa viðskeyti. Hér er dæmi: **ACC-01000-BVRCPS**

Þegar samþættingarlausn fyrir Sales er beitt stillir uppfærsluforskrift dálkinn **Númer tengiliðs** fyrir fyrirliggjandi reikninga í Sales. Ef engin **Reikningsnúmer** gildi eru til staðar er númeraröðin sem var minnst á áður notuð.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

- **CustomerGroupId** vörpun verður að vera uppfærð í gilt gildi í Supply Chain Management. Hægt er að tilgreina sjálfgefið gildi eða setja upp gildi með því að nota gildisvörpun.

    Sjálfgefið sniðmátsgildi er **10**.

- Með því að bæta við eftirfarandi vörpunum er hægt að hjálpa til við að minnka fjölda handvirkra uppfærslna sem eru nauðsynlegar í Supply Chain Management. Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.

    - **SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Supply Chain Management. Sjálfgefið svæði er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum.

        Sjálfgefið sniðmátsgildi er **1**.

    - **WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Supply Chain Management. Sjálfgefið vöruhús er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum í Supply Chain Management.

        Sjálfgefið sniðmátsgildi er **13**.

    - **LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Supply Chain Management. Sjálfgefið er að tungumálið í pöntunarhausnum frá viðskiptavininum sé notað.

        Sjálfgefið sniðmátsgildi er **en-us**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

> [!NOTE]
> **Greiðsluskilmálar**, **Farmskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti í sjálfgefinni vörpun. Til að varpa þessum dálkum, verður að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem taflan er samstillt á milli.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. 

> [!NOTE]
> Vörpunin sýnir hvaða dálkupplýsingar verða samstilltar úr Sales í Supply Chain Management.

![Sniðmátsvörpun í Gagnasamþættingu.](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Tengd efnisatriði


[Viðfang til sjóðstreymis](prospect-to-cash.md)

[Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management](accounts-template-mapping-direct.md)

[Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management](contacts-template-mapping-direct.md)

[Samstilling sölupantana beint á milli Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Samstilla hausa og línur sölureiknings beint úr Supply Chain Management í Sales](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]