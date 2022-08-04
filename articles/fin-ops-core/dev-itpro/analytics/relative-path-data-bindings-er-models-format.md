---
title: Notaðu viðeigandi slóð í gagnabindingum ER-líkana og sniða
description: Í rafrænu skýrsluverkfæri er hægt að skilgreina skipulag rafræns sniðs og lýsa því síðan hvernig á að fylla þetta út.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: be2c0f921fde13598685553ea01bfcf3f8255362
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108672"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Notaðu viðeigandi slóð í gagnabindingum ER-líkana og sniða

[!include[banner](../includes/banner.md)]

Verkfærið Rafræn skýrslugerð (ER) gerir notendum kleift að skilgreina skipulag á rafrænu sniði og lýsa síðan hvernig fylla skal út þetta skipulag með því að nota gögn og reiknirit sem eru til í forritinu. Frekari upplýsingar er að finna í [Stofna skilgreiningar rafrænnar skýrslugerðar (ER)](electronic-reporting-configuration.md). Til að tilgreina gagnaflæði til að sækja fjárhags- og rekstrargögn og nota þau til að búa til rafrænt skjal þarftu að gera eftirfarandi:

- Binda skilgreinda gagnagjafa við einingar í uppsettu lénasértæku gagnalíkani. Skipulag líkans og valdir gagnagjafar kunna að vera hluti af flóknu stigveldisskipulagi. Vegna þessa geta endanleg bindingar verið mjög stórar og innihaldið margar einingar af mismunandi gerðum (til dæmis vensl, töflur og aðferðir). Bindingarnar geta orðið minna læsilegar og nokkuð flóknar yfirferðar og skilnings, sérstaklega fyrir aðra en eigendur. 
- Binda gagnalíkaneiningar við sniðsíhluti til að skilgreina hvaða gögn verði fyllt út úr gagnalíkani í úttak myndaðs sniðs.

Til að bæta notagildi vörpunarhönnuða rafrænnar skýrslugerðar er búið að gefa út eiginleikann [tengd slóð](er-formula-language.md#relative-path). Sjálfgefið er að kveikt er á hlutfallslegri framsetningu á slóð fyrir hvert nýtt tilvik af forritinu þar sem ER hönnunarupplifun er virkjuð (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service). Við innleiddum færibreytu viðkomandi slóðar þannig að notendur geta haldið áfram að nota alla slóðina þegar unnið er með þessa kynningu á ER-bindingum.

[![Færibreytur notanda.](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Þegar slökkt er á notkunarfæribreytum viðkomandi slóðar kemur einn @ stafur í stað slóðar á yfirvöru í bindingu núverandi líkanareiningar. Öll bindandi slóðin verður styttri, sem gerir alla vörpunina augljósari og auðveldari í skilningi. Í flestum tilfellum þarf ekki frekari skrun í ER-hönnuði til að skoða allar bindingar gagnalíkansins.

[![Hönnun fyrir vörpun gagnalíkans.](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Þegar þú byrjar uppsetningu á nýrri ER-segð þarftu aðeins að slá inn einn staf til að skilgreina bindingu við reit yfirvörunnar.

[![Formúluhönnuður.](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Þegar þú ákveður að breyta gagnagjafa yfiratriðis með algildri slóðarnotkun þarftu endurbinda þessi líkansatriði, ásamt öllum földuðum atriðum, í nýjan gagnagjafa. Þegar slökkt er á notkun viðkomandi slóðar og þú velur nýjam gagnagjafa til að binda við yfiratriði, er þér boðið upp á valkost til að tengja sjálfkrafa allar faldaðar einingar þessa yfiratriðis með einum smelli.

[![Skilaboðin Skipta um slóð sem er þegar til staðar.](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Ef þú staðfestir endurheimt á földuðum atriðum verður nýtt yfiratriði sett í slóð hvers faldaðs atriðis sem inniheldur fyrirliggjandi yfiratriði.
Þessi eiginleiki brýtur ekki eldra samhæfi ER-rammans. Allar áður uppsettar ER-skilgreiningar munu virka með þessum nýja eiginleika og engar uppfærslur eða umreikningar verða nauðsynleg.

> [!NOTE]
> Allar breytingar sem eru kynntar með fjöldabreytingum á bindingum faldaðra eininga í líkanavörpunum eru rétt vistaðar í skilgreiningar-delta (rakningu breytinga). Þetta gerir viðskiptavinum kleift að endurreikna grunn afleiddrar útgáfu líkanavarpana í nýja grunnútgáfu af því sem hefur verið breytt með því að nota þennan nýja eiginleika.

## <a name="additional-resources"></a>Frekari upplýsingar

[Formúlutungumál rafrænnar skýrslugerðar](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

