---
title: Takmarkanir á kostnaðarútgáfum fyrir staðalkostnað
description: Þessi grein fjallar um þær takmarkanir sem gilda um kostnaðarútgáfu fyrir staðalkostnað.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5c00ae8952e2c80d97d039271a6f5c63e9a72f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867986"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Takmarkanir á kostnaðarútgáfum fyrir staðalkostnað

[!include [banner](../includes/banner.md)]

Þessi grein fjallar um þær takmarkanir sem gilda um kostnaðarútgáfu fyrir staðalkostnað. 

Eftirfarandi takmarkanir stuðla að því að reglum um staðalkostnað sé fylgt:

-  Gjöld verða að vera innifalinn í kostnaði vöru. Gjöld vegna framleiddrar vöru standa fyrir afskrifaðan fastan kostnað í uppskriftum (BOM) og leiðarlýsingar. Þess vegna verða gjöldin að vera innifalinn í einingarkostnaði. Gjöldin vegna keyptra vara eru einnig innifalin í einingarkostnaði vörunnar.

-  Útreikningur á staðalkostnaði framleiddrar vöru verður að byggja á kostnaðarfærslum í kostnaðarútgáfu fyrir staðalkostnað. Annan uppruna kostnaðargagna er aðeins hægt að nota með kostnaðarútgáfu fyrir áætlaðan kostnað, eins og viðskiptasamningi um innkaupaverð fyrir keyptar vörur. Annar uppruni kostnaðargagna er skilgreindur af flokki uppskriftarútreiknings.

-  Útreikningar uppskrifta verður að framkvæma með eins stigs niðurbroti.

Hægt er að afrita kostnaðargögn vöru fyrir staðlaðan kostnað í aðra kostnaðarútgáfu sem inniheldur staðlaðan kostnað eða áætlaðan kostnað. Hins vegar er ekki hægt að afrita kostnaðargögn vöru yfir í kostnaðarútgáfu sem inniheldur staðalkostnað, þar sem takmarkanirnar sem er lýst fyrr í þessari grein eiga ekki við áætlaðan kostnað.

## <a name="related-articles"></a>Tengdar greinar

[Yfirlit kostnaðarútgáfa](costing-versions.md)

[Uppfæra staðalkostnað í umhverfi sem er ekki fyrir framleiðslu](update-standard-costs-non-manufacturing-environment.md)

[Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]