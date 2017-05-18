---
title: "Áfylling"
description: "Þessi skrá lýsir áfyllingaráætlunum sem eru tiltækar fyrir vöruhús sem nota aðgerðirnar sem eru tiltækar í vöruhúsakerfi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c808ec202bdb271f08a36a2b25ebed22a9477414
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="replenishment"></a>Áfylling

[!include[banner](../includes/banner.md)]


Þessi skrá lýsir áfyllingaráætlunum sem eru tiltækar fyrir vöruhús sem nota aðgerðirnar sem eru tiltækar í vöruhúsakerfi.

Þessi skrá lýsir áfyllingaráætlunum sem eru tiltækar fyrir vöruhús sem nota aðgerðirnar sem eru tiltækar í vöruhúsakerfi. Þessar upplýsingar á ekki við um vöruhúsalausn sem er tiltæk í birgðastjórnun. Þrjár áfyllingaráætlanir eru tiltækar:

-   **Áfylling samkvæmt bylgjueftirspurn** – Þessi áætlun stofnar áfyllingarvinnu fyrir pantanir á útleið eða hleður ef birgðir eru ekki tiltækir þegar vinnunni stofnað fyrir bylgjuna. Til dæmis, ef magnið sem er krafist fyrir sölupöntun er ekki tiltækur þegar unnið er úr bylgju er hægt að stofna áfyllingarvinnu.
-   **lágmarks og hámarks áfylling** -Þessi aðferð notar lágmarks og hámarks birgðamörk til að ákvarða hvenær á að fylla á staðsetningar. Skilyrði vöru og staðsetninga skilgreina birgða eru metnar fyrir áfyllingu. sniðmát fyrir Lágmarks- og hámarks áfyllingar er aðaltækið til að viðhalda ákjósanlegu stigi í tiltektarstaðsetningar. Til að tryggja að nægt vel aðgengilegt lagerrými fyrir tiltekt sendinga sé tiltækt til að uppfylla bylgjueftirspurn, geturðu notað eftirspurnaráfyllingu sem viðbót á milli lágm./hám. áfyllingarferla
-   **Áfylling farmeftirspurnar** – Þessa aðferð leggur saman eftirspurn fyrir nokkra farma og stofnar áfyllingarvinna sem er nauðsynlegt til að geta hýst viðeigandi tiltektarstaðsetningar. Þessi aðferð hjálpar til við að tryggja að farm sem eru stofnaðar má taka til í vöruhúsi eftir að þær eru losaðar.

Allar þrjár aðferðir stofna áfyllingarvinnu byggð á áfyllingarsniðmáti.

## <a name="wave-demand-replenishment"></a>Áfylling Bylgjueftirspurnar
Áfylling Bylgjueftirspurnar stofnar áfyllingarvinnu, sem byggist á eftirspurn, fyrir magnið sem er nauðsynlegt fyrir sendingar á útleið eða farmar eru ekki tiltækir þegar bylgjan stofnar vinnu. Áfyllingarsniðmát inniheldur upplýsingar um vöruskilyrði, mælieiningu, aukning eftirspurnar, og staðsetningu. 

Staðsetningarleiðbeiningar eru notaðar til að ákvarða hvaða staðsetningu skal fylla á. Þú tengir þessar staðsetningarleiðbeiningar við áfyllingarsniðmát með því að nota í **leiðbeiningakóða** svæði. Ef í **leiðbeiningakóðar** svæðið er ekki stillt, eru fyrirspurnir notaðar til að ákvarða hvaða staðsetningarleiðbeiningar skuli nota. Athugið að ef leiðbeiningarkóðinn er ekki tilgreint í áfyllingarsniðmát, og staðsetningarleiðbeiningar eru með leiðbeiningakóða, verður staðsetningarleiðbeininga hunsuð, jafnvel þótt fyrirspurn á staðsetningarleiðbeiningu sé rétt. Tiltektarstaðsetningarleiðbeiningum eru notaðar til að ákvarða hvar á að sækja birgðir fyrir áfyllingu. 

Auk þess að stofna sniðmát, verður að tilgreina einhverjar áfyllingarstillingar í bylgjusniðmátið. Bylgjusniðmátið ætti að innihalda bylgjuskref fyrir áfyllingu sem er keyrð einungis ef úthlutun vöru tókst ekki. Þetta áfyllingarskref bylgju notar bylgjuskrefskóða til að ákvarða hvaða áfyllingarsniðmát skuli nota. Auk þess að þurfa skrefbylgju fyrir áfyllingu, þarf að tryggja að **fylla á** er valin í á **Aðferðir** hluta bylgjusniðmáts. 

**áfyllingarsniðmát** síða inniheldur **Leyfa bylgjueftirspurn til að nota ófrátekið magn** gátreit. Þú ætti að velja þennan gátreit ef á að leyfa eftirspurnaráfyllingu til að draga ófrátekið magn af vinnu sem er mynduð úr völdu áfyllingarsniðmáti. Þessi gátreitur þarf að vera stillt fyrir hvert áfyllingarsniðmát til að virkja áfyllingarsniðmát  eftirspurnar til að nota þessa reglum. Þegar eftirspurnaráfylling er ræst í vöruhúsi, mun það draga eftirspurn frá fyrirliggjandi áfyllingarvinnu sem er með ófrátekið magn, ef vinnan er upprunnið úr áfyllingarsniðmáti þar sem gátreiturinn **Leyfa bylgjueftirspurn að nota ófrátekið magn** er valinn.

## <a name="minmax-replenishment"></a>Lágm./hám. áfylling
í Lágm. / Hám áfylling, eru fyllt á Birgðir  þannig að þær er á milli lágmarks og hámarks mörk sem hafa verið settar. Venjulega á þetta ferli á sér stað einu sinni hvern dag til að tryggja að allar tiltektarstaðsetningar séu áfylltar upp að hæsta stig áður en tiltekt hefst. 

Lágmarks- og hámarksupphæðir eru settar í áfyllingarsniðmáti. Margar aðrar stillingar í sniðmátinu líkjast stillingar í sniðmátum sem notaðar eru í áfyllingu bylgjueftirspurnar. sniðmát ætti að vera með eina línu fyrir hverja vöru og staðsetningu. Þegar keyrð er áfylling með því að nota runuvinnslu, metur Microsoft Dynamics 365 hvort áfyllingar er krafist í röðinni sem línurnar eru skipulagðar. 

Athugið að Lágm. / Hám áfyllingaráætlun getur ekki fylla á tómar staðsetningar nema staðsetning er stillt sem föst staðsetning fyrir vöruna. Ef staðsetning sem þarf að fylla á er ekki föst staðsetning, getur Dynamics 365 for Operations ekki ákvarðað hvaða vöru skal fylla á. Þess vegna er krafist einhvers magns á lager áður en áfylling fer fram.

## <a name="load-demand-replenishment"></a>Áfylling farmeftirspurnar
Áfylling farmeftirspurnar leggur saman eftirspurn fyrir nokkra farma og stofnar áfyllingarvinna sem er nauðsynlegt til að geta hýst viðeigandi tiltektarstaðsetningar. Áfylling Farmeftirspurnar svipar til áfyllingar bylgjueftirspurnar á marga vegu. Megin munurinn er hvernig og hvenær áfyllingar farmeftirspurnar og bygljueftirspurnar eru keyrðar. Líkt og Lágm. / Hám áfylling , er farmeftirspurnar keyrð með því að nota runuvinnslu. Til að setja upp runuvinnslu, á í **áfylling Farmeftirspurnar** síðunni, veljið áfyllingarsniðmát til að nota og stilla fyrirspurn fyrir síu til að tilgreina hvaða farmar eru notaðar til að ákvarða eftirspurn. Fyrirspurnin umn staðsetningu skilgreinir staðsetningar sem hvaða tiltækt magn verður dreginn frá til að uppfylla uppsafnaðri eftirspurn fyrir farma.

## <a name="replenishment-prerequisites"></a>Skilyrði fyrir áfyllingu
| Skilyrði            | Lýsing                                                                                                                                                                                                                                        |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vara                    | Varan verður að vera virkur fyrir vöruhúsakerfisferli.                                                                                                                                                                                       |
| Vöruhús               | Vöruhús verður að vera virkur fyrir vöruhúsakerfisferli. Til að virkja vöruhús fyrir vöruhúsakerfisferli, skal velja vöruhús í skjámyndinni **Vöruhús** og velja síðan valkostinn **Nota vöruhúsakerfisferli**. |
| Sniðmát áfyllingar | Minnst ein áfyllingarsniðmát verður að vera sett upp fyrir Lágm. / Hám áfyllingu, áfyllingu bylgueftirspurnar, eða farmeftirspurnar.                                                                                                             |
| Staðsetningar               | verður að stofna staðsetningar og tengja við staðsetningarforstilling                                                                                                                                                                                     |
| Forstillingar staðsetningar       | Staðsetningarforstillingar eru nauðsynlegar til að stofna staðsetningar.                                                                                                                                                                                       |
| Staðsetningarleiðbeiningar     | Staðsetningarleiðbeiningar eru nauðsynleg til leiða vinnu til staðsetninga þar sem áfylling er nauðsynlegt, og til staðsetningar þar sem birgðir eru upprunnar frá.                                                                                     |
| Vinnusniðmát          | Vinnusniðmát af gerðinni **Áfylling** er krafist til að geta stofna áfyllingarvinnu svo að birgðir sé hægt að færa í æskilega staðsetningu.                                                                                           |






