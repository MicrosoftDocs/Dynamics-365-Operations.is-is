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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8d3fca57ca5f2c899a5d1994df1dc2d4d8d0b818
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="financial-period-close-workspace"></a>Vinnusvæði lokunar fjárhagstímabils

[!include[banner](../includes/banner.md)]


Þessi skrá veitir yfirlit yfir vinnusvæðið lokun fjárhagstímabils og tengdar skilgreiningar.

Vinnusvæði lokunar fjárhagstímabils

Vinnusvæðið **Lokun fjárhagstímabils** gerir kleift að rekja ferli við lokun fjárhagslegar milli fyrirtækja, svæði og einstaklinga. Samkvæmt yfirliti í vinnusvæðinu **Lokun fjárhagstímabils** muntu sjá annaðhvort öll verk og stöður fyrir lokunaráætlun eða aðeins þau verkefni sem þér er úthlutað. 

Fyrst verður að velja lokunaráætlun efst í vinnusvæðinu. Öll gögn sem birtast á vinnusvæðinu eru síðan síuð með valinni lokunaráætlun.

### <a name="summary-tiles"></a>Samantektarreitir

**Samantektarreitir** veita yfirlit yfir ferlið og vísar hjálpa til við að halda lokunarferlinu á áætlun. Hægt er að sjá verkefni sem eru komnir fram yfir gjalddaga, eftirstandandi verkefni fyrir daginn í dag, verk sem eru á gjalddaga í dag en lokað vegna tengsla og öll eftirstandandi verk fyrir ferlið. Þessar upplýsingar eru fyrir öll fyrirtæki sem eru tekin með í valinni lokunaráætlunar.

### <a name="tasks-and-status-section"></a>Hlutinn Verkefni og staða

Í hlutanum **Verkefni og staða** er staða heildarlokunaráætlunar brotin niður á mismunandi vegu: stöðu eftir fyrirtæki, staða eftir svæði og staða einstaklinga sem eru ábyrgir. Hægt er að skoða stöðu fyrir öll verk í lokunaráætlun, aðeins verk sem eru á gjalddaga í dag, verkefni eða verk sem eru komin fram yfir gjalddaga. Einnig er hægt að velja fyrirtæki síu til að skoða stöðu fyrir sérstakt fyrirtæki. Hver flipi stöðu gefur sundurliðun eftir prósentu sem hefur verið lokið og fjölda verka sem eftir er. Smellið á kortið eða aðgerðina **Skoða upplýsingar** til að sía nákvæmar verk með völdu korti. 

Síðasti flipinn eru fyrir nákvæman verkefnalista. Listinn sýnir fullan verkefnalista og hann má sía svo að hann sýni einungis verkin sem þú hefur áhuga á. Hægt er að sía lista yfir verk með nokkrum aðferðum. Til dæmis er hægt að sía eftir verki fyrir gjalddaga, tengdu fyrirtæki og tengdu svæði. Einnig er hægt að velja að sýna eða fela lokið verk í lista yfir verk. 

Tveir vísar eru notaðir fyrir verk:

-   Upphrópunarmerki táknið gefur til kynna að verkið sé fram yfir gjalddaga. Fyrir verk sem eru fram yfir gjalddaga er gjalddaginn einnig upplýstur rauður.
-   Hengilás táknið gefur til kynna að verkefni er háð öðrum verkum sem ekki er enn lokið. Ekki er hægt að merkja verk sem er læst af tengslum sem lokið. Hægt er að setja tengslin fyrir verkefni með því að nota aðgerðina **Setja tengsl**.

Heiti verksins er tengill síðu Microsoft Dynamics 365 for Operations eða aðra vefsíðu sem notandinn verður að fara á til að ljúka vinnu. Hægt er að setja þennan tengil með því að nota reitinn **Verkefnatengill** þegar verki er breytt eða það stofnað. 

Tengja má skrárnar, athugasemdir, myndir og Vefslóðir við verk með aðgerð **fylgiskjöl** Til dæmis er hægt að tilgreina númer færslubókar sem er notað sem hluti af verki, bæta við athugasemd um sérstakt verk eða tengja skýrsluskrá sem var prentuð fyrir verk. Tákn birtist í dálknum **Viðhengi** fyrir verkefni ef viðhengi eru til staðar. 

Valkosturinn **Ljúka verki** verður að vera handvirkt valinn þegar verkefninu er lokið. Þegar verkefni er merkt sem lokið er reiturinn **Lokadagsetning** sjálfkrafa uppfært á núgildandi dagsetningu og tíma. Tengslavísar eru uppfærðir eins og við á.

## <a name="all-financial-period-close-tasks-list-page"></a>Listasíðan Öll lokunarverk fjárhagstímabils
Hægt er að skoða öll núgildandi og fyrri lokunarverk tímabils úr listasíða **Öll lokunarverk fjárhagstímabils**. Þessi listasíða hentar best fyrir sögulega greiningu á ferli við lokun, þar sem hún inniheldur upplýsingar um áætlaðan gjalddaga, raunverulega lokadagsetningu og þann sem hefur lokið verkinu. Auðveldlega er hægt að flytja upplýsingar af þessari listasíðu í Microsoft Excel fyrir skýrslugerð og endurskoðun tilgangi.

## <a name="financial-period-close-configuration-page"></a>Síðan Lokunarskilgreining fjárhagstímabils
Áður en hægt er að nota vinnusvæðið **Lokað fjárhagstímabil**, þarf að skilgreina ferlið í Microsoft Dynamics 365 for Operations með því að nota síðuna **Lokaskilgreining fjárhagstímabils**. (Smellið á **Fjárhagur** &gt; **> Loka tímabils >** &gt; **Lokaskilgreining fjárhagstímabils**.)

### <a name="resources"></a>Forði

Á flipanum **Tilföng** skilgreinirðu fólki sem kemur við sögu í lokunarferlum. Alla starfsmenn sem verða ábyrgir fyrir verkefni lokunarverki þarf fyrst að tengja hér. Einnig verður að tilgreina sýn starfsmanns af vinnusvæðinu. Eftirtaldir valkostir eru í boði:

-   **Aðeins úthlutuð verkefni** – Þá mun notandinn sjá aðeins þau verkefni sem eru úthlutaðar á hann eða hana.
-   **Öll verkefni og staða** – Notandinn mun sjá öll lokunarverk og stöðu heildarferlisins.

Notendur með heimild til að skoða aðeins úthlutuð verkefni sín geta ekki bætt verkum við lista yfir verkefni, breytt verkum eða fjarlægt verk úr lista yfir verk.

### <a name="task-areas"></a>Verksvæði

Verksvæði eruð notuð til að flokka lokunarverk í röklegt svæði eignarhalds innan fyrirtækisins. Til dæmis gætu Viðskiptaskuldir, Viðskiptakröfur eða Fjárhagur verið notuð sem verksvæði.

### <a name="calendars"></a>Dagatöl

Stofna og breyta dagatal lokun fjárhags með flipanum Dagatöl.  Hér er skilgreina vinnudagar fyrir lokunarferli og notað til að tímasetja lokunarverk.  Stofna nýtt dagatal og merkja vinnudagar sem nota fyrir tímasetning verka.  Best er að stofna dagatal fyrir langt tímabil t.d. ár eða mörg ár því að hægt að breyta eftir að búa til.  Eftir að stofna dagatal skal smella á hnappinn Breyta til að uppfæra dagatal fyrir sérstaka daga, t.d. frídaga.  Lokunarverk verða tímasetja á dagar þegar stýringargildi er stillt á Opið.  Ef lokunarverk er ekki á tímasetja á tilgreint dagur skal sá dagur vera með stýringargildi á Lokað.

### <a name="templates"></a>Sniðmát

Lokunarsniðmát fjárhags er notað til að skilgreina öll verk sem eru hluti af lokunarferlinu. Lokunarverk er endurtekið vinnuframlag sem er úthlutað á einstakling til að ljúka við sem hluti af hverju lokunarferli. Skilgreina þarf viðeigandi gjalddaga í sniðmátinu fyrir hvert lokunarverk. Hlutfallslegt gjalddagi er fjöldi daga áður en eða eftir skilgreindan lokadag tímabils þegar verkið verður á gjalddaga á hverju tímabili. Skilatími er einnig úthlutað til hvert verk. Gjalddaginn er stilltur í samhengi við tímabelti þitt og verður umbreytt í viðeigandi tímabelti hvers notanda. 

Hægt er að úthluta verki í sniðmátinu einu eða fleiri fyrirtækjum þar sem verkið á við. Ef öðrum einstaklingi er úthlutað til að ljúka því vinnuframlagi í hverju fyrirtæki gæti verið gagnlegt til að stofna mörg verkefni fyrir sama framlag vinnu. Stofna eitt verk fyrir hvert fyrirtæki. 

Valmyndaratriðið **Verkefnatengill** er tengt við verkframlag vinnu og hægt er að nota hann til að fara beint á tengda síðu af verktengli í vinnusvæðinu. Til dæmis er hægt að tengja verkefni lokun til að keyra vinnslu fyrir endurmat á gjaldmiðli fyrir Viðskiptaskuldir á tengdri síðu **Endurmat á erlendum gjaldmiðli** í Microsoft Dynamics 365 for Operations. Einnig er hægt að tengja við ytri vefslóð. 

> [Ábending]: Ef óskað er að tengja ákveðna Management Reporter skýrslu við lokunarverk fjárhagstímabils er hægt að nota vefslóð skýrslu. Til að fá aðgang að vefslóð skýrslu skal opna skýrsluna í skýrsluhönnun og smella síðan á **Skrá** &gt; **Skoða skýrslu** til að opna skýrsluna í vafra. Síðan er hægt að afrita vefslóð í aðseturslínunni í vafra og líma þau inn í **Verkefni tengil** **Vefslóð** svæði. 

Hægt er að skilgreina tengsl verks í sniðmátinu: Ef verk hefur verið sett upp með tengsl við eitt eða fleiri verkefni er ekki hægt að merkja það verk sem lokið fyrr en öllum tengslum er lokið. 

Hægt er að stofna mörg Lokunarsniðmát fjárhags. Síðan er hægt að nota ýmis sniðmát til að rekja lokunarferli fyrir mismunandi gerðir tímabila, eins og mánaðarlok eða árslok eða til að rekja fyrirtæki sem nota mismunandi lokunarferli. Þegar eitt sniðmát hefur verið stofnað er hægt að afrita það í nýja sniðmátið og gera nauðsynlegar breytingar. Aðeins er hægt að tengja eitt sniðmát við hverja lokunaráætlun.

### <a name="closing-schedules"></a>Lokunaráætlanir

Lokunaráætlun er notuð til að úthluta tilteknu fjárhagstímabili á tiltekið fjárhagstímabil sem verður að loka. Verk úr sniðmátinu eru síðan sjálfvirkt mynduð fyrir tilgreint tímabil og nýrri lokunaráætlun er bætt við vinnusvæðið. Þegar ný lokunaráætlun er stofnuð er reiturinn **Lokadagsetning tímabils** notaður til að ákvarða raunverulega gjalddaga fyrir lokunarverk, samkvæmt hlutfallslegum gjalddaga sem er úthlutað í lokunarsniðmáti fjárhags. 

Úthluta dagatali sem er viðeigandi fyrir lokunaráætlun til að tilgreina vinnudaga sem nota á í verkáætlun. Ef ekki er tilgreint dagatal munu gjalddagar verks nota alla daga vikunnar. 

Einnig verður að skilgreina þau fyrirtæki sem eiga að tengjast við lokunaráætlun. Ef sniðmátsverkum er úthlutað til margra fyrirtækja verða sérstök verk stofnuð fyrir hvert fyrirtæki sem er í lokunaráætluninni og úthlutað á sniðmátsverkið. 

Ef lokunaráætlun er lokið, velja valkostur **Lokað** fyrir hana. Ferill verksins verður enn tiltæk á listasíðunni **Öll lokunarverk fjárhagstímabils** en lokunaráætlun verður fjarlægð af vinnusvæðinu. Eftir að lokunaráætlun hefur verið merkt sem **lokað** er ekki hægt að bæta verkum við, breyta verkum eða fjarlægja verk úr henni.




