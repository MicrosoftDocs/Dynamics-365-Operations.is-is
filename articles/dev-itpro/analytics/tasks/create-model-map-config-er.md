--- 
title: "Stofna skilgreiningum á líkanavörpun fyrir rafræna skýrslugerð"
description: "Notaðu þessa aðferð til að hanna nýja stillingu fyrir líkanavörpun rafrænnar skýrslugerðar og nota innbyggða eiginleika Rafrænnar skýrslugerðar fyrir skilvirka samanlagða útreikninga."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 614ef06fcf5761f1cf2afb6e7655558d2858d763
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Stofna skilgreiningum á líkanavörpun fyrir rafræna skýrslugerð

[!include [task guide banner](../../includes/task-guide-banner.md)]

Notaðu þessa aðferð til að hanna nýja stillingu fyrir líkanavörpun rafrænnar skýrslugerðar og nota innbyggða eiginleika Rafrænnar skýrslugerðar fyrir skilvirka samanlagða útreikninga. Í þessu ferli stofnar þú skilgreiningu fyrir sýnifyrirtæki, Litware, Inc. 

Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.

Skrefin er hægt að klára með því að nota hvaða gagnasafn sem er. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka.“

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk. Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka“.  
2. Smelltu á Grunnstillingar skýrslugerðar
3. Smellt er á Sýna síur.
4. Í svæðinu „Nafn“ skal færa inn síugildið „Intrastat“ og nota virknitáknið „byrjar á“.
    * Notið þessa síu til að finna skilgreiningu á gagnalíkaninu „Intrastat“. Þetta líkan kann þegar að vera til í grunnstillingatrénu. Ef það gerist skal sleppa næsta undirverkefni.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Sækja skilgreiningar Intrastat-líkansins sem Microsoft útvegar
1. Lokið síðunni.
2. Lokið síðunni.
3. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja skal Microsoft reitinn.  
5. Smella á Geymslur.
    * Smella skal á Geymslur í Microsoft reitinum.  
6. Smellt er á Sýna síur.
7. Í svæðið „Slá inn heiti“ skal slá inn síugildið „tilföng“ og nota virknitáknið „inniheldur“. 
8. Smellt er á Opin.
9. Í trénu skal velja „Intrastat líkan“.
10. Smelltu á Flytja inn.
11. Smella á Já.
    * Þú fluttir inn grunnstillingu líkans fyrir Rafræna skýrslugerð sem inniheldur gagnalíkan sem skal nota til að læra hvernig hægt er að nota virknina Rafræn skýrslugerð.  
12. Lokið síðunni.
13. Lokið síðunni.
14. Smelltu á Grunnstillingar skýrslugerðar

## <a name="add-a-new-model-mapping-configuration"></a>Bæta við nýrri grunnstillingu líkanavörpunar
1. Í trénu skal velja „Intrastat líkan“.
2. Smellt er á stofna skilgreiningu til að opna fellilistanum.
3. Í svæðið Nýtt skal slá inn „Vörpun líkans byggð á gagnalíkaninu Intrastat“.
4. Í svæðið Heiti skal slá inn „Intrastat sýnivörpun“.
    * Intrastat sýnivörpun  
5. Smelltu á Stofna skilgreiningu.


