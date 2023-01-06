---
title: Vinnusvæði eignastýringar
description: Í þessari grein er að finna upplýsingar um vinnusvæði eignastýringar. Þetta vinnusvæði sýnir upplýsingar sem tengjast eignum sem eru færðar inn í kerfið. Það felur í sér samantektaryfirlit og greiningaryfirlit.
author: moaamer
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetWorkspace
audience: Application User
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 95b45a91cd201a6d3a4817c315053e98a7693e05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894056"
---
# <a name="fixed-asset-management-workspace"></a>Vinnusvæði eignastýringar

[!include [banner](../includes/banner.md)]

Vinnusvæðið **Eignastýring** sýnir upplýsingar sem tengjast eignum sem eru færðar inn í kerfið. Þetta vinnusvæði inniheldur samantektaryfirlit og greiningayfirlit. Flipinn **Mín vinna** sýnir samantektarreiti fastra eigna upplýsingar og magntengdar upplýsingar um eignir í gildandi fyrirtæki. Þú getur einnig bætt greiningum við Power BI-greiningarhlutann beint á vinnusvæðið. Flipinn **Greiningar - öll fyrirtæki** notar getu Microsoft Power BI til að sýna myndefni sem tengist eignum í öllum fyrirtækjum.

## <a name="my-work"></a>Vinnan mín

### <a name="summary"></a>Samantekt

Reitir í hlutanum **Samantekt** veita yfirlit yfir eignir. Upplýsingarnar fela í sér mælikvarða um eignir sem ekki eru enn keyptar, eignir sem hafa verið keypt á gildandi ári og eignir sem hefur verið losað á gildandi ári. Hlutinn **Samantekt** hefur einnig flýtiræsistikunni á listasíðuna **Eign**, afskriftatillögu runu og eignabókina.

### <a name="find-fixed-assets"></a>Finna eignir

Hlutinn **Finna eignir** gerir kleift að leita að eignum með því að gefa upp númer eignar, flokk, heiti, staðsetningu eða manneskja sem ber ábyrgð á. Allar eignir sem uppfylla leitarskilyrði munu birtast á listanum.

Á listanum er hægt að skoða eftirfarandi síður:

 - Síðuna **Upplýsingar** fyrir eignina
 - Síðuna **Bóka** fyrir allar skýrslur sem eru tengdir við hverja eign
 - Síðuna **Eignamat**

### <a name="valuations"></a>Mat

Síðan **Eignamat** síðan gerir mögulegt að sjá á einni síðu mikilvægustu upplýsingarnar um eignir og einnig upplýsingar um allar bækur sem tengjast eign. Valkosturinn **Stöður** efst í hægra horni síðunnar sýnir gildandi mat fyrir hverja bók sem tengist eign. Hægt er að kafa aftur úr gildi til að skoða nánar þær færslur sem mynda samantektargildi. Valkosturinn **Fortilling** efst í hægra horni síðunnar sýnir gildandi mat fyrir hverja bók sem tengist eign.

Hægt er að fara á síðuna **Eignamat** af vinnusvæðinu **Eignastjórnun** eða listasíðunni **Eignir**.

### <a name="related-information"></a>Tengdar upplýsingar

Hægt er að fara beint á síðuna **Uppsetning afskriftabóka**, síðuna **Fyrirspurn um eignafærslur** og margar skýrslur með því að nota tenglana í hlutanum **Tengdar upplýsingar** á vinnusvæðinu.

### <a name="analytics--all-companies"></a>Greiningar – öll fyrirtæki

Síðan **Greiningar** veitir mikilvæga mælikvarða um eignir í öllum lögaðilum í kerfinu. Aðgangi að þessum flipa er stjórnað með Skoða greiningar á eignum fyrir öll fyrirtækin öryggi heimildinni Yfirlitið.

Eftirfarandi tafla sýnir sýnigögn sem eru tiltæk á hverri skýrslusíðu.

| Skýrslusíða            | Myndbirting        |
|------------------------|----------------------|
| Eignamat | Samtals bókað nettóvirði |
| Eignamat | Bókað nettóvirði eftir eignaflokki |
| Eignamat | Kaupvirði |
| Eignamat | Afskráningargildi |
| Eignamat | Upplýsingar eignar |
| Matsvarpanir        | Samtals bókað nettóvirði |
| Matsvarpanir        | Staðsetningar eigna |
| Matsvarpanir        | Upplýsingar eignar |

Til að skoða greiningu með gögnum þarf fyrst að endurnýja uppsafnaða mælingu AssetTransactionMeasure á síðunni **Einingarverslun**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
