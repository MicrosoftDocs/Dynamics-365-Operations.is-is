---
title: Áætluð keyrsla
description: Þetta efni útskýrir tímasetta framkvæmd í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d9c8afc139c96e32efb3161d35fde685b8abcc5
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874671"
---
# <a name="scheduled-execution"></a>Áætluð keyrsla

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þú getur notað þjónustustig fyrir verkbeiðni til að setja upp áætlaða framkvæmd. (Sjá nánari upplýsingar um þjónustustig í verkbeiðni [Þjónustustig og lýsing](service-level-and-description.md) .) Fyrirhuguð framkvæmd veitir sveigjanleika í verkáætlun fyrir viðhaldsstarfsmenn, vegna þess að þú getur sett upp ítarlegri eða minna nákvæmar kröfur um það bil sem ljúka skal verkbeiðni á. Sem dæmi má nefna að viðhaldsstarfsmaður sem lýkur verki hraðar en gert var ráð fyrir í framleiðslustöð gæti farið í annað starf í nágrenninu sem áætlað var fyrir núverandi viku en ekki endilega fyrir núverandi dag. Þessi aðferð gerir kleift að hámarka skipulagningu starfsmanna og verklok.

Tímasett framkvæmdaruppsetning, sem tengist verkbeiðnum, getur verið almenn eða sértæk. Þú getur sett upp almennar línur sem eru ekki takmarkaðar við sérstakar gerðir verkbeiðni, eignagerðir og svo framvegis. Að öðrum kosti er hægt að búa til áætlaðar framkvæmdalínur sem eiga við um tiltekna gerð verkbeiðni, eignagerð, gerð viðhaldsverks og svo framvegis.

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Áætluð framkvæmd**.
2. Veldu **Nýtt** til að stofna áætlaða framkvæmdalínu.
3. Í reitunum **Virk staðsetning**, **Gerð verkbeiðni**, **Gerð eigna**, **Framleiðandi**, **Tegund**, **Tegundaflokkur viðhaldsverka**, **Gerð viðhaldsverks**, **Tegundaafbrigði af viðhaldsverka** og **Viðskipti** velurðu gildi eftir þörfum.
4. Í reitnum **Þjónustustig** velurðu þjónustustig verkbeiðni. Ef þú skilur þennan reit eftir auðan, þá gerirðu almenna gerð áætlaðrar framkvæmdalínu. Fyrir dæmi um almenna línu, sjá fyrstu skrána á myndinni sem hér fylgir. Sú lína virkjar allar verkbeiðnir sem hafa ekkert þjónustustig verkbeiðni sem á að tímasetja fyrir tiltekinn dag og tíma.
5. Í reitnum **Áætluð framkvæmd** velurðu tímamillibilið.
6. Veljið **Vista**.

![Mynd 1](media/20-setup-for-work-orders.png)
