---
title: "Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations"
description: "Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölupöntunar beint úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölupöntunar beint úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales. Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Finance and Operations og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.

[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations:

- **Heiti sniðmátsins í Gagnaflutningi:** Sölupantanir (Fin og Ops í Sales) - Beint
- **Heiti verksins í gagnasamþættingarverki:**

    - OrderHeader
    - OrderLine

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstillingar sölureikningshausa og línum geta átt sér stað:

- Vörur (Fin og Ops til Sales) - bein
- Reikningar (Sales við Fin and Ops) - Beint (ef notað)
- Tengiliðir við viðskiptavini (Sales við Fin og Ops) - Beint (ef notað)

## <a name="entity-set"></a>Einingastamstæða

| Finance and Operations  | Sölur             |
|-------------------------|-------------------|
| Hausar CDS-sölupöntunar | SalesOrders       |
| CDS sölupöntunarlínur   | SalesOrderDetails |

## <a name="entity-flow"></a>Einingaflæði

Sölupantanir eru búnar til í Finance and Operations og samstilltar við Sales.

Síur í sniðmáti auðvelda að aðeins viðeigandi sölupantanir séu innifaldar í samstillingu:

- Á sölupöntun þarf bæði viðskiptavinurinn sem pantar og sá sem reikningsfært að eiga uppruna sinn í Sales til að vera teknir með í samstillingu. Í Finance and Operations er reitirnir **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** notaðir til að rekja samstillingu í gagnaeiningum.
- Sölupöntun í Finance and Operations verður að vera staðfest. Aðeins staðfestar sölupantanir eða sölupantanir með hærri vinnslustöðu, til dæmis, **Sent** eða **Reikningsfært**, eru samstilltar við Sales.
- Eftir að sölupöntun er búin til eða henni breytt verður að keyra runuvinnsluna **Reikna heildarsölu** í Finance and Operations. Aðeins sölurekningar þar sem sölutölur eru reiknaðar verður samstilltir við Sales.

> [!NOTE]
> Eins og er er skattur tengdur gjöldum á sölupöntunarhaus er ekki tekinn með í samstillingu úr Finance and Operations í Sales. Sales styður ekki skattupplýsingar á hausstiginu. Hinsvegar er skattur sem tengist gjöldum á línustigi er innifalinn í samstillingu.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Nýjum reitum hefur verið bætt við eininguna **Pöntun** og birtist á síðunni:

- **Er viðhaldið utanfrá** - Stillið á **Já** þegar pöntunin er úr Finance and Operations.
- **Vinnslustaða** - Þessi reitur sýnir vinnslustöðu pantanar í Finance and Operations. Eftirtalin gildi eru tiltæk:

    - Í gangi
    - Staðfest
    - Fylgiseðill
    - Reikningsfært
    - Tekið til
    - Tínt að hluta
    - Tekið til að hluta
    - Sent
    - Afhent að hluta
    - Reikningsfært að hluta
    - Afturkallað

Stillingin **Er aðens með utanaðkomandi vörur** er notuð í öðrum sviðsmyndum sölupantana (til dæmis samstillingu úr Sales í Finance and Operation) til að halda utan um það hvort sölupöntun sé eingöngu með Vörur sem viðhaldið er utanfrá. Ef sölupöntun inniheldur aðeins utanaðkomandi vörur er vörunum viðhaldið í Finance and Operations. Þetta tryggir að þú reynir ekki að virkja og samstilla sölupöntunarlínur með vörum sem eru óþekktar Finance and Operations.

**Stofna reikning**, **Hætta við pöntun**, **Endurreikna**, **Sækja vörur** og **Leita að aðsetri** hnapparnir á síðunni **Sölupöntun** síðan er falin fyrir pantanir sem er viðhaldið að utan, þar sem reikningar verða stofnaðir í Finance and Operations og samstilltir við Sales. Ekki er hægt að breyta pöntunarsíðunni vegna þess að sölupantanir verða samstilltar úr Finance and Operations.

Staða sölupöntunar verður áfram **Virk** til að tryggja að gjöld úr Finance and Operations geti flætt í sölupöntun í Sales. Til að stjórna þessu er sjálfgefið **Statecode \[Status\]** stillt á **Virkt** í gagnasamþættingarferlinu.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en sölupantanir eru samstilltar er mikilvægt að eftirfarandi stillingar séu uppfærðar í kerfunum.

### <a name="setup-in-sales"></a>Uppsetning í Sales

- Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á. Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki. Ef teymi hefur ekki stjórnandaaðgang, þegar þú keyrir verkefnið úr Gagnasamþáttara færðu villuskilaboð sem segja að aðalteymi vantar.

    Undir **Stillingar** > **Öryggi** > **Teymi**, velurðu viðkomandi teymi, smellir á **Stjórna hlutverkum** og velur hlutverk með viðkomandi heimildum, t.d. **Kerfisstjóri**.

- Farið í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:

    - **Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.
    - **Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.

### <a name="setup-in-finance-and-operations"></a>Uppsetning Finance and Operations

Stilltu **Sala og markaðssetning** > **Reglubundin verkefni** > **Reikna heildarsölu** til að keyra sem runuvinnsla. Stilltu **Reikna út samtölu sölupantana** valkostinn á **Já**. Þetta skref er mikilvægt þar sem aðeins sölurekningar þar sem sölutölur eru reiknaðar verður samstilltir við Sales. Tíðni runuvinnslunnar ætti að vera í samræmi við tíðni samstillingu sölupöntunar.

### <a name="setup-in-the-data-integration-project"></a>Setja upp gagnasamþættingarverk

#### <a name="salesheader-task"></a>SalesHeader verkefni

- Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **InvoiceCountryRegionId** to **BillingAddress\_land** og fyrir **DeliveryCountryRegionId** í **DeliveryAddress\_land**.

    Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð.

- Verðlisti er nauðsynlegur til að búa til pantanir í Sales. Uppfæra gildarvörpun í **pricelevelid.name \[Heiti verðlista\]** í verðlistann sem er notaður í Sales eftir gjaldmiðli. Hægt er að nota sjálfgefinn verðlista fyrir einn gjaldmiðil. Einnig er hægt að nota gildarvörpun ef verðlistar eru til staðar í mörgum gjaldmiðlum.

    Sjálfgefið sniðmátsgildi fyrir **pricelevelid.name \[Heiti verðlista\]** er **CRM Service USA (dæmi)**.

#### <a name="salesline-task"></a>SalesLine verkefni

- Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **DeliveryCountryRegionId** to **DeliveryAddress\_land**.

    Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð.

- Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** í Finance and Operations sé til staðar.

    Sniðmátsgildi með gildisvörpun er skiglreint fyrir **SalesUnitSymbol** í **Magn\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Template mapping in Data integration

> [!NOTE]
> Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. 

> [!NOTE]
> Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar ´ru Sales í Finance and Operations.

### <a name="orderheader"></a>OrderHeader

![Sniðmátsvörpun í Gagnasamþáttara](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Sniðmátsvörpun í Gagnasamþáttara](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Tengd efnisatriði

[Prospect to cash](prospect-to-cash.md)

[Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations](accounts-template-mapping-direct.md)

[Samstilla vörur beint úr Finance and Operations við vörur í Sales](products-template-mapping-direct.md)

[Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations](contacts-template-mapping-direct.md)

[Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations](sales-invoice-template-mapping-direct.md)




