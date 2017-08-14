---
title: "Samstilla reikninga frá Sales til viðskiptavina í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla lykla úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: b497f078d9786a5c7630e924da6bb04cad37f5e9
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Samstilla reikninga frá Sales til viðskiptavina í Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla lykla úr Microsoft Dynamics 365 for Sales (Sales) í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="template-and-task"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla lykla úr Sales í Finance and Operations:

- **Nafn sniðmáts:** Lyklar (Sales í Fin and Ops)
- **Heiti á verkefninu í verkinu:** - Lyklar - Lykill - Viðskiptavinir

Samstilling verkefna nauðsynleg fyrir samstillingu Lykils/Viðskiptavinar: Engin

## <a name="entity-set"></a>Einingastamstæða

| Sala    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Lyklar | Lykill | Viðskiptavinir              |

## <a name="entity-flow"></a>Einingaflæði

Lyklum er stýrt í Sales og þeir eru samstilltir í Finance and Operations sem Viðskiptavinir. Eiginleikinn **Unnið með utan frá** á þessum Viðskiptavinum er stilltur á **Já** til að rekja Viðskiptavini sem koma frá Sales. Við reikningsfærslu eru þessar upplýsingar notaðar til að sía reikninga sem eru samstilltir við Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Reiturinn **Lykilnúmer** er tiltækur á síðunni **Lykill**. Hann hefur verið gerður einkvæmur raunlykill til að styðja samþættinguna. Raunlykilseiginleikinn í Tengslastjórnunarlausninni (CRM) gæti haft áhrif á viðskiptavini sem nota þegar reitinn **Lykilnúmer** en nota ekki einkvæm **Lykilnúmersgildi** fyrir hvern lykil. Eins og er styður samþættingarlausin ekki slík tilfelli.

Þegar nýr lykill er stofnaður, og ef **Lykilnúmersgildi** er ekki þegar til, er það sjálfkrafa búið til með talnaröð. Gildið samanstendur af **ACC**, því næst hækkandi talnaröð og svo sex stafa viðskeyti. Hér er dæmi: **ACC-01000-BVRCPS**

Þegar samþættingarlausnin fyrir Sales er notuð, stillir uppfærsluforskrift reitinn **Lykilnúmer** fyrir lykla sem þegar eru til í Sales. Ef það eru engin **Lykilnúmersgildi** er talnaröðin sem var lýst hér á undan notuð.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

- **CustomerGroupId** þarf að uppfæra í gilt gildi í Finance and Operations. Hægt er að tilgreina sjálfgefið gildi eða setja upp gildi með því að nota gildisvörpun. Sjálfgefið sniðmátsgildi er **10**.
- **Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations. Til að koma í veg fyrir samstillingarvillur er hægt að tilgreina sjálfgefið gildi. Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales.

    - Sjálfgefið sniðmátsgildi fyrir **AddressCountryRegionISOCode** er **USA**.
    - Sjálfgefið sniðmátsgildi fyrir **DeliveryAddressCountryRegionISOCode** er **USA**.

- Með því að bæta eftirfarandi vörpunum úr **CDS &gt; Ákvörðunarstað** geturðu dregið úr fjölda handvirkra uppfærslna sem nauðsynlegar eru í Finance and Operations. Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.

    - **SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations. Sjálfgefið svæði er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum. Sjálfgefið sniðmátsgildi fyrir **SiteId** er **1**.
    - **WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations. Sjálfgefið vöruhús er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum í Finance and Operations. Sjálfgefið sniðmátsgildi fyrir **WarehouseId** er **13**.
    - **LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations. Sjálfgefið er að tungumálið í pöntunarhausnum frá viðskiptavininum sé notað. Sjálfgefið sniðmátsgildi fyrir **LanguageId** er **en-us**.

- Uppfærðu CDS-fyrirtækjaauðkenni (**Organization_OrganizationId**) í **Uppruni &gt; CDS**. Sjálfgefið sniðmátsgildi er **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Sniðmátsvörpun í gagnasamþáttara

> [!NOTE]
> Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum verður að setja upp á gildisvörpun. Gildisvarpanir eiga sérstaklega við um gögnin í fyrirtækjunum sem einingin er samstillt á milli.

Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.

![Sniðmátsvörpun í gagnasamþáttara](./media/accounts-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun fyrir Lykla í gagnasamþáttara](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Tengd efnisatriði

[Samstilla afurðir úr Finance and Operations í afurðir í Sales](products-template-mapping.md)

[Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations](contacts-template-mapping.md)

[Samstilla sölutilboðshausa og línur úr Sales í Finance and Operations](sales-quotation-template-mapping.md)




