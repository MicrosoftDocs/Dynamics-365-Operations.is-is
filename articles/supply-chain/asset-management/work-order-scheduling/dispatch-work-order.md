---
title: Senda verkbeiðni
description: Þetta efni útskýrir hvernig á að senda verkbeiðni í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887206"
---
# <a name="dispatch-work-order"></a>Senda verkbeiðni

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þú getur tímasett eina verkbeiðni eða verkbeiðnivinnslur fyrir einn starfskraft með því að nota aðgerðina **Senda**.

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.

2. Verkbeiðnin er valin af listanum.

3. Á flipanum **Almennt** er smellt á **Senda**.

4. Í glugganum **Áætla verkbeiðni** velurðu starfskraftinn í reitnum **Starfskraftur**.

5. Í reitinn **Áætlunartíma** er hægt að setja inn áætlaða vinnutíma ef áætlaður vinnutími er frábrugðinn spátímanum.

6. Í reitnum **Áætlað upphaf** er hægt að breyta upphafsdegi og -tíma, ef þess er krafist.

7. Ef áætlunarferlið á að fylgjast með takmörkunum afkastagetu varðandi tilföng sem eru þegar áætluð á aðrar vinnslur skal tryggja að skiptihnapparnir **Eign**, **Verkfæri** og **Starfskraftur** séu stilltir á „Já“. Ef þú vilt sjá ítarlegar upplýsingar um áætlunarferlið skaltu velja „Já“ á skiptihnappnum **Oflengd**. Þetta þýðir að nákvæmar upplýsingar um reiknuð stig á verkbeiðninni eru sýndar í athugasemdakladda.

8. Veldu „Já“ á skipthnappnum **Hunsa áætlun** til að hunsa lokaða daga í dagatalinu (á við um eignir, starfskrafta og verkfæri). Veldu „Já“ á skiptihnappnum **Hunsa áætlaða framkvæmd** til að hunsa takmarkanir sem kunna að hafa verið valdar í verkbeiðni varðandi áætlun. Sjá kaflann [Áætluð framkvæmd](../setup-for-work-orders/scheduled-execution.md) til að fá upplýsingar um uppsetningu áætlaðrar framkvæmdar.

9. Smellt er á **OK**. Líftímastaða verkbeiðni er sjálfkrafa uppfærð í líftímastöðuna „Áætlað“ sem er tilgreind í **Eignastýringu** > **Uppsetningu** > **Verkbeiðnum** > **Líftímalíkön**.

Myndin hér að neðan sýnir dæmi um sendingarval í glugganum **Áætla verkbeiðni**.

![Mynd 1](media/04-work-order-scheduling.png)

>[!NOTE]
>Ef þú vilt eyða áætlun í vinnupöntun er það gert með því að velja verkbeiðnina í **Allar verkbeiðnir** og smella á **Eyða áætlun** á flipanum **Almennt**. Mundu að uppfæra handvirkt líftímastöðu verkbeiðni ef þú eyðir áætluninni.

