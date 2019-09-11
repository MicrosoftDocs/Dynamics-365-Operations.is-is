---
title: Sjálfvirk uppfærsla á eignateljurum
description: Þetta efni lýsir sjálfvirkri uppfærslu á eignateljurum í eignastýringu.
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
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875721"
---
# <a name="automatic-update-of-asset-counters"></a>Sjálfvirk uppfærsla á eignateljurum

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Í fyrri hlutanum er lýst handvirkri skráningu eignateljara. Uppsetning eignateljara er lýst í [Teljarar](../setup-for-objects/counters.md).

Einnig er hægt að uppfæra teljaragildi sjálfkrafa úr framleiðsluskráningum, byggt á framleiðslutíma eða framleiðslumagni. Þetta er gert í **Uppfæra eignateljara**. Þú getur uppfært eina eða fleiri eignir með því að setja eina færibreytu inn, **Frá dagsetningu**. Þessi færibreyta tilgreinir upphafsdagsetningu framleiðsluskráninga (klukkustundir eða magn framleitt), sem þýðir upphafsdagsetninguna sem uppfæra ætti teljaragildi frá.

Allar eignir sem tengjast tilföngum *og* hafa eignateljara, sem eru settar upp til að uppfæra miðað við framleitt magn eða framleiðslutíma, verða með í sjálfvirkri uppfærslu og ný teljaragildi verða til.

Varðandi teljarana sem eru miðaðir við framleiðslumagn, þá er gallalaust magn sem og villumagn skráð með í talningunni. Ef einingin sem notuð er fyrir skráningu á framleiddu magni er frábrugðin einingunni sem notuð er í teljaranum er magni breytt til að samsvara teljaraeiningunni.

Eins og getið er hér að ofan er hægt að uppfæra sjálfvirka teljara úr framleiðsluskráningum. Þess vegna verður eignin sem þú vilt uppfæra teljara sjálfkrafa fyrir að tengjast tilföngum (vél). Eftirfarandi lýsingar veita yfirlit yfir uppsetningu og vinnslu framleiðslupantana (í einingunni **Framleiðslustýring**), sem er notuð sem grunnur fyrir sjálfvirka uppfærslu á teljurum á eign í einingunni **Eignastýring**.

Þegar framleitt magn eða framleiðslutími hefur verið skráður á tilföngin geturðu uppfært tengda eignateljara.

1. Smelltu á **Eignastýring** > **Reglubundið** > **Eignir** > **Uppfæra eignateljara**.

2. Veldu upphafsdagsetningu sjálfvirku uppfærslunnar í reitnum **Frá dagsetningu**.

>[!NOTE]
>Dagsetningin í þessum reit er dagsetningin „verk í vinnslu“ frá og með **Leiðarfærslur** (reiturinn **Framleiðslustýring** > **Fyrirspurnir og skýrslur** > **Framleiðsla** > **Leiðarfærslur** > **Efnisleg dagsetning**).

3. Ef þú vilt velja tilteknar eignir, eignategundir eða tilföng fyrir sjálfvirka uppfærslu skaltu smella á **Sía** á flýtiflipanum **Færslur til að hafa með** og gera viðeigandi val.

4. Ef með þarf er hægt að setja upp sjálfvirka uppfærslu sem runuvinnslu á flýtiflipanum **Keyra í bakgrunni**.

![Mynd 1](media/12-work-orders.png)

5. Smellt er á **OK**. Þegar sjálfvirka uppfærsla á eignateljara er lokið geturðu séð teljaraskráningar tengdar eigninni í **Eignateljar** (**Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir** > veldu eign > hnappurinn **Teljarar**).

Í **Heildartala eigna** er hægt að fá yfirlit yfir nýjustu skráningu sem var gerð á öllum teljaragerðum á öllum eignum. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Uppsafnað gildi eigna**. Yfirlitið er mjög svipað og **Eignateljar**, en þú getur ekki bætt við eða breytt skráningum í **Samanlagt verðmæti eigna**. Það er aðeins til yfirlits.

![Mynd 2](media/13-work-orders.png)


- Enn er hægt að búa til handvirkar teljaragildisskráningar fyrir teljaragerðir sem eru uppfærðar sjálfkrafa. Nánari upplýsingar er að finna í hlutanum „Handvirk uppfærsla á eignateljurum“.
- Hægt er að setja upp teljara sem tengjast öðrum teljara, sem þýðir að þegar teljari er uppfærður eru skyldir teljarar uppfærðir sjálfkrafa um leið. Sjá [Teljarar](../setup-for-objects/counters.md) varðandi uppsetningu á tengdum teljurum.
