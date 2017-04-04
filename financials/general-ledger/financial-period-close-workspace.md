---
title: "Vinnusvæði lokunar fjárhagstímabils"
description: "Þessi skrá veitir yfirlit yfir vinnusvæðið lokun fjárhagstímabils og tengdar skilgreiningar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Vinnusvæði lokunar fjárhagstímabils

Þessi skrá veitir yfirlit yfir vinnusvæðið lokun fjárhagstímabils og tengdar skilgreiningar.

Vinnusvæði lokunar fjárhagstímabils

Í **lokað fjárhagstímabil** vinnusvæði gerir kleift að rekja ferli við lokun fjárhagslegar milli fyrirtækja, svæði og einstaklinga. Eftir yfirliti í **lokað fjárhagstímabil** vinnusvæði, verður sést annaðhvort yfir öll verk og stöður fyrir lokun áætlun eða rétt verkefni sem þér er úthlutað. 

Áætlun efst í vinnusvæði lokun þarf fyrst að velja. Öll gögn sem birtast á vinnusvæðið er síðan síuð eftir lokun valda áætlun.

### <a name="summary-tiles"></a>Samantektarreitir

**Samantektarreitir** veita yfirlit yfir ferlið og vísar hjálpa til við að halda lokunarferlinu á áætlun. Hægt er að sjá verkefnum sem eru komnir fram yfir gjalddaga eftir verkefni fyrir daginn í dag, verk sem eru á gjalddaga í dag en lokað vegna tengsla og öll eftirstandandi verk á fyrir ferli. Þessar upplýsingar eru fyrir öll fyrirtæki sem eru teknar með í áætluninni valda lokun.

### <a name="tasks-and-status-section"></a>Hlutinn Verkefni og staða

Í á **Verkefni og stöðu** hlutanum stöðu af heildaruppsöfnun lokun áætlun er brotin niður á mismunandi vegu: stöðu eftir fyrirtæki, staða eftir svæði og stöðu einstaklinga sem er ábyrgur. Hægt er að skoða stöðu fyrir öll verk á raða bara eru á gjalddaga í dag, verkefni eða verk sem eru komnir fram yfir gjalddaga með því að breyta síu efst á listanum kort. Einnig er hægt að velja fyrirtæki síu til að skoða stöðu fyrir tiltekins fyrirtækis. Hver flipi stöðu gefur sundurliðun eftir prósentu sem lokið og fjöldi verka sem eftir er. Smellið á kortinu eða **Skoða upplýsingar um** aðgerð til að sía nákvæmar verk með valinnar kortategundar. 

Síðasta flipa er nákvæmar verkefnalisti. Listinn sýnir fullt verkefnalisti og hægt er að sía þannig að það sýnir einungis verk sem er verið að áhuga á. Hægt er að sía lista yfir verk með nokkrum aðferðum. Til dæmis er hægt að sía eftir verki fyrir gjalddaga, tengda fyrirtæki, og tengd svæði. Einnig er hægt að velja að sýna eða fela lokið verk í lista yfir verk. 

Tveir vísar eru notaðir fyrir verk:

-   Upphrópunarmerki táknið gefur til kynna að verkið sé fram yfir gjalddaga. Fyrir verk sem eru gjaldfallnir gjalddaga er einnig upplýstur rauður.
-   Hengilás táknið gefur til kynna á verkefni er háð öðrum verkum sem ekki eru kostnaðarjafnaðar enn lokið. Ekki er hægt að merkja verk sem er læst af tengsl sem lokið. Hægt er að setja tengslin fyrir verkefni með því að nota í **Setja fylgni** aðgerð.

Heiti verksins er tengil í Microsoft Dynamics 365 Aðgerðir síðu eða öðrum vefsíða þar sem notandinn verða að fara að ljúka vinnu. Hægt er að setja þennan tengil með því að nota í **Verkefni tengil** þegar breyta eða stofna verk. 

Hægt er að tengja skrár, víxla, myndir og Vefslóðir til verk með því að nota í **Viðhengi** aðgerð. Til dæmis er hægt að tilgreina númer færslubókar sem er notað sem hluti af verki, bæta við athugasemd um sérstakt verk eða tengja skýrslu skrá sem var prentaður fyrir verk. Tákn birtist í á **Viðhengið** dálkur fyrir verkefni ef viðhengi eru til staðar. 

Í **ljúka Verki** valkost verður að vera handvirkt valinn eftir að verkefninu er lokið. Þegar verkefni er merkt sem lokið er við **Lokið dagsetning** svæðið er sjálfkrafa uppfært á núgildandi dagsetningu og tíma. Fylgni vísar eru uppfærð eins og við á.

## <a name="all-financial-period-close-tasks-list-page"></a>Listasíðan Öll lokunarverk fjárhagstímabils
Þú getur skoðað alla núgildandi og fyrra tímabils loka verkefni úr á **Öll fjárhagstímabil loka verkefni** listasíðu. Þessari listasíðu hentar best fyrir söguleg greining á ferli við lokun, þar sem hún inniheldur upplýsingar um áætluðu gjalddaga, raunveruleg lokadagsetning og sá sem hefur lokið verkinu. Auðveldlega er hægt að flytja upplýsingar á þessari listasíðu í Microsoft Excel fyrir skýrslugerð og endurskoðun tilgangi.

## <a name="financial-period-close-configuration-page"></a>Síðan Lokunarskilgreining fjárhagstímabils
Áður en hægt er að nota í **lokað fjárhagstímabil** vinnusvæði, þarf að skilgreina það í Microsoft Dynamics 365 aðgerða með því að nota í **Fjárhagslegar tímabils loka skilgreiningu** síðu. (Smellið á **fjárhags**&gt;**loka Tímabili**&gt;**Fjárhagslegar tímabils loka skilgreiningu**.)

### <a name="resources"></a>Forði

Á við **Tilföng** flipa er að skilgreina fólki sem koma við sögu í ferli lokun. Allar sem verður ábyrgur fyrir verkefni lokun þarf fyrst að tengja hér. Skoða starfsmanns vinnusvæðisins verður einnig að tilgreina. Eftirtaldir valkostir eru í boði:

-   **Aðeins úthlutuð verkefni** – Þá mun notandinn sjá aðeins þau verkefni sem eru úthlutaðar á hann eða hana.
-   **Öll verkefni og staða** – Notandinn mun sjá öll lokunarverk og stöðu heildarferlisins.

Notendur með heimild til að skoða aðeins úthlutuð verkefni sín geta ekki bætt verkum við lista yfir verkefni, breytt verkum eða fjarlægt verk úr lista yfir verk.

### <a name="task-areas"></a>Verksvæði

Verksvæði eruð notuð til að flokka lokunarverk í röklegt svæði eignarhalds innan fyrirtækisins. Til dæmis gætu Viðskiptaskuldir, Viðskiptakröfur eða Fjárhagur verið notuð sem verksvæði.

### <a name="calendars"></a>Dagatöl

Stofna og breyta fjárhagslegum lokun með því að nota flipann Dagatöl dagatöl.  Þetta er þar sem þú verður að skilgreina vinnudaga fyrir lokunarferlinu og verður notað fyrir röðun lokunarverkefni.  Stofna nýtt dagatal og tilgreina vinnudaga sem nota á verkáætlun.  Best er að stofna dagatal langt tímabil, ár eða ár margar þar sem hægt er að breyta henni eftir stofnun.  Eftir að hafa stofnað dagatal, smellið á hnappinn Breyta til að uppfæra dagatal fyrir ákveðna daga, svo sem frídaga.  Verkefni er lokað verður raðað á dögum þegar gildi Stýringu er stillt á Opin.  Ef verk er lokað má ekki vera áætlun á ákveðnum degi, dag sem ætti að hafa Stýringu gildið sett í Lokað.

### <a name="templates"></a>Sniðmát

Nota loka fjárhagslegar sniðmát til að tilgreina öll verk sem eru hluti af lokunarferlinu stendur. Loka verkefni er endurtekna vinnu framlag sem er úthlutað á stakar til að ljúka við sem hluta af hverju ferli lokun. Í sniðmátsuppskrift er tengd gjalddaga dagsetning verður að skilgreina fyrir hvert verkefni lokun. Hlutfallslegt gjalddaga er fjöldi daga áður en eða eftir skilgreinda lok tímabils dagsetningu þar sem verkið verður gjalddaga hvert tímabil. Gjalddaga tíma eru einnig tengdar hvert verkefni. Tími skila er með því að nota í samhengi tímabelti og verður umbreytt í tímabelti hvers notanda. 

Hægt er að úthluta verki í sniðmátinu eitt eða fleiri fyrirtæki þar sem á að verkinu. Ef mismunandi einstaklingur er úthlutað á ljúka til að vinna framlag í hverju fyrirtæki, það gæti verið gagnlegt til að stofna mörg verkefni fyrir sama framlag vinnu. Stofna eitt verk fyrir hvert fyrirtæki. 

Í **Verkefni tengil** valmyndaratriði er tengd við verkframlag vinnu og hægt er að nota til að fara beint tengda síðan úr verki tengil í vinnusvæðið. Til dæmis er hægt að tengja verkefni lokun að keyra vinnslu fyrir endurmat gjaldmiðils fyrir lánardrottna á tengdar **endurmat á Erlendum gjaldmiðli** síðu í Microsoft Dynamics 365 fyrir Aðgerðir. Einnig er hægt að tengja við ytri vefslóð. 

> [! Ábending] Ef óskað er að tengja ákveðna Management Reporter skýrslu fjárhagslegar tímabils loka verkefni, er hægt að nota SLÓÐ skýrslu. Til að fá aðgang að SLÓÐ skýrslu opna skýrsluna í report designer og smellið síðan á **Skrá**&gt;**Skoða skýrslu** ef opna á skýrslu í vafra. Síðan er hægt að afrita vefslóð í aðseturslínunni í vafra og líma þau inn í **Verkefni tengil** **Vefslóð** svæði. 

Hægt er að skilgreina verkþáttatengsl í sniðmátinu. Ef verk hefur verið sett upp til að fara á eina eða fleiri verkefni, ekki sem verkefnið að merkja sem lokið þar til öll tengsl er lokið. 

Hægt er að stofna mörg fjárhagslegar loka sniðmát. Síðan er hægt að nota ýmsar sniðmát til að rekja ferli lokað fyrir mismunandi tímabila, mánuði lok eða lok árs, eða til að rekja fyrirtæki sem nota mismunandi lokun ferli. Eftir eitt sniðmát er stofnað er hægt að afrita nýja sniðmátið og gera nauðsynlegar breytingar. Hægt er að tengja aðeins eitt sniðmát til að raða hverri lokun.

### <a name="closing-schedules"></a>Lokunaráætlanir

Lokun áætlun er notuð til að úthluta tilteknum fjárhagstímabil sem verða að vera lokaðar fjárhagslegar loka sniðmát. Verk úr sniðmáti sjálfvirkt myndaðar fyrir tilgreint tímabil og ný lokun röðun er bætt við vinnusvæðið. Þegar ný áætlun lokun á **lokadag** svæði er notað til að ákvarða raunverulega gjalddaganum dagsetningar fyrir lokunarverkefni byggð á gjalddaga fyrir afstæða dagsetningu sem er úthlutað í fjárhagslegar loka sniðmát. 

Úthluta dagatali viðeigandi fyrir lokun áætlun til að tilgreina vinnudaga sem nota á í verkáætlun. Ef ekki tilteknu dagatali, verkið gjalddaga dagsetningar verða að nota alla daga vikunnar. 

Einnig verður að skilgreina fyrirtækin sem eru tengd við lokun áætlun. Ef sniðmát verkefni er úthlutað til margra fyrirtækja, aðskildum verkum stofnuð fyrir hvert fyrirtæki sem er í áætluninni lokun og sniðmát verkefnið úthlutað. 

Veljið eftir röðun lokun er lokið við **Lokað** valkost fyrir hana. Saga verkið verður enn tiltæk úr á **Öll fjárhagstímabil loka verkefni** listasíðu en áætlun lokun verða fjarlægðar úr vinnusvæðið. Eftir að lokun áætlun hefur verið merkt sem **Lokað**, er ekki hægt að bæta verkum við, breyta verkum eða fjarlægja verk úr henni.


