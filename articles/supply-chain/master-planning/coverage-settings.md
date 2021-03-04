---
title: Þekjustillingar
description: Þetta efnisatriði veitir upplýsingar um þekjustillingar sem aðalröðun notar til að reikna út vöruþarfir.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1134f734f1025151a56b2a72266a6baa5763ba4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430579"
---
# <a name="coverage-settings"></a>Þekjustillingar

[!include [banner](../includes/banner.md)]

Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir.

Hægt er að tilgreina þekjustillingar með nokkrum aðferðum:

- Tilgreina þekjustillingar fyrir þekjuflokk.

    Hægt er að stofna þekjuflokk sem inniheldur stillingar fyrir allar afurðir sem eru tengdar við þekjuflokkinn. Til að stofna þekjuflokk skal opna **Aðaláætlanagerð &gt; Uppsetning &gt; Þekja &gt; Þekjuflokkar**. Hægt er að tengja þekjuflokk við vöru. Ef tengillinn er tilgreindur fyrir svæði, vöruhús eða afurðarvídd skal nota reitinn **Þekjuflokk** á síðunni **Vöruþekja**. Sé tengillinn almennur, án tillits til afurðarvídda, skal nota reitinn **Þekjuflokk** á flýtiflipanum **Áætlun** á síðunni **Afurðarupplýsingar**. Ef þú tengir ekki þekjuflokk við afurð notar aðaláætlanagerð sem sjálfgildi almennan þekjuflokk sem tilgreindur er á síðunni **Færibreytur áætlanagerðar**.

- Tilgreinið þekjustillingar fyrir afurð.

    Hægt er að breyta stillingunni fyrir ákveðna framleiðslupöntun hvenær sem er. Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**. Veljið afurðina og síðan í Aðgerðarrúðu á flipanum **Áætlun**, í flokknum **Þekja**, skal velja **Vöruþekja** til að opna síðuna **Vöruþekja**. Ef afurð er tengd þekjuflokki er hægt að hnekkja þekjuflokksstillingum með því að nota reitinn **Hnekkja**. Þekjustillingar á síðunni **Vöruþekja** taka forgang yfir stillingar á síðunni **Þekjuflokkur**.

- Tilgreinið þekjustillingar fyrir afurð með því að nota leiðsagnarforrit.

    Leiðsagnarforritið leiðir þig skref fyrir skref í gegnum ferlið við að setja upp færibreytur fyrir helstu vöruþekjuna. Á síðunni **Vöruþekja**, í aðgerðarúðunni, er valið **Leiðsagnarforrit** til að opna **Leiðsagnarforrit vöruþekju**.

- Tilgreinið þekjustillingar fyrir víddarflokk.

    Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**. Á síðunni **Upplýsingar um losaðar afurðir** á flýtiflipanum **Almennt**, í hlutanum **Stjórnun**, er smellt á tengilinn í reitnum **Geymsluvíddarflokkur**. Á síðunni **Geymsluvíddarflokkur** skal velja gátreitinn **Þekjuáætlun eftir vídd** til að stofna þekjustillingar fyrir vídd í geymsluvíddarflokknum. Velja verður reitinn **Þekjuáætlun eftir vídd** fyrir allar afurðarvíddir, t.d. skilgreiningu, lit, stærð og stíl.


## <a name="coverage-codes"></a>Þekjukóðar

Hægt er að stilla aðalskipulagningu til að nota mismunandi áfyllingaraðferðir. Áfyllingaraðferðirnar eða lotustærðaraðferðirnar eru aðferðirnar sem kerfið notar til að ákvarða runustærð fyrir keyptar eða framleiddar vörur. 

Hverri áfyllingaraðferð er úthlutað einum af eftirfarandi umfjöllunarkóðum:

- **Handbók** - Lotustærðaraðferðin þar sem kerfið bendir ekki til kaupa, flutnings eða framleiðslupantana fyrir hlutinn. Skipuleggjandi fyrir hlutinn mun sjá um að búa til nauðsynlegar pantanir fyrir áfyllingu hlutarins.
- **Eftir þörfum** - Lotustærðaraðferðin þar sem kerfið býr til fyrirhugaða innkaupa-, flutnings- eða framleiðslupöntun eftir þörfum fyrir hlutinn. Þetta er almennt notað fyrir dýrar vörur með óreglulega eftirspurn.  
- **Á hvert tímabil** - Lotustærðaraðferðin sem sameinar alla eftirspurnina á tímabili í eina pöntun á vörunni. Pöntunin verður áætluð fyrir fyrsta dag tímabilsins og magn hennar uppfyllir nettókröfur á tilteknu tímabili. Tímabilið byrjar með fyrstu eftirspurn eftir vörunni og nær yfir skilgreinda tímalengd. Næsta tímabil byrjar með næstu eftirspurn eftir vörunni.
- **Lágm./Hám.** - Lotustærðaraðferðin sem inniheldur áfyllingu birgða upp að vissu marki þegar spáð lagermagn er undir viðmiðunarmörkum. Áfyllingarmagnið verður munurinn á milli hámarksstigs og spáðs stigs lagermagns.


## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit aðaláætlana](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]