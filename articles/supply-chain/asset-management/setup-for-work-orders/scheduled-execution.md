---
title: Áætluð keyrsla
description: Þetta efni útskýrir tímasetta framkvæmd í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215517"
---
# <a name="scheduled-execution"></a>Áætluð keyrsla

[!include [banner](../../includes/banner.md)]

 

Þú getur notað þjónustustig fyrir verkbeiðni til að setja upp áætlaða framkvæmd. (Sjá nánari upplýsingar um þjónustustig í verkbeiðni [Þjónustustig og lýsing](service-level-and-description.md) .) Fyrirhuguð framkvæmd veitir sveigjanleika í verkáætlun fyrir viðhaldsstarfsmenn, vegna þess að þú getur sett upp ítarlegri eða minna nákvæmar kröfur um það bil sem ljúka skal verkbeiðni á. Sem dæmi má nefna að viðhaldsstarfsmaður sem lýkur verki hraðar en gert var ráð fyrir í framleiðslustöð gæti farið í annað starf í nágrenninu sem áætlað var fyrir núverandi viku en ekki endilega fyrir núverandi dag. Þessi aðferð gerir kleift að hámarka skipulagningu starfsmanna og verklok.

Tímasett framkvæmdaruppsetning, sem tengist verkbeiðnum, getur verið almenn eða sértæk. Þú getur sett upp almennar línur sem eru ekki takmarkaðar við sérstakar gerðir verkbeiðni, eignagerðir og svo framvegis. Að öðrum kosti er hægt að búa til áætlaðar framkvæmdalínur sem eiga við um tiltekna gerð verkbeiðni, eignagerð, gerð viðhaldsverks og svo framvegis.

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Áætluð framkvæmd**.
2. Veldu **Nýtt** til að stofna áætlaða framkvæmdalínu.
3. Í reitunum **Virk staðsetning**, **Gerð verkbeiðni**, **Gerð eigna**, **Framleiðandi**, **Tegund**, **Tegundaflokkur viðhaldsverka**, **Gerð viðhaldsverks**, **Tegundaafbrigði af viðhaldsverka** og **Viðskipti** velurðu gildi eftir þörfum.
4. Í reitnum **Þjónustustig** velurðu þjónustustig verkbeiðni. Ef þú skilur þennan reit eftir auðan, þá gerirðu almenna gerð áætlaðrar framkvæmdalínu. Fyrir dæmi um almenna línu, sjá fyrstu skrána á myndinni sem hér fylgir. Sú lína virkjar allar verkbeiðnir sem hafa ekkert þjónustustig verkbeiðni sem á að tímasetja fyrir tiltekinn dag og tíma.
5. Í reitnum **Áætluð framkvæmd** velurðu tímamillibilið.
6. Veljið **Vista**.

![Áætluð keyrsla](media/20-setup-for-work-orders.png)
