---
title: Setja upp lágmark og hámark fyrir áfyllingarferli
description: Þessi verklýsing sýnir hvernig á að setja upp nýja áfyllingarvinnslu sem notar hámark/lágmark áfyllingaráætlun.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3aafd9b77b34328a9adb0571e6935aea748f2a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847152"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Setja upp lágmark og hámark fyrir áfyllingarferli

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp nýja áfyllingarvinnslu sem notar hámark/lágmark áfyllingaráætlun. Þegar birgðir fara niður fyrir lágmarkið, verður stofnuð vinna til að fylla á staðsetninguna. Ferlið sýnir einnig hvernig á að nota fast tiltektarstaðsetningar til að leyfa endurnýjun stofna jafnvel þótt birgðir fara niður fyrir lágmark stig og hvernig á að virkja áfyllingarvinnslu til að keyra reglulega með því að nota runuvinnslu. Þessi verkefni myndu yfirleitt vera framkvæmd af yfirmanni vöruhúss. Hægt er að keyra þetta ferli á USMF sýnifyrirtæki með dæmagildum úr glósum eða hægt er að keyra hana á eigin gögn. Ef verið er að nota eigin gögn, skal ganga úr skugga um að hafa vöruhús sem er virkt fyrir vöruhúsakerfisferli.


## <a name="create-a-fixed-picking-location"></a>Stofna fastar tiltektarstaðsetningar
1. Fara í vöruhúsakerfi > Uppsetning > Vöruhús > Fastar staðsetningar.
    * Er valfrjáls verkefni fyrir áfyllingu lágm-hám en ef fastan tiltektarstað er notaður er hægt að fylla á birgðir jafnvel þó hún fellur undir lágmarksstig, þar sem kerfið getur ákvarðað hvaða vörur þarf að fylla á, jafnvel þótt engar séu eftir.  
2. Smellið á „Nýtt“.
3. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Ef verið er að nota USMF er hægt að velja vöru A0001.  
4. Sláið inn eða veldu gildi í reitnum svæði.
    * Ef verið er að nota USMF er hægt að velja ‚svæði 2‘.  
5. Sláðu inn eða veldu gildi í reitnum Vöruhús.
    * Ef verið er að nota USMF er hægt að velja vöruhús 24.  
6. Sláið inn eða veldu gildi í staðsetning reitnum.
    * Ef verið er að nota USMF er hægt að velja CP 003.  
7. Lokið síðunni.

## <a name="create-a-replenishment-location-directive"></a>Stofna staðsetningarleiðbeiningar áfyllingar
1. Fara í vöruhúsakerfi > Uppsetning > Staðsetningarleiðbeiningar.
    * Staðsetningarleiðbeiningar eru notaðar til að ákvarða hvaðan á að taka vörur í áfyllingarferlinu.  
2. Í svæðinu gerð vinnupöntunar, skal velja áfylling.
3. Smellið á „Nýtt“.
4. Í reitinn Heiti skal slá inn gildi.
5. Veljið í svæðinu vinnutegund 'Taka'.
6. Sláið inn eða veldu gildi í reitnum svæði.
    * Ef verið er að nota USMF er hægt að velja ‚svæði 2‘.  
7. Sláðu inn eða veldu gildi í reitnum Vöruhús.
    * Ef verið er að nota USMF er hægt að velja vöruhús 24.  
8. Smellið á „Vista“.
9. Smellið á „Nýtt“.
10. Í listanum skal merkja valda línu.
11. Í reitinn Til magn skal slá inn númer.
    * Til dæmis er hægt að nota 9999.  
12. Veljið gátreitinn leyfa að skipta.
    * Ef þessi valkostur er valinn leyfir ferli verkstofnunar línumagn vinnu að skiptast á marga stöðum.  
13. Smellið á „Vista“.
14. Smellið á „Nýtt“.
15. Í listanum skal merkja valda línu.
16. Í reitinn Heiti skal slá inn gildi.
17. Smellið á „Vista“.
18. Smellt er á Breyta fyrirspurn.
    * Hægt er að breyta þessari fyrirspurn til að bæta við takmarkanir þar sem hægt að velja úr birgðum við áfyllingarferlið. Til dæmis, gæti verið að birgðir á aðeins að nota frá megingeymslusvæði vöruhússins.  
19. Smellið á „Í lagi“.
20. Lokið síðunni.

## <a name="create-a-replenishment-work-template"></a>Stofna áfyllingarsniðmát verks
1. Fara í vöruhúsakerfi > Uppsetning > Vinna > Vinnusniðmát.
    * Vinnusniðmátið er notuð til að leiðbeina kerfið um hvernig verður að stofna lágm. / hám. áfyllingar. Að lágmark verður að vera vinnusniðmátslínu fyrir tiltekt og frágang. Vinnusniðmátið segir hún er Ógild þar til allar nauðsynlegar upplýsingar hefur verið fyllt út.  
2. Í svæðinu gerð vinnupöntunar, skal velja áfylling.
3. Smellið á „Nýtt“.
4. Færa inn gildi í reitnum Vinnusniðmát.
5. Smellið á „Vista“.
6. Smellið á „Nýtt“.
7. Veljið í svæðinu vinnutegund 'Taka'.
8. Færa inn eða velja gildi í reitnum Kenni Vinnuklasa.
    * Þetta ætti að vera vinnuklasi sem tengjast áfyllingu. Ef verið er að nota USMF, veldu fylla á.  
9. Smellið á „Nýtt“.
10. Í listanum skal merkja valda línu.
11. Í reitnum Vinnutegund velurðu ‚Frágangur‘.
12. Færa inn eða velja gildi í reitnum Kenni Vinnuklasa.
13. Smellið á „Vista“.
14. Lokið síðunni.

## <a name="create-a-new-replenishment-template"></a>Stofnið nýjan áfyllingarsniðmát.
1. Fara í vöruhúsakerfi > Uppsetning > Áfylling > Áfyllingarsniðmát.
    * Áfyllingarsniðmát er notað til að skilgreina vörur og magn, og staðsetningu fyrir áfyllingu.  
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum áfyllingarsniðmát.
    * Gefðu sniðmátinu heiti til að gefa til kynna að það er ætlað fyrir hám./lágm. áfyllingu.  
4. Sláið inn gildi í reitnum „Lýsing“.
5. Veldu gátreitinn leyfa bylgjueftirspurn að nota magn sem ekki er frátekið.
    * Ef þessi valkostur er valinn virkjar hann eftirspurnarbylgju áfyllingar sem á að nota magn sem tengjast lágm. / hám. áfyllingu. Til dæmis, þetta gæti verið gagnlegt ef lágm. / hám áfyllingarvinnu var ekki unnin strax, til að koma í veg fyrir óþarfa eftirspurn áfyllingarvinnu.  
6. Smellið á „Nýtt“.
7. Í reitinn raðnúmer skal slá inn númer.
8. Sláið inn gildi í reitnum „Lýsing“.
9. Í listanum skal merkja valda línu.
10. Færa inn eða veljið gildi í reitinn áfyllingareining.
    * Veljið til dæmis stk. Þetta er nauðsynleg stilling. Það gerir mögulegt að tilgreina aðra mælieiningar áfyllingarvinnu borin saman við einingu sem er tilgreind fyrir sem lágmark og hámark geymslustig í þessu sniðmáti.  
11. Sláið inn eða veldu gildi í reitnum vinnusniðmát.
    * Velja sniðmát sem búið var til áður.  
12. Í reitinn lágmarksmagn skal slá inn númer.
    * Velja lágmarksmagn sem setur af stað áfylling. T.d. stilla á 50. Mögulegt er að skilja eftir þessa stillt á núll, ef verið er að fylla á föst staðsetning og fylla á auðar fastar staðsetningar valkostur er stilltur á Já. Einnig er ráðlagt að velja fylla á aðeins fastar staðsetningar valkost til að skila betri afköstum.  
13. Í reitinn hámarksmagn skal slá inn númer.
    * T.d. stilla á 100.  
14. Í reitinn eining skal slá inn eða velja gildi.
    * Úthluta einingu fyrir lágmarks- og hámarksmagn. T.d. stilla á stk.  
15. Velja skal gátreitinn fylla á auða föstum stöðum.
    * Velja skal þennan reit til að fylla á föstum stöðum þegar þeir eru tóm. Annars eru einungis þær staðsetningar þar sem er magn á lager fylltar.  
16. Velja skal gátreitinn fylla aðeins á föstum stöðum.
17. Smellið á Velja afurðir.
    * Staðurinn til að skilgreina hvaða vörur eiga að fylla á. Ef Fast tiltektarstaðsetning valkostur er valinn þarf einnig að skilgreina staðsetningar í þessari fyrirspurn. Fyrirspurnir sem byggjast á afbrigðum eru tiltæk, sem og fyrirspurnir tengdar ákveðnum vörum.  
18. Veljið vöruröðina.
19. Í reitinn Skilyrði skal slá inn gildi.
    * Veljið þær vörur sem á að fylla á föstum staðsetningum. Til dæmis sláið inn A* til að velja allar vörunúmer sem byrjar á A.  
20. Smelltu á Bæta við.
    * Bæta við Staðsetningu einingar (nema það sé þegar til) til að hægt sé að takmarka áfyllingarvinnu fasta tiltektarstaðsetningar innan tiltekins svæði vöruhúss.  
21. Í listanum skal merkja valda línu.
22. Stillið töflusvæðið á Staðsetningum.
23. Í svæðinu Svæði skal slá inn Auðkenni forstillingar staðsetningar.
24. Í reitinn Skilyrði skal slá inn eða veldu gildi.
25. Smellið á „Í lagi“.
26. Lokið síðunni.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Setja upp áfyllingaferlið til að keyra sem runuvinnslu.
1. Fara í vöruhúsakerfi > Áfylling > Áfyllingar.
    * Síðan áfyllingar gerir kleift að setja upp áfyllingar til að keyra sem runuvinnslu eða til að gera kröfu um að það er ræst handvirkt.  
2. Smellt er á Síu.
3. Í listanum skal merkja valda línu.
4. Í reitinn Skilyrði skal slá inn eða veldu gildi.
5. Smellt er á Í lagi.
6. Stækka útvíkkun á liðnum Keyra í bakgrunni.
7. Stillið runuvinnsluvalkost á Já.
8. Smellið á Endurtekning.
9. Velja Valkosturinn enginn valkostur um lokadag.
10. Velja endurtekningarmynstur.
    * Til dæmis velja dagar.  
11. Smellið á „Í lagi“.
12. Smellið á „Í lagi“.

