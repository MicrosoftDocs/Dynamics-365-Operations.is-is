---
title: Viðhaldsáætlun
description: Þessi grein útskýrir viðhaldsáætlun í eignastýringu.
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
ms.openlocfilehash: 782a8cc1f9e64b8c2d4364212c9c5755c103bbfb
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017059"
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

1. Smellur **Eignastýring** > **Viðhaldsáætlun** > **Öll viðhaldsáætlun** eða **Opnar viðhaldsáætlunarlínur** eða **Opnar viðhaldsáætlunarlaugar**.

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