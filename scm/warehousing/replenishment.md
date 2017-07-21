---
title: "Áfylling"
description: "Þetta efnisatriði lýsir tiltækum áfyllingaráætlunum fyrir vöruhús sem nota aðgerðirnar sem eru tiltækar í vöruhúsakerfi."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: c3bbf35b98416cbc3feca2b0d01015a79cdb2659
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="replenishment"></a>Áfylling

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir tiltækum áfyllingaráætlunum fyrir vöruhús sem nota aðgerðirnar sem eru tiltækar í vöruhúsakerfi. Þessar upplýsingar á ekki við um vöruhúsalausn sem er tiltæk í birgðastjórnun. Eftirfarandi áfyllingaráætlanir eru tiltækar:

-   **Áfylling samkvæmt bylgjueftirspurn** – Þessi áætlun stofnar áfyllingarvinnu fyrir pantanir á útleið eða hleður ef birgðir eru ekki tiltækir þegar vinnunni stofnað fyrir bylgjuna. Til dæmis, ef magnið sem er krafist fyrir sölupöntun er ekki tiltækur þegar unnið er úr bylgju er hægt að stofna áfyllingarvinnu.
-   **lágmarks og hámarks áfylling** -Þessi aðferð notar lágmarks og hámarks birgðamörk til að ákvarða hvenær á að fylla á staðsetningar. Skilyrði vöru og staðsetninga skilgreina birgða eru metnar fyrir áfyllingu. sniðmát fyrir Lágmarks- og hámarks áfyllingar er aðaltækið til að viðhalda ákjósanlegu stigi í tiltektarstaðsetningar. Til að tryggja að nægt aðgengilegt tiltektarrými sé til staðar til að mæta bylgjueftirspurn getur þú notað eftirspurnaráfyllingu sem viðbót milli lágm./hám. áfyllingarferla.
-   **Áfylling farmeftirspurnar** – Þessa aðferð leggur saman eftirspurn fyrir nokkra farma og stofnar áfyllingarvinna sem er nauðsynlegt til að geta hýst viðeigandi tiltektarstaðsetningar. Þessi aðferð hjálpar til við að tryggja að hægt sé að taka til stofnaðan farm í vöruhúsi þegar hann hefur verið gefinn út.

Allar þrjár aðferðir stofna áfyllingarvinnu byggð á áfyllingarsniðmáti.

## <a name="wave-demand-replenishment"></a>Áfylling Bylgjueftirspurnar

Áfylling eftir bylgjueftirspurn stofnar áfyllingarvinnu, sem byggist á eftirspurn, fyrir magnið sem er nauðsynlegt fyrir framleiðslupantanir, kanban-kerfi, pantanir á útleið eða farm sem ekki er tiltækur þegar bylgja stofnar verk. Áfyllingarsniðmát inniheldur upplýsingar um vöruskilyrði, mælieiningu, aukning eftirspurnar, og staðsetningu. 

Staðsetningarleiðbeiningar eru notaðar til að ákvarða hvaða staðsetningu skal fylla á. Þú tengir þessar staðsetningarleiðbeiningar við áfyllingarsniðmát með því að nota í **leiðbeiningakóða** svæði. Ef í **leiðbeiningakóðar** svæðið er ekki stillt, eru fyrirspurnir notaðar til að ákvarða hvaða staðsetningarleiðbeiningar skuli nota. Athugið að ef leiðbeiningarkóðinn er ekki tilgreint í áfyllingarsniðmát, og staðsetningarleiðbeiningar eru með leiðbeiningakóða, verður staðsetningarleiðbeininga hunsuð, jafnvel þótt fyrirspurn á staðsetningarleiðbeiningu sé rétt. Tiltektarstaðsetningarleiðbeiningum eru notaðar til að ákvarða hvar á að sækja birgðir fyrir áfyllingu. 

Auk þess að stofna sniðmát, verður að tilgreina einhverjar áfyllingarstillingar í bylgjusniðmátið. Bylgjusniðmátið ætti að innihalda bylgjuskref fyrir áfyllingu sem er keyrð einungis ef úthlutun vöru tókst ekki. Þetta áfyllingarskref bylgju notar bylgjuskrefskóða til að ákvarða hvaða áfyllingarsniðmát skuli nota. Auk þess að hafa bylgjuskref fyrir áfyllingu verður þú að ganga úr skugga um að **Áfylling** sé valin í hlutanum **Aðferðir** í bylgjusniðmáti. 

**áfyllingarsniðmát** síða inniheldur **Leyfa bylgjueftirspurn til að nota ófrátekið magn** gátreit. Þú ætti að velja þennan gátreit ef á að leyfa eftirspurnaráfyllingu til að draga ófrátekið magn af vinnu sem er mynduð úr völdu áfyllingarsniðmáti. Hakaðu við í þennan gátreit fyrir hvert fyrirliggjandi áfyllingarsniðmát svo sniðmát fyrir bylgjuáfyllingu geti notað þessa reglu. Þegar eftirspurnaráfylling er ræst í vöruhúsi, mun það draga eftirspurn frá fyrirliggjandi áfyllingarvinnu sem er með ófrátekið magn, ef vinnan er upprunnið úr áfyllingarsniðmáti þar sem gátreiturinn **Leyfa bylgjueftirspurn að nota ófrátekið magn** er valinn.


Áfyllingareftirspurn er studd fyrir sölupantanir, flutningspantanir, framleiðslupantanir og kanban-kerfi. 

## <a name="minmax-replenishment"></a>Lágm./hám. áfylling
í Lágm. / Hám áfylling, eru fyllt á Birgðir  þannig að þær er á milli lágmarks og hámarks mörk sem hafa verið settar. Venjulega á þetta ferli á sér stað einu sinni á dag til að tryggja hámarksáfyllingu á öllum tiltektarstaðsetningum áður en tiltekt hefst. 

Lágmarks- og hámarksupphæðir eru settar í áfyllingarsniðmáti. Margar aðrar stillingar í sniðmátinu líkjast stillingar í sniðmátum sem notaðar eru í áfyllingu bylgjueftirspurnar. sniðmát ætti að vera með eina línu fyrir hverja vöru og staðsetningu. Þegar keyrð er áfylling með því að nota runuvinnslu metur Finance and Operations AX hvort áfyllingar er krafist, í sömu röð og línurnar eru. 

Athugið að Lágm. / Hám áfyllingaráætlun getur ekki fylla á tómar staðsetningar nema staðsetning er stillt sem föst staðsetning fyrir vöruna. Ef staðsetningin sem þarf að fylla á er ekki föst staðsetning er ekki mögulegt að skera úr um hvaða vöru þarf að fylla á. Þess vegna er krafist einhvers magns á lager áður en áfylling fer fram.

## <a name="load-demand-replenishment"></a>Áfylling farmeftirspurnar
Áfylling farmeftirspurnar leggur saman eftirspurn fyrir nokkra farma og stofnar áfyllingarvinnu sem er nauðsynleg til að hægt sé að fylla á viðkomandi tiltektarstaðsetningar. Áfylling Farmeftirspurnar svipar til áfyllingar bylgjueftirspurnar á marga vegu. Megin munurinn er hvernig og hvenær áfyllingar farmeftirspurnar og bygljueftirspurnar eru keyrðar. Líkt og Lágm. / Hám áfylling , er farmeftirspurnar keyrð með því að nota runuvinnslu. Til að setja upp runuvinnslu, á síðunni **Áfylling farmeftirspurnar** skal velja það áfyllingarsniðmát sem þú vilt nota og stilla síufyrirspurn til að tilgreina hvaða farma á að nota til að skera úr um eftirspurnina. Fyrirspurnin umn staðsetningu skilgreinir staðsetningar sem hvaða tiltækt magn verður dreginn frá til að uppfylla uppsafnaðri eftirspurn fyrir farma.

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

