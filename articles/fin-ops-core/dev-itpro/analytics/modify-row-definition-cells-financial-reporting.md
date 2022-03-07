---
title: Breyta hólfum línuskilgreiningar
description: Þetta efnisatriði lýsir upplýsingunum sem krafist er fyrir hvert hólf í línuskilgreiningu á fjárhagsskýrslu og útskýrir hvernig á að færa inn þær upplýsingar.
author: ShylaThompson
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80df992ce14577ba78587648f8af2c35b382a589
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344886"
---
# <a name="modify-row-definition-cells"></a>Breyta hólfum línuskilgreiningar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir upplýsingunum sem krafist er fyrir hvert hólf í línuskilgreiningu á fjárhagsskýrslu og útskýrir hvernig á að færa inn þær upplýsingar.

## <a name="specify-a-row-code-in-a-row-definition"></a>Línukóði tilgreindur í línuskilgreiningu

Í línuskilgreiningum eru það númer eða merki í hólfinu **Línukóði** sem auðkenna hverja línu í línuskilgreiningunni. Hægt er að tiltaka línukóðann sem á að vísa til gagna í útreikningum og samtölum.

### <a name="row-code-requirements"></a>Kröfur um línukóða

Þörf er á línukóða fyrir allar línur. Hægt er að blanda saman tölulegum línukóðum, línukóðum úr bók- og tölustöfum og afvöldum (tómum) línukóðum innan línuskilgreiningar. Línukóðinn getur verið hvaða jákvæða heiltala sem er (undir 100.000.000) eða lýsandi merki sem auðkennir þá línu. Lýsandi merki verður að uppfylla eftirfarandi reglur:

- Merki Verður að byrja á bókstaf (frá a til z eða frá A til Z) og getur verið hvaða samsetning talna og bókstafa, allt að 16 stafir.

    > [!NOTE]
    > Merki getur notast við undirstrik (\_), en engir aðrir sérstafir eru leyfðir.

- Merki getur ekki notað neitt af eftirfarandi fráteknum orðum: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL eða CPO, RPO.

Eftirfarandi eru dæmi um gilda línukóða:

- 320
- TL\_NETTÓ\_TEKJUR
- TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Línukóða breytt í línuskilgreiningu

1. Report Designer smellt **Línuskilgreiningar**, og opnið síðan línuskilgreiningu til að breyta.
2. Sláið nýtt gildi inn í hólfið í dálknum **Línukóði** í viðeigandi línu.

### <a name="reset-numeric-row-codes"></a>Endurstilla alla tölusetta línukóða

1. Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.
2. Á valmyndinni **Breyta** er smellt á **Endurnúmera línur**.
3. Í **endurnúmera línur** svarglugga, Tilgreinið nýju gildin fyrir upphafskóða línu og stighækkun línukóða. Hægt er að endursetja tölulega línukóða í gildi sem eru jöfn bil. Hinsvegar endurtölusetur Skýrsluhönnun línukóða sem hefjast á tölum, (til dæmis 130, 246), Hann endurtölusetur ekki línukóða sem hefjast á bókstöfum, (til dæmis INCOME\_93, TP0693).

> [!NOTE]
> Þegar línukóðar eru endurtölusettir uppfærir Skýrsluhönnun sjálfkrafa **TOT-** og **CAL**-tilvísanir. Ef **TOT**-lína vísar til dæmis til sviðs sem hefst á línukóðanum 100 og línur eru endurtölusettar þannig að þær hefjist á 90 mun fyrsta **TOT**-tilvísunin breytast úr 100 í 90.

## <a name="add-a-description"></a>Bæta við Lýsing
Í lýsingarhólfinu er lýsing á fjárhagsgögnunum í línu skýrslunnar, til dæmis Tekjur eða Nettótekjur. Textinn í hólfinu **Lýsing** birtist í skýrslunni nákvæmlega eins og hann er sleginn inn í línuskilgreiningunni.

> [!NOTE]
> Breidd lýsingardálksins í skýrslunni er stillt í dálkskilgreiningunni. Ef textinn í línuskilgreiningardálknum **Lýsing** er of langur verður að staðfesta breiddina á dálknum **DESC**. Þegar svarglugginn **Setja inn línur úr** er notaður eru gildin í dálkinum **Lýsing** hlutagildi eða víddargildi úr fjárhagsgögnunum. Hægt er að setja inn línur til að bæta við lýsandi texta, eins og fyrirsögn hluta eða samtölu hluta, og til að bæta við sniði, eins og línu á undan samtölulínu. Ef í skýrslunni er skipurit er hægt að innifela viðbótartexta sem er skilgreindur fyrir skipuritseiningarnar í skipuritinu. Einnig er hægt að takmarkaður Viðbótartexti við tiltekna einingu skipurits

### <a name="add-the-description-for-a-line-on-a-report"></a>Bæta við lýsingu á línu í skýrslu

1. Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.
2. Veljið hólfið **Lýsing** og færið síðan inn heiti skýrslulínunnar.
3. Sníðið textann.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Viðbótartexta bætt við úr skipuriti í lýsingunni

1. Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.
2. Færið inn viðbótartextakóða og hvers kyns annan texta í það hólf undir **Lýsing** sem við á.
3. Sníðið textann.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Viðbótartexti takmarkaður við tiltekna einingu skipurits

1. Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.
2. Finnið línuna þar sem stofna á viðbótartextann og tvísmellið síðan á hólfið í dálkinum **Related Formulas/Rows/Units**.
3. Í svarglugganum **Einingaval skipurits** er valinn reiturinn **Skipurit**.
4. Í því **Velja skýrslugerð einingu takmarkanir** svæðið, útvíkkun eða hrun skýrslugerð tréð og síðan velja skýrslugerð einingu.

## <a name="add-a-format-code"></a>Sniðkóða bætt við
Hólfið **Sniðkóði** býður upp á úrval forsniðinna valkosta fyrir innihald þeirrar línu. Ef hólfið **Sniðkóði** er autt verður línan túlkuð sem upplýsingalína fjárhagsgagna.

> [!NOTE]
> Ef skýrsla inniheldur upphæðarlausar sniðmátslínur sem tengjast upphæðalínum sem hafa verið faldar, til dæmis vegna þess að þær eru með núllupphæðir, er hægt að fela prentun titil- og sniðmátslína með því að nota dálkinn **Tengdar formúlur/línur/einingar**.

### <a name="add-a-format-code-to-a-report-row"></a>Sniðkóða bætt við skýrslulínu

1. Smellt er á **Línuskilgreiningar** í Skýrsluhönnun og línuskilgreining sem á að breyta því næst valin.
2. Tvísmellið á hólfið **Sniðkóði**.
3. Veljið sniðkóði í listanum. Eftirfarandi tafla lýsir sniðkóðum og aðgerðir sem gilda fyrir þá.

    | Sniðkóði                   | Túlkun á sniðkóðanum | Aðgerð |
    |-------------------------------|-----------------------------------|--------|
    | (Ekkert)                        |                                   | Hreinsar hólfið **Sniðkóði**. |
    | TOT                           | Samtals                             | Auðkennir línu sem notar stærðfræðilega virkja í dálkinum **Tengdar formúlur/línur/einingar**. Samtölur innihalda einfalda virkja, til dæmis **+** eða **-**. |
    | CAL                           | Útreikningur                       | Auðkennir línu sem notar stærðfræðilega virkja í dálkinum **Tengdar formúlur/línur/einingar**. Útreikningar innihalda flókna virkja, til dæmis **+**,**-**, **\**_, _*/**, og **IF/THEN/ELSE** yrðingar. |
    | DES                           | lýsing                       | Auðkennir hauslínu eða auða línu í skýrslu. |
    | LFT RGT CEN                   | Hægri vinstri miðja                 | Stillir staðsetningu texta línulýsingar á skýrslusíðunni, óháð staðsetningu textans í dálkskilgreiningunni. |
    | CBR                           | Breyta grunnlínu                   | Auðkennir línu sem ákvarðar grunnlínu fyrir dálkaútreikninga. |
    | DÁLKUR                        | Dálkaskil                      | Byrjar nýjan dálka í skýrslunni |
    | PAGE                          | Síðuskil                        | Byrjar nýjan síðu í skýrslunni |
    | \---                          | Einföld undirstrikun                  | Setur einfalda línu undir alla upphæðardálka í skýrslunni. |
    | ===                           | Tvöföld undirstrikun                  | Setur tvöfalda línu undir alla upphæðardálka í skýrslunni. |
    | LINE1                         | Mjó lína                         | Dregur einfalda, mjóa línu þvert yfir síðuna. |
    | LINE2                         | Þykk lína                        | Dregur einfalda, þykka línu þvert yfir síðuna. |
    | LINE3                         | Punktalína                       | Dregur einfalda punktalínu þvert yfir síðuna. |
    | LINE4                         | Þykk lína og mjó lína          | Dregur tvöfalda punktalínu þvert yfir síðuna. Efsta línan er þykk, neðasta línan er þunn. |
    | LINE5                         | Mjó lína og þykk lína          | Dregur tvöfalda punktalínu þvert yfir síðuna. Efsta línan er þunn, neðasta línan er þykk. |
    | BXB BXC                       | Innrömmuð lína                         | Dregur ramma utan um skýrslulínuna sem hefst með **BXB**-línunni og lýkur með **BXC**-línunni. |
    | REM                           | Athugasemd                            | Auðkennir línu sem er athugasemdalína og ætti ekki að vera prentuð í skýrslunni. TIl dæmis gæti athugasemdalína verið til að skýra sniðmátsaðferðir. |
    | SORT ASORT SORTDESC ASORTDESC | Raða                              | Raðar kostnaðar- eða tekjuliðum, raðar raunskýrslum eða fjárhagsfrávikaskýrslum eftir mestu frávikum eða raðar línulýsingum eftir stafrófsröð. |

## <a name="specify-related-formulasrowsunits"></a>Tilgreina Tengdar formúlur/línur/einingar
Hólfið **Tengdar formúlur/línur/einingar** hefur margvíslegan tilgang. Hólfið **Tengdar formúlur/línur/einingar** getur gert eina af eftirfarandi aðgerðum, allt eftir tegund línunnar:

- Skilgreint línurnar sem taka á með í útreikningi þegar **TOT**- eða **CAL**-sniðkóði er notaður.
- Tengt sniðslínu við upphæðarlínu til að prenta sniðið aðeins þegar tengd upphæð er prentuð.
- Takmarka línu við tiltekna einingu skipurits.
- Skilgreint grunnlínuna fyrir útreikninga þegar sniðkóðinn **BASEROW** er notaður.
- Skilgreint línurnar sem á að flokka þegar notaður er einhver af röðunarsniðkóðunum.

### <a name="use-a-row-total-in-a-row-definition"></a>Línusamtala notuð í línuskilgreiningu

Notið formúlu fyrir línusamtölu til að bæta við eða draga frá upphæðir í öðrum röðum. Formúla til að stofna línusamtölu getur haft + og - virkja til að sameina einstaka línukóða og svið. Svið eru tilgreind af Tvípunktur (:). Hver formúla getur innihaldið allt að 1.024 stafi. Eftirfarandi er dæmi um staðlaða samantektarformúlu: 400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Íhlutir formúlu fyrir línusamtölu

Þegar stofnuð er formúla fyrir línusamtölu verður að notast við línukóða til að tilgreina hvaða línum á að bæta við eða draga frá í fyrirliggjandi línuskilgreiningu, sem og virkja til að tilgreina hvernig á að sameina línurnar. Hægt er að nota samtölulínur og upphæðarlínur í hvaða samsetningu sem er.

> [!NOTE]
> Allar samtölulínur sem eru innan sviðs eru útilokaðar. Til að stofna lokasamtölu er hægt að tilgreina svið línanna. Ef fyrsta lína sviðs er samtala línu, er sú lína höfð með í nýju samtölunni. Eftirfarandi tafla lýsir því hvernig virkjar eru notaðir í formúlum fyrir línusamtölur.

| Virki | Dæmi um formúlu | lýsing                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Bætir upphæðinni í línu 100 við upphæðina í línu 330.        |
| :        | 100:330         | Bætir við samtölur allra lína á milli línu 100 og línu 330.    |
| -        | 100-330         | Dregur upphæðina í línu 100 frá upphæðinni í línu 330. |

### <a name="create-a-row-total"></a>Línusamtala stofnuð

1. Smellið á **Línuskilgreiningar** í Report Designer og opnið svo línuskilgreininguna sem á að breyta.
2. Tvísmellið á hólfið **Sniðkóði** í línuskilgreiningunni og veljið **TOT**.
3. Í hólfinu **Tengdar formúlur/línur/einingar** er slegin inn formúla fyrir samtölu.

### <a name="relate-a-format-row-to-an-amount-row"></a>Sniðmátslína tengd við upphæðarlínu

Í **Sniðkóði** dálkinum í línuskilgreiningu beita sniðkóðar **DES**, **LFT**, **RGT**, **CEN**, **---** og **===** sniði á raðir sem innihalda ekki upphæð. Til að forðast að prenta þetta sniðmát þegar tengdar upphæðarlínur eru faldar vegna þess að upphæðarlínur innihalda núllgildi eða ef engin virkni er á tímabilinu þarf að tengja sniðmátslínurnar við samsvarandi upphæðarlínur. Þessi virkni er gagnlegt þegar æskilegt er að fela prentun hausa eða snið tengd millisamtölum þegar engar ítarupplýsingar liggja fyrir til að prenta fyrir það tímabil.

> [!NOTE]
> Þú getur einnig komið í veg fyrir að nákvæmur fjöldi raða með upphæðum séu prentaðar með því að hreinsa valkostinn til að birta raðir án upphæða. Þessi valkostur finnst á flipanum **Stillingar** í skýrsluskilgreiningunni. Sjálfgefið er að reikningar færsluupplýsinga með núllstöðu og enga tímabilsvirkni eru faldir í skýrslum. Til að sýna reikninga færsluupplýsinga er valinn gátreiturinn **Birta línur sem ekki innihalda upphæðir** á flipanum **Stillingar** í skýrsluskilgreiningunni.

### <a name="relate-a-format-row-to-an-amount-row"></a>Sniðmátslína tengd við upphæðarlínu

1. Smellt er á **Línuskilgreiningar** í Skýrsluhönnun og línuskilgreining sem á að breyta því næst valin.
2. Í hólfinu **Tengdar formúlur/línur/einingar** í sniðmátslínunni er línukóði upphæðarlínunnar sem á að fela sleginn inn.

    > [!NOTE]
    > Til fela upphæð línu verður staða línunnar að vera 0 (núll). Upphæð línu sem hefur staða er ekki falin.

3. Á valmyndinni **Skrá** er smellt á **Vista**.

### <a name="example-of-preventing-printing-of-rows"></a>Dæmi um að koma í veg fyrir prentunar á línum

Í eftirfarandi dæmi vill notandi koma í veg fyrir prentun haussins og undirstrikana í línunni **Reiðufé alls** vegna þess að hvorugur lausafjárreikninganna sýndi neina virkni. Þess vegna, í línu 220 (sem, eins og **---**--- sniðkóði gefur til kynna, er sniðmátslína) í **Tengdar formúlur/línur/einingar** dálki, færir hann inn **250**, sem er línukóði upphæðarlínunnar sem á að fela.

[![RelatedRowsRowDefinition.](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Grunnlínan valin fyrir dálkútreikning
Í vensluðu skipuriti eru einni eða fleiri grunnlínum úthlutað í línuskilgreiningu með því að nota **CBR**-kóða (Change Base Row). Síðan er vísað til grunnlínu með útreikningi í skilgreiningu dálks. Hér eru nokkur dæmi um CBR-útreikninga:

- Prósentu af heildartekjum eins og hún tengist einstökum tekjuatriðum.
- Prósentu af heildarkostnaði eins og hún tengist einstökum kostnaðaratriðum.
- Prósentu af brúttóframlegð eins og hún tengist upplýsingum um svið eða deild.

Ein eða fleiri grunnlínur eru skilgreindar í línuskilgreiningu og síðan ákvarðar skilgreining dálks tengslin sem grunnlínan er skráð í. Kóðinn sem notaður er í dálkformúlunni er **BASEROW**. Eftirfarandi einföldu stærðfræðiaðgerðir eru notaðar **BASEROW**: deiling, margföldun, samlagning eða frádráttur. Aðgerð sem er oftast notað er að deila með **BASEROW**, þar sem niðurstaðan er sýnd sem prósenta. Dálkaútreikningar sem nota **BASEROW** í formúlunni nota línuskilgreininguna fyrir tengda(n) grunnlínukóða. **CBR**-línur hafa eftirfarandi einkenni:

- **CBR**-línur eru ekki prentaðar í fullgerðri skýrslu.
- **CBR**-sniðskóðinn og tengdir línukóðar eru staðsettir yfir línunni eða hlutanum sem birtir tengda útreikninga.

Í dálkskilgreiningu tilgreinir dálktegundin **CALC** dálk sem tilgreinir formúlu í línunni **Formúla**. Formúlan vinnur með gögnin fyrir þennan dálk skýrslunnar og notar lykilorð grunnlínu sem grunn útreikninga út frá **CBR**-sniðskóðum í línunni. Í línuskilgreiningunni skilgreinir **CBR**-sniðskóðinn grunnlínuna fyrir dálka sem reikna út prósentu af eða margfalda með grunnlínunni fyrir hverja línu í skýrslunni. Hægt er að hafa mörg **CBR** sniðkóða í línusniði, eins og eitt með nettósölu, annað með brúttósölu og enn annað með heildarkostnaði. Alla jafna er **CBR** sniðkóða notað til að stofna prósentu fyrir reikninga sem bornir eru saman við samtölulínu. Grunnlína er notuð fyrir alla útreikninga þar til önnur grunnlína er skilgreind. Skilgreina verður **CBR** sniðkóða í upphafi og **CBR** sniðkóða í lokin. Til dæmis, til að ákvarða kostnað sem prósentu af nettósölu, er hægt að deila í gildið í hverri kostnaðarlínu með gildinu í nettósölulínunni. Í því tilviki er nettósölulínan grunnlínan. Hægt er að skilgreina dálksskilgreiningu sem skráir núgildandi niðurstöður og niðurstöður það sem af er árinu, ásamt grunnprósentu hverrar niðurstöðu, eins og sýnt er í eftirfarandi dæmi. Byrjið með ítarlegum rekstrarreikningi.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Grunnlína valin í línuskilgreiningu fyrir dálkaútreikning

1. Smellið á **Dálkskilgreiningar** í Skýrsluhönnun og opnið því næst dálkskilgreiningu fyrir rekstrarreikning.
2. Bætið nýjum dálki við dálkskilgreininguna og stillið dálktegundina **CALC**.
3. Í hólfinu **Formúla** í nýja dálkinum skal færa inn formúluna **X/BASEROW**, þar sem **X** er dálkur af gerðinni **fjárhagsvídd** sem birta á prósentu fyrir.
4. Tvísmellið á hólfið **Hnekking sniðs/gjaldmiðils**.
5. Í **Hnekkja sniði** svarglugganum í **sniðaflokkur** listanum veljið **Prósentu**, og smellið síðan á **í lagi**.
6. Á valmyndinni **Skrá** er smellt á **Vista sem** til að vista dálkskilgreininguna. Bæta **CBR** við gildandi skráarnafn (til dæmis **CUR\_YTD\_CBR**). Þessi dálkskilgreining er dálkskilgreining grunnlínu.
7. Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið því næst línuskilgreiningu sem á að breyta með grunnlínuútreikningnum.
8. Setjið inn nýja línu fyrir ofan línuna þar sem grunnlínuútreikningurinn á að hefjast.
9. Tvísmellið á hólfið **Sniðkóði** í línuskilgreiningunni og veljið **CBR**.
10. Í hólfinu **Tengdar formúlur/línur/einingar** er slegið inn númer í Línukóði fyrir grunnlínuna.

### <a name="example-of-base-row-calculation"></a>Dæmi um grunnlínuútreikning

Í eftirfarandi dæmi um línuskilgreiningu sýnir lína 100 að grunnlínan fyrir útreikninginn er lína 280.

[![Dæmi um grunnlínuútreikning.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png)

Í eftirfarandi dæmi um dálkskilgreiningu nota útreikningarnir **CBR**-sniðkóðann. Útreikningurinn í dálki C hefur þau áhrif að deilt er í gildið í dálki B í skýrslunni með gildinu í línu 280 í dálki B. Hnekking sniðsins í dálki B prentar niðurstöðu útreikningsins sem prósentutölu. Á sama hátt er hver upphæð í dálki E upphæðin í dálki D sem prósenta af nettósölu.

[![Dæmi um dálkskilgreiningu.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png)

Eftirfarandi dæmi sýnir skýrslu sem gæti verið stofnuð á grundvelli fyrri útreikninga

[![Dæmi um skýrslu sem byggist á fyrri dæmaútreikningum.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Röðunarkóði valinn fyrir línuskilgreiningu
Röðunarkóðar raða reikningum og gildum, raða raunskýrslum eða fjárhagsfrávikaskýrslum eftir mestu frávikum eða raða línulýsingum eftir stafrófsröð. Eftirtaldir röðunarkóðar eru tiltækir:

- **SORT** – Raðar skýrslum í hækkandi röð eftir gildum í tilgreindum dálki.
- **ASORT** – Raðar skýrslum í hækkandi röð Grundvallað á algildi í tilgreindum dálki. Með öðrum orðum, tákn hvers gildis er hunsað við þegar gildum er raðað. Þessi sniðkóði raðar gildunum samkvæmt umfangi frávikanna, óháð hvort afbrigði er jákvæðra eða neikvæðra.
- **SORTDESC** – Raðar skýrslum í lækkandi röð eftir gildum í tilgreindum dálki.
- **ASORTDESC** – Raðar skýrslum í lækkandi röð Grundvallað á algildi í tilgreindum dálki.

### <a name="select-a-sorting-code"></a>Röðunarkóði valinn

1. Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.
2. Tvísmellið á hólfið **Sniðkóði** og veljið síðan röðunarkóða.
3. Í hólfið **Tengdar formúlur/línur/einingar** tilgreindu svið línukóða sem á að flokka. Til að tilgreina svið skal slá inn fyrsta línukóðann, dálk (:) og síðan síðasta línukóða Til dæmis, færa inn **160:490** til að tilgreina að sviðið er lína 160 til og með lína 490.
4. Í hólfið **Dálktakmörkun** skal slá inn dálkstaf skýrsludálksins sem þú vilt nota á fyrir röðunina.

    > [!NOTE]
    > Aðeins skal taka með upphæðarlínur í röðunarútreikningi.

### <a name="examples-of-ascending-and-descending-column-values"></a>Dæmi um hækkandi og lækkandi dálkagildi

Eftirfarandi dæmi um einingar sýnir hækkandi röðun gilda í dálki D í skýrslunni fyrir línur 160 til og með 490. Að auki verður raungildum í dálki G raðað í lækkandi röð í skýrslunni fyrir röð 610 til og með 940.

| Línukóði | Lýsing                                         | Sniðkóði | Tengdar formúlur/línur/einingar | Eðlileg staða | Dálktakmörkun | Tengill í fjárhagsvíddir |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Raðað eftir mánaðarlegum frávikum í hækkandi röð       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Sala                                               |             |                             | C              |                    | 4100                         |
| 190      | Söluskil                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Vaxtatekjur                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Raðað eftir YTD-raunfrávikum í lækkandi röð | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Sölur                                               |             |                             | F              |                    | 4100                         |
| 640      | Söluskil                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Vaxtatekjur                                     |             |                             | F              |                    | 7000                         |


## <a name="specify-a-format-override-cell"></a>Tilgreina hólf sniðshnekkingar.
Hólfið **Hnekkja sniði** tilgreinir prentsniðið fyrir línuna. Þetta snið hnekkir sniðinu sem er tilgreint í dálkskilgreiningunni og skýrsluskilgreiningunni. Sjálfgefið er að Sniðið sem er tilgreind í þessum skilgreiningum er gjaldmiðli. Ef skýrslan birtir fjölda eigna í einni línu, t.d. fjölda bygginga, og önnur lína sýnir og fjárhagslegt gildi þeirra eigna, hægt er að hnekkja gjaldmiðilssniðinu og færa inn talnasnið fyrir línuna sem tilgreinir fjölda bygginga. Þú tilgreinir þessar upplýsingar í svarglugganum **Hnekkja sniði**. Valkostirnir fara eftir völdum sniðflokki. Sýnishorn sniða eru birt á svæðinu **Dæmi** í svarglugganum. Eftirfarandi sniðflokkar eru í boði.

- Gjaldmiðilssnið
- Talnasnið
- Prósentusnið
- Sérsnið

### <a name="override-cell-formatting"></a>Hólfasniði hnekkt

1. Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.
2. Tvísmellið á hólfið í dálknum **Hnekkja sniði** í línunni þar sem á að hnekkja sniði.
3. Veljið sniðvalkostina sem á að nota fyrir þá línu í skýrslunni er valið í svarglugganum **Hnekkja sniði**.
4. Smelltu á **Í lagi**.

### <a name="currency-formatting"></a>Gjaldmiðilssnið

Gjaldmiðilssnið er notað fyrir upphæðir í peningum og því fylgir gjaldmiðilstákn. Eftirtaldir valkostir eru í boði:

- **Gjaldmiðilstákn** – Gjaldmiðilstákn skýrslunnar. Þetta gildi hnekkir stillingunni **Svæðisbundnir valkostir** í upplýsingum fyrirtækisins.
- **Neikvæðar tölur** – Neikvæðar tölur geta verið með mínusmerki (-), geta þau birtast í sviga, eða þær geta haft þríhyrningur (∆).
- **Aukastafir** – Fjöldi aukastafa eftir tugakommu.
- **Hnekkingartexti núllgildis** – Texti sem birtur er í skýrslunni þegar upphæðin er núll (0). Textinn birtist í síðustu línunni á svæðinu **Dæmi**.

    > [!NOTE]
    > Ef núllgildi eru falin við prentun eða engin virkni er á tímabilinu er þessi texti falinn.

### <a name="numeric-formatting"></a>Talnasnið

Snið gjaldmiðils við fjárhagsárs upphæð og inniheldur gjaldmiðilstáknið. Eftirtaldir valkostir eru í boði:

- **Neikvæðar tölur** – Neikvæðar tölur geta verið með mínusmerki (-), geta þau birtast í sviga, eða þær geta haft þríhyrningur (∆).
- **Aukastafir** – Fjöldi aukastafa eftir tugakommu.
- **Hnekkingartexti núllgildis** – Texti sem birtur er í skýrslunni þegar upphæðin er núll (0). Textinn birtist í síðustu línunni á svæðinu **Dæmi**.

    > [!NOTE]
    > Ef núllgildi eru falin við prentun eða engin virkni er á tímabilinu er þessi texti falinn.

### <a name="percentage-formatting"></a>Prósentusnið

Prósentusnið er með prósentumerki (%). Eftirtaldir valkostir eru í boði:

- **Neikvæðar tölur** – Neikvæðar tölur geta verið með mínusmerki (-), geta þau birtast í sviga, eða þær geta haft þríhyrningur (∆).
- **Aukastafir** – Fjöldi aukastafa sem er birtur eftir tugakommu.
- **Hnekkingartexti núllgildis** – Texti sem birtur er í skýrslunni þegar upphæðin er núll (0). Textinn birtist í síðustu línunni á svæðinu **Dæmi**.

    > [!NOTE]
    > Ef núllgildi eru falin við prentun eða engin virkni er á tímabilinu er þessi texti falinn.

### <a name="custom-formatting"></a>Sérsnið

Sérsniðsflokkurinn er notaður til að velja sérsniðna hnekkingu. Eftirtaldir valkostir eru í boði:

- **Gerð** – Sérsniðið.
- **Hnekkingartexti núllgildis** – Texti sem birtur er í skýrslunni þegar upphæðin er núll (0). Textinn birtist í síðustu línunni á svæðinu **Dæmi**.

    > [!NOTE]
    > Ef núllgildi eru falin við prentun eða engin virkni er á tímabilinu er þessi texti falinn.

Gerðin ætti að tákna jákvæða og neikvæða gildið. Yfirleitt er fært inn svipað snið sem skilur á milli jákvæðra og neikvæðra gilda. Til að tilgreina að bæði jákvætt og neikvætt gildi séu með tveimur aukastöfum, en neikvæð gildi birtast í sviga skal færa inn **0,00;(0,00)**. Eftirfarandi tafla inniheldur sérsnið sem hægt er að nota til að stýra sniði gilda þinna. Öll dæmi byrja frá gildi 1234.56.

| Snið                         | Jákvætt   | Neikvætt     | Núll    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);""       | 1.235      | (1.235)      | (Autt) |
| \#,\#\#0,00;(\#,\#\#0,00);núll | 1.234,56   | (1.234,56)   | núll    |
| 0,00%;(0,00%)                  | 123456,00% | (123456,00%) | 0,00%   |

## <a name="specify-a-normal-balance-cell"></a>Hólfið Eðlileg staða tilgreind
Hólfið **Eðlileg staða** í línuskilgreiningu stjórnar tákninu fyrir fjárhæðir í línu. Ef breyta á tákni línu eða ef eðlileg staða reiknings er kreditstaða skal færa **C** inn í hólfið **Eðlileg staða** fyrir viðkomandi línu. Skýrsluhönnun breytir tákninu fyrir alla kreditstöðureikninga í viðkomandi línu. Þegar Skýrsluhönnun breytir þessum reikningum fjarlægir það eiginleikann debet/kredit af öllum reikningum, og gerir þess vegna samantekt mjög einfalda. Sem dæmi má nefna að til að reikna út hreinar tekjur eru útgjöld dregin frá tekjum. Yfirleitt, **C**-kóði hefur ekki áhrif á samanteknar og útreiknaðar línur. Hinsvegar, **XCR**- stillingin fyrir prentun í dálkskilgreiningunni breytir tákni allra lína þar sem **C** kemur fyrir í dálkinum **Eðlileg staða**. Þetta snið er einkar mikilvægt þegar sýna á öll óæskileg frávik sem mínustölur. Ef samantekin eða útreiknuð tala er með röngu tákni skal setja **C** í hólfið **Eðlileg staða** til þess að breyta tákninu fyrir línuna.

## <a name="specify-a-row-modifier-cell"></a>Tilgreindu reit fyrir línubreytingu
Innihald hólfsins **Línubreyting** í línuskilgreiningu hnekkir fjárhagsárunum, tímabilum og öðrum upplýsingum sem tilgreindar eru í línuskilgreiningu fyrir þá línu. Valda breytingin gildir fyrir alla reikninga í línunni. Hægt er að breyta hverri línu með einni eða fleiri gerðum breytinga:

- Breytingar á reikningi
- Breytingar á bókarkóða
- Reikningseigindir og færslueigindir

### <a name="override-a-column-definition"></a>Dálkskilgreiningu hnekkt

1. Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.
2. Tvísmellið á hólfið **Línubreyting** í línunni þar sem hnekkja á dálkskilgreiningunni.
3. Í svarglugganum **línubreyting**, Veljið valkost í reitnum **Breyting á reikningi**. Lýsingar á valkostunum eru í Breytingar á reikningi hluta.
4. Í reitnum **Breyting bókarkóða** er valinn bókarkóði sem nota á fyrir línuna.
5. Undir **Eiginleikar** skaltu fylgja þessum skrefum til að bætt við færslu fyrir hvern eiginleika sem taka á með í línukóða:

    1. Tvísmellið á hólfið **Eigind** og veljið síðan eiginleikaheiti.

        > [!IMPORTANT]
        > Skiptið út númeratákninu (\#) fyrir talnagildi.

    2. Tvísmellið á hólfið **Frá** og færið inn fyrsta gildið fyrir sviðið.
    3. Tvísmellið á hólfið **Til** og færið inn síðasta gildið fyrir sviðið.

6. Smelltu á **Í lagi**.

### <a name="account-modifiers"></a>Breytingar á reikningi

Þegar tiltekinn reikningur er valinn sameinar Skýrsluhönnun yfirleitt reikninginn saman við fjárhagsárin, tímabilin og allar aðrar upplýsingar sem tilgreindar eru í dálkskilgreiningunni. Hægt er að nota mismunandi upplýsingar, svo sem mismunandi fjárhagsár, fyrir tilteknar línur. Eftirfarandi tafla sýnir lykrabreytingar sem eru tiltækar. Skiptið út tölutákninu (\#) fyrir gildi sem er jafnt eða minna en fjöldi tímabila á fjárhagsári.

| Breyting á reikningi | Hvað er prentað                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Upphafsstaða reiknings.                                                     |
| /\#              | Staða á tilgreindu tímabili.                                                     |
| /-\#             | Staða á tímabilinu sem kemur \# tímabilum á undan yfirstandandi tímabili.                  |
| /+\#             | Staða á tímabilinu sem kemur \# tímabilum á eftir yfirstandandi tímabili.                   |
| /C               | Staða á yfirstandandi tímabili.                                                       |
| /C-\#            | Staða á tímabilinu sem kemur \# tímabilum á undan yfirstandandi tímabili.                  |
| /C+\#            | Staða á tímabilinu sem kemur \# tímabilum á eftir yfirstandandi tímabili.                   |
| /Y               | Staða það sem af er ári á yfirstandandi tímabili.                                      |
| /Y-\#            | Staða það sem af er ári á tímabilinu sem kemur \# tímabilum á undan yfirstandandi tímabili. |
| /Y+\#            | Staða það sem af er ári á tímabilinu sem kemur \# tímabilum á eftir yfirstandandi tímabili.  |

### <a name="book-code-modifiers"></a>Breytingar á bókarkóða

Hægt er að takmarka línu við fyrirliggjandi bókarkóða. Línuskilgreiningin verður að taka með minnst einn **FD**-dálk sem er með bókarkóða.

> [!NOTE]
> Takmörkun bókarkóða fyrir línu hnekkir öllum bókarkóðatakmörkunum sem hefur verið úthlutað í dálkskilgreiningunni fyrir þá línu.

### <a name="account-and-transaction-attributes"></a>Reikningseigindir og færslueigindir

Sum bókhaldskerfi styðja reikningseigindir og færslueigindir í fjárhagsgögnum. Þessar eigindir virka eins og sýndarhlutar reikninga og geta flutt viðbótarupplýsingar um reikninginn eða færsluna. Þessi viðbótarupplýsingar gæti verið Kenni lykla, Kenni runu, póstnúmer, eða öðrum eigindum. Ef bókhaldskerfið sem unnið er með styður notkun eiginda er hægt að nota reikningseigindir eða færslueigindir sem línubreytingar í línuskilgreiningu. Frekari upplýsingar um hvernig á að hnekkja línuupplýsingum eru í Hnekkja dálkskilgreiningum fyrr í þessari grein.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Tilgreindu Tengill í fjárhagsvíddarhólf
Hólfið **Tengill í fjárhagsvíddir** inniheldur tengla í fjárhagsgögn sem taka á með í hverri línu skýrslunnar. Þetta hólf inniheldur víddargildi. Svarglugginn **Víddir** er opnaður með því að tvísmella á hólfið **Tengill í fjárhagsvíddir**.

> [!NOTE]
> Report Designer getur ekki valið reikninga, víddir eða reiti úr Microsoft Dynamics ERP kerfinu sem nota eftirfarandi frátekin stafatákn: &, \*, \[, \], {, eða }. Ef tilgreina á upplýsingar fyrir röð sem er nú þegar í línuskilgreiningu skal bæta upplýsingunum við í hólfinu **Tengill í fjárhagsvíddir**. Ef bæta á við nýjum línum sem tengja í fjárhagsgögn skal nota svargluggann **Setja inn línur úr** til að stofna nýjar línur í skýrsluskilgreiningunni. Dálkheitið breytist eftir því hvernig dálkurinn er grunnstilltur, eins og sýnt er í eftirfarandi töflu.

| tegund tengils sem er valin       | Lýsingin í tengildálkinum breytist í þetta |
|----------------------------------|----------------------------------------------------|
| Fjárhagsvíddir             | Tengill í fjárhagsvíddir                       |
| Skýrsluvinnublað                 | Skýrsla fjárhagsskýrslugerðar                         |

### <a name="specify-a-dimension-or-range"></a>Vídd eða svið tilgreind

1. Opnið skilgreiningu raðar í Report Designer til að gera breytingar.
2. Tvísmellið á hólfið í dálkinum **Tengill í fjárhagsvíddir**.
3. Í svarglugganum **Víddir** er tvísmellt á hólf undir víddarheitinu.
4. Í svarglugganum fyrir víddina skal velja **Stakur eða svið**.
5. Færið inn upphafsvídd í reitinn **Frá** eða smellið á ![Fletta.](media/browse.gif "Fletta") til að leita að tiltækum víddum. Ef færa á inn svið vídda skal færa inn lokavíddina í reitinn **Til**.
6. Smellið á **Í lagi** til að loka svarglugganum fyrir víddina. Uppfærða víddin eða sviðið er birt í svarglugganum **Víddir**.
7. Smellt er á **Í lagi** til að loka svarglugganum **Víddir**.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Núllstöðureikningar birtir í línuskilgreiningu
Sjálfgefið er að Skýrsluhönnun prentar ekki línu sem hefur ekki samsvarandi stöðu í fjárhagsgögnunum. Því er hægt að stofna eina línuskilgreiningu sem inniheldur öll gildi meginhluta eða öll víddargildi og nota síðan þá línuskilgreiningu fyrir hvaða deild sem er.

### <a name="modify-zero-balance-settings"></a>Stillingum núllstöðu breytt

1. Opnið skilgreiningu skýrslu í Skýrsluhönnun til að gera breytingar.
2. Í flipanum **stillingar**, Undir **Önnur snið** eru valdir valkostir fyrir línuskilgreininguna sem notuð er í skýrsluskilgreiningunni.
3. Á valmyndinni **Skrá** er smellt á **Vista** til að vista breytingarnar.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Notaðu Algildisstafir og svið í línuskilgreiningu
Þegar færð eru inn meginhlutagildi í svargluggann **Víddir** er hægt að setja algildisstaf (? eða \*) hvar sem er í hluta. Skýrsluhönnun tekur út öll gildi fyrir skilgreindu stöðurnar án tillits til algildisstafanna. Til dæmis línuskilgreiningarinnar inniheldur aðeins gildi meginhluta, og meginhlutar hafa fjórir stafir. Með því að færa inn **6???** í röð, er verið að biðja Report Designer að taka með alla reikninga sem hafa gildi meginhluta sem byrjar á 6. Ef fært er inn **6\**_, eru sömu niðurstöður fengnar, en niðurstöður sýna einnig vídd-breidd gildi, eins og _* 60** og **600000**. Skýrsluhönnun skiptir út öllum algildisstöfum (?) fyrir allt svið mögulegra gilda, þar á meðal bókstafi og sérstafi. Til dæmis á sviðinu frá **12?0** til **12?4**, er algildisstafnum í **12?0** skipt út fyrir lægsta gildi stafamengisins og algildisstafnum í **12?4** er skipt út fyrir hæsta gildið í stafamenginu.

> [!NOTE]
> Forðast ætti notkun algildistafa í sviðum fyrir upphafs- og endareikningana. Ef algildistafir eru notaðir annaðhvort fyrir upphafsreikninginn eða endareikninginn getur það skilað óvæntum niðurstöðum.

### <a name="single-segment-or-single-dimension-ranges"></a>Svið stakra hluta eða stakra vídda

Hægt er að tilgreina svið hlutagilda eða víddargilda. Kostur þess að tilgreina svið er að þá þarf ekki að uppfæra línuskilgreininguna í hvert skipti sem nýju hlutagildi eða víddargildi er bætt við fjárhagsgögnin. Til dæmis sækir sviðið **Reikningur=\[6100:6900\]** gildin frá reikningi 6100 til reiknings 6900, meðtalið, og færir í línuupphæðina. Þegar svið inniheldur algildisstaf (?) metur Skýrsluhönnun ekki sviðið bókstaf fyrir bókstaf. Þess í stað eru lágu og háu endar sviðsins skilgreindir og svo eru endagildin öll gildi á milli þeirra innifalin að auki.

> [!NOTE]
> Report Designer getur ekki valið reikninga, víddir eða reiti úr Microsoft Dynamics ERP kerfinu sem nota eftirfarandi frátekin stafatákn: &, \*, \[, \], {, eða }. Aðeins er hægt að nota og-merki (&) þegar línuskilgreiningar eru búnar til sjálfkrafa með því að nota svargluggann **Setja inn línur úr víddum**.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Svið margra hluta eða margra vídda

Þegar fært er inn svið með því að nota samsetningu margra víddargilda næst sviðssamanburðurinn á ..\\fjárhags-víddir\\vídd fyrir vídd. Sviðssamanburðurinn næst ekki staf fyrir staf eða út frá ókláruðum hluta. Til dæmis inniheldur afmörkun **+ Reikningur=\[5000:6000\], Deild=\[1000:2000\] Kostnaðarstaður=\[00\]** aðeins þá reikninga sem stemma hvern hluta. Í þessu dæmi verður fyrsta vídd að vera á bilinu 5000 til 6000, önnur vídd verður að vera á bilinu 1000 til 2000 og síðusta vídd verður að vera 00. Til dæmis er **+ Reikningur=\[5100\], Deild =\[1100\], Kostnaðarstaður=\[01\]** ekki tekinn með í skýrslunni, þar sem síðasti hluti er utan tilgreinds sviðs. Ef hlutagildi inniheldur bil, ber að hafa það gildi innan hornklofa (\[ \]). Eftirfarandi gildi eru gild fyrir fjögurra stafa hluta: **\[ 234\], \[123 \], \[1 34\]**. Víddargildi ættu að vera innan hornklofa (\[ \]), og Report Designer sér um að gera það fyrir þig. Þegar svið margra hluta eða margra vídda inniheldur algildisstafi (? eða \*) eru lág- og háendar alls sviðs margra hluta eða margra vídda ákvarðaðir, og þá eru endarnir og öll gildi á milli þeirra innifalin. Ef um stórt svið er að ræða, til dæmis svið allra reikninga frá 40000 til og með 99999, ætti að tilgreina gilda upphafs- og endareikninga, þegar kostur er á.

> [!NOTE] 
> Report Designer getur ekki valið reikninga, víddir eða reiti úr Microsoft Dynamics ERP kerfinu sem nota eftirfarandi frátekin stafatákn: &, \*, \[, \], {, eða }. Aðeins er hægt að nota og-merki (&) þegar línuskilgreiningar eru búnar til sjálfkrafa með því að nota svargluggann **Setja inn línur úr víddum**.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Bætt við og dregið frá öðrum reikningum í línuskilgreiningu
Ef bæta á við eða draga peningaupphæðir í einum reikningi frá peningaupphæðum í öðrum reikningi er hægt að nota plúsmerkið (+) og mínusmerkið (-) í hólfinu **Tengill í fjárhagsvíddir**. Eftirfarandi tafla sýnir viðunandi snið þegar tenglum er bætt við eða þeir dregnir frá fjárhagsgögnum.

| Aðgerð                                                                               | Nota þetta snið                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Bæta við tveimur Fullnægjandi lyklum.                                                       | +Svið=\[000\], Reikningur=\[1205\], Deild=\[00\]+Svið=\[100\], Reikningur=\[1205\], Deild=\[00\] |
| Bæta við tveimur hlutagildum                                                                 | +Reikningur=\[1205\]+Reikningur=\[1210\]                                                                           |
| Bæta við hlutagildum sem innihalda algildisstafi                                    | +Reikningur=\[120?+Reikningur=\[11??\]                                                                             |
| Bæta við sviði heildstæða reikninga                                                | +Svið=\[000:100\], Reikningur=\[1205\], Deild=\[00\]                                                   |
| Bæta við sviði hlutagilda                                                          | +Reikningur=\[1200:1205\]                                                                                       |
| Bæta við sviði hlutagilda sem innihalda algildisstafi                         | +Reikningur=\[120?:130?\]                                                                                       |
| Draga einn heildstæðan reikning frá öðrum heildstæðum reikningi.              | +Svið=\[000\], Reikningur=\[1205\], Deild=\[00\]-Svið=\[100\], Reikningur=\[1205\], Deild=\[00\] |
| Draga eitt hlutagildi frá öðru hlutagildi                                  | +Reikningur=\[1205\]-Reikningur=\[1210\]                                                                           |
| Draga hlutagildi sem inniheldur algildisstaf frá öðru hlutagildi | +Reikningur=\[1200\]-Reikningur=\[11??\]                                                                           |
| Draga frá sviði heildstæða reikninga                                           | -Svið=\[000:100\], Reikningur=\[1200:1205\], Deild=\[00:01\]                                           |
| Draga frá svið hlutagilda                                                     | -Reikningur=\[1200:1205\]                                                                                       |
| Draga frá svið hlutagilda sem innihalda algildisstafi                    | -Reikningur=\[120?:130?\]                                                                                       |

Þótt hægt sé að breyta reikningum með beinum hætti er einnig hægt að nota svargluggann **Víddir** til að nota rétt snið á fjárhagslega gagnatengla. Hvert og eitt gildi getur innihaldið algildisstafi (? eða \*). Hins vegar getur Report Designer ekki valið reikninga, víddir eða reiti úr Microsoft Dynamics ERP kerfinu sem nota eftirfarandi frátekin stafatákn: &, \*, \[, \], {, eða }.

> [!NOTE]
> Ef draga á frá gildi verður að setja þau gildi innan sviga. Ef til dæmis er slegið inn **450?-(4509)** birtist það sem **+Reikningur=\[4509\]-reikningur=\[450?\]** og verið er að gefa Report Designer skipun um að draga upphæðina fyrir reikningshluta 4509 frá upphæðinni fyrir hvaða reikningshluta sem er sem byrjar á 450.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Reikningum bætt við eða þeir dregnir frá öðrum reikningum

1. Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.
2. Tvísmellið á hólfið í dálkinum **Tengill í fjárhagsvíddir** í viðkomandi línu.
3. Í fyrstu línu svargluggans **Víddir** skal fylgja þessum skrefum:

    1. Veljið allar víddir (sjálfgefið) í fyrsta reitnum, eða smellið til að opna svargluggann **Vinna með samstæður víddargilda** þar sem má búa til, breyta, afrita eða eyða samstæðu.
    2. Tvísmellið á hólfið **Virki +/-** og veljið virknitáknið plús (**+**) eða mínus (**-**) eftir því sem við á um eitt eða fleiri víddargildi eða -samstæður í línunni.
    3. Tvísmellið á hólfið í viðkomandi víddargildisdálki til að opna svarglugga **vídda** og veljið hvort þetta er Stakur eða svið, Víddargildissamstæða eða Samtölur reikninga. Fyrir Lýsingar á svæðum í á **Víddir** svarglugganum, sjá hlutann "Lýsingu á vídd svarglugganum".
    4. Færið inn hlutagildi í dálkinn **Frá** og dálkinn **Til**.

4. Endurtakið skref 2 til og með 3 til að bæta við fleiri aðgerðum.

> [!NOTE]
> Virkinn á alltaf við um allar víddirnar í línunni.

## <a name="description-of-the-dimensions-dialog-box"></a>Lýsing á víddasvarglugganum
**Vídda** svarglugginn inniheldur reitina sem lýst er í eftirfarandi töflu.

| Vara                | Lýsing |
|---------------------|-------------|
| Stakur eða svið | Í reitinn **Frá** skal slá inn heiti reiknings eða smella á **Fletta** hnappinn til að ![fletta.](media/browse.gif "Fletta") til að fletta í reikningum. Til að velja svið skal slá inn eða fletta upp á gildi í reitnum **Til**. |
| Víddargildissamstæða | Sláið heiti víddargildissamstæðu inn í reitinn **Heiti**. Til að búa til, breyta, afrita eða eyða samstæðu skal smella á **Vinna með samstæður víddargilda**. **Formúla** reiturinn er skipaður formúlunni úr hólfinu **Tengill í fjárhagsvídd** fyrir þessa samstæðu fjárhagsvídda í línuskilgreiningunni. |
| Samtölur reikninga   | Í reitnum **Heiti** skal slá inn heiti reiknings eða fletta yfir í vídd samtölureikninga. Reiturinn fyrir **formúlu** er skipaður formúlunni úr hólfinu **Tengill í fjárhagsvídd** fyrir þessa samstæðu fjárhagsvídda í línuskilgreiningunni. |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Samstæðum víddagilda bætt við línuskilgreiningu
Víddargildissamstæða er hópur víddargilda með tilteknu heiti. Í víddargildissamstæðu geta einungis verið gildi í einni vídd en hægt er að nota víddargildissamstæðu í mörgum línu-, dálk-, skipurita- og skýrsluskilgreiningum. Einnig er hægt að sameina víddargildasamstæður í skýrsluskilgreiningu. Þegar breyting á fjárhagsgögnum notanda krefst þess að víddargildissamstæðu sé breytt, er hægt að uppfæra skilgreiningu víddargildissamstæðunnar og nær sú uppfærsla til allra svæða sem nota víddargildissamstæðuna. Ef notandi til dæmis tilgreinir oft svið gilda sem tengja á við fjárhagsgögn notanda, eins og gildi frá 5100 til og með 5600, er hægt að úthluta þessu sviði til lyklasafns sem gefið er heitið Sala. Þegar samstæða víddargilda hefur verið stofnuð getur notandinn valið þá samstæðu sem fjárhagsgagnatengil sinn. Svo annað dæmi sé tekið, ef gildissviðið 5100 til 5600 er úthlutað til Sala og 4175 úthlutað til Afslættir er hægt að ákvarða heildarsöluna með því að draga afslætti frá sölu. Þessi virkni er táknuð sem **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Samstæða víddargilda stofnuð

1. Opnið línu-, dálk- eða skipuritsskilgreiningu í Skýrsluhönnun til að gera breytingar.
2. Á valmyndinni **Breyta** er smellt á **Vinna með samstæður víddargilda**.
3. Í svarglugganum **Vinna með samstæður víddargilda** er valin tegund víddargildasamstæðunnar sem stofna á í reitnum **Vídd** og síðan smellt á **Nýtt**.
4. Færið inn heiti og lýsingu fyrir samstæðuna í svarglugganum **Nýtt**.
5. Í dálkinum **Frá** er tvísmellt inn í hólf.
6. Í svarglugganum **lykill**, Veljið reikningsheiti á listanum eða leitið að færslu í reitinum **Leita**. Svo er smellt á **Í lagi**.
7. Endurtakið skref 5 til 6 í dálkinum **Til** til að hanna formúlu fyrir það virknitákn.
8. Þegar lokið er við formúluna skal smella á **Í lagi**.
9. Í svarglugganum **Vinna með víddasamstæður** er smellt á **Loka**.

### <a name="update-a-set-of-dimension-values"></a>Samstæða víddargilda uppfærð

1. Opnið línu-, dálk- eða skipuritsskilgreiningu í Report Designer til að gera breytingar.
2. Á valmyndinni **Breyta** er smellt á **Vinna með samstæður víddargilda**.
3. Í svarglugganum **Vinna með samstæður víddargilda** er valin tegund víddar í reitnum **Vídd**.
4. Veljið víddargildissamstæðu sem á að uppfæra af listanum og smellið á **Breyta**.
5. Í svarglugganum **Breyta** er formúlugildunum breytt þannig að þau innihaldi samstæðuna.

    > [!NOTE]
    > Ef nýjum reikningi eða víddum er bætt við verður að tryggja að fyrirliggjandi víddargildasamstæðum sé breytt til samræmis við breytingarnar.

6. Tvísmellið á hólfið til að velja viðeigandi virkja, **Frá**-reikning og **Til**-reikning.
7. Smellið á **Í lagi** til að loka svarglugganum **Breyta** og vista breytingarnar.

### <a name="copy-a-dimension-set"></a>Víddasamstæða afrituð

1. Opnið línu-, dálk- eða skipuritsskilgreiningu í Skýrsluhönnun til að gera breytingar.
2. Á valmyndinni **Breyta** er smellt á **Vinna með samstæður víddargilda**.
3. Í svarglugganum **Vinna með samstæður víddargilda** er valin tegund víddar í reitnum **Vídd**.
4. Veljið samstæðuna sem á að afrita á listanum og smellið svo á **Vista sem**.
5. Færið inn nýtt heiti fyrir afrituðu samstæðuna og smellið á **Í lagi**.

### <a name="delete-a-dimension-set"></a>Víddasamstæðu eytt

1. Opnið línu-, dálk- eða skipuritsskilgreiningu í Report Designer til að gera breytingar.
2. Á valmyndinni **Breyta** er smellt á **Vinna með samstæður víddargilda**.
3. Í svarglugganum **Vinna með samstæður víddargilda** er valin tegund víddar í reitnum **Vídd**.
4. Samstæðan sem á að eyða er valin og svo er smellt á **Eyða**. Smellið á **Já** til að eyða víddagildasamstæðunni varanlega.

## <a name="additional-resources"></a>Frekari upplýsingar

[Fjárhagsskýrslugerð](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
