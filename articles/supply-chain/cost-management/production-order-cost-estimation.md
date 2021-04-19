---
title: Kostnaðaráætlun framleiðslupöntunar
description: Þessi grein gefur upplýsingar um mat á framleiðslukostnaði. Mat á framleiðslukostnaði veitir upplýsingar um efnis- og afkastanotkunarkostnað við framleiðslu á vöru í áætluðu framleiðslupöntunarmagni.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59b93b41b74bd3f4cc480c8e60e8c69b25e40e51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830246"
---
# <a name="production-order-cost-estimation"></a>Kostnaðaráætlun framleiðslupöntunar

[!include [banner](../includes/banner.md)]

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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]