---
title: Viðhaldsbeiðnir
description: Þetta efni veitir yfirlit um stjórnun viðhaldsbeiðna í eignastjórnun
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e0071ae745987a1217525b2841e3320933a9242
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019630"
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

Veldu til að skoða viðhaldsbeiðnir **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir**, **Virkar viðhaldsbeiðnir**, eða **Beiðnir mínar um viðhald á staðsetningu minni**. Hver listasíða sýnir nokkrar upplýsingar sem tengjast viðhaldsbeiðni.

![Skoða viðhaldsbeiðnir](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Notaðu listasíðuna **Beiðnir mínar um viðhald á staðsetningu minni** til að skoða lista yfir viðhaldsbeiðnir sem innihalda annaðhvort virka staði sem þú ert skyldur sem starfsmaður eða eignir sem eru settar upp á starfrænum stöðum sem þú ert skyldur sem starfsmaður. (Sjá upplýsingar um hvernig á að setja upp starfshætti á viðhaldsstarfsmönnum [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) .)
> 
> Þrátt fyrir að upplýsingar um viðskiptareikninga séu tiltækar í þjónustustjórnun eigna (utanaðkomandi viðhald) eru þær ekki tiltækar í eignastýringu (innra viðhald).

Til að opna smáatriðið yfir plötuna á listasíðunni **Allar viðhaldsbeiðnir** velurðu tengil í hnitalínuyfirlitinu í dálkinum **Viðhaldsbeiðni**.

![Skoða upplýsingar um viðhaldsbeiðni](media/02-manage-maintenance-requests.png)

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