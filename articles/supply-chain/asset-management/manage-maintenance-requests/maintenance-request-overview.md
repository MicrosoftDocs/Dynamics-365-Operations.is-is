---
title: Viðhaldsbeiðnir
description: Þessi grein veitir yfirlit um stjórnun viðhaldsbeiðna í eignastýringu
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 488b6505aba246aa3a6ea69436514a274403bf49
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015639"
---
# <a name="maintenance-requests"></a>Viðhaldsbeiðnir

[!include [banner](../../includes/banner.md)]

Viðhaldsbeiðnir eru athugasemdir eða yfirlýsingar sem eru búnar til til að tilkynna stjórnanda eða skipuleggjanda um að eign gæti krafist viðhalds- eða viðgerðarstarfa, en án þess að búa til vinnupöntun. Ef innihald viðhaldsbeiðni er talið gilt, þá er hægt að búa til viðhaldsbeiðni út frá viðhaldsbeiðninni.

Hægt er að búa til viðhaldsbeiðnir fyrir hverja eign í eignastýringu. Hægt er að búa til ýmsar viðhaldsbeiðnir, allt eftir því hvernig fyrirtæki þitt notar viðhaldsbeiðnir. Hér eru nokkur dæmi:

- Viðhaldsbeiðnir
- Athugasemdir
- Leiðréttingar eða viðbætur
- Fjárfestingar
- Depot viðgerð (þessi tegund er notuð þegar þú færð eignir frá öðrum stað svo þú getir sinnt viðhalds- eða viðgerðarstarfi og þú skilar síðan eigninni eftir að verkinu er lokið.)

## <a name="view-maintenance-requests"></a>Skoða viðhaldsbeiðnir

Til að skoða viðhaldsbeiðnir velurðu **Eignastýring** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir**, **viðhaldsbeiðnir**, eða **Beiðnir mínar um viðhald á hagnýtri staðsetningu**. Hver listasíða sýnir nokkrar upplýsingar sem tengjast viðhaldsbeiðni.

![Skoða viðhaldsbeiðnir.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Notaðu listasíðuna **Beiðnir mínar um viðhald á staðsetningu minni** til að skoða lista yfir viðhaldsbeiðnir sem innihalda annaðhvort virka staði sem þú ert skyldur sem starfsmaður eða eignir sem eru settar upp á starfrænum stöðum sem þú ert skyldur sem starfsmaður. (Sjá upplýsingar um hvernig á að setja upp starfshætti á viðhaldsstarfsmönnum [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) .)
> 
> Þrátt fyrir að upplýsingar um viðskiptareikninga séu tiltækar í þjónustustjórnun eigna (utanaðkomandi viðhald) eru þær ekki tiltækar í eignastýringu (innra viðhald).

Til að opna smáatriðið yfir plötuna á listasíðunni **Allar viðhaldsbeiðnir** velurðu tengil í hnitalínuyfirlitinu í dálkinum **Viðhaldsbeiðni**.

![Skoða upplýsingar um viðhaldsbeiðni.](media/02-manage-maintenance-requests.png)

Hnapparnir á aðgerðarglugganum eru skipulagðir á flipa. Eftirfarandi tafla lýsir stuttlega hnöppunum sem tengjast eignastýringu.

| Heiti hnapps                      | Lýsing |
|----------------------------------|-------------|
| Breyta                             | Breyta valinni viðhaldsbeiðni. |
| Nýjar                              | Stofna nýja viðhaldsbeiðni. |
| Eyða                           | Eyða valinni viðhaldsbeiðni. |
| Verkbeiðnihópur                  | Tengdu valda viðhaldsbeiðni við verkbeiðnasafn. |
| Verkbeiðni                       | Stofnaðu verkbeiðni byggða á valinni viðhaldsbeiðni. |
| Bilun eignar                      | Smelltu á **Eignabilanir**, þar sem þú getur búið til bilanaskráningu á valinni viðhaldsbeiðni. |
| Verkbeiðnir                      | Sýna lista yfir allar viðhaldsbeiðnir sem tengjast völdum viðhaldsbeiðnum. |
| Uppfæra stöðu viðhaldsbeiðni | Uppfæra stöðu viðhaldsbeiðni. |
| Kladdi líftímastöðu              | Skoða kladdaskrá sem sýnir líftímastöður valinnar viðhaldsbeiðni. |
| Upplýsingar yfir viðhaldsbeiðnir      | Prentaðu skýrslu sem sýnir upplýsingar um valda viðhaldsbeiðni. |
| Senda lánseign                  | Veldu lánaeign sem ætti að koma tímabundið í staðinn fyrir þá eign sem er valin á valinni viðhaldsbeiðni. |
| Skila lánseign                | Skráðu lánaeignina sem að henni hafi verið skilað. |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]