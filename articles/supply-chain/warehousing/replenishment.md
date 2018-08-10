---
title: "Áfylling"
description: "Þetta efnisatriði lýsir áfyllingaráætlunum sem eru tiltækar fyrir vöruhús sem nota aðgerðirnar sem eru tiltækar í vöruhúsakerfi."
author: Mirzaab
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 41f77a837f446e0ef263f1554a333d6e48248a0e
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="replenishment"></a>Áfylling

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir áfyllingaráætlunum sem eru tiltækar fyrir vöruhús sem nota aðgerðirnar sem eru tiltækar í vöruhúsakerfi. Upplýsingarnar í þessu efnisatriði á ekki við um vöruhúsalausn sem er tiltæk í birgðastjórnun.

Eftirfarandi áfyllingaráætlanir eru tiltækar:

- **Áfylling samkvæmt bylgjueftirspurn** – Þessi áætlun stofnar áfyllingarvinnu fyrir pantanir á útleið eða hleður ef birgðir eru ekki tiltækir þegar vinnunni stofnað fyrir bylgjuna. Til dæmis, ef magnið sem er krafist fyrir sölupöntun er ekki tiltækur þegar unnið er úr bylgju er hægt að stofna áfyllingarvinnu.
- **lágmarks og hámarks áfylling** -Þessi aðferð notar lágmarks og hámarks birgðamörk til að ákvarða hvenær á að fylla á staðsetningar. Skilyrði vöru og staðsetninga skilgreina birgða eru metnar fyrir áfyllingu. sniðmát fyrir Lágmarks- og hámarks áfyllingar er aðaltækið til að viðhalda ákjósanlegu stigi í tiltektarstaðsetningar. Til að tryggja að nægt vel aðgengilegt lagerrými fyrir tiltekt sendinga sé tiltækt til að uppfylla bylgjueftirspurn, geturðu notað eftirspurnaráfyllingu sem viðbót á milli lágm./hám. áfyllingarferla
- **Áfylling farmeftirspurnar** – Þessa aðferð leggur saman eftirspurn fyrir nokkra farma og stofnar áfyllingarvinna sem er nauðsynlegt til að geta hýst viðeigandi tiltektarstaðsetningar. Þessi aðferð hjálpar til við að tryggja að farm sem eru stofnaðar má taka til í vöruhúsi eftir að þær eru losaðar.
- **Skjót áfylling** - Þessi stefna endurnýjar birgðir áður en bylgjan er keyrð ef úthlutun mistekst fyrir línu staðsetningarleiðbeiningar sem innihalda áfyllingarsniðmát. 

Allar fjórar aðferðir stofna áfyllingarvinnu byggð á áfyllingarsniðmáti.

## <a name="wave-demand-replenishment"></a>Áfylling Bylgjueftirspurnar
Áfylling Bylgjueftirspurnar stofnar áfyllingarvinnu, sem byggist á eftirspurn, fyrir magnið sem er nauðsynlegt fyrir framleiðslupantanir, kanban, sendingar á útleið eða farmar eru ekki tiltækir þegar bylgjan stofnar vinnu. Áfyllingarsniðmát inniheldur upplýsingar um vöruskilyrði, mælieiningu, aukning eftirspurnar, og staðsetningu. 

Staðsetningarleiðbeiningar eru notaðar til að ákvarða hvaða staðsetningu skal fylla á. Þú tengir þessar staðsetningarleiðbeiningar við áfyllingarsniðmát með því að nota í **leiðbeiningakóða** svæði. Ef í **leiðbeiningakóðar** svæðið er ekki stillt, eru fyrirspurnir notaðar til að ákvarða hvaða staðsetningarleiðbeiningar skuli nota. Athugið að ef leiðbeiningarkóðinn er ekki tilgreint í áfyllingarsniðmát, og staðsetningarleiðbeiningar eru með leiðbeiningakóða, verður staðsetningarleiðbeininga hunsuð, jafnvel þótt fyrirspurn á staðsetningarleiðbeiningu sé rétt. Tiltektarstaðsetningarleiðbeiningum eru notaðar til að ákvarða hvar á að sækja birgðir fyrir áfyllingu. 

Auk þess að stofna sniðmát, verður að tilgreina einhverjar áfyllingarstillingar í bylgjusniðmátið. Bylgjusniðmátið ætti að innihalda bylgjuskref fyrir áfyllingu sem er einungis keyrð ef úthlutun vöru tekst ekki. Þetta áfyllingarskref bylgju notar bylgjuskrefskóða til að ákvarða hvaða áfyllingarsniðmát skuli nota. Auk þess að þurfa skrefbylgju fyrir áfyllingu, þarf að tryggja að **Fylla á** er valin í á **Aðferðir** hluta bylgjusniðmáts. 

**áfyllingarsniðmát** síða inniheldur **Leyfa bylgjueftirspurn til að nota ófrátekið magn** gátreit. Veljið þennan gátreit ef leyfa á eftirspurnaráfyllingu til að draga ófrátekið magn af vinnu sem er mynduð úr völdu áfyllingarsniðmáti. Hakaðu við í þennan gátreit fyrir hvert fyrirliggjandi áfyllingarsniðmát svo sniðmát fyrir bylgjuáfyllingu geti notað þessa reglu. Þegar eftirspurnaráfylling er ræst í vöruhúsi, mun það draga eftirspurn frá fyrirliggjandi áfyllingarvinnu sem er með ófrátekið magn, ef vinnan er upprunnið úr áfyllingarsniðmáti þar sem gátreiturinn **Leyfa bylgjueftirspurn að nota ófrátekið magn** er valinn.

Áfyllingareftirspurn er studd fyrir sölupantanir, flutningspantanir, framleiðslupantanir og kanban-kerfi. 

## <a name="minmax-replenishment"></a>Lágm./hám. áfylling
í Lágm. / Hám áfylling, eru fyllt á Birgðir  þannig að þær er á milli lágmarks og hámarks mörk sem hafa verið settar. Venjulega á þetta ferli á sér stað einu sinni hvern dag til að tryggja að allar tiltektarstaðsetningar séu áfylltar upp að hæsta stig áður en tiltekt hefst. 

Lágmarks- og hámarksupphæðir eru settar í áfyllingarsniðmáti. Margar aðrar stillingar í sniðmátinu líkjast stillingar í sniðmátum sem notaðar eru í áfyllingu bylgjueftirspurnar. sniðmát ætti að vera með eina línu fyrir hverja vöru og staðsetningu. Þegar keyrð er áfylling með því að nota runuvinnslu, metur Microsoft Dynamics 365 for Finance and Operations hvort áfyllingar er krafist með því að nota röðina þar sem línurnar eru skipulagðar. 

Athugið að Lágm. / Hám áfyllingaráætlun getur ekki fylla á tómar staðsetningar nema staðsetning er stillt sem föst staðsetning fyrir vöruna. Ef staðsetning sem þarf að fylla á er ekki föst staðsetning getur kerfið ekki ákvarðað hvaða vöru skal fylla á. Þess vegna er krafist einhvers magns á lager áður en áfylling fer fram.

## <a name="load-demand-replenishment"></a>Áfylling farmeftirspurnar
Áfylling farmeftirspurnar leggur saman eftirspurn fyrir nokkra farma og stofnar áfyllingarvinna sem er nauðsynlegt til að geta hýst viðeigandi tiltektarstaðsetningar. Áfylling Farmeftirspurnar svipar til áfyllingar bylgjueftirspurnar á marga vegu. Megin munurinn er hvernig og hvenær áfyllingar farmeftirspurnar og bygljueftirspurnar eru keyrðar. Líkt og Lágm. / Hám áfylling , er farmeftirspurnar keyrð með því að nota runuvinnslu. Til að setja upp runuvinnslu, á í **áfylling Farmeftirspurnar** síðunni, veljið áfyllingarsniðmát til að nota og stilla fyrirspurn fyrir síu til að tilgreina hvaða farmar eru notaðar til að ákvarða eftirspurn. Fyrirspurnin umn staðsetningu skilgreinir staðsetningar sem hvaða tiltækt magn verður dreginn frá til að uppfylla uppsafnaðri eftirspurn fyrir farma.

## <a name="immediate-replenishment"></a>Umsvifalaus áfylling
Í stað þess að þurfa að draga saman eftirspurn í lok úthlutunarferlisins og endurnýja á grundvelli samandregins magns, getur þú strax notað umsvifalausa áfyllingaráætlun. Þegar þú notar þessa áætlun er hægt að endurnýja birgðir strax eftir að lína staðsetningarleiðbeiningar mistekst. Þess vegna er hægt að setja upp áfyllinguna þannig að hún sé takmörkuð af sérstökum einingum og noti því magn sem er stillt fyrir tilteknar staðsetningar.

## <a name="replenishment-prerequisites"></a>Skilyrði fyrir áfyllingu

|      Skilyrði       |                                                                                                                                lýsing                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Vara           |                                                                                                        Varan verður að vera virkur fyrir vöruhúsakerfisferli.                                                                                                        |
|        Vöruhús        | Vöruhús verður að vera virkur fyrir vöruhúsakerfisferli. Til að virkja vöruhús fyrir vöruhúsakerfisferli, skal velja vöruhús í skjámyndinni <strong>Vöruhús</strong> og velja síðan valkostinn <strong>Nota vöruhúsakerfisferli</strong>. |
| Sniðmát áfyllingar |                                                                   Minnst ein áfyllingarsniðmát verður að vera sett upp fyrir Lágm. / Hám áfyllingu, áfyllingu bylgueftirspurnar, eða farmeftirspurnar.                                                                   |
|        Staðsetningar        |                                                                                                       verður að stofna staðsetningar og tengja við staðsetningarforstilling                                                                                                       |
|    Forstillingar staðsetningar    |                                                                                                        Staðsetningarforstillingar eru nauðsynlegar til að stofna staðsetningar.                                                                                                        |
|   Staðsetningarleiðbeiningar   |                                                       Staðsetningarleiðbeiningar eru nauðsynleg til leiða vinnu til staðsetninga þar sem áfylling er nauðsynlegt, og til staðsetningar þar sem birgðir eru upprunnar frá.                                                        |
|     Vinnusniðmát      |                                                   Vinnusniðmát af gerðinni <strong>Áfylling</strong> er krafist til að geta stofna áfyllingarvinnu svo að birgðir sé hægt að færa í æskilega staðsetningu.                                                    |


