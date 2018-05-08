--- 
title: "Setja upp sniðmát fyrir taxta"
description: "Þessi verklýsing sýnir hvernig á að setja upp taxtasniðmát."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b7c02e5a6f5eeee270ca4b6f91e90f7799c2ca11
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rate-masters"></a>Setja upp sniðmát fyrir taxta

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp taxtasniðmát. stjórnandi vörustjórnunar setur yfirleitt upp taxtasniðmát, allt eftir samningum sem voru undirritað með í flutningsaðila. Í þessu tilfelli verður að setja upp taxtasniðmát fyrir flutningsaðila í lofti. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="set-up-rate-master"></a>Setja upp taxtasniðmát
1. Fara í flutningsstjórnun > Uppsetning >Einkunn > Taxtasniðmát.
2. Smellið á „Nýtt“.
3. Í reitinn Taxtasniðmát skal færa inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitnum Lýsigagnakenni fyrir taxta skal smella á fellilistahnappinn til að opna leitina.
    * Lýsigagnakenni fyrir taxta ákvarða gögn sem þarf fyrir taxtasniðmátið, þar sem það skilgreinir lýsigögn sem TMS vél býst við með þessu taxtasniðmát.  
6. Í þessu dæmi skal velja valkostinn P2P
7. Í listanum skal smella á tengilinn í valinni línu.
8. Smellið á „Vista“.

## <a name="set-up-rate-base"></a>Setja upp taxtagrunn
1. Smellt er á taxtagrunn.
    * Taxtagrunn ákvarðar gengi farmflytjanda og hægt er að nota til að setja upp uppbyggingu taxta þar sem það byggir upp taxta á rofstöðum sem skilgreint í aðalgögnum skila.  
2. Smellið á „Nýtt“.
3. Í reitnum Taxtagrunnur skal færa inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitnum Sniðmát hlés skal smella á fellilistahnappinn til að opna leitina.
    * Sniðmát hlés eru notuð til að skilgreina uppbyggingu verðlagningar og rofstaði hennar. Uppbygging verðlagningar notar lagskipt verðlagningu sem byggir á efnislegum víddum.  
6. Í þessu dæmi notarðu þyngd
7. Í listanum skal smella á tengilinn í valinni línu.
8. Víxla útvíkkun á liðnum upplýsingar.
9. Smellt er á Nýtt.
10. Í reitnum Póstnúmer affermingar frá skal slá inn ‚30301‘.
11. Í reitnum Póstnúmer affermingar til skal slá inn ‚30318‘.
12. Í reitnum Landsvæði affermingar skal slá inn ‚USA‘.
13. Í reitnum <1,00 pund ritið '100'.
    * Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minna en 1 pund.  
14. Í reitnum <5.00 pund ritið '300'.
    * Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minna en 5 pund.  
15. Í reitnum < 20,00 pund ritið '500'.
    * Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minna en 20 pund.  
16. Í reitnum < 100,00 pund ritið '1000'.
    * Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minna en 100 pund.  
17. Í reitnum < 1000,00 pund ritið '3000'.
    * Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minni en 1000 pund.  
18. Smellið á „Vista“.
19. Lokið síðunni.

## <a name="assign-rate-base"></a>Úthluta taxtagrunn
1. Víxla útvíkkun á hluta úthlutana úr taxtagrunnum .
2. Smellið á „Nýtt“.
    * Hægt er að hafa nokkrar úthlutanir taxtagrunns fyrir hverja taxtasniðmát. Þetta gerir mögulegt að stofna nokkra mismunandi verðpunkta fyrir hvern farmflytjanda eftir áfangastaði, þjónustu eða mismunandi taxtagrunnum. Í þessu ferli verður aðeins að stofna eina úthlutun taxtagrunns.  
3. Í reitinn Heiti skal slá inn gildi.
4. Í reitnum Taxtagrunnur skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Í reitnum Þjónusta skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í Svæðið Póstnúmer þar sem sótt er, skal færa inn '98052'.
    * Tilgreina hvaða póstnúmer þessa úthlutun taxtagrunns á að gilda frá.    
10. Í reitnum Landsvæði þar sem sótt er, skal slá inn ‚USA‘.
11. Smellið á „Vista“.


