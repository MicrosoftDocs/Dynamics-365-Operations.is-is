---
title: Senda verkbeiðni
description: Þetta efni útskýrir hvernig á að senda verkbeiðni í eignastýringu.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87f67f4db143fabbfae926e30e7e5d97ac6af0f6fa5469218e4ab3605aa44dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778725"
---
# <a name="dispatch-work-order"></a>Senda verkbeiðni

[!include [banner](../../includes/banner.md)]

 

Þú getur tímasett eina verkbeiðni eða verkbeiðnivinnslur fyrir einn starfskraft með því að nota aðgerðina **Senda**.

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.

2. Verkbeiðnin er valin af listanum.

3. Á flipanum **Almennt** er smellt á **Senda**.

4. Í glugganum **Áætla verkbeiðni** velurðu starfskraftinn í reitnum **Starfskraftur**.

5. Í reitinn **Áætlunartíma** er hægt að setja inn áætlaða vinnutíma ef áætlaður vinnutími er frábrugðinn spátímanum.

6. Í reitnum **Áætlað upphaf** er hægt að breyta upphafsdegi og -tíma, ef þess er krafist.

7. Ef áætlunarferlið á að fylgjast með takmörkunum afkastagetu varðandi tilföng sem eru þegar áætluð á aðrar vinnslur skal tryggja að skiptihnapparnir **Eign**, **Verkfæri** og **Starfskraftur** séu stilltir á **Já**. Ef þú vilt sjá ítarlegar upplýsingar um áætlunarferlið skaltu velja **Já** á skiptihnappnum **Oflengd**. Þetta þýðir að nákvæmar upplýsingar um reiknuð stig á verkbeiðninni eru sýndar í athugasemdakladda.

8. Veldu **Já** á skipthnappnum **Hunsa áætlun** til að hunsa lokaða daga í dagatalinu (á við um eignir, starfskrafta og verkfæri). Veldu **Já** á skiptihnappnum **Hunsa áætlaða framkvæmd** til að hunsa takmarkanir sem kunna að hafa verið valdar í verkbeiðni varðandi áætlun. 

    Upplýsingar um uppsetningu á áætlaðri framkvæmd er að finna í kaflanum [Áætluð framkvæmd](../setup-for-work-orders/scheduled-execution.md).

9. Smellt er á **OK**. Líftímastaða verkbeiðni er sjálfkrafa uppfærð í líftímastöðuna **Áætlað** sem er tilgreind í **Eignastýringu** > **Uppsetningu** > **Verkbeiðnum** > **Líftímalíkön**.

Myndin hér að neðan sýnir dæmi um sendingarval í glugganum **Áætla verkbeiðni**.

![Mynd 1.](media/04-work-order-scheduling.png)

[!NOTE]
Ef þú vilt eyða áætlun í vinnupöntun velurðu verkbeiðnina í **Allar verkbeiðnir** og smellir síðan á **Eyða áætlun** á flipanum **Almennt**. Mundu að uppfæra handvirkt líftímastöðu verkbeiðni ef þú eyðir áætluninni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]