---
title: Samstilling sölupantana beint á milli Sales og Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem notuð eru til að keyra samstillingu sölupantana beint á milli Dynamics 365 Sales og Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 05/09/2019
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 9e95ba361bddf4e43b205fe580bb6f4a91dd88248a0c059ad65e66ef07de83c0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753229"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Samstilling sölupantana beint á milli Sales og Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem notuð eru til að keyra samstillingu sölupantana beint á milli Dynamics 365 Sales og Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales. Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna fyrir reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.

[![Gagnaflæði í Prospect to cash.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu sölupöntunar beint milli Sales og Supply Chain Management:

- **Heiti sniðmátsins í Gagnaflutningi:** 

    - Sölupantanir (Sales til Supply Chain Management) - Beint
    - Sölupantanir (Supply Chain Management til Sales) - Beint

- **Heiti verksins í gagnasamþættingarverki:**

    - OrderHeader
    - OrderLine

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstillingar sölureikningshausa og línum geta átt sér stað:

- Afurðir (Supply Chain Management itl Sales) - Beint
- Lyklar (Sales til Supply Chain Management) - Bein (ef notað)
- Tengiliðir við viðskiptavini (Sales til Supply Chain Management) - Beint (ef notað)

## <a name="entity-set"></a>Einingastamstæða

| Birgðakeðjustjórnun  | Sala             |
|-------------------------|-------------------|
| Dataverse hausar sölupöntunar | SalesOrders       |
| Dataverse sölupöntunarlínur   | SalesOrderDetails |

## <a name="entity-flow"></a>Einingaflæði

Sölupantanir eru búnar til í Sales og samstilltar við Supply Chain Management þegar **Keyra verk** er keyrt fyrir verk byggt á sniðmátinu **Sölupantanir (Sales í Supply Chain Management) - Beint**. Þú getur aðeins virkjað og samstillt pantanir úr Sales ef allar **Pöntunarvörur** samanstanda af vörum sem eru utanaðkomandi. Þess vegna geta ekki vörur ekki verið innskriftarvörur. Eftir að pöntunin er virk, verður sölupöntunin aðeins með lesaðgangi í notendaviðmótinu (UI). Á þeim tímapunkti eru uppfærslur gerðar úr Supply Chain Management. Eftir að sölutilboð hefur stöðuna **Staðfest** er verkefnið byggt á **Sölupöntunum (Supply Chain Management í Sales) - Beint** sniðmát er hægt að nota til að samstilla uppfærslur eða uppfyllingarstöður úr Supply Chain Management í Sales.

Ekki þarf að stofna pantanir í Sales. Hægt er að stofna nýjar sölupantanir í Supply Chain Management í stað þess. Eftir að sölutilboð hefur stöðuna **Staðfest** er það samstillt við Sales eins og lýst er í fyrri málsgrein.

Í Supply Chain Management hjálpa síur í sniðmáti að aðeins viðeigandi sölupantanir séu innifaldar í samstillingu:

- Á sölupöntun þarf bæði viðskiptavinurinn sem pantar og sá sem reikningsfært að eiga uppruna sinn í Sales til að vera teknir með í samstillingu. Í Supply Chain Management er dálkarnir **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** notaðir til að sía sölupantanir úr gagnaeiningum.
- Sölupöntun í Supply Chain Management verður að vera staðfest. Aðeins staðfestar sölupantanir eða sölupantanir með hærri vinnslustöðu, til dæmis, **Sent** eða **Reikningsfært**, eru samstilltar við Sales.
- Eftir að sölupöntun er búin til eða henni breytt verður að keyra runuvinnsluna **Reikna heildarsölu** í Supply Chain Management. Aðeins sölurekningar þar sem sölutölur eru reiknaðar verður samstilltir við Sales.

## <a name="freight-tax"></a>Flutningsskattar

Sales styður ekki skatt á hausstiginu vegna þess að skattur er vistaður á línustigi. Til að styðja við skatta á hausstigi úr Supply Chain Management, svo sem flutningsskatt, samstillir kerfið skatta við Sales sem innritað vöru sem heitir **Flutningsskattar**, og hefur skattfjárhæðina úr Supply Chain Management. Þannig er hægt að nota staðlaða verðútreikninguna í Sales fyrir samtölu, jafnvel þótt skattur sé í upphafi úr hausstigi Supply Chain Management.

## <a name="discount-calculation-and-rounding"></a>Afsláttarútreikningur og sléttun

Útreikningur útreikningslíkansins í Sales er frábrugðin útreikningslíkaninu í Supply Chain Management. Í Supply Chain Management má endanlega afsláttarverð á sölulínu vera niðurstaða af samsetningu af afslætti og afsláttarhlutföllum. Ef lokaafsláttarupphæð er skipt eftir magni sem er á línunni, getur sléttun átt sér stað. Hins vegar er sléttunin ekki talin með ef afsláttarupphæð á einingu er samstillt við Sales. Til að tryggja að öll afsláttarupphæðin úr sölulínu í Supply Chain Management sé rétt samstillt við Sales verður heildarupphæðin að vera samstillt án þess að vera skipt eftir líumagni. Þess vegna verður þú að skilgreina **Afsláttarreikningsaðferðina** sem **Línuvara** í Sales.

Þegar sölupöntunarlína er samstillt úr Sales í Supply Chain Management er heildarlínuafsláttarupphæðin notuð. Vegna þess að Supply Chain Management hefur engan reit sem geymir heildarfjárhæðina fyrir línu, er upphæðinni skipt niður með magni og geymt á reitnum **Línuafsláttur**. Öll frávik sem eiga sér stað eru vistuð í **Sölulaun** á sölulínunni.

### <a name="example"></a>Dæmi

**Samstilling úr Sales við Supply Chain Management**

- **Sala:** Magn= 3, línuafsláttur = $10,00
- **Birgðastjórnun:** Magn = 3, línuafsláttarupphæð = $3,33, sölugjald = - $ 0,01 

**Samstilling úr Supply Chain Management við Sales**

- **Birgðastjórnun:** Magn = 3, línuafsláttarupphæð = $3,33, sölugjald = - $ 0,01
- **Sala:** magn = 3, línuafsláttur = (3 × $3,33) + $0,01 = $10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Nýjum dálkum hefur verið bætt við töfluna **Pöntun** og birtast á síðunni:

- **Er viðhaldið utanfrá** - Stillið á **Já** þegar pöntunin er úr Supply Chain Management.
- **Vinnslustaða** - Þessi dálkur sýnir vinnslustöðu pantanar í Supply Chain Management. Eftirtalin gildi eru tiltæk:

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

**Er aðens með utanaðkomandi vörur** stillingin er notuð meðan á virkjun pöntunar stendur til að fylgjast stöðugt með því hvort sölupöntun samanstendur aðeins af utanaðkomandi vörum. Ef sölupöntun inniheldur aðeins utanaðkomandi vörur er vörunum viðhaldið í Supply Chain Management. Þetta tryggir að þú virkjar ekki og samstillir sölupöntunarlínur með vörum sem eru óþekktar Supply Chain Management.

**Stofna reikning**, **Hætta við pöntun**, **Endurreikna**, **Sækja vörur** og **Leita að aðsetri** hnapparnir á síðunni **Sölupöntun** síðan er falin fyrir pantanir sem er viðhaldið að utan, þar sem reikningar verða stofnaðir í Supply Chain Management og samstilltir við Sales. Ekki er hægt að breyta þessum pöntunum vegna þess að sölupantanir verða samstilltar úr Supply Chain Management eftr virkjun.

Staða sölupöntunar verður áfram **Virk** til að tryggja að gjöld úr Supply Chain Management geti flætt í sölupöntun í Sales. Til að stjórna þessu er sjálfgefið **Statecode \[Status\]** stillt á **Virkt** í gagnasamþættingarferlinu.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en sölupantanir eru samstilltar er mikilvægt að eftirfarandi stillingar séu uppfærðar í kerfunum.

### <a name="setup-in-sales"></a>Uppsetning í Sales

- Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á. Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki. Ef teymið hefur ekki stjórnendaaðgang þegar þú keyri verkefnið úr gagnasamþáttara færðu villuskilaboð sem segir að aðalteymi vantar.

    Undir **Stillingar**&gt;**Öryggi**&gt;**Teymi**, velurðu viðkomandi teymi, smellir á **Stjórna hlutverkum** og velur hlutverk með viðkomandi heimildum, t.d. **Kerfisstjóri**.

- Til að tryggja réttan útreikning á afslætti bæði í Sales og Supply Chain Management verður **Reikningsaðferð reikningsafsláttar** að vera stillt á **Línuatriði**.
- Farið í **Stillingar** &gt; **Stjórnun** &gt; **Kerfisstillingar** &gt; **Sala** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:

    - **Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.
    - **Reikningsaðferð reikningsafslátta** dálkurinn er stilltur á **Línuatriði**.

### <a name="setup-in-supply-chain-management"></a>Uppsetning í Supply Chain Management

- Stilltu **Sala og markaðssetning**&gt;**Reglubundin verkefni**&gt;**Reikna heildarsölu** til að keyra sem runuvinnsla. Stilltu **Reikna út samtölu sölupantana** valkostinn á **Já**. Þetta skref er mikilvægt þar sem aðeins sölurekningar þar sem sölutölur eru reiknaðar verður samstilltir við Sales. Tíðni runuvinnslunnar ætti að vera í samræmi við tíðni samstillingu sölupöntunar.

Ef samþætting vinnupöntunar er einnig notuð er nauðsynlegt að setja upp söluupprunann. Söluuppruninn er notaður til að greina sölupantanir í Supply Chain Management sem voru stofnaðar út frá vinnupöntunum í Field Service. Þegar sölupöntun hefur söluuppruna af gerðinni **Samþætting vinnupöntunar** birtist reiturinn **Ytri staða vinnupöntunar** á sölupöntunarhausnum. Til viðbótar tryggir söluuppruni að sölupantanir sem voru stofnaðar úr vinnupöntunum í Field Service séu síaðar út á meðan samstilling stendur yfir á sölupöntunum Supply Chain Management við Field Service.

1. Farðu í **Sala og markaðssetning** \> **Uppsetning** \> **Sölupantanir** \> **Söluuppruni**.
2. Veldu **Nýr** til að búa til nýjan söluuppruna.
3. Í dálkinn **Söluuppruni** skal slá inn heiti söluuppruna, t.d. **SalesOrder**.
4. Í dálkinum **Lýsing** skal færa inn lýsingu, t.d. **Sölupöntun úr Sales**.
5. Veldu gátreitinn **Úthlutun upprunagerðar**.
6. Stillið dálkinn **Upprunagerð sölu** á **Samþætting sölupöntunar**.
7. Veljið **Vista**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Uppsetning í sölupöntunum (Sales við Supply Chain Management) - Beint Gagnasamþættingarverk

- Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Shipto\_land** í **DeliveryAddressCountryRegionISOCode**. Þú getur gert autt að sjálfgefnu gildi á gildisvörpun til að koma í veg fyrir að þú þurfir að slá inn land fyrir innlendar pantanir. Stilltu vinstri hliðina á ‚Autt' og stilltu hægri hliðina að viðkomandi landi eða svæði.

    Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð, og þar sem ‚Autt' = US.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Uppsetning í sölupöntunum (Supply Chain Management við Sales) - Beint Gagnasamþættingarverk

#### <a name="salesheader-task"></a>SalesHeader verkefni

- Verðlisti er nauðsynlegur til að búa til pantanir í Sales. Uppfæra gildarvörpun í **pricelevelid.name \[Heiti verðlista\]** í verðlistann sem er notaður í Sales eftir gjaldmiðli. Hægt er að nota sjálfgefinn verðlista fyrir einn gjaldmiðil. Einnig er hægt að nota gildarvörpun ef verðlistar eru til staðar í mörgum gjaldmiðlum.

    Sjálfgefið sniðmátsgildi fyrir **pricelevelid.name \[Heiti verðlista\]** er **CRM Service USA (dæmi)**.

#### <a name="salesline-task"></a>SalesLine verkefni

- Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** í Supply Chain Management sé til staðar.
- Gangið úr skugga um að nauðsynelgar einingar séu skilgreindar í Sales.

    Sniðmátsgildi með gildisvörpun er skilgreint fyrir **SalesUnitSymbol** í **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

> [!NOTE]
> **Greiðsluskilmálar**, **Farmskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefinni vörpun. Til að varpa þessum dálkum, verður að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem taflan er samstillt á milli.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.

> [!NOTE]
> Vörpunin sýnir hvaða dálkupplýsingar verða samstilltar úr Sales í Supply Chain Management eða úr Supply Chain Management í Sales.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Sölupantanir (Supply Chain Management til Sales) - Beint: OrderHeader

[![Sniðmátsvörpun í Gagnasamþættingu.](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Sölupantanir (Supply Chain Management til Sales) - Beint: OrderLine

[![Sniðmátsvörpun í Gagnasamþættingu.](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Sölupantanir (Sales til Supply Chain Management) - Beint: OrderHeader

[![Sniðmátsvörpun í Gagnasamþættingu.](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Sölupantanir (Sales til Supply Chain Management) - Beint: OrderLine

[![Sniðmátsvörpun í Gagnasamþættingu.](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Tengd efnisatriði

[Viðfang til sjóðstreymis](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]