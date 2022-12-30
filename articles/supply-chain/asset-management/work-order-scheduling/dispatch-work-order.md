---
title: Senda verkbeiðni
description: Þessi grein útskýrir hvernig á að senda verkbeiðni í Eignastýringu.
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
ms.openlocfilehash: f78e8642715b0c3fd3d01e8072645ccd9c58d685
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016856"
---
# <a name="dispatch-work-order"></a>Senda verkbeiðni

[!include [banner](../../includes/banner.md)]

 

Þú getur tímasett eina verkbeiðni eða verkbeiðnivinnslur fyrir einn starfskraft með því að nota aðgerðina **Senda**.

1. Smellið á **Eignastýring** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

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