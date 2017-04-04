---
title: "Sundurliðanir verkþátta"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 1666691ec122e65128b74056817a0c40551f49b5
ms.lasthandoff: 03/31/2017


---

# <a name="work-breakdown-structures"></a>Sundurliðanir verkþátta



Sundurliðanir verkþátta Sundurliðun verkþátta (WBS) er lýsing á vinnu sem verður að gera fyrir verk. Það er stigveldi af verkum sem táknar skilning verkhópsins á samsetningu vinnu og á stærð, kostnaði og tímalengd hvers efnisþáttar eða verks. WBS hefur þrennan megintilgang:

-   Lýsa sundurliðun eða samsetningu vinnu í verkum.
-   Tímasettu verkþáttinn.
-   Meta kostnað fyrir hvert verkefni.

Stig upplýsinga í WBS fer eftir því stigi nákvæmni sem krafist er í mati og stigi rakningar sem er krafist gegn þessu mati. Verk sem hafa mjög lág vikmörk fyrir verðskrið í áætlun eða kostnaði krefjast yfirleitt ítarlegra WBS og nákvæm rakning á framvindu vinnu og kostnaði á móti WBS. Þessi tegund verks er algeng í byggingar- og verkfræðiatvinnugreinum. 

Aftur á móti eru verkefni í atvinnugreinum eins og miðlun og auglýsingum, hugbúnaði og upplýsingatæknitölvukerfum yfirleitt einstök og framleiðni er í samræmi við reynslu og hæfni einstaklingsins sem framkvæmir verkið. Þess vegna nota þessar atvinnugreinar WBS til að fá áætlun á stærð verksins, en ekki til að rekja sundurliðaða framvindu verksins. 

Uppbygging WBS er vinnslufrekt ferli sem er yfirleitt gert yfir langt tímabil og sem krefst samvinnu og upplýsinga frá víðtækum hópi einstaklinga. Þetta efnisatriði lýsir því hvernig hægt er að nota viðbætur WBS í Microsoft Dynamics 365 fyrir Aðgerðir eftir þörfum fyrir mat og rakningu.

## <a name="prerequisites-for-creating-a-wbs"></a>Forkröfur fyrir stofnun WBS
Til að stofna WBS, verður að vera hægt að stofna vinnuáætlun og meta kostnað vinnu.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Skilyrði fyrir stofnun vinnuáætlunar

Til nota fulla röðun getu WBS-aðgerðir, skal ljúka eftirfarandi uppsetningu:

1.  Setja upp sjálfgefið dagatal og dagatal verks:
    1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**Uppsetningu**&gt;**Röðun**. Í reitnum **Sjálfvalið verkdagatal** skal tilgreina sjálfgefið dagatal. Þetta verður sjálfgefið dagatal vinnutíma fyrir öll ný verk sem eru stofnuð.
    2.  Það er hægt að breyta sjálfgefnu dagatali fyrir tilgreint verk. Smellt er á upplýsingasíðu verksins og síðan, á flýtiflipanum **Verkhópur og áætlun**, uppfærirðu reitinn **Áætlunardagatal** með því að velja annað dagatal.

2.  Setja upp staðlaða vinnudaga og vinnustundir. Dagatal sem er sett sem vinnudagatal fyrir verkið sem verður notað í WBS til að ákvarða eftirfarandi upplýsingar:

-   Vinnudagar og frídagar
-   Fjöldi vinnutíma á dag

Til að setja upp vinnudaga og vinnustundir fyrir dagatal, eða til að stofna nýtt dagatal er smellt á **fyrirtækisstjórnun**&gt;**Algengar**&gt;**Dagatöl**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Skilyrði fyrir mati á kostnaði við vinnu

Til að nota alla getu kostnaðarmats WBS þarf að setja upp kostnað og söluverð fyrir starfsmenn, tegundir af vinnu, kostnað, og þóknanir og vörur.

-   Smellið til að setja upp kostnað og söluverð vinnu-, útgjalda-og þóknunartegundir, **verkefnastjórnun Og bókhald**&gt;**Uppsetningu**&gt;**Verð**.
-   Til að setja upp kostnað og söluverð vara skal nota síðuna **Viðskiptasamningar **fyrir hverja vöru á listasíðunni **Útgefnum afurðum** í Upplýsingar um afurðarstjórnun.

## <a name="creating-a-wbs"></a>Stofna sundurliðun verkþátta
Stofnun sundurliðunar verkþátta felur í sér þrjár aðgerðir:

1.  **Sundurliðun vinnu** – Stofna sundurliðun vinnu í meðfærilega búta eða verkefni.
2.  **Vinnuáætlun** – Áætla þann tíma sem er áskilinn til að ljúka verkefni, stilla víxlverkun verkefna og velja upphafs- og lokadagsetningar fyrir verkefni.
3.  **Kostnaðaráætlun** – Meta kostnað fyrir hvert verkefni.

Í eftirfarandi hluta fjalla um hvernig getu WBS getur hjálpað við hver af þessum verkþætti.

### <a name="work-decomposition"></a>Sundurliðun vinnu

Stofnun sundurliðunar verkþátta eða niðurbrots vinnu er yfirleitt fyrsta skrefið í því ferli að búa til WBS. WBS aðgerð styður eftirfarandi grunnur constructs sundurliðun eða sundurliðaðar. 

**Rótarverkefni í verki** Rótarverkefni í verki er efsta-stigs samantektarverkefni fyrir verk. Öll önnur verkefni verks eru stofnuð undir því. Heiti rótarverksins er alltaf stillt á heiti verksins. Framlag, dagsetningar og lengd rótarhnútsins veita yfirlit yfir gildi fyrir verkefni fyrir neðan rótarverkefni. Ekki er hægt að breyta eiginleikum rótarhnúts eða eyða honum.

**Samantektar- eða gámaverk** Samantektarverk er verk sem hefur undirverkefni eða verk sem það samanstendur af undir því. Samantektarverk hefur ekki neitt vinnuframlag eða eigin kostnað. Þess í stað er vinnuframlag og kostnaður af samantektarverki samtala vinnuframlags og kostnaðar af verkþáttum sem það samanstendur af. Fyrsta upphafsdagsetning uppstöðuverkanna er notuð sem upphafsdagsetning samantektarverks og síðasta lokadagsetning uppistöðuverkanna er notuð sem lokadagsetning. Hægt er að breyta heiti samantektarverks en ekki er hægt að breyta áætlunareiginleikum framlags, dagsetningar og tímalengdar. Ef samantektarverki er eytt er öllum uppistöðuverkum einnig eytt. 

**Laufhnúthnútarverk** Laufhnútarverk stendur fyrir grófasta vinnupakkann í verkinu. Laufhnútur hefur áætlað framlag, áætlaðan fjölda tilfanga, áætlaða upphafsdagsetning og lokadagsetning og tímalengd. 

Hægt er að ljúka eftirfarandi aðgerðum stigveldis til að virkja stofnun vinnustigveldis eða sundurliðunar fyrir verk. 

**Nýtt verk** Öllum nýjum verkum sem eru stofnuð er sjálfkrafa bætt við rótarhnútinn og WBS tölu er sjálfkrafa úthlutað á verkið. WBS-númer stendur fyrir verk á stigi í stigveldi. Fyrir verkefni í fyrsta stigi undir rótarverkefni verks er tölusetningarskema upp á 1, 2, 3 og svo framvegis notað. Fyrir verkefni sem eru undir fyrsta stigi er tölusetningarskema upp á 1.1, 1.2, 1.3 og svo framvegis notað. Fyrir hvert stig sem bætt er við undir fyrra stigi er röð nýrra brotanúmera bætt við. 

Sem stendur er ekki hægt að sérsníða númer sundurliðunar verkþátta. 

**Inndregið verk** Þegar verk er dregið inn verður það undireining verksins á undan því. WBS-númer nýs undirverks er sjálfvirkt endurreiknað samkvæmt WBS-númeri nýrrar yfireiningar. Yfirverkið er nú samantektar- eða uppistöðuverk og verður þess vegna samantekt á uppistöðuverkum þess. 

> [!NOTE] 
> Þegar verkefni undir verkið sem var áður en aðgerð inndrátt laufhnút, inndraga tapar nýlega stofnaða verkið samantekt sitt dagsetningar framlag og fjölda tilfanga. Núna notar það samantekt á gildum á ný uppistöðuverk sín. 

**Draga út verk** Þegar verk er dregið út er það ekki lengur uppistöðuverk í yfireiningu. WBS-númer þessa verks er sjálfvirkt endurreiknað til að endurspegla nýtt stig verksins í stigveldinu. Framlag, kostnaður og dagsetningar fyrra yfirverks eru endurreiknaðar til að útiloka það verkefni. 

**Færa upp og Færa niður** Þegar smellt er á **Færa upp** og **Færa niður** breytist staða verks innan stigveldis yfireiningar þess. Staða verks hefur ekki áhrif á framlag verks, kostnað, dagsetningar eða tímalengd. Hins vegar er WBS-númer verksins sjálfvirkt endurreiknað til að endurspegla nýja stöðu verksins.

### <a name="schedule-estimation"></a>Tímasetja mat

Tímasetning áætlunar er yfirleitt annað skrefið í stofnun WBS. Bestu starfsvenjur eru að ljúka við tímasetningu áætlunar þegar búið er að stofna verk. Í **sundurliðun Verkþátta** síðuna í Microsoft Dynamics 365 fyrir Aðgerð hefur tvo kafla. Efri rúðan er ætluð fyrir tímasetningu áætlunar og sú neðri inniheldur flipann **Áætlaður kostnaður og tekjur** sem hægt er að nota fyrir kostnaðarmat. 
**Tengsl verkefnis** Í WBS er hægt að stofna forveravensl milli verka. Þegar forveraverkefni er úthlutað á verk getur það verk aðeins hafist eftir að öllum forveraverkum þess er lokið. Áætluð upphafsdagsetning verksins er sjálfkrafa stillt á síðustu dagsetningu allra forvera. 

**Verk röðun í Microsoft Dynamics 365 aðgerða** eftirfarandi þáttum ákvarða röðun fyrir verkefni í hnút:

-   Forverar
-   Framlag
-   Fjöldi tilfanga
-   Upphafs- og lokadagsetningar

Upphafsdagsetning laufhnúts verkefnis sem er ekki með forvera er sjálfkrafa stillt á áætlaða upphafsdagsetningu verksins. Tímalengd laufhnútaverks er alltaf reiknuð sem fjöldi vinnudaga milli upphafs- og lokadagsetninga þess. 

Röðun reglur *** Þegar kveikt er á ráðgjöf sjálfvirkrar eftirfarandi reglur eiga við verkáætlun fyrir laufhnút hnút verk:

-   Upphafs- og lokadagsetningar verks verða að vera vinnudagar, samkvæmt áætlunardagatals verksins.
-   Upphafsdagsetning verks sem er með forvera er sjálfkrafa stillt á síðustu lokadagsetningu forvera þess.
-   Framlag fyrir verk er sjálfkrafa reiknað sem hér segir:

Fjöldi einstaklinga × Tímalengd × Fjölda stunda í staðlaður vinnudagur í verkdagatali. 

Í sumum tilvikum getur verið ágætt að víkja frá þessum reglum. Hægt er að slökkva á sjálfvirkri áætlun til að koma í veg fyrir Microsoft Dynamics 365 til Aðgerðir sjálfkrafa stillingu eða leiðrétta eiginleikum fyrir verkefni í hnút. Þegar færðar eru inn upplýsingar um verkefni sem veldur broti á áætlunarreglum er villutákn áætlunar sýnt fyrir verkið. Ef ekki á að birta áætlunarvillur er smellt á **Áætlunarvillur eru sýndar** til að slökkva á eiginleikanum. 

> [!NOTE] 
> Halda áfram að vera reiknuð sem summa gildi constituent verkefni, óháð því hvort ráðgjöf sjálfvirkrar kveikt er á eða slökkt gildi fyrir verkefni samantekt eða í gám. 

**Leiðrétting áætlunarvillna** Þegar kveikt er á ráðgjöf sjálfvirkrar áætlunar er ekki líklegt að áætlunarvillur komi upp. Ef slökkt er hins vegar á ráðgjöf sjálfvirkrar áætlunar og síðan kveikt á henni aftur síðar gætu áætlunarvillutákn birst í WBS. 

**Leiðrétting áætlunarvillna eftir verki** Þegar tvísmellt er á áætlunarvillutáknið fyrir tiltekin verk birtir svargluggi allar áætlunarvillur fyrir það verk. Hægt er að ákveða hvaða áætlunarvillur á að laga fyrir verkið. 

**Leiðrétta allar villur röðun** Ef Microsoft Dynamics 365 aðgerða til að laga öll áætlunarvillur í WBS, á Aðgerðasvæðinu skal smellt á **Laga allt misræmi**. 

> [!NOTE] 
> Þessi eiginleiki getur valdið viðeigandi breytingum á WBS. Villur eru leiðréttar í eftirfarandi röð:

1.  Áætluðu framlagi í öllum verkum er breytt þannig að það sé jafnt þeirri afkastagetu sem er skilgreind í dagatali verksins.
2.  Upphafsdagsetningu hvers verks er breytt þannig að verkið hefst eftir að öllum forveraverkum þess er lokið.
3.  Upphafsdagsetningu hvers verks er breytt til að fjarlægja gloppur í upphafsdagsetningum forveraverka þess.

### <a name="cost-estimation"></a>Kostnaðarmat

Eins og áður er nefnt í þessu skjali skal færa inn kostnaðarmat fyrir hvert laufhnútaverk með því að nota í flipann **Áætlaður kostnaður og tekjur** í neðri rúðunni á síðunni **Sundurliðun verkþátta**. 

> [!NOTE] 
> Ekki er hægt að breyta kostnaðarmat fyrir verkið samantekt eða í gám. Kostnaðarmat fyrir samantektarverk er jafnt og samtala kostnaðarmats fyrir verkhnúta þess. Áætlaður heildarkostnað fyrir hvert verk er reiknaður sem samtala upphæða áætlaðs kostnaðar fyrir eftirfarandi færslugerðir:

-   Vinna
-   Vara eða efni
-   Kostnaður

Færslugerðin **Þóknun** er notuð til að meta tekjur byggðar á þóknun. Þessi færslugerð er ekki með kostnaðaríhlut og þess vegna er ekki tekið tillit til hennar þegar kostnaður er áætlaður. 

Færslugerðin **Áfangareikningur** er notuð til að skrá samningsbundið söluvirði í verkefni af gerð fast gildis. Ekki er heldur tekið tillit til þessarar færslugerðar þegar kostnaður er áætlaður. 

Þegar kostnaður er áætlaður fyrir vinnu, efni og útgjöld fyrir hvert verk verður að úthluta verktegund á áætlaðan kostnað. 

**Mat á launakostnaði** Fyrir hvert laufhnútaverk er úthlutað vinnuframlagi í tímum og sjálfgefinni tegund. Þess vegna er áætluðum launakostnaði fyrir það verkefni sjálfkrafa bætt við sjálfgefna tegund fyrir vinnu, þegar þú setur upp áætlun fyrir verk. Þetta kostnaðarmat birtist á flipanum **Áætlaður kostnaður og tekjur** í hnitanetinu **Línuupplýsingar** fyrir það verkefni. Ef þú þarft fleiri áætlanir á launakostnaði er hægt að bæta þeim við á þessum flipa. Ef þú eykur eða fækkar klukkustundum í áætluðum launakostnaði er áætlun fyrir verkið sjálfkrafa endurreiknuð. 

**Meta kostnað í kostnaðarskýrslu og efni** Flipinn **Áætlaður kostnaður og tekjur** gerir þér einnig kleift að meta útgjöld og efniskostnað fyrir verk, ef þörf er á mati. 

Kostnaðar- og söluverð fyrir hverja vinnu og kostnaðar mat línu eru byggð á uppsetningu sem er skilgreint fyrir hverja tegund í verðlagningu töflum við **verkefnastjórnun Og bókhald**&gt;**Uppsetningu**&gt;**Verðlagning**. Fyrir vörur er kostnaði og söluverði vara sjálfkrafa bætt við úr vöru- eða viðskiptasamningum á listasíðunni **Losaðar afurðir** í stjórnum afurðaupplýsinga.

## <a name="tracking-progress-on-the-wbs"></a>Rakning framvindu á WBS
Sumar atvinnugreinar rekja framvindu verks gagnvart WBS á mjög grófan hátt en aðrar rekja framvindu á hærra stigi í WBS. Þessi hluti lýsir því hvernig hægt er að nota WBS fyrir kröfur verks. 

Microsoft Dynamics 365 aðgerða hefur þremur yfirlitum fyrir WBS verk: Áætlanagerðar yfirlitið, rakningarskoðun framlags og Kostnaðarrakningu.

### <a name="planning-view"></a>Yfirlit áætlana

Yfirlit áætlana birtir áætlað eða yfirlitsmat yfir upplýsingar um upplýsingar um áætlun og kostnað. Þó að það séu engar aðgerðir fyrir rakningu á útgáfu og yfirliti fyrir WBS verks er gildum í þessu yfirliti ætlað að tákna yfirlitsútgáfu. Hlutarnir Áætlunarmat og Kostnaðarmat í þessu efnisatriði lýsa þessu yfirliti og hvernig það er notað til að stofna WBS.

### <a name="effort-tracking-view"></a>Rakningarskoðun framlags

Rakningarskoðun framlags birtir rakningu framvindu fyrir verk í WBS. Hún ber saman uppsafnað raunframlag klukkustunda fyrir verk í áætlað framlag klukkustunda. Eftirfarandi formúlur veita gildin í Rakningu framlags:

-   Framvinduhlutfall = raunframlag til dagsetningar ÷ Áætlað framlag fyrir verkið
-   Eftirstöðvar framlags (einnig þekkt sem Mat-sem-lokið \[O.S.FRV\]) = Áætlað framlag – raunframlag dagsetningu
-   Áætlað við lok (EAC) = Eftirstöðvar framlags + Raunframlag til dagsetningar
-   Áætlaðar framlagsfrávik = Áætlað framlag – EAC

Rakningarskoðun framlags birtir áætlun um framlagsfrávik fyrir verkið, byggt á hvort EAC er meira eða minna en áætlað framlag:

-   Ef EAC er hærri en áætlað framlag er verkið áætlað að verkið taki lengri tíma en upphaflega var áætlað og er á eftir áætlun.
-   Ef EAC er lægri en áætlað framlag er verkið áætlað að verkið taki styttri tíma en upphaflega var áætlað og er á undan áætlun.

**Enduráætlun verkstjóra á framlagi** Einstaka sinnum þarf stjórnandi eða annar einstaklingur sem er að rekja framvindu verks að endurskoða upprunalegt mat á verki. Verkið gæti verið að flytjast hraðar eða hægar en upphaflega var vænst, af mismunandi ástæðum. Til dæmis hefur umfang verið minnkað eða starfsmenn hafa minni reynslu en upphaflega var áætlað. Spár eru túlkun stjórnanda verks á mati, samkvæmt núverandi stöðu verks. Almennt séð á ekki að breyta grunnlínutölum, þar sem grunnlínuverk tákna vel birt skjal röðun fyrir röðun verksins og kostnaðarmat sem allir hagsmunaaðilar verksins hafa samþykkt. 

Til eru tvær leiðir verkefnisstjórar má breyta framlag verkefni:

-   Breyta eftirstöðvum framlags sem eru stillt sjálfkrafa til að uppfæra raunverulegar eftirstöðvar framlags fyrir verkið.
-   Breyta framvinduhlutfalli sem er stillt sjálfkrafa til að uppfæra raunverulega framvindu fyrir verkið.

Báðar þessar nálganir valda endurútreikningi á ETC, EAC og framvinduhlutfalli verks og spáðu framlagsfráviki fyrir verkið. EAC, ETC og framvinduhlutfall í samantektarverkum er einnig endurreiknað og spáð framlagsfrávik þeirra er uppfært. 

**Breytt framlag í samantektarverkum** Hægt er að breyta framlagi í samantektar- eða gámaverkum. Óháð því hvort þessum gildum er breytt með eftirstöðvum framlags eða framvinduhlutfalli á samantektarverka verður útreikningurinn sjálfkrafa í eftirfarandi röð:

1.  EAC, ETC og framvinduhlutfall er reiknað fyrir verkið.
2.  Nýju EAC er dreift á undirverk í sama hlutfalli og upprunaleg EAC-upphæðin.
3.  Nýtt EAC er reiknað á hvert verk í laufhnút.
4.  Eftirstöðvar framlags og framvinduhlutfall er endurreiknað fyrir öll viðkomandi undirverk, samkvæmt nýju EAC-gildi. Framlagsfrávik verka er einnig endurreiknað.
5.  EAC í samantektarverkum er einnig endurreiknað úr laufhnútum.

Smellið á **Útvíkka á stig** í Rakningarskoðun framlags til að stilla stigið þar sem á að rekja og viðhalda þínu WBS. WBS er sjálfkrafa útvíkkað sem stig í Rakningarskoðun framlags í hvert skipti sem það er opnað.

### <a name="cost-tracking-view"></a>Yfirsýn yfir kostnaðarrakningu

Yfirsýn yfir kostnaðarrakningu birtir rakningu á kostnaðarnotkun fyrir verkefni. Í þessu yfirliti er raunkostnaður sem hefur farið í verk til dagsins í dag borinn saman við áætlaðan kostnað fyrir verkið. Eftirfarandi formúlur veita gildin í Yfirsýn yfir kostnaðarrakningu:

-   Hlutfall notaðs kostnaðar = Raunkostnaður að dagsetningu ÷ Áætlaður kostnaður fyrir verkið
-   Kostnaður í heild (CTC) = Áætlaður kostnaður – Raunkostnaður til dagsetningar
-   Áætlað við lok (EAC) = CTC + Raunkostnaður til dagsetningar
-   Áætlað kostnaðarfrávik = Áætlaður kostnaður – EAC

Yfirsýn yfir kostnaðarrakningu birtir áætlun um kostnaðarfrávik fyrir verkið, byggt á hvort EAC er meira eða minna en áætlaður kostnaður:

-   Ef EAC er hærri en áætlaður kostnaður er áætlað að verkið noti meira fé en upphaflega var áætlað og er umfram fjárhagsáætlun.
-   Ef EAC er lægri en áætlaður kostnaður er áætlað að verkið noti minna fé en upphaflega var áætlað og er undir fjárhagsáætlun.

**Enduráætlun verkstjóra á kostnaði** Verkefnisstjórar verða að nota CTC til að endurskoða upprunalegt kostnaðarmat í verki. Stjórnandi verks getur breytt CTC-gildi á kostnaði sem er nauðsynlegur til að ljúka verkinu. Ef þú breytir CTC-gildi eru CTC, EAC og hlutfall notaðs kostnaðar verks og áætlað kostnaðarfrávik verks endurreiknuð. EAC, ETC og hlutfall notaðs kostnaðar í samantektarverkum er einnig endurreiknað og spáð kostnaðarfrávik þeirra er uppfært. 

> [!NOTE] 
> Notað hlutfall kostnaðar þegar hægt er að endurskoða framlags fyrir WBS verk í á rakningarskoðun framlags, CTC verki, EAC, og áætlað kostnaðarfrávik eru allar endurreiknuð í Kostnaðarrakningu. Hins vegar hefur endurskoðun á kostnaði ekki áhrif á gildi í Rakningarskoðun framlags, þar sem kostnaður eftir færslugerð (vinna, efni eða kostnaður) eða tegund verks eru ekki endurskoðuð. 

**Áætluð endurskoðun fyrir kostnað við samantektarverk** Hægt er að endurskoða kostnað samantektarverka og útreikningur verður sjálfkrafa í eftirfarandi röð:

1.  EAC, CTC og hlutfall notaðs kostnaðar við verkið er endurreiknað.
2.  Nýju EAC er dreift á undirverk í sama hlutfalli og upprunalegt EAC í verkum.
3.  Nýtt EAC er reiknað fyrir sérhvert verk.
4.  CTS og hlutfall notaðs kostnaðar er endurreiknað fyrir öll viðkomandi undirverk, samkvæmt nýju EAC-gildi. Kostnaðarfrávik verka er einnig endurreiknað.
5.  EAC fyrir öll samantektarverkefni er endurútreiknað út frá þessari breytingu.

Smellið á **Útvíkka á stig** í Yfirsýn yfir kostnaðarrakningu til að stilla stigið þar sem á að rekja og viðhalda þínu WBS. WBS er sjálfkrafa útvíkkað sem stig í Yfirsýn yfir kostnaðarrakningu í hvert skipti sem það er opnað.

### <a name="earned-value-management"></a>Stjórnun áunnins virðis

Hægt er að nota aðferðina áunnið virði (EVM) til að fylgjast með framvindu verksins. Hægt er að mælikvarða áunnins virðis í Hlutverkamiðstöð stjórnanda verks. Línuritsíhlutur áunnins virðis sýnir tímastillt gildi áætlaðs virðis og raunkostnað. Áunnið virði núverandi dagsetningar er sýnt sem punktur. Tímastillt gögn fyrir áunnið virði eru ekki tiltæk núna. 

Tímastilling á grafi áunnins virði er birt eftir viku eða mánuði. Þessi kafli lýsir því þremur stoðum af EVM: áætluð gildi fékkst gildi og raunverulegan kostnað. 

**Áætlað virði** EVM-kenningin tilgreinir að teiknun áætlaðra gilda stendur fyrir tíðni sem verkteymið áætlaði að ávinna virði í verkinu. 

Microsoft Dynamics 365 aðgerða notar 0:100 tekjukóða reglu þegar hann plots áætluð gildi. Samkvæmt þessari reglu er virði verksins er bókað á verk frá og með lokadagsetningunni. Ekkert gildi er bókað fyrr en verki er 100 prósent lokið. 

Í verkstjórnun og bókhaldi skal færa inn lokadagsetningu laufhnúta og áætlaðan kostnað fyrir það. Þegar graf yfir áætlaða gildi er sýndur eftir vikum eru áætluð gildi samanlögð eftir vikum fyrir öll verk hnút á laufstigi fyrir tímalengd verksins. 

**Áunnið virði** EVM-kenningin tilgreinir að teiknun áunnins virðis stendur fyrir tíðni sem verkteymið ávinnur sér í raun virði í verkinu. 

Microsoft Dynamics 365 aðgerða notar 0:100 söfnun reglu þegar hennar plots fékkst gildi. Samkvæmt þessari reglu er virði verksins er bókað á verk frá og með lokadagsetningunni. Ekkert gildi er bókað fyrr en verki er 100 prósent lokið. 

Þegar áunnið virði er reiknað er tekið tillit til framvinduhlutfalls hvers verks. Samkvæmt 0:100 tekjureglunni er eingöngu tekið tillit til verka sem er lokið á tilteknu tímabili fyrir útreikning á áunnu virði í lok þess tímabils. Áunnið virði verks er reiknað fyrir öll verkefni sem hefur verið lokið þegar línuritið er stofnuð. 

> [!NOTE] 
> Sem stendur er kerfið fyrir WBS rakningu er ekki með gagnaskipan geyma prósentur sögulegar vinnslu í hvert verkefni. Þess vegna er aðeins hægt að tilkynna áunnið virði frá og með þeim tíma sem unnið er úr teningnum. Vinna með teninga reglulega til að uppfæra gögn áunnið virði sem birtist í Hlutverkamiðstöðinni. 

**Raunkostnaður** EVM kenningin tilgreinir að teiknun raunkostnaðar stendur fyrir tíðni þess sem fé er eytt í verkið. 

Færslur sem eru bókaðar á verk eru notaðar til að teikna upp raunkostnaðarlínu. Kostnaðurinn er tekinn saman eftir dagsetningum. Þessi gögn eru síðan notuð til að teikna raunkostnaður eftir vikum eða mánuðum á línurit áunnins virðis.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Hvernig á að nota hugtökin áætlað virði, áunnið virði og raunkostnað

**Áætlunarfrávik** Við áætlun er stofnuð spá fyrir vinnu á tímaásinn. Þess vegna er áætlað virði sá hraði sem verkskipulegglendur áætluðu að vinnu væri lokið í verkinu. Þegar verk er komið í framvindu er vinnu lokið og verkið ávinnur sér gildi. Með því að bera saman áætluð gildi og áunnið virði er hægt að skoða framvindu verks sem er í ferli. Niðurstaða þessa samanburðar kallað áætlunarfrávik. 

Ef áætlað virði fyrir tímabil er meira en áunnið virði er upphæð vinnu sem hefur verið gerð á verk lægri en það var áætlað. Þess vegna er verkið á eftir áætlun. Þar sem áunnið virði og áætluð gildi eru sýnd sem fjárhagsleg gildi fær verkið einnig fjárhagslegt gildi. 

Ef áætlað virði fyrir tímabil er minna en áunnið virði er upphæð vinnu sem hefur verið gerð á verk hærri en það var áætlað. Þess vegna er verkið á undan áætlun. Þessi afhendingartími fær einnig fjárhagslegt gildi.

**Kostnaðarfrávik** Þar sem áunnið gildi notar kostnaðarverð sem margfaldara tilgreinir áunnið virði kostnað á aðgerðum sem eru gerðar á verki. Eftir því sem verki miðar áfram veitir færslukladdi skrá yfir peninga sem er í raun varið í verkið. Með því að bera saman áunnið virði við raunkostnað er hægt að skoða þá fjárupphæð sem er eytt á móti því virði sem er áunnið. Niðurstaða þessa samanburðar er kallað kostnaðarfrávik. 

Ef raunkostnaður sem er varið fyrir tímabil er meiri en áunnið virði var meira fé varið en vannst inn. Þess vegna er verkið umfram fjárhagsáætlun. 

Ef raunkostnaður sem er varið fyrir tímabil er minni en áunnið virði vannst meira fé inn en var varið. Þess vegna er verkið undir fjárhagsáætlun.

## <a name="wbs-templates"></a>WBS-sniðmát
Hægt er að nota virkni WBS sniðmát til að stofna stöðluðu sniðmát fyrir verk. Ef verk sem fyrirtækið býður fela í sér mikið af endurtekinni vinnu, ætti að íhuga að stofna wbs-sniðmát. 

Hægt er að stofna wbs-sniðmát úr WBS í fyrirliggjandi verki, þannig að hægt er að endurnota þá þekkingu og bestu starfsvenjur sem teknar eru saman við áætlanagerð verks við svipuð verk í framtíðinni. Hins vegar er stundum marklaust að vista allt WBS sem sniðmát. Þess vegna er einnig hægt að stofna sniðmát úr hlutum WBS verks.

### <a name="saving-a-projects-wbs-as-a-template"></a>Vista WBS verks sem sniðmát

Þegar sniðmát hefur verið stofnað er hægt að flytja það inn í WBS nýs verks undir rótarhnút eða undir einhverjum verkþætti í WBS verksins.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Innflutningur WBS-sniðmáts í WBS verks

Þegar verkhlutar eru fluttir inn eru verkhlutar í sniðmátinu skipulagðir út frá upphafsdagsetningu verksins sem þeir eru fluttir inn undir. Við innflutning eru vensl forvera á sniðmáti verks eru notuð til að reikna upphafsdagsetningar fyrir innflutt verkefni. Stöðluðu vinnudagatali verks áfangastaðar er beitt til að reikna lokadagsetningar innfluttra verka, þannig að vinnudagar og vinnutímar sem eru tilgreindir í vinnudagatali núgildandi verks eru varðveittir. 

Kostnaðarupphæðir og söluverð í matslínum eru notaðar til að tryggja að verð sem eru sértæk fyrir verk eða verksamning hafi gildar dagsetningar.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Mismunur á milli við WBS verks og WBS-sniðmáti

-   Verk í WBS-sniðmáti eru ekki með upphafs- og lokadagsetningar.

Vinnudagar og frídagar eru ekki stilltir fyrir WBS-sniðmát.

-   WBS-sniðmát nota alltaf áætlunardagatal sem er sett upp sem sjálfgefið dagatal fyrir öll verk.

Sjálfgefið áætlunardagatal er aðeins notað til að finna út klukkustundir á stöðluðum vinnudegi.

-   Vensl forvera ekki eru afrituð í WBS-sniðmát.

Þar sem WBS-sniðmát eru ekki með dagsetningar eru rök upphafdagsetningar sem byggjast á lokadegi forvera óþörf.

-   Matslína launakostnaðar er sjálfkrafa stofnuð þegar verk er stofnað í wbs-sniðmáti. Söluverð og kostnaðarupphæð eru afrituð frá völdum starfsmanni.

Hægt er að stofna útgjöld og birgðakostnað handvirkt, rétt eins og hægt er að gera í WBS verks.

-   Áætlunarvillur eru sýndar þegar frávik eru frá eftirfarandi formúlu:

Framlag = Fjöldi tilfanga × Tímalengd × Tímafjöldi á stöðluðum vinnudegi 

Hægt er að leiðrétta allar áætlunarvillur í einu með því að smella á **Laga allar áætlunarvillur**. 

Einnig er hægt að leiðrétta hverja áætlunarvillu fyrir sig með því að smella á viðvörunartáknið fyrir hvert verkefni.


