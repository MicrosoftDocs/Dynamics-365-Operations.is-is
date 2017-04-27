---
title: "Útskipting efna í framleiðslu"
description: "Þetta efnisatriði lýsir því hvernig skal skipta út efni á meðan á framleiðsluferli stendur."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 1d6f16cad4c985a5628e2589aece8e628c83ef22
ms.lasthandoff: 03/31/2017


---

# <a name="material-substitution-in-manufacturing"></a>Útskipting efna í framleiðslu

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvernig skal skipta út efni á meðan á framleiðsluferli stendur. 

Það eru þrjár aðferðir fyrir að skipta út efni meðan á framleiðsluferlinu stendur:

-   Dagsetningu, þegar eitt efni er skipt út fyrir annað eftir tiltekna dagsetningu
-   Við aðaláætlanagerð, þegar efni í formúlu er skipt út með mismunandi efni, þar sem hún er ekki til á lager
-   Við framleiðslu, þegar efni er óvænt er ekki til á lager og er skipt út með mismunandi efni

## <a name="substituting-material-by-date"></a>Útskipting efnis eftir dagsetningu
Íhugið eftirfarandi aðstæður: vél sem fyrirtæki er að framleiða inniheldur íhluti sem renna út á vörulista lánardrottins innan tveggja mánaða. Frá lokadagsetningu og áfram, mun lánardrottinn bjóða nýjan íhlut sem getur verið skipt út fyrir þann gamla. Gildisdagsetningar frá og til  má setja upp á uppskriftarlínum. Í þessu dæmi er sett upp gamla íhlutinn svo hann renni út með því að færa inn lokadagsetningu í á **til-dagsetning** svæði. Síðan, á Uppskrift, er settur upp nýja, útskiptiíhlutinn svo hann gildir frá þeim degi sem sá gamli rennur út. Til að gera þetta er fært upphafsdagur í reitinn **frá dagsetning**.

## <a name="substituting-material-by-planning"></a>Útskipting efnis eftir áætlun
Hægt er að skipta út efni við áætlanagerð aðeins þegar er verið að nota formúlur, ekki þegar verið er að nota Uppskrift. Íhugið eftirfarandi dæmi: framleiðslufyrirtæki matvara gerir sósu úr formúlu sem er með 20 innihaldsefni. Eitt innihaldsefni í formúlunni getur verið skipt út fyrir eitt eða tvær önnur efni. Hins vegar, þar sem þessar tvær efnanna eru dýrari en ákjósanlega innihaldsefni, er skipti á gildum er bara gert ef æskilega innihaldsefni er ekki til á lager. Efni sem hægt er að skipta út kallast A, en efnin tvö sem er hægt að skipta um hann kallast B og C. útskipting efna samkvæmt áætlun er stjórnað af **Áætlunarflokkur** og **Forgang** svæðum á formúlulína. Til dæmis, er stofnuð formúlulínur fyrir efnin þrjú og tengja formúlu línur með sömu áætlunarflokk. Í uppsetningu, hefur  formúlulína efnis A mestan forgang (lægsta númer), formúlulína fyrir efni C er með minnstan forgang og formúlulína efnis B hefur forgang sem er á milli forgang hinna tveggja línanna. Ef eftirspurn er fyrir endanlega vöru, ákvarðar aðaláætlanagerð fyrst hvort eftirspurnarspá fyrir efni A sé hægt að ná yfir. Ef ekki er hægt að þekja eftirspurn, lítur aðaláætlanagerð til efanna B og C samkvæmt forgangi. Ef efni B er á lager, er það notað eftir að áætlaða runutillögu er fest fyrir formúluna. Ef engin af efni eru á lager, stofnar aðaláætlanagerð tillögu áætluð pöntun fyrir efni A. **Ábending:** Þegar sett er upp formúlulínur í áætlunarflokki, ætti að tilgreina magn einungis fyrir á efni sem hefur mestan forgang. Þetta magn er notað til að reikna út þörfina fyrir að allt efni í áætluninni, jafnvel hráefni sem hafa lægra forgang. Ekki er hægt að tilgreina mismunandi magn á cörur neðri forgangs í áætlunarflokki.

## <a name="substituting-material-during-production"></a>Skipta út efni við framleiðslu
Íhugið eftirfarandi dæmi: á málmiplata er krafist fyrir suðuaðgerð. Við aðgerðina, tilkynnir starfsmaður í vöruhúsi á starfsmanni á vél að plöturnar eru ekki til á lager. Hins vegar er ákveðið að plötunni má skipta út fyrir plötu sem er aðeins þykkari. Hátt er hægt að ljúka aðgerðinni. Hægt er að bæta efni við Uppskrift fyrir opna framleiðslupöntun. Ef framleiðslupöntunin hefur stöðuna **Byrjað**, eru notendur beðnir um að endurmeta pöntunina þegar þeir bæta við nýju atriði við framleiðsluuppskrift. Eftir að efnis er bætt við er hægt að stofna nýja tiltektarlista fyrir nýja vöru. ekki Þarf að bæta nýju efni við framleiðsluuppskrift. Í staðinn er hægt að bæta það beint við tiltektarlista framleiðslu. Síðan, þegar tiltektarlistinn er bókaður, bætir kerfið efninu við  framleiðsluuppskrift.




