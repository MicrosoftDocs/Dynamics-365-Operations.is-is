---
title: Setja upp endurúthlutun fyrir stutta vörutiltekt
description: Þessi verklýsing sýnir hvernig starfsmenn vöruhúss geta fundið aðrar staðsetningar fljótt ef það eru ekki nægilegar birgðir á staðsetningunni þangað sem þeim var beint.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eae86b307ac8d8539c3897293c2fc21ea57d2d60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148240"
---
# <a name="set-up-short-picking-item-reallocation"></a>Setja upp endurúthlutun fyrir stutta vörutiltekt

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig starfsmenn vöruhúss geta fundið aðrar staðsetningar fljótt ef það eru ekki nægilegar birgðir á staðsetningunni þangað sem þeim var beint. Það er hægt að nota sjálfvirkt endurúthlutunarferli, sem notar staðsetningarleiðbeiningar til að sækja vörur ef þær eru tiltækar á aðra staðsetningu. Einnig er þegar handvirka endurúthlutunin er notuð, er lista yfir staðsetningar með tiltæku magni sýndur í fartækinu, þar sem starfsmaður í vöruhúsi getur valið hvaða staðsetningar til að nota birgðir úr. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="set-up-work-exceptions"></a>Setja upp vinnuundantekningar
1. Í **Skoðunarrúðu** ferðu í **Vöruhúsakerfi > Uppsetning > Vinna > Undantekningar verks**.
2. Smellt er á **Nýtt**. Það er hægt að skilgreina margar vinnuundantekningar ásamt mismunandi endurúthlutunarreglum til að gera starfsmaður í vöruhúsi mögulegt að velja eitt á grundvelli þess sem sendingin sem verið er að vinna þarf.  
3. Í reitinn **Kenni undantekningar verks** skaltu færa inn gildi. Gefðu vinnuundantekningunni titil sem segir til um tilgang hennar. Til dæmis, handbók fyrir of litla tiltekt.  
4. Í reitinn **Lýsing** skal slá inn gildi.
5. í reitnum **Gerð undantekningar** skaltu velja „of lítil tiltekt“.
6. Veldu gátreitinn **Leiðrétta birgðir**. Þessi valkostur þýðir að birgðir verða sjálfvirkt leiðréttar á 0 á staðsetningu þar sem tiltekt er of lítil.  
7. Í reitinn **Sjálfgefinn kóði leiðréttingargerðar** skal færa inn eða velja gildi. Til dæmis í USMF er hægt að velja "Remove Res Adj Out".  
8. Í reitnum **Endurúthlutun vöru** er valið "Handvirkt". Ef valið er Handvirkt, eða Sjálfvirkar og Handvirkar, þarf starfsmaður í vöruhúsi að geta notað handvirka endurúthlutun.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Setja upp starfsmann til að nota handvirka endurúthlutun vöru
1. Lokið síðunni.
2. Í **Skoðunarrúðu** ferðu í **Vöruhúsakerfi > Uppsetning > Vinna > Starfskraftur**.
3. Smellið á **Breyta**.
4. Í listanum skal velja starfskraft 24.
5. Útvíkkaðu flýtiflipann **Vinna**.
6. Veldu „Já“ í reitnum **Leyfa handvirka endurúthlutun vöru**.

