---
title: "Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla lykla úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 16bbca2d9eb8c3d9c33752404ebecbe4415517a2
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 Data samþættingu](/common-data-service/entity-reference/dynamics-365-integration).

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla lykla beint úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales.  Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Finance and Operations og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.

[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla lykla frá Sales til Finance and Operations:

- **Heiti sniðmátsins í gagnaflutningi:** Reikningar (Sales í Fin and Ops) - beint
- **Heiti verksins í verkefninu:** Reikningar - Viðskiptamenn

Ekki þarf að samstilla áður en samstilling Reiknings/Viðskiptamanns á sér stað.

## <a name="entity-set"></a>Einingastamstæða

| Sölur    | Finance and Operations |
|----------|------------------------|
| Lyklar | Viðskiptavinir V2           |

## <a name="entity-flow"></a>Einingaflæði

Lyklum er stjórnað í Sales og þeir samstilltir við Finance and Operations sem viðskiptamenn. **Er viðhaldið utanfrá** eignin á þessum viðskiptamönnum er stillt á **Yes** til að rekja viðskiptamenn sem eiga uppruna sinn í Sales. Við reikningsfærslu eru þessar upplýsingar notaðar til að sía reikninga sem eru samstilltir við Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Reiturinn **Lykilnúmer** er tiltækur á síðunni **Lykill**. Það er einkvæmur lykill til að styðja við samþættingu. Raunlykilseiginleikinn í Tengslastjórnunarlausninni (CRM) gæti haft áhrif á viðskiptavini sem nota þegar reitinn **Lykilnúmer** en nota ekki einkvæm **Lykilnúmersgildi** fyrir hvern lykil. Eins og er styður samþættingarlausin ekki slík tilfelli.

Þegar nýr lykill er stofnaður, og ef **Lykilnúmersgildi** er ekki þegar til, er það sjálfkrafa búið til með talnaröð. Gildið samanstendur af **ACC**, því næst hækkandi talnaröð og svo sex stafa viðskeyti. Hér er dæmi: **ACC-01000-BVRCPS**

Þegar samþættingarlausnin fyrir Sales er notuð, stillir uppfærsluforskrift reitinn **Lykilnúmer** fyrir lykla sem þegar eru til í Sales. Ef engin **Reikningsnúmer** gildi eru til staðar er númeraröðin sem var minnst á áður notuð.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

- **CustomerGroupId** vörpun verður að vera uppfærð í gilt gildi í Finance and Operations. Hægt er að tilgreina sjálfgefið gildi eða setja upp gildi með því að nota gildisvörpun.

    Sjálfgefið sniðmátsgildi er **10**.

- Með því að bæta við eftirfarandi vörpunum er hægt að hjálpa til við að minnka fjölda handvirkra uppfærslna sem eru nauðsynlegar í Finance and Operations. Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.

    - **SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations. Sjálfgefið svæði er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum.

        Sjálfgefið sniðmátsgildi er **1**.

    - **WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations. Sjálfgefið vöruhús er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum í Finance and Operations.

        Sjálfgefið sniðmátsgildi er **13**.

    - **LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations. Sjálfgefið er að tungumálið í pöntunarhausnum frá viðskiptavininum sé notað.

        Sjálfgefið sniðmátsgildi er **en-us**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

> [!NOTE]
> Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. 

> [!NOTE]
> Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar ´ru Sales í Finance and Operations.

![Template mapping in Data integration](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Tengd efnisatriði


[Prospect to cash](prospect-to-cash.md)

[Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations](accounts-template-mapping-direct.md)

[Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations](contacts-template-mapping-direct.md)

[Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations](sales-order-template-mapping-direct.md)

[Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations](sales-invoice-template-mapping-direct.md)


