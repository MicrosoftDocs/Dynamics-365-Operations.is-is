---
title: Viðhaldsáætlun
description: Þetta efni skýrir viðhaldsskema í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 780b633af04c38705f8321d19924f3802b2d5c67
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875714"
---
# <a name="maintenance-schedule"></a>Viðhaldsáætlun

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Viðhaldsskemað inniheldur lista yfir allar áætlaðar fyrirbyggjandi viðhaldsáætlanir, viðhaldsbeiðnir og viðhaldslotur sem gera skal. Sumum dagskrárlínum kann að hafa verið breytt í viðhaldsbeiðnir.

Fjögur sýn á viðhaldsskema er aðeins mismunandi eftir því hvaða viðhaldsskemalínur þú vilt sjá.

| Valmyndaratriði                  | Efnisyfirlit                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ítarleg viðhaldsáætlun       | Allar viðhaldsskemalínur eru sýndar.     |
| Eignaáætlunin mín        | Allar viðhaldsskemalínur sem innihalda eignir settar upp á virkum stöðum sem þú tengist sem starfsmaður (sett upp í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md)) eru sýndar á þessum lista. |
| Opna áætlunarlínur viðhalds | Línur um viðhaldsskema með stöðunni „Stofnað“ - sem þýðir að þeim hefur enn ekki verið breytt í verkbeiðni eða þeim hent - eru sýndar á þessum lista.                                            |
| Opna viðhaldsáætlunarhópa | Línur fyrir viðhaldsskema sem tengjast verkpöntunarsafni eru sýndar á þessum lista.                                                                                                                  |

>[!NOTE]
>Ef viðhaldsskemalína er innifalin í nokkrum verkbeiðnisöfnum (sjá [Verkbeiðnisöfn](../work-orders/work-order-pools.md)) er sýnd ein skrá fyrir hvert safn í **Opna viðhaldsskemasöfn**. Þetta er gert til að hámarka síunarvalkosti í verkbeiðnisöfnum.

Til að opna viðhaldsskema:

1. Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Viðhaldsskema** > **Öll viðhaldsskemu** eða **Opna viðhaldsskemalínur** eða **Opna söfn viðhaldsáætlana**.

2. Til að uppfæra viðhaldsskema skaltu smella á **Viðhaldsáætlun** eða **Viðhaldslotur**. 

3. Þú getur breytt viðhaldsskemalínu með því að velja hana og smella á **Breyta**. Til dæmis geturðu auðveldlega uppfært þjónustustigið eða starfsmanninn sem ber ábyrgð á vinnslunni. Þú getur aðeins breytt viðhaldsskemalínum sem hafa ekki enn verið tengdir verkbeiðni.

4. Þú getur eytt viðhaldsskemalínu með því að velja hana á listasíðunni og smella á **Eyða**.

5. Þú getur fleygt viðhaldsskemalínu með því að velja hana á listasíðunni og smella á **Eyða**. Þessi aðgerð er gagnleg ef til dæmis eign er með 2.000 km viðhaldsáætlun og 10.000 km viðhaldsáætlun. Þá gætirðu viljað henda línunni sem búin var til úr viðhaldsáætluninni um 2.000 km þegar hún fellur saman við 10.000 km, 20.000 km, 30.000 km og svo framvegis. Ef þú fargar viðhaldsskemalínu sem tengist viðhaldsáætlun birtist sú lína aldrei aftur þegar sú viðhaldsáætlun er áætluð.

6. Þú getur valið fjölda viðhaldsskemalína í **Öll viðhaldsskemu** og smellt á **Verkbeiðnisafn**, ef þú vilt að allar valdar línur séu með í sama verkbeiðnisafni.

7. Þú getur valið fjölda viðhaldsskemalína í **Öll viðhaldsskemu** eða **Opna viðhaldsskemalínur** eða **Opna viðhaldskemasöfn** og smellt á **Stilla áætlun** ef þú vilt gera sömu leiðréttingar á nokkrum línum. Þú getur breytt áætluðum upphafs- og lokadögum, þjónustustigi og ábyrgum starfsmannahópi eða ábyrgum viðhaldsstarfsmanni tengdum völdum viðhaldsskemalínum.

- Þegar lína fyrir viðhaldsskema hefur verið tengd verkbeiðni verður auðkenni verkbeiðni birt í reitnum **Verkbeiðni**.  
- Í upplýsingaglugganum **Allar eignir** > flýtiflipanum **Viðhaldsáætlanir eigna** er hægt að velja viðhaldsáætlanir fyrir eignina. Seinna, ef þú eyðir viðhaldsáætlunarlínu eða viðhaldslotu sem tengist eign í **Allar eignir**, eyðirðu einnig sjálfkrafa öllum viðhaldsskemalínum með stöðunni „Stofnað“ sem hafa verið stofnaðar út frá þeirri viðhaldsáætlun eða viðhaldsumferð. Sjá einnig [Stofna eign](../objects/create-an-object.md).

Myndin hér að neðan sýnir listasíðuna **Öll viðhaldsskemu**.

![Mynd 1](media/16-preventive-maintenance.png)

