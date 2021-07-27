---
title: Viðhaldsáætlun
description: Þetta efni skýrir viðhaldsskema í eignastýringu.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e2831d4a81f04b19eb894f533ac8768017aa8c98
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360995"
---
# <a name="maintenance-schedule"></a>Viðhaldsáætlun

[!include [banner](../../includes/banner.md)]

 

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

![Mynd 1.](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]