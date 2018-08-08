---
title: "Samstilla afurðir beint úr Finance and Operations við afurðir í Sales"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vörur úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 06/25/2018
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
ms.sourcegitcommit: 03bab1d03be71c0e23a6ea93f542d6a52a212a1f
ms.openlocfilehash: 66506953790fd77c2105591d3211c76991eced08
ms.contentlocale: is-is
ms.lasthandoff: 06/25/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Samstilla afurðir beint úr Finance and Operations við afurðir í Sales

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 Data samþættingu](/common-data-service/entity-reference/dynamics-365-integration).

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vörur beint úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales. Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Finance and Operations og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.

[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla vörur úr Sales við Finance and Operations

- **Heiti sniðmátsins í Gagnaflutningi:** Vörur (Fin og Ops í Sales) - beint
- **Heiti verksins í gagnasamþættingarverki:** Vörur

Ekki þarf að samstilla áður en samstilling vöru á sér stað.

## <a name="entity-set"></a>Einingastamstæða

| Finance and Operations     | Sölur    |
|----------------------------|----------|
| Seljanlegar útgefnar afurðir | Afurðir |

## <a name="entity-flow"></a>Einingaflæði

Afurðum er stýrt í Finance and Operations og þær eru samstilltar í Sales. **Seljanlegar útgefnar afurðir** gagnaeiningin í Finance and Operations flytur aðeins út vörur sem eru *seljanlegar*. Seljanlegar vörur eru vörur sem hafa þær upplýsingar sem þær þurfa til að nota á sölupöntun. Sama regla gildir þegar vara er villuleituð með því að nota **Villuleita** virknina á síðunni **Útgefin afurð**.

Vörunúmerið er notað sem lykill. Þegar afurðarafbrigði eru samstillt við Sales hefur hvert afurðarafbrigði einkvæmt vörukenni.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Í Sales hefur nýjum **Er viðhaldið að utan** reit verið bætt við vörur til að tákna að viðkomandi vöru sé viðhaldið að utan. Gildið er sjálfkrafa stillt á **Já** við innflutning í Sales. Eftirtalin gildi eru tiltæk:

- **Já** – Vara á uppruna í Finance and Operations og er ekki hægt að breyta í Sales.
- **Nei** – varan var upphaflega færð inn í Sales.
- **(Autt)** – Varan var til staðar í Sales áður en Prospect to cash lausnin var virkjuð.

Reiturinn **Er viðhaldið að utan** hjálpar til við að tryggja að aðeins tilboð og sölupantanir með ytri vörur verði samstilltar við Finance and Operations.

Vörum sem er viðhaldið að utan er sjálfkrafa bætt við fyrsta gilda verðlistann með sama gjaldmiðil. Verðlistar eru skipulagðir í stafrófsröð. Söluverð vöru úr Finance and Operations er notað sem verð á verðlistanum. Því verður verðlisti að vera til staðar í Sales fyrir alla sölugjaldmiðla vöru í Finance and Operations. Gengi gjaldmiðilsins á seljanlegu vörunni er stillt á bókhaldsgjaldmiðilinn í lögaðilanum sem varan er flutt út frá.

> [!NOTE]
> - Vörusamstilling mun ekki heppnast nema til sé verðlisti sem hefur samsvarandi gjaldmiðil.
> - Þú getur stjórnað verðskránni sem er notuð með samþættingunni með vörpun pricelevelid.name [Sjálfgildi Verðlisti (Nafn)] í Gagnasamþætting verkefninu. Inntakið verður að vera í lágstöfum eingöngu. Til dæmis yrði sjálfgildið fyrir verðlista í Sölu sem kallast „Staðlaður“: Áfangasvæði: pricelevelid.name [Sjálfgildi Verðskrá (Nafn)] og Kortategund: [ {"transformType": "Default", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

- Áður en samstilling er keyrð í fyrsta skipti þarf að fylla út Einkvæm afurð töfluna fyrir fyrirliggjandi vörur í Finance and Operations. Fyrirliggjandi vörur verða ekki samstilltar fyrr en verki er lokið.

    1. Notaðu Leit í Finance and Operations til að leita að **Fylla út töflu fyrir einkvæma afurð**.
    2. Velja skal **Mynda töflu fyrir einkvæma afurð** til að keyra verkið. Aðeins má keyra verkið einu sinni.

- Gakktu úr skugga um að nauðsynleg virðisvörpun fyrir sölueininguna á milli Finance and Operations og Sales sé til staðar í vörpun **SalesUnitSymbol** í **DefaultUnit (Name)**.
- Uppfæra skal virðisvörpun fyrir **Einingarflokk** (**defaultuomscheduleid.name**) þannig að hann passi við **Einingarflokka** í Sales.

    Sjálfgefið sniðmátsgildi er **Sjálfgefin eining**.

- Ganga skal úr skugga um að mælieining fyrir allar vörur úr Finance and Operations séu til staðar í Sales.
- Ganga skal úr skugga um að verðlisti sé til staðar í Sales fyrir alla sölugjaldmiðla vöru í Finance and Operations.
- Þegar vörur eru stofnaðar í Sales geta þær haft stöðuna **Drög** eða **Virkar**. Þessu er stjórnað í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** í Sales.

    Vörur sem hafa stöðuna **Drög** þegar þær eru búin til verður að virkja áður en hægt er að bæta við tilboðum eða sölupöntunum.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. 

> [!NOTE]
> Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar ´ru Sales í Finance and Operations.

![Sniðmátsvörpun í Gagnasamþáttara](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Tengd efnisatriði

[Prospect to cash](prospect-to-cash.md)

[Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations](accounts-template-mapping-direct.md)

[Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations](contacts-template-mapping-direct.md)

[Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations](sales-order-template-mapping-direct-two-ways.md)

[Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations](sales-invoice-template-mapping-direct.md)




