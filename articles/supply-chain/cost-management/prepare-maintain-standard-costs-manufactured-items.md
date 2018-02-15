---
title: "Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur"
description: "Þetta efnisatriði fjallar um skrefin til að undirbúa viðhald kostnaðar fyrir framleiddar vörur."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 605f4c6391e9c40b1b80fab93d61b88553369069
ms.openlocfilehash: 6f52d2d90d655d1ab465e1808ca55ef3d5ea9e56
ms.contentlocale: is-is
ms.lasthandoff: 01/19/2018

---


# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur

Þetta efnisatriði fjallar um skrefin til að undirbúa viðhald kostnaðar fyrir framleiddar vörur. Skrefin fyrir framleiddar vörur eru örlítið frábrugðin skrefunum fyrir keyptar vörur.

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

<a name="related-topics"></a>Tengd efnisatriði
--------

[Afskrifa fastan kostnað fyrir framleidda vöru](amortize-constant-costs-manufactured-item.md)

[Uppsetning afurða sem hægt er að framleiða eða kaupa](manufactured-items-treated-as-purchased-items.md)


