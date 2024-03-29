---
title: Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur
description: Þessi grein lýsir skrefunum til að undirbúa viðhald kostnaðar fyrir framleiddar vörur.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 423da8022faf8066c5aa524c49c5071d0871de04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886016"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur

[!include [banner](../includes/banner.md)]

Þessi grein lýsir skrefunum til að undirbúa viðhald kostnaðar fyrir framleiddar vörur. Skrefin fyrir framleiddar vörur eru örlítið frábrugðin skrefunum fyrir keyptar vörur.

Reglur sem eru úthlutaðar framleiddum vörum geta haft áhrif á kostnaðarútreikninga fyrir framleiddu móðurvörurnar. Til að undirbúa viðhald kostnaðar fyrir framleiddar vörur skaltu fylgja þessum skrefum.

1. Úthlutaðu framleiddu vörunni vörulíkanaflokki. 

   Vörulíkanaflokkurinn staðfestir að staðlaðar kostnaður verði notaður.

2. Úthlutið framleiddu vörunni vöruflokk. 

   Vöruflokkurinn inniheldur fjárhagslykla sem eiga við um framleiddu vöruna. Fjárhagslyklarnir fyrir framleidda vöru sem hafa birgðalíkan staðalkostnaðar innihalda nokkur framleiðslufrávik, frávik kostnaðarbreytingar og endurmat birgðakostnaðarins.

3. Úthluta vörunni birgðamælieiningu. 

   Kostnaður vörunnar er alltaf gefinn upp í birgðamælieiningu vörunnar.

4. Ekki úthluta framleiddu vörunni kostnaðarflokki nema farið verði með vöruna sem keypta vöru.

5. Úthlutaðu framleiddu vörunni útreikningsflokki uppskriftar (BOM). 

   Flokkur uppskriftarútreiknings vörunnar skilgreinir viðvörunarskilyrði sem eiga við. Þannig er hægt að búa til viðvörunarboð um mögulegar ástæður útreikningsskekkja þegar útreikningur uppskrifta er gerður. Til dæmis getur viðvörunarboð borið kennsl á virka uppskrift eða leið sem er ekki til. Flokkur uppskriftarútreikninga inniheldur reglu um stöðvun niðurbrots sem gefur til kynna hvenær framleidd vara skuli meðhöndluð sem keypt vara.

6. Úthlutaðu stöðluðu pöntunarmagni ef framleiddur hlutur hefur fastan kostnað. 

   Staðlaða pöntunarmagnið er lotustærð bókhalds fyrir afskriftir á föstum kostnaði. Dæmi um fastan kostnað eru uppsetningartími í leiðaraðgerðum og fast magn íhlutar í uppskrift (BOM).

7. Skilgreinið uppskriftina fyrir framleiddu vöruna. 

   Hægt er að skilgreina eina eða fleiri uppskriftarútgáfur fyrir framleiddu vöruna. Staðfestu að útgáfurnar sem þú hefur áhuga á hafi verið merktar sem samþykktar og virkar og að þær hafi þær virku dagsetningar sem óskað er eftir. Hægt er að láta uppskriftarútgáfuna eiga við um allt fyrirtækið eða eitt vefsetur.

8. Skilgreinið leiðina fyrir framleiddu vöruna. 

   Hægt er að skilgreina eina eða fleiri leiðarútgáfur fyrir framleiddu vöruna. Staðfestu að útgáfurnar sem þú hefur áhuga á hafi verið merktar sem samþykktar og virkar og að þær hafi þær virku dagsetningar sem óskað er eftir. Leiðarútgáfan má ekki eiga við um nema eitt vefsetur.

Ef þú vilt nota leiðarlýsingar í kostnaðartilgangi er nauðsynlegt að frekari undirbúningur nauðsynlegur. Til dæmis verða kostnaðarflokkarnir sem eru úthlutaðir til leiðaraðgerða að vera réttir og þeim lokið.

## <a name="related-articles"></a>Tengdar greinar

[Afskrifa fastan kostnað fyrir framleidda vöru](amortize-constant-costs-manufactured-item.md)

[Uppsetning afurða sem hægt er að framleiða eða kaupa](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]