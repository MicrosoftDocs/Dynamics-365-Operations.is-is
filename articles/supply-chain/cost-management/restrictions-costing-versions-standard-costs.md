---
title: Takmarkanir á kostnaðarútgáfum fyrir staðalkostnað
description: Þetta efnisatriði fjallar um þær takmarkanir sem gilda um kostnaðarútgáfu fyrir staðalkostnað.
author: AndersGirke
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
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9d828e2413a20c4e61d162a31d3c2ed2b18718b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187675"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Takmarkanir á kostnaðarútgáfum fyrir staðalkostnað

[!include [banner](../includes/banner.md)]

Þetta efnisatriði fjallar um þær takmarkanir sem gilda um kostnaðarútgáfu fyrir staðalkostnað. 

Eftirfarandi takmarkanir stuðla að því að reglum um staðalkostnað sé fylgt:

-  Gjöld verða að vera innifalinn í kostnaði vöru. Gjöld vegna framleiddrar vöru standa fyrir afskrifaðan fastan kostnað í uppskriftum (BOM) og leiðarlýsingar. Þess vegna verða gjöldin að vera innifalinn í einingarkostnaði. Gjöldin vegna keyptra vara eru einnig innifalin í einingarkostnaði vörunnar.

-  Útreikningur á staðalkostnaði framleiddrar vöru verður að byggja á kostnaðarfærslum í kostnaðarútgáfu fyrir staðalkostnað. Annan uppruna kostnaðargagna er aðeins hægt að nota með kostnaðarútgáfu fyrir áætlaðan kostnað, eins og viðskiptasamningi um innkaupaverð fyrir keyptar vörur. Annar uppruni kostnaðargagna er skilgreindur af flokki uppskriftarútreiknings.

-  Útreikningar uppskrifta verður að framkvæma með eins stigs niðurbroti.

Hægt er að afrita kostnaðargögn vöru fyrir staðlaðan kostnað í aðra kostnaðarútgáfu sem inniheldur staðlaðan kostnað eða áætlaðan kostnað. Hins vegar er ekki hægt að afrita kostnaðargögn vöru yfir í kostnaðarútgáfu sem inniheldur staðalkostnað, þar sem takmarkanirnar sem er lýst fyrr í þessu efnisatriði eiga ekki við áætlaðan kostnað.

## <a name="related-topics"></a>Tengd efnisatriði

[Yfirlit kostnaðarútgáfa](costing-versions.md)

[Uppfæra staðalkostnað í umhverfi sem er ekki fyrir framleiðslu](update-standard-costs-non-manufacturing-environment.md)

[Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]