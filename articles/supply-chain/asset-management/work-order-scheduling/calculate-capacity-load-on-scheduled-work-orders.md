---
title: Reikna álag á áætlaðar verkbeiðnir
description: Þetta efni útskýrir hvernig á að reikna út álag á áætlaðar verkbeiðnir í eignastjórnun.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 164ae10eef8ef3692cd3a8b5232de64ec3d83b1b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354181"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Reikna álag á áætlaðar verkbeiðnir

[!include [banner](../../includes/banner.md)]

 

Hægt er að reikna út álag á áætlaðar verkbeiðnir til að fá yfirsýn yfir vinnuálag á tilföng fyrir tiltekið tímabil. Hægt er að reikna út fyrir eftirfarandi úrræði: Viðhaldsstarfsmenn, starfsmannahópa, verkfæri og eignir.

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Áætlun** > **Álag**.

2. Í valmyndinni **Reikna álag** > reitnum **Sýna** velurðu hvaða álagsgerð þú vilt reikna út: **Afkastageta**, **Frátekið** eða **Eftirstöðvar**.

3. Veldu **Já** á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með núlli.

4. Veldu tilfangagerðirnar sem þú vilt reikna út álag fyrir með því að velja **Já** á viðeigandi skiptihnöppum: **Starfskraftur**, **Hópur viðhaldsstarfsmanna**, **Verkfæri** og **Eignir**.

5. Veldu upphafsdagsetningu fyrir útreikning í reitnum **Frá dagsetningu**.

6. Í reitnum **Gerð millibils** velurðu bilið fyrir útreikninginn: **Dagur**, **Vika**, **Mánuður** eða **Ársfjórðungur**.

7. Í reitnum **Tímabilstíðni** seturðu inn þann fjölda millibila sem þú vilt reikna. Til dæmis, ef þú hefur valið **Dag** sem millibilsgerð og þú setur töluna „5“ inn í þennan reit, verða reiknaðir út fimm dagar frá upphafsdegi.

8. Smellið á **Í lagi** til að byrja að reikna.

Myndin hér að neðan sýnir niðurstöðu útreiknings sem spannaði þrjár vikur fyrir álagsgerðina **Frátekið**.

![Mynd 1.](media/08-work-order-scheduling.png)

[!NOTE]
Ef þú velur álagsgerðina **Afkastageta** eða **Eftirstöðvar** fyrir útreikninginn mun sama niðurstaða birtast ef engir fyrirvarar hafa verið gerðir á tilföngunum á völdu tímabili.

Upplýsingar um hvernig skuli reikna út álag afkastagetu á línum viðhaldsskema og óáætluðum verkbeiðnum eru að finna í [Reikna álag](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]