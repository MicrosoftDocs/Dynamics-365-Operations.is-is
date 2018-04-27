---
title: "Dreifa og ljúka spurningalista"
description: "Þetta efnisatriði útskýrt hvernig dreifa á spurningalista sem er hannaður af þér, þannig að þær eru tiltækar fyrir einstakling eða hóp einstaklinga sem munu ljúka við þær."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 3954ec2a06c7a2ec964b656e088f8c677094c963
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---

# <a name="distribute-and-complete-a-questionnaire"></a>Dreifa og ljúka spurningalista

[!INCLUDE [banner](includes/banner.md)]

Þetta efnisatriði útskýrt hvernig dreifa á spurningalista sem er hannaður af þér, þannig að þær eru tiltækar fyrir einstakling eða hóp einstaklinga sem munu ljúka við þær. 

Það eru margar leiðir til að Dreifa spurningarlista:

-   Merktu spurningalistann sem virkan. Spurningalistanum er þá tiltækur fyrir alla starfsmenn nema flokk spurningalista er sett upp til að takmarka aðgang að honum.
-   Úthluta Notkunarheilmildir á flokk spurningalista. Þá er spurningalista tiltækur öllum meðlimum fyrir valinn flokk.
-   Stofna áætlaðar svarsetur. Spurningalistinn er þá aðeins tiltækur fyrir tiltekinn einstakling.
-   Stofna áætlun. Spurningalisti þá er tiltækt til fjölda fólks.

## <a name="marking-a-questionnaire-as-active"></a>Merkja spurningalistann sem virkan
Með því að stilla svæðið á **Virk** á **Já** á í **Spurningalista** síðu er spurningalistann að nálgast fyrir alla starfsmenn til að ljúka. Svarendur geta svarað spurningalistanum mörgum sinnum. Þessi virkni er gagnlegt ef ætlunin er að safna stöðugri svörun í yfir árið. Til dæmis er hægt að gera spurningalista sem er notuð til að gefa svörun um hádegismat í mötuneyti starfsmanna.

## <a name="questionnaire-groups"></a>Spurningalistaflokkar
Hægt er að setja upp spurningalistaflokka og síðan taka svarendur sem á að dreifa spurningalista til. 

Hægt er að stofna spurningalista úr eftirfarandi síðum:

-   **Spurningalistaflokkar**– Aðeins einstaklinga í spurningalistaflokkur getur lokið valda spurningalistann. Til dæmis er ætlaða markhópur verktakar, þannig að þú stofna spurningalistaflokk sem tilheyra þeim svarendum.
-   **Meðlimir spurningalistaflokka** – hægt er að bæta fólki við spurningalistaflokka .

Til að úthluta spurningalistaflokki á spurningalista, á **Spurningalisti** síða, smellt er á **Notendaheimildir**. Þegar spurningalistinn hefur verið vistaður sem virkt, geta aðilar að spurningalistaflokknum lokið spurningalistanum. Til að úthluta til spurningalistaflokk á spurningalista á Spurningalista síðunni er smellt á notandaréttindi.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Áætluð svarseta í spurningalista
Áætlaðar svarsetur eru spurningalistar sem hefur verið hannaðar og búið að velja svarendur fyrir. 

> **Athugið:** Áður en hægt er að setja upp áætlaða svarsetu verður að hanna spurningalista. 

Á **Áætluð svarseta** síðu er hægt að stofna áætlaða svarlotu fyrir starfsmann. Listinn á síðunni birtir alla áætlaða spurningalista. 

Áætlaðar svarsetur eru einnig notaðar í **áætlanir spurningalista**, þar sem hægt er að áætla spurningalista fyrir marga í einu:

-   Starfsmenn
-   Þátttakendur á námskeiði
-   Skipulagseiningar

Hver einstaklingur getur svara spurningalista aðeins einu sinni.

## <a name="scheduling-a-questionnaire"></a>Röðun spurningalista
Valfrjálst er að raða spurningalista fyrir marga svarendur.

### <a name="planning-types"></a>Áætlunargerðir

Áætlunargerðir eru nauðsynleg ef óskað er að raða áætlaðar svarsetur fyrir marga svarendur. Áætlunargerðir eru notaðar til að flokka spurningalistaáætlanir . Þú getur t.d. raðað spurningalistum fyrir eftirfarandi málefni:

-   Mat
-   Könnun
-   Prófun

Hægt er að tilgreina gerðir fyrir áætlun spurningalista á **áætlanir Spurningalista** síðunni.

### <a name="reference-types-for-questionnaire"></a>Gerð tilvísunar fyrir Spurningalisti

Hægt er að nota tilvísunargerðir til að færa inn skilyrði fyrir svarendur sem þú velur hugsanlega þegar spurningalista er raðað. 

Nota skal **Tilvísunargerðir** síðu til að setja upp gerð tilvísunar fyrir spurningalista. Hver tilvísunargerð samsvarar töflu í Microsoft Dynamics 365 for Finance and Operations. Þegar áætlanir spurningalista er stofnað, er hægt að tilgreina einstaka færslum í töflunni eða svið færsla sem spurningalistinn verður að tengjast. 

Til dæmis, ef taflan Námskeið er valin, er hægt að ákveða hvaða námskeiða spurningalista verður fyrir. Þegar sett er upp tilvísun fyrir Námskeiðstöfluna eru sum svæði og hnappar á **Námskeið** síðunni verða tiltækar.

### <a name="questionnaire-schedules"></a>Áætlanir spurningalista

Hægt er að nota spurningalisti áætlun til að Mynda margt áætlað svarseta fyrir flokka notenda, á grunni gerð tilvísunar. Stofnaðu áætlun á síðunni **áætlanir Spurningalista**. Veldu áætlunargerð til að flokka áætlun, og einnig velurðu gerð tilvísunar sem ætti að nota til að fyrirspurn kerfið um tilgreinda notendur. Til dæmis ef þú stillir gerð tilvísunar á námskeiðatöflu er hægt að velja tilgreint námskeið í svæðinu **tilvísun**. 

Smellið á **upplýsingar um Uppsetningu** til að velja spurningalista og öðrum skilyrðum. Til dæmis skal tilgreina nafn leiðbeinanda sem skilyrði ef spurningalistinn er mat á leiðbeinanda. Eftir að lokið hefur verið að færa inn upplýsingar um uppsetningu, myndar kerfið áætlaðar svarsetur fyrir notendur sem eru teknar með í fyrirspurninni. 

Smellið á **Áætlaðar svarsetur** til að skoða svarsetur fyrir röðunina. Síðan er að stofna handvirkt viðbótar áætlaðar svarsetur eða eyða áætluðum svarsetum sem hefur ekki verið svarað. 

Smellið á **Aðgerðir** &gt; **Ræsa** til að gera spurningalista tiltæka fyrir notendur í tengdar áætlaðar svarsetur. Smellið á **Svör** til að skoða útfyllt svör fyrir spurningalistann. Einnig er hægt að afrita stillingar fyrir áætlun spurningalista, áætlaðar svarsetur og svör við nýrri röðun spurningalista.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Tilkynna svarendum um tiltæka spurningalista
Þegar spurningalistum er dreift verður að tilkynna svarendum að spurningalistar eru þeim aðgengilegir. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Tilkynna svarendum um áætlaða svarsetu

Ef notuð er áætluð svarseta tilkynna þarf að tilkynna einstaklingurinn beint, eins og með símtali eða tölvupósti.

### <a name="notifying-respondents-about-a-scheduling"></a>Tilkynna svarendum um röðun

Nota **röðun fyrirspurnar** síðu til að útbúa og senda tölvupóst til allra svarenda sem eru tengdir við spurningalistann. Færa inn texta tölvupósts í **tölvupóstur fyrir sjálfsafgreiðslu starfsmanns** flipanum. Eftir að áætlun hefur verið ræst er smellt á **Aðgerðir** &gt; **Senda tölvupóst** til að búa til og senda í tölvupósti til svarenda. Svarendur geta síðan innskráð sig á vefsvæðið og svarað spurningalistanum. 

> **Athugið:** Áður en hægt er að nota tölvupóstsvirkni þarf kerfisstjóri að færa inn stillingar fyrir tölvupóst á síðunni **Færibreytur tölvupósts**.

## <a name="ending-a-scheduled-questionnaire"></a>Ljúka áætluðum spurningalista
Hægt er að loka röðuðum spurningalista eftir að allir svarendur hafa lokið úthlutuðum svarlotum. Eftir að röðun spurningalista er lokið er ekki lengur hægt að afrita stillingar hennar í nýja röðun. 

> **Athugið:** Ef einn eða fleiri svarendur hafa ekki lokið við spurningalistann en þú vilt samt loka röðuninni verður þú fyrst að eyða þeim svarendum úr listanum í síðunni **Áætluð svarseta**. Að því loknu er hægt að loka röðuninni.

## <a name="completing-questionnaires"></a>Að klára spurningalista
Eftir að búið er að hannað og dreift spurningalistum, má ljúka við spurningalista af valda svarendur. Hægt er að ljúka við spurningalistana sem eru tiltækir úr tveimur staðsetningum:

-   Í skoðunarrúðunni þarf að smella á **Spurningalista** &gt; **dreifa** &gt; **klára Spurningalistanum**.
-   Í sjálfsafgreiðslu Starfsmanns, smellið á **Spurningalista til að ljúka**.

Hægt er að gera spurningalista tiltæka fyrir tiltekna notendur eða notendahópa, eða fyrir allt fólk á tilteknu neti.

<a name="see-also"></a>Sjá einnig
--------

[Hönnun spurningalista](design-questionnaires.md)

[Nota spurningalista.](questionnaires.md)

[Skoða og meta niðurstöður spurningalista](evaluate-questionnaire-results.md)



