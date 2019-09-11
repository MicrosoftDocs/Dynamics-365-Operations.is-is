---
title: Reikna álag á áætlaðar verkbeiðnir
description: Þetta efni útskýrir hvernig á að reikna út álag á áætlaðar verkbeiðnir í eignastjórnun.
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
ms.openlocfilehash: 0c0dd1e306c54d3f99b86ad6f1816d5acabe6c18
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887160"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Reikna álag á áætlaðar verkbeiðnir

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Hægt er að reikna út álag á áætlaðar verkbeiðnir til að fá yfirsýn yfir vinnuálag á tilföng fyrir tiltekið tímabil. Hægt er að reikna út fyrir eftirfarandi úrræði: Viðhaldsstarfsmenn, starfsmannahópa, verkfæri og eignir.

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Áætlun** > **Álag**.

2. Í valmyndinni **Reikna álag** > reitnum **Sýna** velurðu hvaða álagsgerð þú vilt reikna út: "Afkastageta", "Frátekið" eða "Eftirstöðvar".

3. Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með núlli.

4. Veldu tilfangagerðirnar sem þú vilt reikna út álag fyrir með því að velja "Já" á viðeigandi skiptihnöppum: **Starfskraftur**, **Hópur viðhaldsstarfsmanna**, **Verkfæri** og **Eignir**.

5. Veldu upphafsdagsetningu fyrir útreikning í reitnum **Frá dagsetningu**.

6. Í reitnum **Gerð millibils** velurðu bilið fyrir útreikninginn: „Dagur“, „Vika“, „Mánuður“ eða „Ársfjórðungur“.

7. Í reitnum **Tímabilstíðni** seturðu inn þann fjölda millibila sem þú vilt reikna. Til dæmis, ef þú hefur valið „Dag“ sem millibilsgerð og þú setur töluna „5“ inn í þennan reit, verða reiknaðir út fimm dagar frá upphafsdegi.

8. Smellið á **Í lagi** til að byrja að reikna.

Myndin hér að neðan sýnir niðurstöðu útreiknings sem spannaði þrjár vikur fyrir álagsgerðina „Frátekið“.

![Mynd 1](media/08-work-order-scheduling.png)

>[!NOTE]
>Ef þú velur álagsgerðina „Afkastagega“ eða „Eftirstöðvar“ fyrir útreikninginn mun sama niðurstaða birtast ef engir fyrirvarar hafa verið gerðir á tilföngunum á völdu tímabili.

Sjá [Reikna álag](../capacity-planning/calculate-capacity-load.md) til að fá upplýsingar um hvernig á að reikna út álag á viðhaldsskemalínum og ekki á áætluðum verkbeiðnum.

