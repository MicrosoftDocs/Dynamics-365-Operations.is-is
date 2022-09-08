---
title: Forútgáfa af Dynamics 365 Commerce 10.0.30 (nóvember 2022)
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýir eða breyttir Microsoft Dynamics 365 Commerce 10.0.30.
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405523"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Forútgáfa af Dynamics 365 Commerce 10.0.30 (nóvember 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein sýnir eiginleika sem eru annað hvort nýir eða breyttir Microsoft Dynamics 365 Commerce forskoðunarútgáfa 10.0.30. Þessi útgáfa hefur byggingarnúmer 10.0.1362 og er fáanleg samkvæmt eftirfarandi áætlun:

- **Forskoðun útgáfu:** september 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Október 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Nóvember 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að innihalda eiginleika sem var bætt við smíðina eftir að þessi grein var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---------|------------------|----------------|--------------| 
| Þjónustudeild   | Spjallaðu á netverslunarsíðu með því að nota a Power Virtual Agents láni. | Þessi eiginleiki mun gefa notendum netverslunarsíðunnar val um að nota a Power Virtual Agents spjallboti fyrir stuðningsbeiðnir. | Virkt af stjórnendum/framleiðendum fyrir endanotendur |
| Innsýn  |  Straumaðu rekstrarinnsýn (POS) atburðum til þín Application Insights reikning. | [Aðgangsskrár inn Application Insights](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  IT Pro/þróunaraðili valinn   |
|  Greiðslur  | Pantanastuðningur PayPal umfram 29 daga heimildartímabil. | Hámarksheimildartímabil PayPal er 29 dagar, eftir það verður að búa til nýtt heimild og pöntunarauðkenni. Sem valkostur býður PayPal upp á valmöguleika þar sem hægt er að vísa til pöntunar sem PayPal pöntun er almenn pöntun, sem gerir kleift að fá margar heimildir og fanga á sama pöntunarkenni, í stað þess að búa til nýja heimild og pöntunarkenni eftir 29 daga). | Þegar PayPal greiðslutengi er stillt í höfuðstöðvum Commerce skal reiturinn **OrderIntent** hefur verið bætt við og getur haft tvö gildi:<p><p>- **Heimild** - Þessi stilling er sjálfgefin (ef reiturinn er skilinn eftir auður, **Heimild** mun virka sem sjálfgefið). Stillir **OrderIntent** til **Heimild** tengist PayPal **vinnslu_kennsla** verðmæti á **NO_INSTRUCTION**. Pöntunin verður heimiluð með PayPal og ekki er hægt að breyta heimildinni þegar þetta gildi er notað.<p>- **Vista** - Þegar **OrderIntent** gildi er stillt á **Vista**, þetta tengist PayPal **vinnslu_kennsla** verðmæti á **ORDER_SAVED_EXPLICITLY**. Pöntunartilvísanir verða vistaðar í PayPal þjónustunni þegar þetta gildi er notað.  |
| POS innskráning  | [Virkja sjálfsafgreiðslugreiningarmöguleika fyrir POS innskráningu](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Þessi eiginleiki býður upp á sjálfsafgreiðslugreiningarmöguleika á sölustöðum (POS) og viðskiptahöfuðstöðvum til að hjálpa starfsmönnum og stjórnendum verslunar að greina fljótt og laga grunnorsakir POS innskráningarvandamála.<p><p>- Bilunarskilaboðin sem sýnd voru á POS innskráningarskjánum voru endurbætt til að veita áþreifanlegar upplýsingar um uppruna sem geta hjálpað verslunarstarfsmönnum sem nota POS að skilja hvað fór úrskeiðis svo þeir geti framkvæmt nauðsynlegar aðgerðir til að leysa málið.<p>- A **Prófa innskráningu** aðgerð er fáanleg á **Verkamenn** síðu í höfuðstöðvum Commerce svo að verslunarstjórar sem setja upp POS tæki geta líkt eftir POS innskráningu. Ef um innskráningarbilun er að ræða veitir þessi aðgerð hagkvæmar bilanaleitarleiðbeiningar svo stjórnendur geti athugað viðeigandi stillingar, leiðrétt vandamál og staðfest lagfæringar.  | Sjálfgefið kveikt |


## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Palluppfærslur fyrir Finance and Operations öpp

Dynamics 365 Finance 10.0.30 inniheldur vettvangsuppfærslur. Til að læra meira, sjá [Palluppfærslur fyrir útgáfu 10.0.30 af fjármála- og rekstrarforritum](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingar sem fylgja hverri uppfærslu sem er hluti af útgáfu 10.0.30 skaltu skrá þig inn á Lifecycle Services (LCS) og skoða [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 2 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 2 áætlun](/dynamics365-release-plan/2022wave2/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-features"></a>Fjarlægðir og úreltir eiginleikar

The [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Commerce](removed-deprecated-features-commerce.md) grein lýsir eiginleikum sem hafa verið fjarlægðir eða úreltir fyrir Commerce.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um úreldingu tilkynnt í [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Commerce](removed-deprecated-features-commerce.md) grein 12 mánuðum fyrir brottnám.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
