---
title: Handvirk uppfærsla á eignateljurum
description: Þetta efni lýsir handvirkri uppfærslu á eignateljurum í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875716"
---
# <a name="manual-update-of-asset-counters"></a>Handvirk uppfærsla á eignateljurum

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Teljarar eru notaðir til að búa til skráningar á eign varðandi t.d. fjölda vinnustunda eða fjölda framleidds magns.

Ef teljaragerðin sem er valin fyrir teljara er stillt á að erfa teljaragildi (**Eignastjórnun** > **Uppsetning** > **Gerðir eigna** > **Teljarar** > **Almennt** flýtiflipa > skiptihnappurinn **Erfð teljaragildi eigna** stilltur á „Já“), þá er hver undireign sem notar sömu gerð teljara sjálfvirkt uppfærð þegar þú býrð til nýja teljaralínu af þeirri gerð.

Í **Öllum eignum** stofnarðu teljaraskráningarnar klukkustundir eða magn á eign, byggt á lestri þínum af eigninni.

1. Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Eignir** > **Allar eignir**.

2. Veldu eignina á listanum og smelltu á **Teljarar**. Í glugganum **Eignateljarar** sérðu lista yfir allar fyrri gagnaskráningar á valda eign.

3. Smelltu á **Nýtt** til að stofna nýja skráningu. Auðkenni eignarinnar er sjálfkrafa sett inn.

4. Í reitinn **Teljari** skaltu velja viðeigandi teljara. Aðeins teljarar sem tengjast eignategundinni sem valin er á eigninni eru tiltækir. Tengda einingin er sjálfvirkt sett inn í reitinn **Eining**.

5. Veldu dagsetningu og tíma fyrir teljaraskráningu.

6. Í reitinn **Gildi** skaltu setja inn töluna frá síðustu teljaraskráningu, eða, í reitinn **Uppsafnað gildi** skaltu setja inn heildarfjölda talningar.

- Ef þú setur upp nýjan teljara á eign þarftu að skrá breytinguna á eignina í **Eignateljarar**. Næst verður þú að stofna tvær skráningarlínur með sömu tímastimplum og á línunni varðandi nýja teljarann velurðu gátreitinn **Endurstilling teljara**. Þegar þú býrð til skráningarlínurnar tvær verður fyrsta línan að vera fyrir teljarann sem þú ert að skipta um. Í reitnum **Samtals** er heildartala talningar summan af samanlagðri talningu allra skráðra gilda á þeirri teljaragerð.  
- Ef gátreiturinn **Endurstilling teljara** er valinn á eign með viðhaldsáætlun með bilgerðinni „Einu sinni frá...“ eða „Einu sinni náð...“ er teljarinn enn virkur á nýju teljaralínunni því þú býrð til aðskilda teljaralínu og byrjar upp á nýtt með nýjum teljara.

![Mynd 1](media/11-work-orders.png)


Ef þú þarft að gera teljaraskráningar á nokkrum eignum er hægt að gera það í **Eignastjórnun** > **Fyrirspurnir** > **Eignir** > **Eignateljarar**.

>[!NOTE]
>Þú getur sett upp svið til að skilgreina frávik í handvirkum teljaraskráningum og gerð skilaboða sem á að birtast ef skráningar eru utan skilgreinds sviðs. Sjá efnið [Teljarar](../setup-for-objects/counters.md) varðandi uppsetningu á tengdum teljurum.
