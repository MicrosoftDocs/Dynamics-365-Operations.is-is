---
title: "Stjórnun vaktar og peningaskúffu"
description: "Þessi grein útskýrir hvernig skal setja upp ot nota tvær gerðir af vöktum fyrir sölustaður í smásölu (POS) : Samnýttur og sjálfstæður. Hægt er að nota samnýtta vaktir með marga notendur á mörgum stöðum, en hægt er að nota sjálfstæða vaktir með aðeins einn starfsmann í einu."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
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
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

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

## <a name="shift-operations"></a>Vaktaaðgerðir
Hægt er að grípa til ýmissa aðgerða til að breyta stöðu vaktar eða til að auka eða minnka magn af peningum í skúffunni. Í kaflanum hér að neðan er þessum vaktaaðgerðum lýst fyrir Dynamics 365 for Retail Modern POS og sölukerfi í skýinu.

**Opna vakt**

Sölustaður krefst þess að notandi hafi virka, opna vakt til að framkvæma allar aðgerðir sem myndu leiða til fjárhagsfærslu eins og sölu-, skila- eða viðskiptavinapöntun.  

Þegar þú skráir þig inn á sölustað athugar kerfið fyrst hvort notandi sé með virka vakt í boði á núverandi afgreiðslukassa. Ef ekki, þá getur notandi valið að opna nýja vakt, halda áfram með vakt sem er til staðar eða fara í innskráningu í „utan skúffu“ sniði, fer allt eftir grunnstillingu kerfis og heimildum þess.

**Skilgreina upphafsupphæð**

Þessi aðgerð er oft fyrsta aðgerðin sem er gerð í nýlega opnaðri vakt. Notendur tilgreina upphafsupphæð reiðufjárs í skúffunni fyrir vaktina. Þetta er mikilvægt vegna þess að yfir/undir útreikningur sem á sér stað þegar vakt er lokið á við um þessa upphæð.

**Skiptimyntarfærsla**

Skiptimyntarfærslur eru ekki-sölufærslur sem eru gerðar á virkri vakt og þær auka upphæð reiðufés í skúffunni. Algengt dæmi um skiptimyntarfærslu væri að bæta við viðbótarskiptimynt í skúffuna þegar lítið er eftir af henni.

**Skiptimynt fjarlægð**

Fjarlæging skiptimyntar er ekki-sölufærslur sem eru gerðar á virkri vakt til að draga úr upphæð reiðufés í skúffunni. Þetta er oftast notað í tengslum við skiptimyntarfærslu á annarri vakt. Til dæmis, afgreiðslukassi 1 er með lítið af skiptimynt eftir, þannig að notandi á afgreiðslukassa 2 framkvæmir fjarlægingu skiptimyntar til að draga úr skúffuupphæðinni. Notandi á afgreiðslukassa 1 myndi þá framkvæma skiptimyntarfærslu til að auka upphæðina.

**Ljúka vakt**

Notendur geta frestað virkri vakt til að losa núverandi afgreiðslukassa fyrir annan notanda, eða fært vaktina yfir á annan afgreiðslukassa (þetta er oft nefnt „skúffuskipti"). 

Að fresta vaktinni kemur í veg fyrir nýjar færslur eða breytingar á vaktinni þar til haldið er áfram með hana.

**Halda vakt áfram**

Þessi aðgerð gerir notandanum kleift að halda áfram á fyrri vakt sem var frestað á afgreiðslukassa sem er ekki þegar með virka vakt.

**Talning skiptimyntar**

Talning skiptimyntar er aðgerð sem notandi gerir til að tilgreina heildarupphæð peninga sem eru nú í skúffunni, oftast áður en vakt er lokið. Þetta er gildið sem er borið saman við væntanlega vakt til að reikna út yfir/undir upphæð.

**Peningaflutningur í öryggisskáp**

Hægt er að framkvæma peningaflutning í öryggisskáp hvenær sem er á virkri vakt. Þessi aðgerð fjarlægir peninga úr skúffunni þannig að hægt sé að flytja hann á öruggari stað eins og peningaskáp í bakherbergi. Heildarupphæðin sem er skráð fyrir peningaflutning í öryggisskáp er ennþá hluti af samtölu vaktar, en þarf ekki að teljast sem hluti af talning skiptimyntar.

**Peningaflutningur í banka**

Eins og peningaflutningur í öryggisskáp, er peningaflutningur í banka einnig framkvæmdur á virkri vakt. Þessi aðgerð fjarlægir peninga af vaktinni til að undirbúa fyrir innlögn í banka.

**Loka vakt blindandi**

Að loka vakt blindandi er vakt sem er ekki lengur virk en hefur ekki verið lokað að fullu. Ekki er hægt að fara aftur í „Loka vöktum blindandi“ eins og fyrir frestaða vakt, en hægt er að framkvæma ferli eins og að tilgreina upphafsupphæð og talning skiptimyntar síðar meir eða frá öðrum afgreiðslukassa.

Að loka vöktum blindandi er oft notað til að losa afgreiðslukassa fyrir nýjan notanda eða vakt, án þess að þurfa að telja að fullu, afstemma og loka þessari vakt fyrst. 

**Loka vakt**

Þessi aðgerð reiknar samtölu vaktar, yfir/undir uppphæðir og lýkur síðan við vakt sem er virk eða lokuð blint. Ekki er hægt að halda áfram eða breyta lokuðum vöktum.  

**Stjórna vöktum**

Þessi aðgerð gerir notendum kleift að skoða allar vaktir sem eru virkar, frestaðar og sem hefur verið lokað blint fyrir verslunina. Það fer eftir heimildum notenda hvort þeir geta framkvæmt lokaferli lokunar, eins og talningu skiptimyntar og lokað vöktum fyrir vöktum sem er lokað blint. Þessi aðgerð mun einnig leyfa notendum að skoða og eyða ógildum vöktum í sjaldgæfum tilfellum þar sem skilið er við vakt í slæmu ástandi eftir að hafa skipt á milli stillinga með og án nettengingar. Þessar ógildu vaktir innihalda ekki fjárhagsupplýsingar eða færslugögn sem þarf fyrir afstemmingu. 

