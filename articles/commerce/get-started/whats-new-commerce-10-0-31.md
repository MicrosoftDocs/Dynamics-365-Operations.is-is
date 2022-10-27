---
title: Forskoðun Dynamics 365 Commerce 10.0.31 (febrúar 2023)
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýir eða breyttir Microsoft Dynamics 365 Commerce 10.0.31.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 05ccd9794ffeba6a09d6fec0a57ffad2b59707ad
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709872"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Forskoðun Dynamics 365 Commerce 10.0.31 (febrúar 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein sýnir eiginleika sem eru annað hvort nýir eða breyttir Microsoft Dynamics 365 Commerce forskoðunarútgáfa 10.0.31. Þessi útgáfa hefur byggingarnúmer 10.0.1406 og er fáanleg samkvæmt eftirfarandi áætlun:

- **Forskoðun forútgáfu:** Október 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Janúar 2023
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Febrúar 2023

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að innihalda eiginleika sem var bætt við smíðina eftir að þessi grein var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Villukóðar | Commerce kynnti staðlaðar villutilvísanir til að vera með í stöðvunarvillum á netinu sem kynntar eru netkaupendum.| [Villukóðar fyrir Checkout mát](../checkout-module-error-codes.md)  | Sjálfgefið kveikt |
| Greiðslur | [Virkjaðu Apple Pay með Dynamics 365 Payment Connector fyrir Adyen](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | Viðskiptavinir í rafrænum viðskiptum geta notað Apple Pay á körfu- og afgreiðslusíðum þegar þeir nota studd tæki eða vafra. | Hönnuður valinn |
| Greiðslur  |  Commerce bætti við getu til að takmarka hvernig notendur hafa samskipti við endurtekna greiðslutákn í gegnum notendaviðmót Commerce höfuðstöðvar. Greiðslueyðublöð, svo sem **Sölupöntun símaver** síðu, birta ekki lengur áður notaða endurtekna greiðslulykil viðskiptavinar til notkunar í nýrri færslu. Aðeins ákveðið „kort á skrá“ inntak í verslunina **Greiðslur viðskiptavina** skjár, eða með samkomulagi við viðskiptavin á meðan greitt er með sölupöntun, verður kynnt fyrir notendum símaversins eða höfuðstöðvum Commerce þegar unnið er úr greiðslu fyrir nýja færslu. | [Takmarkaðu notkun greiðslulykils](../dev-itpro/limit-token-usage.md)  |  Stjórnun eiginleika<p>*Takmarka notkun greiðslulykils við pöntunarsamhengi*  |
| Sölustaður | [Búðu til innkaupapantanir frá POS](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Bætt birgðaaðgerð á innleið í sölustað (POS) app til að leyfa notendum að búa til, breyta og staðfesta innkaupapöntunarbeiðnir. |  Stjórnun eiginleika<p>*Möguleiki á að búa til innkaupapöntunarbeiðni á sölustað*   |



## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Palluppfærslur fyrir Finance and Operations öpp

Microsoft Dynamics 365 Commerce 10.0.31 inniheldur uppfærslur á vettvangi. Til að læra meira, sjá [Palluppfærslur fyrir útgáfu 10.0.31 af fjármála- og rekstrarforritum (febrúar 2023)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingar sem fylgja hverri uppfærslu sem er hluti af útgáfu 10.0.31, skráðu þig inn á Microsoft Dynamics Lifecycle Services og skoða [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 2 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 2 áætlun](/dynamics365-release-plan/2022wave2/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-commerce-features"></a>Fjarlægðir og úreltir viðskiptaeiginleikar

The [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Commerce](removed-deprecated-features-commerce.md) grein lýsir eiginleikum sem hafa verið fjarlægðir eða úreltir fyrir Commerce.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um úreldingu tilkynnt í [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Commerce](removed-deprecated-features-commerce.md) grein 12 mánuðum fyrir brottnám.


Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
