---
title: Eftirspurnarstýrð áætlanagerð
description: Greinin lýsir því hvernig á að búa til áætlaðar pantanir fyrir vörur sem eru settar upp sem aftengingarpunktar.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740303"
---
# <a name="demand-driven-planning"></a>Eftirspurnarstýrð áætlanagerð

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Greinin lýsir því hvernig á að búa til áætlaðar pantanir fyrir vörur sem eru settar upp sem aftengingarpunktar.

## <a name="net-flow-and-qualified-demand"></a>Hreint flæði og hæf eftirspurn

Við aðalskipulag beitir kerfið hugmyndinni um *nettóflæði* til að ákvarða virkt birgðamagn byggt á raunverulegum birgðum á lager, að viðbættum birgðum sem eru í pöntun (núverandi birgðapantanir sem eru ekki enn mótteknar), að frádregnum því sem vísað er til sem *hæfa eftirspurn* (hæfur komandi sala), eins og sýnt er á eftirfarandi mynd. Þegar kerfið er að ákvarða hvaða biðminni hlutur tilheyrir og hvert pantað magn ætti að vera, metur það nettóflæðið, ekki raunverulega birgðabirgðir.

![Dæmi um nettóflæðisreikningsrit.](media/ddmrp-net-flow-example.png "Dæmi um nettóflæðisreikningsrit")

Þegar skipulögð pöntun er ræst í áætlunarkeyrslu verður pantað magn hámarksstig að frádregnum nettóflæði. Til að úthluta pöntunarforgangi notar kerfið [forgangsmiðaða áætlanagerð](priority-based-planning.md) virkni í stað kröfudagsetningar. Eftirspurnardrifin efnisþörf áætlanagerð (DDMRP) úthlutar forgangi áætlaðrar pöntunar byggt á pöntuðu magni sem hlutfall af hámarksbirgðum. Í fyrri myndinni er pantað magn 53 prósent af hámarksmagni. Þess vegna verður pöntunarforgangur fyrir áfyllingu 53. (Fyrir samhengi er 0 hæsti forgangurinn og 100 er lægstur.)

*Hæfð eftirspurn* er gjaldfallin eftirspurn, plús eftirspurn í dag, plús hækkuð pöntunarhækkanir í framtíðinni. Eftirfarandi mynd sýnir dæmi um eftirspurnarstig í dag (12. júní) og næstu þrjá daga. DDMRP gerir þér kleift að stilla pöntunarhámarksþröskuld til að bera kennsl á eftirspurn sem er umfram venjulegar væntingar. Ef þröskuldurinn er stilltur á 25 stykki, munu tvær af framtíðardagsetningunum sem sýndar eru á myndinni gilda sem pöntunarauka. Þú verður að úthluta pöntunarhámarksþröskuldi fyrir hverja vöru fyrir sig með því að nota hana **Vöruumfjöllun** síðu, eins og lýst er í [Settu upp biðminni fyrir hlut aftengingarpunkts](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Dæmi um hæft útreikningstöflu fyrir eftirspurn.](media/ddmrp-net-qualified-demand-example.png "Dæmi um hæft útreikningstöflu fyrir eftirspurn")

Að því tilskildu að það sé engin eftirspurn eftir gjalddaga geturðu nú bætt eftirspurn dagsins (18) við magn tveggja pöntunarhámarka (29 og 26) til að fá fullgilda eftirspurn upp á 73. Jafnvel þó það sé eftirspurn fyrir 23. júní, taktu eftir því að það er ekki innifalið í nettóflæðisútreikningnum, vegna þess að DDMRP kallar fram áætlunarpöntun á annan hátt en hefðbundnir áætlanagerðarhópar.

## <a name="generating-planned-orders-with-ddmrp"></a>Búa til fyrirhugaðar pantanir með DDMRP

Meðan á áætlunarkeyrslu stendur mun kerfið búa til nýja áætlunarpöntun ef nettóflæði vöru fer niður fyrir endurpöntunarpunkt. Þegar þú notar DDMRP muntu venjulega gera áætlanagerð á hverjum degi. Þess vegna ertu í rauninni að athuga birgðastöðurnar þínar einu sinni á dag til að ákvarða hvaða vörur þarf að fylla á.

Eftirfarandi mynd sýnir dæmi um aðstæður þar sem þú ert með pöntun fyrir 18 stykki 20. júní, 29 stykki 21. júní, 26 stykki 22. júní og 20 stykki 23. júní. Vegna þess að toppþröskuldurinn er stilltur á 25 stykki eru tvær af þessum pöntunum merktar sem toppa. Það eru 220 stykki af þessum hlut á hendi.

![Skipulagsdæmi 1.](media/ddmrp-planning-example-1.png "Skipulagsdæmi 1")

Ef þú keyrir aðaláætlanagerð núna mun það búa til áætlaða pöntun ef nettóflæðið finnst fara niður fyrir endurpöntunarpunktinn (219 stykki í þessu dæmi).

![Skipulagsdæmi 2.](media/ddmrp-planning-example-2.png "Skipulagsdæmi 2")

Þetta dæmi framleiðir áætlaða innkaupapöntun fyrir magnið 130, sem jafngildir hámarksstigi mínus nettóflæði. Fyrirhugaðri pöntun er úthlutað forgangi 53,07, miðað við hlutfall hennar af hámarksmagni. Vegna þess að þessi gildi fundust 20. júní, býr kerfið til áætlaða pöntun sem er dagsett 20. júní auk aftengdra afgreiðslutíma vörunnar (fimm virkir dagar í þessu dæmi). Því vegna þess að fimm virkir dagar eru ein vika frá deginum í dag er fyrirhuguð pöntun dagsett 27. júní.

> [!NOTE]
> Aðalskipulag reiknar aðeins aftengda hluti með því að nota DDMRP. Allir aðrir hlutir eru reiknaðir út með því að nota staðlaða áætlanagerð um efniskröfur (MRP).
