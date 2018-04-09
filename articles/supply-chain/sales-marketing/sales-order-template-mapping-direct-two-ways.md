---
title: "Samstilling sölupöntunar beint úr Sales við Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem notuð eru til að keyra samstillingu sölupantana beint á milli Microsoft Dynamics 365 for Sales og Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e26244ffc380291a40edfbd2c2cb5911b0d8b3cb
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Samstilling sölupöntunar beint úr Sales við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem notuð eru til að keyra samstillingu sölupantana beint á milli Microsoft Dynamics 365 for Sales og Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu sölupöntunar beint milli Sales og Finance and Operations:

- **Heiti sniðmátsins í Gagnaflutningi:** 

    - Sölupantanir (Sales við Fin og Ops) - Beint
    - Sölupantanir (Fin og Ops í Sales) - Beint

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

Sölupantanir eru búnar til í Sales og samstilltar við Finance and Operations þegar **Keyra verk** er keyrt fyrir verk byggt á **Sölupantanir (Sales í Fin og Ops) - Beint** sniðmát. Þú getur aðeins virkjað og samstillt pantanir úr Sales ef allar **Pöntunarvörur** samanstanda af vörum sem eru utanaðkomandi. Þess vegna geta ekki vörur ekki verið innskriftarvörur. Eftir að pöntunin er virk, verður sölupöntunin aðeins með lesaðgangi í notendaviðmótinu (UI). Á þeim tímapunkti eru uppfærslur gerðar úr Finance and Operations. Eftir að sölutilboð hefur stöðuna **Staðfest** er verkefnið byggt á **Sölupöntunum (Fin og Ops í Sales) - Beint** sniðmát er hægt að nota til að samstilla uppfærslur eða uppfyllingarstöður úr Finance and Operations í Sales.

Ekki þarf að stofna pantanir í Sales. Hægt er að stofna nýjar sölupantanir í Finance and Operations í stað þess. Eftir að sölutilboð hefur stöðuna **Staðfest** er það samstillt við Sales eins og lýst er í fyrri málsgrein.

Í Finance and Operations hjálpa síur í sniðmáti að aðeins viðeigandi sölupantanir séu innifaldar í samstillingu:

- Á sölupöntun þarf bæði viðskiptavinurinn sem pantar og sá sem reikningsfært að eiga uppruna sinn í Sales til að vera teknir með í samstillingu. Í Finance and Operations er reitirnir **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** notaðir til að sía sölupantanir úr gagnaeiningum.
- Sölupöntun í Finance and Operations verður að vera staðfest. Aðeins staðfestar sölupantanir eða sölupantanir með hærri vinnslustöðu, til dæmis, **Sent** eða **Reikningsfært**, eru samstilltar við Sales.
- Eftir að sölupöntun er búin til eða henni breytt verður að keyra runuvinnsluna **Reikna heildarsölu** í Finance and Operations. Aðeins sölurekningar þar sem sölutölur eru reiknaðar verður samstilltir við Sales.

## <a name="freight-tax"></a>Flutningsskattar

Sales styður ekki skatt á hausstiginu vegna þess að skattur er vistaður á línustigi. Til að styðja við skatta á hausstigi úr Finance and Operations, svo sem flutningsskatt, samstillir kerfið skatta við Sales sem innritað vöru sem heitir **Flutningsskattar**, og hefur skattfjárhæðina úr Finance and Operations. Þannig er hægt að nota staðlaða verðútreikninguna í Sales fyrir samtölu, jafnvel þótt skattur sé í upphafi úr hausstigi Finance and Operations.

## <a name="discount-calculation-and-rounding"></a>Afsláttarútreikningur og sléttun

Útreikningur útreikningslíkansins í Sales er frábrugðin útreikningslíkaninu í Finance and Operations. Í Finance and Operations má endanlega afsláttarverð á sölulínu vera niðurstaða af samsetningu af afslætti og afsláttarhlutföllum. Ef lokaafsláttarupphæð er skipt eftir magni sem er á línunni, getur sléttun átt sér stað. Hins vegar er sléttunin ekki talin með ef afsláttarupphæð á einingu er samstillt við Sales. Til að tryggja að öll afsláttarupphæðin úr sölulínu í Finance and Operations sé rétt samstillt við Sales verður heildarupphæðin að vera samstillt án þess að vera skipt eftir líumagni. Þess vegna verður þú að skilgreina **Afsláttarreikningsaðferðina** sem **Línuvara** í Sales.

Þegar sölupöntunarlína er samstillt úr Sales í Finance and Operations er heildarlínuafsláttarupphæðin notuð. Vegna þess að Finance and Operations hefur engan reit sem geymir heildarfjárhæðina fyrir línu, er upphæðinni skipt niður með magni og geymt á reitnum **Línuafsláttur**. Öll frávik sem eiga sér stað eru vistuð í **Sölulaun** á sölulínunni.

### <a name="example"></a>Dæmi

**Samstilling frá Sales í Finance and Operations**

- **Sala:** Magn= 3, línuafsláttur = $10,00
- **Finance and Operations:** Magn = 3, línuafsláttur = $3,33, sölulaun = -$0,01 

**Samstilla Finance and Operations í Sales**

- **Finance and Operations:** Magn = 3, línuafsláttur = $3,33, sölulaun = -$0,01
- **Sala:** magn = 3, línuafsláttur = (3 × $3,33) + $0,01 = $10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Nýjum reitum hefur verið bætt við eininguna **Pöntun** og birtist á síðunni:

- **Er viðhaldið utanfrá** - Stillið á **Já** þegar pöntunin er úr Finance and Operations.
- **Vinnslustaða** - Þessi reitur sýnir vinnslustöðu pantanar í Finance and Operations. Eftirtalin gildi eru tiltæk:

    - **Drög** - upphafleg staða þegar pöntun er stofnuð í Sales. Í Sales má aðeins breyta pöntunum með þessari vinnslustöðu.
    - **Virk** - Staða eftir að pöntun er virkjuð í Sales með því að nota hnappinn **Virkja**.
    - **Staðfest**
    - **Fylgiseðill**
    - **Reikningsfært**
    - **Tekið til**
    - **Tínt að hluta**
    - **Tekið til að hluta**
    - **Sent**
    - **Afhent að hluta**
    - **Reikningsfært að hluta**
    - **Afturkallað**

**Er aðens með utanaðkomandi vörur** stillingin er notuð meðan á virkjun pöntunar stendur til að fylgjast stöðugt með því hvort sölupöntun samanstendur aðeins af utanaðkomandi vörum. Ef sölupöntun inniheldur aðeins utanaðkomandi vörur er vörunum viðhaldið í Finance and Operations. Þetta tryggir að þú virkjar ekki og samstillir sölupöntunarlínur með vörum sem eru óþekktar Finance and Operations.

**Stofna reikning**, **Hætta við pöntun**, **Endurreikna**, **Sækja vörur** og **Leita að aðsetri** hnapparnir á síðunni **Sölupöntun** síðan er falin fyrir pantanir sem er viðhaldið að utan, þar sem reikningar verða stofnaðir í Finance and Operations og samstilltir við Sales. Ekki er hægt að breyta þessum pöntunum vegna þess að sölupantanir verða samstilltar úr Finance and Operations eftr virkjun.

Staða sölupöntunar verður áfram **Virk** til að tryggja að gjöld úr Finance and Operations geti flætt í sölupöntun í Sales. Til að stjórna þessu er sjálfgefið **Statecode \[Status\]** stillt á **Virkt** í gagnasamþættingarferlinu.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en sölupantanir eru samstilltar er mikilvægt að eftirfarandi stillingar séu uppfærðar í kerfunum.

### <a name="setup-in-sales"></a>Uppsetning í Sales

- Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á. Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki. Ef teymið hefur ekki stjórnendaaðgang þegar þú keyri verkefnið úr gagnasamþáttara færðu villuskilaboð sem segir að aðalteymi vantar.

    Undir **Stillingar**&gt;**Öryggi**&gt;**Teymi**, velurðu viðkomandi teymi, smellir á **Stjórna hlutverkum** og velur hlutverk með viðkomandi heimildum, t.d. **Kerfisstjóri**.

- Til að tryggja réttan útreikning á afslætti bæði í Sales og Finance and Operations verður **Reikningsaðferð reikningsafsláttar** að vera stillt á **Línuatriði**.
- Farið í **Stillingar**&gt;**Stjórnun**&gt;**Kerfisstillingar**&gt;**Sales** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:

    - **Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.
    - **Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.

### <a name="setup-in-finance-and-operations"></a>Uppsetning Finance and Operations

- Stilltu **Sala og markaðssetning**&gt;**Reglubundin verkefni**&gt;**Reikna heildarsölu** til að keyra sem runuvinnsla. Stilltu **Reikna út samtölu sölupantana** valkostinn á **Já**. Þetta skref er mikilvægt þar sem aðeins sölurekningar þar sem sölutölur eru reiknaðar verður samstilltir við Sales. Tíðni runuvinnslunnar ætti að vera í samræmi við tíðni samstillingu sölupöntunar.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Uppsetning í sölupöntunum (Sales við Fin og Ops) - Beint Gagnasamþættingarverk

- Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Shipto\_land** í **DeliveryAddressCountryRegionISOCode**. Þú getur gert autt að sjálfgefnu gildi á gildisvörpun til að koma í veg fyrir að þú þurfir að slá inn land fyrir innlendar pantanir. Stilltu vinstri hliðina á ‚Autt' og stilltu hægri hliðina að viðkomandi landi eða svæði.

    Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð, og þar sem ‚Autt' = US.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Uppsetning í Sölupantanir (Fin og Ops við Sales) - Beint Gagnasamþættingarverk

#### <a name="salesheader-task"></a>SalesHeader verkefni

- Verðlisti er nauðsynlegur til að búa til pantanir í Sales. Uppfæra gildarvörpun í **pricelevelid.name \[Heiti verðlista\]** í verðlistann sem er notaður í Sales eftir gjaldmiðli. Hægt er að nota sjálfgefinn verðlista fyrir einn gjaldmiðil. Einnig er hægt að nota gildarvörpun ef verðlistar eru til staðar í mörgum gjaldmiðlum.

    Sjálfgefið sniðmátsgildi fyrir **pricelevelid.name \[Heiti verðlista\]** er **CRM Service USA (dæmi)**.

#### <a name="salesline-task"></a>SalesLine verkefni

- Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** í Finance and Operations sé til staðar.
- Gangið úr skugga um að nauðsynelgar einingar séu skilgreindar í Sales.

    Sniðmátsgildi með gildisvörpun er skilgreint fyrir **SalesUnitSymbol** í **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

> [!NOTE]
> Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.

> [!NOTE]
> Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar úr Sales í Finance and Operations eða úr Finance and Operations í Sales.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Sölupantanir (Fin og Ops við Sales) - Beint: OrderHeader

[![Sniðmátsvörpun í Gagnasamþættingu](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Sölupantanir (Fin and Ops við Sales) - Beint: OrderLine

[![Sniðmátsvörpun í Gagnasamþættingu](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Sölupantanir (Sales við Fin og Ops) - Beint: OrderHeader

[![Sniðmátsvörpun í Gagnasamþættingu](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Sölupantanir (Sales við Fin og Ops) - Beint: OrderLine

[![Sniðmátsvörpun í Gagnasamþættingu](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Tengd efnisatriði

[Prospect to cash](prospect-to-cash.md)

