--- 
title: "Setja upp endurúthlutun fyrir stutta vörutiltekt"
description: "Þessi verklýsing sýnir hvernig starfsmenn vöruhúss geta fundið aðrar staðsetningar fljótt ef það eru ekki nægilegar birgðir á staðsetningunni þangað sem þeim var beint."
author: ShylaThompson
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b67965b6c8641b5d91ab3c5b0a7a7fd28a07cba6
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Setja upp endurúthlutun fyrir stutta vörutiltekt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig starfsmenn vöruhúss geta fundið aðrar staðsetningar fljótt ef það eru ekki nægilegar birgðir á staðsetningunni þangað sem þeim var beint. Það er hægt að nota sjálfvirkt endurúthlutunarferli, sem notar staðsetningarleiðbeiningar til að sækja vörur ef þær eru tiltækar á aðra staðsetningu. Einnig er þegar handvirka endurúthlutunin er notuð, er lista yfir staðsetningar með tiltæku magni sýndur í fartækinu, þar sem starfsmaður í vöruhúsi getur valið hvaða staðsetningar til að nota birgðir úr. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="set-up-work-exceptions"></a>Setja upp vinnuundantekningar
1. Fara í Vöruhúsakerfi > Uppsetning > Vinna > Undantekningar verks.
2. Smellið á „Nýtt“.
    * Það er hægt að skilgreina margar vinnuundantekningar ásamt mismunandi endurúthlutunarreglum til að gera starfsmaður í vöruhúsi mögulegt að velja eitt á grundvelli þess sem sendingin sem verið er að vinna þarf.  
3. Færa inn gildi í reitnum Kenni undantekningar verks.
    * Gefðu vinnuundantekningunni titil sem segir til um tilgang hennar. Til dæmis, handbók fyrir of litla tiltekt.  
4. Sláið inn gildi í reitnum „Lýsing“.
5. Veljið "of lítil tiltekt" í svæðinu gerð undantekningar.
6. Velja gátreitinn leiðrétta birgðir
    * Þessi valkostur þýðir að birgðir verða sjálfvirkt leiðréttar á 0 á staðsetningu þar sem tiltekt er of lítil.  
7. Sláið inn eða veldu gildi í reitnum sjálfgefinn kóði leiðréttingargerðar.
    * Til dæmis í USMF er hægt að velja "Remove Res Adj Out".  
8. Í reitnum Endurúthlutun vöru er valið "Handvirkt".
    * Ef valið er Handvirkt, eða Sjálfvirkar og Handvirkar, þarf starfsmaður í vöruhúsi að geta notað handvirka endurúthlutun.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Setja upp starfsmann til að nota handvirka endurúthlutun vöru
1. Lokið síðunni.
2. Fara í Vöruhúsakerfi > Uppsetning > Starfskraftur.
3. Smellið á „Breyta“.
4. Í listanum skal velja starfskraft 24.
5. Víkkið út hlutann vinna.
6. Velja skal Já í svæðinu Leyfa handvirka endurúthlutun vöru.


