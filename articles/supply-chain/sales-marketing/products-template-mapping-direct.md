---
title: Samstilla vörur beint úr Sales við viðskiptavini í Supply Chain Management við vörur í Sales
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verk sem notuð eru til að samstilla vörur úr Dynamics 365 Supply Chain Management við Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6ffd55585ff43f993876de6c669eb61e74a9fd79
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527315"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Samstilla vörur beint úr Sales við viðskiptavini í Supply Chain Management við vörur í Sales

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verk sem notuð eru til að samstilla vörur beint úr Dynamics 365 Supply Chain Management við Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales. Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.

[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [Power Apps Admin Center](https://admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla afurðir frá Supply Chain Management til Sales.

- **Heiti sniðmátsins í Gagnaflutningi:** Vörur (Supply Chain Management í Sales) - beint
- **Heiti verksins í gagnasamþættingarverki:** Vörur

Ekki þarf að samstilla áður en samstilling vöru á sér stað.

## <a name="entity-set"></a>Einingastamstæða

| Birgðakeðjustjórnun    | Sala    |
|----------------------------|----------|
| Seljanlegar útgefnar afurðir | Afurðir |

## <a name="entity-flow"></a>Einingaflæði

Afurðum er stjórnað í Supply Chain Management og þær samstilltar við Sales. **Seljanlegar útgefnar afurðir** gagnaeiningin í Supply Chain Management flytur aðeins út vörur sem eru *seljanlegar*. Seljanlegar vörur eru vörur sem hafa þær upplýsingar sem þær þurfa til að nota á sölupöntun. Sama regla gildir þegar vara er villuleituð með því að nota **Villuleita** virknina á síðunni **Útgefin afurð**.

Vörunúmerið er notað sem lykill. Þegar afurðarafbrigði eru samstillt við Sales hefur hvert afurðarafbrigði einkvæmt vörukenni.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Í Sales hefur nýjum **Er viðhaldið að utan** reit verið bætt við vörur til að tákna að viðkomandi vöru sé viðhaldið að utan. Gildið er sjálfkrafa stillt á **Já** við innflutning í Sales. Eftirtalin gildi eru tiltæk:

- **Já** – Vara á uppruna í Supply Chain Management og er ekki hægt að breyta í Sales.
- **Nei** – varan var upphaflega færð inn í Sales.
- **(Autt)** – Varan var til staðar í Sales áður en Prospect to cash lausnin var virkjuð.

Reiturinn **Er viðhaldið að utan** hjálpar til við að tryggja að aðeins tilboð og sölupantanir með ytri vörur verði samstilltar við Supply Chain Management.

Vörum sem er viðhaldið að utan er sjálfkrafa bætt við fyrsta gilda verðlistann með sama gjaldmiðil. Verðlistar eru skipulagðir í stafrófsröð. Söluverð vöru úr Supply Chain Management er notað sem verð á verðlistanum. Því verður verðlisti að vera til staðar í Sales fyrir alla sölugjaldmiðla vöru í Supply Chain Management. Gengi gjaldmiðilsins á seljanlegu vörunni er stillt á bókhaldsgjaldmiðilinn í lögaðilanum sem varan er flutt út frá.

> [!NOTE]
> - Vörusamstilling mun ekki heppnast nema til sé verðlisti sem hefur samsvarandi gjaldmiðil.
> - Þú getur stjórnað verðskránni sem er notuð með samþættingunni með vörpun pricelevelid.name [Sjálfgildi Verðlisti (Nafn)] í Gagnasamþætting verkefninu. Inntakið verður að vera í lágstöfum eingöngu. Til dæmis yrði sjálfgildið fyrir verðlista í Sölu sem kallast „Staðlaður“: Áfangasvæði: pricelevelid.name [Sjálfgildi Verðskrá (Nafn)] og Kortategund: [ { "transformType": "Default", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

- Áður en samstilling er keyrð í fyrsta skipti þarf að fylla út Einkvæm afurð töfluna fyrir fyrirliggjandi vörur í Supply Chain Management. Fyrirliggjandi vörur verða ekki samstilltar fyrr en verki er lokið.

    1. Notaðu Leit í Supply Chain Management til að leita að **Fylla út töflu fyrir einkvæma afurð**.
    2. Velja skal **Mynda töflu fyrir einkvæma afurð** til að keyra verkið. Aðeins má keyra verkið einu sinni.

- Gakktu úr skugga um að nauðsynleg virðisvörpun fyrir sölueininguna á milli Supply Chain Management og Sales sé til staðar í vörpun **SalesUnitSymbol** í **DefaultUnit (Name)**.
- Uppfæra skal virðisvörpun fyrir **Einingarflokk** (**defaultuomscheduleid.name**) þannig að hann passi við **Einingarflokka** í Sales.

    Sjálfgefið sniðmátsgildi er **Sjálfgefin eining**.

- Ganga skal úr skugga um að mælieining fyrir allar vörur úr Supply Chain Management séu til staðar í Sales.
- Ganga skal úr skugga um að verðlisti sé til staðar í Sales fyrir alla sölugjaldmiðla vöru í Supply Chain Management.
- Þegar vörur eru stofnaðar í Sales geta þær haft stöðuna **Drög** eða **Virkar**. Þessu er stjórnað í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** í Sales.

    Vörur sem hafa stöðuna **Drög** þegar þær eru búin til verður að virkja áður en hægt er að bæta við tilboðum eða sölupöntunum.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. 

> [!NOTE]
> Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar úr Sales í Supply Chain Management.

![Sniðmátsvörpun í Gagnasamþáttara](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Tengd efnisatriði

[Viðfang til sjóðstreymis](prospect-to-cash.md)

[Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management](accounts-template-mapping-direct.md)

[Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management](contacts-template-mapping-direct.md)

[Samstilling sölupantana beint á milli Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Samstilla hausa og línur sölureiknings beint úr Supply Chain Management í Sales](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]