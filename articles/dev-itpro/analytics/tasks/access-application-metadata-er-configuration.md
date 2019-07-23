---
title: Fá aðgang að lýsigögnum hugbúnaðar með notkun á grunnstillingum rafrænnar skýrslugerðar
description: Skrefin í þessu efni útskýra hvernig notandi Regulatory Configuration Service (RCS) getur sett upp nýja líkanavörpun rafrænnar skýrslugerðar með notkun á lýsigögnum í Finance and Operations
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b95b41b27cecd4c71ed7646f329cf5736a01b561
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727030"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Fá aðgang að lýsigögnum hugbúnaðar með notkun á grunnstillingum rafrænnar skýrslugerðar

[!include [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi Regulatory Configuration Service í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp nýja líkanavörpun rafrænnar skýrslugerðar með því að nota lýsigögn forritsins Dynamics 365 for Finance and Operations. Farið verður í lýsigögn forrits með því að nota skilgreiningar ER-lýsigagna sem innihalda sýnishorn af lýsigögnum til að fá aðgang að utanríkisviðskiptum. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í RCS í efnisatriðinu, ferlinu [Stofna skilgreiningarveitendur og merkja þá sem virka](er-configuration-provider-mark-it-active-2016-11.md). Í Finance and Operations skaltu síðan ljúka við skrefin í efninu, [(ER) Undirbúa lýsigögn hugbúnaðar sem á að nota í RCS](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>Forkröfur
1. Farðu í **Öll vinnusvæði** > **Rafræn skýrslugerð**. 
2. Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="import-metadata-configuration"></a>Flytja inn skilgreiningu lýsigagna 
1. Smelltu á **Skilgreiningu lýsigagna**. 
2. Flyttu inn lýsigögn rafrænnar skýrslugerðar sem inniheldur lýsigögn úr forritinu Finance and Operations sem er stillt til að búa til rafræn skjöl fyrir utanríkisviðskipta. Þessi lýsigagnastilling rafrænnar skýrslugerðar hefur verið flutt út sem XML-skrá á meðan skrefin í ferlinu [(ER) Undirbúa umsóknardagatalið sem á að nota í RCS](prepare-application-metadata-rcs.md) hefur verið lokið. 
3. Smelltu á **Skipta út**. 
4. Smelltu á **Hlaða úr XML-skrá**. 
5. Smelltu á **Skoða** og veldu skrána „Foreign trade metadata.xml“. 
6. Smellt er á **OK**. 
7. Lokið síðunni. 

## <a name="create-data-model-configuration"></a>Stofna nýja skilgreiningu gagnalíkans
1. Smellið á **Skilgreiningar skýrslugerðar**. 
2. Smellið á **Stofna skilgreiningu** til að opna felligluggann. 
3. Í reitinn **Heiti** slærðu inn „Líkan utanríkisverslunar“. 
4. Smellið á **Stofna skilgreiningu**. 
5. Smellið á **Hönnuður**. 
6. Smelltu á **Nýtt** til að opna felligluggann. 
7. Í reitnum **Heiti** skaltu færa inn „Rót“. 
8. Smelltu á **Bæta við**. 
9. Smelltu á **Nýtt** til að opna felligluggann. 
10. Í reitinn **Heiti** slærðu inn „Færsla“. 
11. Í reitnum **Gerð vöru** velurðu **Skráalisti**. 
12. Smelltu á **Bæta við**. 
13. Smelltu á **Nýtt** til að opna felligluggann. 
14. Í reitinn **Heiti** slærðu inn „Grunnvörukóði“. 
15. Í reitnum **Gerð vöru** velurðu **Strengur**. 
16. Smelltu á **Bæta við**. 
17. Smelltu á **Nýtt** til að opna felligluggann. 
18. Í reitinn **Heiti** slærðu inn „Reikningsfærð upphæð“. 
19. Í reitnum **Gerð vöru** velurðu **Rauntala**. 
20. Smelltu á **Bæta við**. 
21. Smelltu á **Nýtt** til að opna felligluggann. 
22. Í reitinn **Heiti** slærðu inn „Dags.“. 
23. Í reitnum **Gerð vöru** velurðu **Dags.**. 
24. Smelltu á **Bæta við**. 
25. Smelltu á **Rótartilvísun**. 
26. Smellt er á **OK**. 
27. Smellt er á **Vista**. 
28. Lokið síðunni. 
29. Smelltu á **Breyta stöðu**. 
30. Smelltu á **Ljúka**. 
31. Smellt er á **OK**. 

## <a name="create-model-mapping-configuration"></a>Búa til skilgreiningu líkanavörpunar 
1. Smellið á **Stofna skilgreiningu** til að opna felligluggann. 
2. Í reitinn **Nýtt** slærðu inn „Vörpun líkans byggir á gagnalíkani Líkan utanríkisverslunar“. 
3. Í reitinn **Heiti** slærðu inn „Vörpun utanríkisverslunar“. 
4. Smellið á **Stofna skilgreiningu**. 
5. Stækkaðu hlutann **Skilyrði**. 
6. Smellið á **Breyta**. 
7. Smellt er á **Nýtt**. 
8. Í listanum skal merkja valda línu. 
9. Í reitnum **Gerð forkröfuíhlutar** velurðu **Skilgreining**. 
10. Veldu skilgreininguna **Lýsigögn utanríkisviðskipta**. 
11. Smellt er á **Vista**. 
12. Við bættum tilvísuninni við í útgáfu 1 af skilgreiningunni „Lýsigögn utanríkisviðskipta“. Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan verið er að setja þessa líkanavörpun upp. 
13. Lokið síðunni. 
14. Smellið á **Hönnuður**. 
15. Smellið á **Hönnuður**. 
16. Í trénu velurðu **Dynamics 365 for Operations\Töflufærslur**. 
17. Smelltu á **Bæta rót við**. 
18. Í reitinn **Heiti** slærðu inn „Intrastat“. 
19. Veldu **Intrastat**-töflufærslur. 
20. Smellt er á **OK**. 

> [!NOTE]
> Einu 2 töflurnar voru boðnar þar sem aðeins 2 töflum var bætt í sett af lýsigögnum sem eru í notkun. 

21. Smelltu á **Binda**. 
22. Í trénu víkkarðu út **Intrastat**. 
23. Í trénu velurðu **Intrastat\AmountMST**. 
24. Í trénu víkkarðu út **Færsla = Intrastat**. 
25. Í trénu velurðu **Færsla = Intrastat\Reikningsfærð upphæð**. 
26. Smelltu á **Binda**. 
27. Í trénu velurðu **Intrastat\TransDate**. 
28. Í trénu velurðu **Færsla = Intrastat\Dags.**. 
29. Smelltu á **Binda**. 
30. Í trénu víkkarðu út **Intrastat\>Vensl**. 
31. Í trénu víkkarðu út **Intrastat\>Vensl\IntrastatCommodity**. 
32. Í trénu víkkarðu út **Intrastat\>Vensl\IntrastatCommodity\Kóði**. 
33. Í trénu velurðu **Færsla = Intrastat\Grunnvörukóði**. 
34. Smelltu á **Binda**. 
35. Smelltu á **Villuleita**. 

> [!NOTE]
> Okkur tókst að binda þætti gagnalíkans við atriði gagnagjafa sem er lýst með því að nota upplýsingar um lýsigögn forrits úr þeirri skilgreiningu lýsigagna rafrænnar skýrslugerðar. 
36. Smellt er á **Vista**. 
37. Lokið síðunni. 
38. Lokið síðunni. 
39. Þegar þú þarft að framlengja núverandi safn lýsigagna geturðu gert það í Finance and Operations. Síðan er hægt að flytja út nýlokna útgáfu af skilgreiningu lýsigagna rafrænnar skýrslugerðar úr Finance and Operations, flytja hana inn í RCS og uppfæra skilyrði þess að skilgreind líkanavörpun vísi í nýja útgáfu af innfluttri skilgreiningu lýsigagna. 

> [!NOTE]
> Þessi leið til að sækja upplýsingar um lýsigögn hugbúnaðar er sú eina sem er í boði fyrir staðbundið uppsett forrit (þegar uppsetningarlíkan staðbundinna eða innanhúss viðskiptagagna (LBD) er notað fyrir Dynamics 365 for Finance and Operations).
        
