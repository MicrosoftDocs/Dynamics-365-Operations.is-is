---
title: "Kostnaðaráætlun framleiðslupöntunar"
description: "Þessi grein gefur upplýsingar um mat á framleiðslukostnaði. Mat á framleiðslukostnaði veitir upplýsingar um efnis- og afkastanotkunarkostnað við framleiðslu á vöru í áætluðu framleiðslupöntunarmagni."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9ae0bbb641d7517d33ad087faec231cb0bda3f78
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="production-order-cost-estimation"></a>Kostnaðaráætlun framleiðslupöntunar

[!include[banner](../includes/banner.md)]


Þessi grein gefur upplýsingar um mat á framleiðslukostnaði. Mat á framleiðslukostnaði veitir upplýsingar um efnis- og afkastanotkunarkostnað við framleiðslu á vöru í áætluðu framleiðslupöntunarmagni. 

Eftir að þú stofnar framleiðslupöntun verður þú að meta framleiðslukostnað. Tilgangurinn er mat á vöru- og leiðanotkun fyrir framleiðsluferlið, því matið er notað sem grunnurinn að næstu röðunar- og framleiðsluferlum.

## <a name="production-cost-estimation"></a>Framleiðslukostnaðarmat
Mat á framleiðslukostnaði er byggt á eftirfarandi upplýsingum:

-   Magni í framleiðslupöntun.
-   Íhlutir í uppskriftum (BOMs) framleiðslu.
-   Leiðaraðgerð í framleiðsluleið.
-   Óbeinn kostnaður sem eiga við íhluti og aðgerðir
-   Virk kostnaðargögn frá og með útreikningsdegi.

Ef til staðar er skuggalínuvara í framleiðsluuppskriftinni endurspegla útreikningarnir þætti skuggavörunnar og leiðaaðgerða. Hægt er að nota matsverkefnið til að endurreikna áætlaðan kostnað til að endurspegla uppfærðar upplýsingar. Til dæmis gætu uppfærðu upplýsingarnar verið breytingar á magni framleiðslupöntunarinnar, íhlutunum í framleiðsluuppskriftunum, leiðaraðgerðunum í framleiðsluleiðinni, óbeina kostnaðinum sem á við um þessa þætti og aðgerðir eða virk kostnaðargögn frá og með dagsetningu endurreikningsins. Útreikningarnir á áætluðum kostnaði gefa líka til kynna söluverð fyrir framleiðsluvöruna á grundvelli nálgunarinnar kostnaður-plús-álag. Útreikningar á áætluðum kostnaði geta einnig gilt um tilvísunarpantanir sem endurspegla aðrar framleiðslupantanir sem eru tengdar við framleiðslupöntunina.

## <a name="view-the-estimated-costs"></a>Skoða áætlaður kostnaður.
Þegar mat hefur verið keyrt er hægt að skoða niðurstöður á **Verðútreikning** síðu. Matið reiknar eftirfarandi gildi:

-   **Framleiðslukostnaður** – Framleiðslukostnaður er efsta lína matsins. Hún sýnir heildarkostnað við keyrslu framleiðslupöntunar og heildar söluverð framleiðslunnar. Hún er samtala allra kostnaðarlína í matinu.
-   **Leið eða kostnaður tilfanga** – Leið eða tilfangakostnaður er kostnaður fyrir framleiðsluaðgerðir. Þau taka með kostnað fyrir einingar eins og uppsetningartíma, keyrslutíma og umstang.
-   **Efniskostnaður** – Efniskostnaður er kostnaður og verð uppskriftaíhluta sem eru nauðsynlegir til þess að framleiða vöruna. Þessi kostnaður hefur áður verið fastsettur og færa inn í kerfið.

## <a name="other-uses-of-cost-estimation"></a>Önnur not kostnaðarmats
Kostnaðarmat felur líka í sér eftirfarandi upplýsingar:

-   Auðskilin verðtilboð
-   Mat á arðsemi pöntunarinnar
-   Mat á hráefnisnotkun
-   Samanburð á kostnaðarupplýsingum úr fyrri framleiðslum
-   Áætlunar- og spáupplýsingar
-   Mat á nauðsynlegri framleiðslustærð til þess að geta viðhaldið tilteknum kostnaði.




