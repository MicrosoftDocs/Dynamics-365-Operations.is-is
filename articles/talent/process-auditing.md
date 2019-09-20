---
title: Merkja breytingar í ráðningargögnum
description: Eiginleikinn fyrir endurskoðunarferlið gerir þér kleift að fylgjast með hvenær umsækjendur, laus störf eða umsóknir um starf breytast út af skýrslugerð eða samræmisástæðum.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 448fceccb507bec5b60b686043a303c1997a9ac0
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742672"
---
# <a name="track-changes-in-recruiting-data"></a>Merkja breytingar í ráðningargögnum

Hægt er að fylgjast með breytingum sem gerðar eru á umsækjendum, lausum störfum eða umsóknum um starf með því að nota endurskoðunarferli. Þetta er gagnlegt út af skýrslugerð eða af samræmisástæðum.

Þú getur skoðað gögnin sem fylgst með í Power BI með því að nota OData tengið. Frekari upplýsingar er að finna í [Tengjast við OData straum í Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Rekja breytingar
Til að setja upp rakningu breytinga í ráðningargögnum skal fylgja þessum skrefum:

1. Í [PowerApps](https://web.powerapps.com) skal velja viðeigandi umhverfi.

2. Veljið **Stillingar** (tannhjólstáknið), veljið **Ítarlegar sérstillingar** og síðan skal velja **Tilföng** undir **Tilföng fyrir þróunaraðila**. 

3. Á síðunni **Tilföng fyrir þróunaraðila** skal afrita gildið í reitinn **Tilvik af gildi vef-API**. Til dæmis gæti gildið litið út eins og: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Þú getur þá beðið um gögnin úr einni af eftirfarandi einingum:
  - Ferill fyrir laust starf (msdyn_jobopeninghistories)
  - Starfsumsóknarferill (msdyn_jobapplicationhistories) 
  - Ferill umsækjanda (msdyn_candidatehistories)

## <a name="data-reported"></a>Tilkynnt gögn

Eftirfarandi gögn eru tiltæk með endurskoðunarferli.

| Tilkynnt gögn | Lýsing |
| --- | --- |
| Breytt af (msdyn_ChangedbyId) | Tilvísun í notanda |
| Stofnað (createdon) |  Dagsetning og tími samkvæmt UTC þegar breytingin átti sér stað |
| Breyta gerð (msdyn_changetype) | Hvaða breyting átti sér stað |
| Algeng gildi fyrir umsækjendur, laus störf, <br></br>og starfsumsóknir | Stofnaður<br></br>Uppfært |
| Ferill starfsumsóknar | Gerving bætt við <br></br>Gervingur fjarlægður |
| Ferill fyrir laust starf | VERKEFNALISTI: auglýsingu bætt við <br></br>VERKEFNALISTI: auglýsing fjarlægð <br></br>VERKEFNALISTI: auglýsing uppfærð <br></br>VERKEFNALISTI: þátttakanda bætt við <br></br>VERKEFNALISTI: þátttakandi fjarlægður |
| Ferill umsækjanda | Gerving bætt við <br></br>Gervingur fjarlægður <br></br>Starfsreynslu bætt við <br></br>Starfsreynsla fjarlægð <br></br>Menntun bætt við <br></br>Menntun fjarlægð <br></br>Hæfni bætt við <br></br>Hæfni fjarlægð <br></br>Merki bætt við <br></br>Merki fjarlægt <br></br>Samfélagsmiðli bætt við <br></br>Samfélagsmiðill fjarlægður <br></br>Persónuupplýsingum bætt við <br></br>Persónuupplýsingar uppfærðar<br></br> |
| Breytt svæði (msdyn_changedfields) | Skráning á breyttum svæðum JSON-hlutar geymir hugsanlega ekki gildi fyrir öll svæði.<br></br><br></br>Fyrir breytingar á „Stofnað“ og „Uppfært“, birtir það svæðin í færslu fyrir stofnað eða breytt.<br></br><br></br>Fyrir „Bætt“ breytingargerðir, birtir hún svæðin í undirfærslunni.<br></br><br></br>**Dæmi:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": satt } <br></br>} |
|Ferill starfsumsóknar | Starfsumsókn (msdyn_JobapplicatonId)<br></br>Staða (msdyn_status) <br></br>Ástæða stöðu (msdyn_statusreason) <br></br>Ástæða fyrir höfnun (msdyn_rejectionreason) |
| Ferill fyrir laust starf | Laust starf (msdyn_JobopeningId) <br></br>Staða (msdyn_jobopeningstatus) <br></br>Ástæða stöðu (msdyn_jobopeningstatusreason) |
| Ferill umsækjanda | Umsækjandi (msdyn_CandidateId) |
