---
title: Setja upp lágmark og hámark fyrir áfyllingarferli
description: Þessi verklýsing sýnir hvernig á að setja upp nýja áfyllingarvinnslu sem notar hámark/lágmark áfyllingaráætlun.
author: perlynne
ms.date: 10/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence, WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0fbfcceece2883c32a266bcbe659211b0b56ce
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069727"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Setja upp lágmark og hámark fyrir áfyllingarferli

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp nýja áfyllingarvinnslu sem notar hámark/lágmark áfyllingaráætlun. Þegar birgðir fara niður fyrir lágmarkið, verður stofnuð vinna til að fylla á staðsetninguna. Ferlið sýnir einnig hvernig á að nota fast tiltektarstaðsetningar til að leyfa endurnýjun stofna jafnvel þótt birgðir fara niður fyrir lágmark stig og hvernig á að virkja áfyllingarvinnslu til að keyra reglulega með því að nota runuvinnslu. Þessi verkefni myndu yfirleitt vera framkvæmd af yfirmanni vöruhúss. Hægt er að keyra þetta ferli á USMF sýnifyrirtæki með dæmagildum hér að neðan eða hægt er að keyra það á eigin gögn. Ef verið er að nota eigin gögn, skal ganga úr skugga um að hafa vöruhús sem er virkt fyrir vöruhúsakerfisferli (vöruhúsakerfi).


## <a name="create-a-fixed-picking-location"></a>Stofna fastar tiltektarstaðsetningar
1. Farðu í **Skoðunnarúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Vöruhús > Fastar staðsetningar**. Er valfrjáls verkefni fyrir áfyllingu lágm-hám en ef fastan tiltektarstað er notaður er hægt að fylla á birgðir jafnvel þó hún fellur undir lágmarksstig, þar sem kerfið getur ákvarðað hvaða vörur þarf að fylla á, jafnvel þótt engar séu eftir.
2. Smellt er á **Nýtt**.
3. Í reitinn **Vörunúmer** skal slá inn eða velja gildi. Ef þú ert að nota USMF er hægt að velja vöru A0001.  
4. Í reitnum **Svæði** slærðu inn eða velur gildi. Ef verið er að nota USMF er hægt að velja svæði 2.  
5. Í reitnum **Vöruhús** slærðu inn eða velur gildi. Ef verið er að nota USMF er hægt að velja vöruhús 24.  
6. Í reitinn **Staðsetning** slærðu inn eða velur gildi. Ef verið er að nota USMF er hægt að velja CP-003.  
7. Lokið síðunni.

## <a name="create-a-replenishment-location-directive"></a>Stofna staðsetningarleiðbeiningar áfyllingar
1. Farðu í **Vöruhúsakerfi > Uppsetning > Staðsetningarleiðbeiningar**. Staðsetningarleiðbeiningar eru notaðar til að ákvarða hvaðan á að taka vörur í áfyllingarferlinu.
2. Í reitnum **Gerð vinnupöntunar** velurðu Áfylling.
3. Í **aðgerðasvæðinu** er smellt á **Nýtt**.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitnum **Vinnutegund** velurðu Taka til.
6. Í reitnum **Svæði** slærðu inn eða velur gildi. Ef verið er að nota USMF er hægt að velja svæði 2.  
7. Í reitnum **Vöruhús** slærðu inn eða velur gildi. Ef verið er að nota USMF er hægt að velja vöruhús 24.  
8. Smellt er á **Vista**.
9. Í kaflanum **Línur** skaltu smella á **Nýtt**.
10. Í listanum skal merkja valda línu.
11. Í reitinn **Til magns** skal slá inn númer. Til dæmis er hægt að nota 9999.  
12. Veldu gátreitinn **Leyfa að skipta**. Ef þessi valkostur er valinn leyfir ferli verkstofnunar línumagn vinnu að skiptast á marga stöðum.  
13. Smellt er á **Vista**.
14. Í hlutanum **Aðgerðir í staðsetningarleiðbeiningum** smellirðu á **Nýtt**.
15. Í listanum skal merkja valda línu.
16. Í reitinn **Heiti** skal slá inn gildi.
17. Smellt er á **Vista**.
18. Á **Aðgerðasvæði** er smellt á **Breyta fyrirspurn**. Hægt er að breyta þessari fyrirspurn til að bæta við takmarkanir þar sem hægt að velja úr birgðum við áfyllingarferlið. Til dæmis, gæti verið að birgðir á aðeins að nota frá megingeymslusvæði vöruhússins.
19. Smellt er á **OK**.
20. Lokið síðunni.

## <a name="create-a-replenishment-work-template"></a>Stofna áfyllingarsniðmát verks
1. Farðu í **Vöruhúsakerfi > Uppsetning > Vinna > Vinnusniðmát**. Vinnusniðmátið er notuð til að leiðbeina kerfið um hvernig verður að stofna lágm. / hám. áfyllingar. Að lágmark verður að vera vinnusniðmátslínu fyrir tiltekt og frágang. Vinnusniðmátið segir hún er Ógild þar til allar nauðsynlegar upplýsingar hefur verið fylltar út. 
2. Í reitnum **Gerð vinnupöntunar** velurðu Áfylling.
3. Í **aðgerðasvæðinu** er smellt á **Nýtt**.
4. Í reitnum **Vinnusniðmát** skal færa inn gildi.
5. Smellt er á **Vista**.
6. Í **upplýsingahluta vinnusniðmáts** smellirðu á **Nýtt**.
7. Í reitnum **Vinnutegund** velurðu Taka til.
8. Í reitnum **Kenni vinnuklasa** skal færa inn eða velja gildi. Þetta ætti að vera vinnuklasi sem tengjast áfyllingu. Ef verið er að nota USMF velurðu Fylla á.  
9. Í **upplýsingahluta vinnusniðmáts** smellirðu á **Nýtt**.
10. Í listanum skal merkja valda línu.
11. Í reitnum **Vinnutegund** velurðu ‚Frágangur‘.
12. Í reitnum **Kenni vinnuklasa** skal færa inn eða velja gildi.
13. Smellt er á **Vista**.
14. Lokið síðunni.

## <a name="create-a-new-replenishment-template"></a>Stofnið nýjan áfyllingarsniðmát.
1. Farðu í **Vöruhúsakerfi > Uppsetning > Áfylling > Áfyllingarsniðmát**. Áfyllingarsniðmát er notað til að skilgreina vörur og magn, og staðsetningu fyrir áfyllingu.
2. Í **aðgerðasvæðinu** er smellt á **Nýtt**.
3. Í reitnum **Áfyllingarsniðmát** skaltu rita gildi. Gefðu sniðmátinu heiti til að gefa til kynna að það er ætlað fyrir hám./lágm. áfyllingu.  
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Veldu gátreitinn **Leyfa bylgjueftirspurn að nota magn sem ekki er frátekið**. Ef þessi valkostur er valinn virkjar hann eftirspurnarbylgju áfyllingar sem á að nota magn sem tengjast lágm. / hám. áfyllingu. Til dæmis gæti þetta verið gagnlegt ef lágm./hám. áfyllingarvinnu er ekki unnið strax, til að koma í veg fyrir óþarfa eftirspurn áfyllingarvinnu.
6. Í **Upplýsingahluta áfyllingarsniðmáts** smellirðu á **Nýtt**.
7. Í reitinn **Raðnúmer** skal slá inn númer.
8. Í reitinn **Lýsing** skal slá inn gildi.
9. Í listanum skal merkja valda línu.
10. Í reitnum **Áfyllingareining** færirðu inn eða velur gildi. Veljið til dæmis stk. Þetta er nauðsynleg stilling. Það gerir mögulegt að tilgreina aðra mælieiningar áfyllingarvinnu borin saman við einingu sem er tilgreind fyrir sem lágmark og hámark geymslustig í þessu sniðmáti.
11. Í reitnum **Vinnusniðmát** færirðu inn eða velur gildi. Velja sniðmát sem búið var til áður.  
12. Í reitinn **Lágmarksmagn** skal slá inn tölu. Velja lágmarksmagn sem setur af stað áfylling. T.d. stilla á 50. Mögulegt er að skilja eftir þessa stillt á núll, ef verið er að fylla á fasta staðsetningu og valkosturinn **Fylla á auðar fastar staðsetningar** er stilltur á Já. Einnig er ráðlagt að velja valkostinn **Fylla aðeins á fastar staðsetningar** til að skila betri afköstum.
13. Í reitinn **Hámarksmagn** skal slá inn tölu. T.d. stilla á 100.  
14. Í reitinn **Eining** skal slá inn eða velja gildi. Úthluta einingu fyrir lágmarks- og hámarksmagn. T.d. stilla á stk.  
15. Veldu gátreitinn **Fylla á auðar fastar staðsetningar**. Velja skal þennan reit til að fylla á föstum stöðum þegar þeir eru tóm. Annars eru einungis þær staðsetningar þar sem er magn á lager fylltar.
16. Veldu gátreitinn **Fylla aðeins á fastar staðsetningar**.
17. Smelltu á **Velja afurðir**. Staðurinn til að skilgreina hvaða vörur eiga að fylla á. Ef Fast tiltektarstaðsetning valkostur er valinn þarf einnig að skilgreina staðsetningar í þessari fyrirspurn. Fyrirspurnir sem byggjast á afbrigðum eru tiltæk, sem og fyrirspurnir tengdar ákveðnum vörum.
18. Veldu línuna **Vörur**.
19. Í reitnum **Skilyrði** skal slá inn gildi. Veljið þær vörur sem á að fylla á föstum staðsetningum. Til dæmis sláið inn A* til að velja allar vörunúmer sem byrjar á A.
20. Smelltu á **Bæta við**. Bæta við Staðsetningu einingar (nema það sé þegar til) til að hægt sé að takmarka áfyllingarvinnu fasta tiltektarstaðsetningar innan tiltekins svæði vöruhúss.
21. Í listanum skal merkja valda línu.
22. Stilltu reitinn **Tafla** á Staðsetningar.
23. Í reitinn **Reitur** skal velja Kenni forstillingar staðsetningar.
24. Í reitinn **Skilyrði** skal slá inn eða velja gildi.
25. Smellt er á **OK**.
26. Lokið síðunni.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Setja upp áfyllingaferlið til að keyra sem runuvinnslu.
1. Farðu í **Vöruhúsakerfi > Áfylling > Áfyllingar**. Síðan áfyllingar gerir kleift að setja upp áfyllingar til að keyra sem runuvinnslu eða til að gera kröfu um að það er ræst handvirkt.
2. Smella á **Sía**.
3. Í listanum skal merkja valda línu.
4. Í reitinn **Skilyrði** skal slá inn eða velja gildi.
5. Smellt er á **OK**.
6. Stækkaðu hlutann **Keyra í bakgrunni**.
7. Stilltu valkostinn **Runuvinnsla** á Já.
8. Smelltu á **Endurtekning**.
9. Veldu valkostinn **Engin lokadagsetning**.
10. Stilltu **Endurtekningarmynstur**. Til dæmis velja dagar.  
11. Smellt er á **OK**.
12. Smellt er á **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]