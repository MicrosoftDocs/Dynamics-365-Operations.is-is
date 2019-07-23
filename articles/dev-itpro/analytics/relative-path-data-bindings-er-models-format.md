---
title: Notaðu viðeigandi slóð í gagnabindingum ER-líkana og sniða
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6582cca9b912868f88de2770a17cbb6e67328660
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726553"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Notaðu viðeigandi slóð í gagnabindingum ER-líkana og sniða

[!include[banner](../includes/banner.md)]

Verkfærið Rafræn skýrslugerð (ER) gerir notendum kleift að skilgreina skipulag á rafrænu sniði og lýsa síðan hvernig fylla skal út þetta skipulag með því að nota gögn og reiknirit sem eru til í Dynamics 365 for Finance and Operations. Frekari upplýsingar er að finna í [Stofna skilgreiningar rafrænnar skýrslugerðar (ER)](electronic-reporting-configuration.md). Til að tilgreina gagnaflæði til að sækja gögn úr Finance and Operations og nota þau til að búa til rafrænt skjal þarftu að gera eftirfarandi:

- Binda skilgreinda gagnagjafa við einingar í uppsettu lénasértæku gagnalíkani. Skipulag líkans og valdir gagnagjafar kunna að vera hluti af flóknu stigveldisskipulagi. Vegna þessa geta endanleg bindingar verið mjög stórar og innihaldið margar einingar af mismunandi gerðum (til dæmis vensl, töflur og aðferðir). Bindingarnar geta orðið minna læsilegar og nokkuð flóknar yfirferðar og skilnings, sérstaklega fyrir aðra en eigendur. 
- Binda gagnalíkaneiningar við sniðsíhluti til að skilgreina hvaða gögn verði fyllt út úr gagnalíkani í úttak myndaðs sniðs.

Til að bæta nothæfi ER-vörpunarhönnuða hefur hlutfallsleg slóðaeiginleiki hefur verið gefinn út. Sjálfgefið er að slökkt sé á framsetningarvalkosti viðkomandi slóðar fyrir öll ný tilvik Finance and Operations þar sem ER-hönnunarreynsla er virkjuð (Microsoft Dynamics 365 for Finance and Operations, Microsoft Regulatory Configuration Service). Við innleiddum færibreytu viðkomandi slóðar þannig að notendur geta haldið áfram að nota alla slóðina þegar unnið er með þessa kynningu á ER-bindingum.

[![Færibreytur notanda](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Þegar slökkt er á notkunarfæribreytum viðkomandi slóðar kemur einn @ stafur í stað slóðar á yfirvöru í bindingu núverandi líkanareiningar. Öll bindandi slóðin verður styttri, sem gerir alla vörpunina augljósari og auðveldari í skilningi. Í flestum tilfellum þarf ekki frekari skrun í ER-hönnuði til að skoða allar bindingar gagnalíkansins.

[![Hönnun fyrir vörpun gagnalíkans](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Þegar þú byrjar uppsetningu á nýrri ER-segð þarftu aðeins að slá inn einn staf til að skilgreina bindingu við reit yfirvörunnar.

[![Formúluhönnuður](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Þegar þú ákveður að breyta gagnagjafa yfiratriðis með algildri slóðarnotkun þarftu endurbinda þessi líkansatriði, ásamt öllum földuðum atriðum, í nýjan gagnagjafa. Þegar slökkt er á notkun viðkomandi slóðar og þú velur nýjam gagnagjafa til að binda við yfiratriði, er þér boðið upp á valkost til að tengja sjálfkrafa allar faldaðar einingar þessa yfiratriðis með einum smelli.

[![Skilaboðin Skipta um slóð sem er þegar til staðar](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Ef þú staðfestir endurheimt á földuðum atriðum verður nýtt yfiratriði sett í slóð hvers faldaðs atriðis sem inniheldur fyrirliggjandi yfiratriði.
Þessi eiginleiki brýtur ekki eldra samhæfi ER-rammans. Allar áður uppsettar ER-skilgreiningar munu virka með þessum nýja eiginleika og engar uppfærslur eða umreikningar verða nauðsynleg.

> [!NOTE]
> Allar breytingar sem eru kynntar með fjöldabreytingum á bindingum faldaðra eininga í líkanavörpunum eru rétt vistaðar í skilgreiningar-delta (rakningu breytinga). Þetta gerir viðskiptavinum kleift að endurreikna grunn afleiddrar útgáfu líkanavarpana í nýja grunnútgáfu af því sem hefur verið breytt með því að nota þennan nýja eiginleika.
