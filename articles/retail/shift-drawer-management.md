---
title: "Stjórnun vaktar og peningaskúffu"
description: "Þessi grein útskýrir hvernig skal setja upp ot nota tvær gerðir af vöktum fyrir sölustaður í smásölu (POS) : Samnýttur og sjálfstæður. Hægt er að nota samnýtta vaktir með marga notendur á mörgum stöðum, en hægt er að nota sjálfstæða vaktir með aðeins einn starfsmann í einu."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b8e12f3f4c2f8f5a596c8994f2a4571d8a907062
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="shift-and-cash-drawer-management"></a>Stjórnun vaktar og peningaskúffu

[!include[banner](includes/banner.md)]


Þessi grein útskýrir hvernig skal setja upp ot nota tvær gerðir af vöktum fyrir sölustaður í smásölu (POS) : Samnýttur og sjálfstæður. Hægt er að nota samnýtta vaktir með marga notendur á mörgum stöðum, en hægt er að nota sjálfstæða vaktir með aðeins einn starfsmann í einu.

Til eru tvær gerðir af vöktum fyrir sölustaður í smásölu (POS) : sjálfstæður og samnýttur. Sjálfstæðar vaktir geta aðeins verið notaðar af einum starfskrafti í einu. Hægt er að nota samnýtta vaktir með marga notendur á mörgum stöðum. Þess vegna stofna þeir á árangursríkan hátt eina vakt fyrir marga starfskrafta í verslun.

## <a name="standalone-shifts"></a>Sjálfstæðar vaktir
Sjálfstæðar vaktir eru notaðar í hefðbundið, föst POS-aðstæður, þar sem reiðufé er stemmt af sérstaklega fyrir hvern afgreiðslukassa. Til dæmis, í stillingu matvöruverslunar, eru yfirleitt nokkrum fasta afgreiðslukassar og gjaldkeri er úthlutað á hverjum afgreiðslukassa. Í þessu tilfelli notar hvern afgreiðslukassa líklegt sjálfstæða vakt og gjaldkeri er ábyrgur fyrir skúffunni og efnislegu reiðufé á kassanum. Sjálfstæðar vaktir innifela allar aðgerðir á þeim afgreiðslukassa á meðan stendur á vakt gjaldkera. Aðgerðir getur innihaldið upphæð við opnun sem er lögð er inn á afgreiðslukassa, allar úttektir og viðbætur reiðufjár gegnum aðgerðir eins og peningaflutningur í banka og skiptimyntarfærslu, og talning skiptimyntar í lok vaktar.

### <a name="set-up-a-stand-alone-shift"></a>Setja upp sjálfstæða vakt

Sjálfstæð vakt vakt tiltekin á stigi skúffunnar. Þessu ferli er útskýrt hvernig á að setja upp sjálfstæða vaktinni á afgreiðslukassa Sölustaðar.

1.  Smelltu á **Smásala** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Forstillingar sölustaðar** &gt; **Vélbúnaðarreglur**.
2.  Veljið vélbúnaðarregluna sem á að nota fyrir sjálfstæðu vaktina.
3.  Á við **Skúffu** flýtiflipa, staðfesta að **Samnýttum skúffa vaktar** valkostur er stilltur á **Nei**.
4.  Smellt er á **Vista**.
5.  Smelltu á **Smásala** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Afgreiðslukassar**.
6.  Veljið afgreiðslukassa sem þarf sjálfstæða vakt krefst og smellið síðan á **Breyta**.
7.  Í því **vélbúnaðarreglu** svæðinu, veljið vélbúnaðarregluna sem var valin í skrefi 2.
8.  Smellt er á **Vista**.
9.  Smelltu á **Smásala** &gt; **Upplýsingatækni smásölu** &gt; **Dreifingaráætlun**.
10. Veljið í **1090** dreifingaráætlun og smelltu svo á **Keyra nú** til að samstilla breytingar á Sölustað.

### <a name="use-a-stand-alone-shift"></a>Nota sjálfstæða vakt

1.  Skráðu þig inn POS
2.  Ef engin vakt er opin veldu **Opna nýja vakt**.
3.  Farið í **Gefa upp upphafsupphæð** aðgerð, og tilgreina upphæð reiðufjár sem hefur verið bætt við skúffuna til að hefja vinnudagur.
4.  Framkvæma nokkrar færslur
5.  Við lok dagsins, veljið **Telja skiptimynt** til að gefa upp upphæð reiðufjár sem eftir er í peningaskúffu.
6.  Færið inn upphæð reiðufés og og smellið svo á **vista** til að vista talning skiptimyntar.
7.  Veljið **Loka vakt** til að loka vaktinni.

**Athugasemd:** Aðrar aðgerðir eru mögulegar á vakt, eftir því hvaða viðskiptaferli sem eru til staðar. Aðgerðirnar **Peningaflutningur í öryggisskáp**, **peningaflutningur í Banka**, og **Skiptimynt fjarlægð** er hægt að nota til að fjarlægja peninga frá á afgreiðslukassa yfir daginn eða áður en vaktinni er lokað. Ef skúffan er með lítið magn reiðufés, er **Skiptimyntarfærsla** aðgerð möguleg til notkunar til að bæta peningum við afgreiðslukassa.

## <a name="shared-shifts"></a>Samnýttar vaktir
Samnýttrar vaktar er notað í umhverfi þar sem margir gjaldkerar samnýta peningaskúffu eða nokkrar peningaskúffur í gegnum vinnudagur. Yfirleitt eru samnýttrar vaktar notað í aðstæðum þar sem notaðir eru færanlegir sölustaðir. Í færanlegu umhverfi, er Hver gjaldkeri ekki úthlutað á og ábyrgur fyrir eina peningaskúffu. Þess í stað verða allir gjaldkerar að geta framkvæmt sölu og bæt reiðufé í hvaða peningaskúffu sem er nálægust þeim. Í þessu dæmi, eru peningaskúffur samnýttar á milli gjaldkerar og um leið teknar með í samnýttrar vaktar. Allar peningaskúffur í samnýttrar vaktar eru teknar með í sama vaktinni vegna verkþætti sem tengjast stjórnun reiðufjár fyrir þá vakt. Þess vegna skal upphafsupphæð fyrir vaktina að innifela samtala allra reiðufjár í öllum peningaskúffur sem eru innifaldar í samnýttrar vaktar. Þess vegna mun talning skiptimyntar vera samtala allra reiðufjár í öllum peningaskúffur sem eru innifaldar í samnýttrar vaktar. **Athugasemd:** Aðeins er hægt að hafa eina samnýtta vakt opna í hverri verslun í einu. Hægt er að nota samnýtta vaktir og sjálfstæðar vaktir í sama verslunarinnar.

### <a name="set-up-a-shared-shift"></a>Setja upp samnýttar vaktir

1.  Smelltu á **Smásala** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Forstillingar sölustaðar** &gt; **Vélbúnaðarreglur**.
2.  Veljið vélbúnaðarregluna sem á að nota fyrir sjálfstæðu vaktina.
3.  Á við **Skúffu** flýtiflipa, skal stilla **Samnýttum skúffa vaktar** valkostur á **Já**.
4.  Smellt er á **Vista**.
5.  Smelltu á **Smásala** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Afgreiðslukassar**.
6.  Veljið afgreiðslukassa sem þarf samnýtta vakt og smellið síðan á **Breyta**.
7.  Í því **vélbúnaðarreglu** svæðinu, veljið vélbúnaðarregluna sem var valin í skrefi 2.
8.  Smellt er á **Vista**.
9.  Smelltu á **Smásala** &gt; **Upplýsingatækni smásölu** &gt; **Dreifingaráætlun**.
10. Veljið í **1090** dreifingaráætlun og smelltu svo á **Keyra nú** til að samstilla breytingar á Sölustað.

### <a name="use-a-shared-shift"></a>Nota samnýttra vakt.

1.  Skráðu þig inn POS
2.  Ef Sölustað er ekki enn tengt við vélbúnaðarstöð, veljið **aðgerð utan skúffu**, og því næst **Velja vélbúnaðarstöð** aðgerð til að virkja vélbúnaðarstöð fyrir samnýttrar vaktar. Þetta skref er nauðsynlegt aðeins í fyrsta sinn sem afgreiðslukassa er bætt við umhverfi samnýttrar vaktar.
3.  Skrá út af Sölustað og síðan skrá aftur inn.
4.  Veljið **Stofna nýja vakt**.
5.  Veljið **Gefa upp upphafsupphæð**
6.  Færið inn upphafsupphæð allar peningaskúffur í verslunarinnar sem eru hluti af samnýttrar vaktar og smellið síðan á **Vista**.
    -   Til að bæta við hluta upphafsupphæðar í  hverja síðari peningaskúffu skal nota **Velja vélbúnaðarstöð** aðgerð til að gera vélbúnaðarstöðina virka.
    -   Til að bæta skúffu á tiltekna peningaskúffu skal nota **Opna skúffu** aðgerð.
    -   Halda áfram þartil allar peningaskúffur í samnýttrar vaktar hafa þeirra hluta upphafsupphæðar.

7.  Opna hverja peningaskúffu í lok dags og fjarlægja reiðufjár.
8.  eftir reiðufjár hefur verið fjarlægð úr síðasta peningaskúffu skal telja allt reiðufjár úr öllum peningaskúffur.
9.  Nota skal **telja skiptimynd** aðgerð til að telja fram heildarupphæð reiðufjár úr öllum peningaskúffur sem eru innifaldar í samnýttrar vaktar.
10. Nota skal **Loka vakt** aðgerð til að loka samnýttrar vaktar.





