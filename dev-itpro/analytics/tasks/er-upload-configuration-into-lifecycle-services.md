--- 
title: "Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) og hlaða upp í Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0681ff81ea673e90b3d281a8e8836e0afb9f5f0
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a>Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) og hlaða upp í Microsoft Lifecycle Services (LCS).

Í þessu dæmi, verður að stofna skilgreiningu og hlaða henni upp í LCS fyrir sýnifyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka". Aðgangur að LCS er einnig nauðsynlegur til að ljúka þessum skrefum.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Velja Litware, Inc. og stillið sem virka.
3. Smellt er á Skilgreiningum.

## <a name="create-a-new-data-model-configuration"></a>Stofna nýjan skilgreiningu gagnalíkans
1. Smellt er á stofna skilgreiningu til að opna fellilistanum.
    * Stofna verður skilgreiningu sem inniheldur dæmi um gagnalíkan fyrir rafræn skjöl. Skilgreining gagnalíkans verður hlaðið upp í LCS síðar.  
2. Í svæðið Heiti, Færðu inn 'dæmi um skilgreining líkans '.
    * Dæmi um líkanaskilgreiningu  
3. Í svæðið lýsing, Færðu inn 'dæmi um skilgreining líkans '.
    * Dæmi um líkanaskilgreiningu  
4. Smelltu á Stofna skilgreiningu.
5. Smellt er á hönnuður Líkana.
6. Smellið á „Nýtt“.
7. Í reitnum Heiti skal færa inn 'aðgangsstaður'.
    * Aðgangsstaður  
8. Smelltu á Bæta við.
9. Smellið á „Vista“.
10. Lokið síðunni.
11. Smellið á „Breyta stöðu“.
12. Smelltu á Ljúka.
13. Smellið á „Í lagi“.

## <a name="register-a-new--repository"></a>Skrá nýjan gagnasafn
1. Lokið síðunni.
2. Smella á Geymslur.
    * Þannig er hægt að opna lista yfir gagnasöfn fyrir Litware, Inc. skilgreiningaveituna.  
3. Smelltu á Bæta við til að opna felligluggann.
    * Þannig er hægt að bæta við nýjum gagnasafni.  
4. Í reitnum gerð gagnasafns fyrir skilgreiningar, veljið LCS.
5. Smellið á Stofna gagnasafn.
6. Færa inn eða veljið gildi í svæðinu verk.
    * Veljið viðeigandi LCS-verk. Þú verður að hafa aðgang að verkinu.  
7. Smellið á „Í lagi“.
    * Ljúka við nýja færslu í gagnasafni.  
8. Í listanum skal merkja valda línu.
    * Velja LCS-færslu gagnasafns.  
    * Athugið að skráð gagnasafn er merkt eftir núverandi veitu þ.e.a.s aðeins skilgreiningar í eigu þeirrar veitu er hægt að setja í þetta gagnasafn, þar af leiðandi hlaðið upp í valið LCS-verk.  
9. Smellt er á Opin.
    * Opna gagnasafn til að skoða lista yfir skilgreiningar Rafræn skýrslugerð . Það verður auður ef þetta verk hefur ekki enn verið notað fyrir samnýtingu skilgreininga fyrir Rafræn skýrslugerð.  
10. Lokið síðunni.
11. Lokið síðunni.

## <a name="upload-configuration-into-lcs"></a>Hlaða skilgreiningu í LCS
1. Smellt er á Skilgreiningum.
2. Veljið 'dæmi um skilgreiningu líkans', í trénu.
    * Velja stofnaða skilgreiningu sem þegar hefur verið lokið.  
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið útgáfu valinnar skilgreiningar með stöðuna "Lokið".  
4. Smellið á „Breyta stöðu“.
5. Smellt er á samnýta.
    * Staða Skilgreiningar breytist úr "Lokið" til 'Samnýttar' þegar hún er birt á LCS.  
6. Smellið á „Í lagi“.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veldu Útgáfa skilgreiningar stöðuna samnýtt.  
    * Athugið að staða valda útgáfu hefur breyst úr "Lokið" í 'Samnýttar'.  
8. Lokið síðunni.
9. Smella á Geymslur.
    * Þannig er hægt að opna lista yfir gagnasöfn fyrir Litware, Inc. skilgreiningaveituna.  
10. Smellt er á Opin.
    * Velja lcs-gagnasafn og opna hana.  
    * Athugið að valin skilgreining er sýnd sem eign valins LCS verks.  
    * Opnaðu LCS með því að nota https://lcs.dynamics.com. Opna verkið sem var notuð áður til skráningar gagnasafns, opna 'eignasafni' þessa verks og útvíkka innihald eignagerðarinnar 'GER skilgreining' – upphlaðin skilgreining Rafrænnar skýrslugerðar verða tiltæk. Athugaðu að upphalaðri LCS skilgreiningu er hægt að flytja inn í annað tilvik af Microsoft Dynamics Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ef veiturnar hafa aðgang að þessu LCS verkinu.  


