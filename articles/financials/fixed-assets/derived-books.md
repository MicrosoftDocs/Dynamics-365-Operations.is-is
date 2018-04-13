---
title: "Afleiddar bækur"
description: "Þessi grein veitir yfirlit yfir notagildi afleidds Bók."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e43dcc15212ae90a33d59fa32692aabcba7a19cb
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="derived-books"></a>Afleiddar bækur

[!INCLUDE [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir notagildi afleidds Bók.

Tilgangur afleiddra bóka er að einfalda bókun á færslum bóka fasta eigna sem eru áætlaðar með reglulegu millibili.  Eitt bók er valið sem aðalbók. Þetta er venjulega bókin sem er notað fyrir bókhaldslegar afskriftir. Síðan er það tengt við önnur bækur sem eru sett upp til að bóka færslur á sömu tímabilum og bóka. Bækur skattaafskrifta eru oft uppsett sem afleidd bækur. 

Algengustu færslurnar sem eru settar upp til að bóka á afleiddar bækur eru kaup, leiðréttingar kaupa og losanir. 

## <a name="example"></a>Dæmi

Bók B og bók C eru uppsett sem afleidd bækur fyrir bók A fyrir kaupfærslugerð. Fyrir Bók A er færð inn kaupfærsla fyrir eign 123 upp á 1.500,00. 

Þegar færslan er bókuð er kaupfærsla mynduð og bókuð í eign 123 í fyrir bók B og í eign 123 fyrir bók C upp á 1.500,00. Þegar færslur aðalbókar eru búnar til fyrir bókun í eignabók, er einnig hægt að skoða og breyta færslum fyrir afleidd bækur. Þegar færslur aðalbókar eru búnar til í annarri bók, er ekki hægt að skoða færslur fyrir afleidd virðislíkön. Hins vegar eru þær bókaðar á viðeigandi lykla og bókunarlög þegar færslur aðalbókar eru bókaðar.

> [!NOTE]                                                                                                                               
> Bækur sem eru uppsett til að bóka færslur með öðrum millibilum en aðalbókar verða að vera tengd eigninni sem aðskilin bækur en ekki sem afleidd bækur.  

Nánari upplýsingar eru í [Bókað í afleiddar bækur](post-derived-value-models.md).




