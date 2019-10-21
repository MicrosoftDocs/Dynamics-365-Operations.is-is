---
title: Losa fasta eign sem rýrnun
description: Umræðuefnið lýsir ferli úthlutunar á losunarfærslum fyrir fasta eign sem var losuð sem rýrnun.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: de105e061712540fc8e3d720a65c029f865b8948
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187292"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Losa fasta eign sem rýrnun

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Umræðuefnið lýsir ferli úthlutunar á losunarfærslum fyrir fasta eign sem var losuð sem rýrnun. Færslutegundir sem hægt er að losa eru m.a. yfirtaka eignar og uppsafnaðar afskriftarfærslur og aðrar færslur fastra eigna. Losun þessara færslna hefur áhrif á efnahagsreikninga, svo sem aðlögun yfirtöku, afskriftarleiðréttingu, endurmat, niðurfærslu og niðurfærslu reikninga.

| Færsla                                         | Debet (Dr.) | Kredit (Cr.) |
|-----------------------------------------------------|-------------|--------------|
| Uppsöfnuð afskrift Dr.                        | X           |              |
| Hagnaður/tap Cr. fastra eigna                          |             | X            |
| Hagnaður/tap Dr. fastra eigna                          | X           |              |
| Bókunarlykill Cr. eignakaupa                 |             | X            |
| Hagnaður/tap Dr. fastra eigna (bókfært virði \[BNV\]) | X           |              |
| Hagnaður/tap Cr. fastra eigna (BNV)                    |             | X            |

> [!NOTE]
> Við mælum með að þú vinnur náið með fjármálastjóra fyrirtækisins (fjármálastjóra) eða stjórnanda til að bera kennsl á réttu reikningana sem nota ætti fyrir hverja tegund viðskipta og einnig til að sannreyna að förgunarferlið og viðskiptin sem það býr uppfæra reikninga rétt.

Áður en þú losar fasta eign sem rýrnun verðurðu að stofna bókhald sem er tengt við yfirtökuverðmæti eignarinnar, afskriftir yfirstandandi árs, afskriftir fyrri ára og BNV eignarinnar. Færslugerðir fastra eigna eru skráðar á síðunni **Bókunarforstillingar fastra eigna**. Farðu í **Fastar eignir \> Uppsetning \> Bókunarforstillingar fastra eigna**, og síðan á flýtiflipann **Losun**, veldu **Rýrnun** í reitnum fyrir ofan hnitanetið. Eftirfarandi mynd sýnir lista yfir færslugerðir fastra eigna á síðunni **Bókunarforstillingar fastra eigna**.


[![Eign lostuð sem rýrnun, mynd 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Fyrir eftirfarandi dæmi var föst eign keypt þann 1. janúar 2018 og hún verður úrelt þann 31. mars 2019.

- **Kaupverð:** 24.000,00 Bandaríkjadalir (USD)
- **Líftími:** Tvö ár
- **Afskriftaraðferð:** Línuleg á líftíma
- **Afskriftarfjárhæð:** 1,000.00 USD á mánuði

BNV af fastri eign er reiknað með því að nota eftirfarandi formúlu:

Nettó bókað virði = yfirtökuverð - afskriftir

Í þessu dæmi var fasta eignin keypt og var afskrifuð í 15 mánuði, frá janúar 2018 til mars 2019. Þess vegna er BNV eignarinnar 9,000.00 USD (24.000,00 USD - 15.000,00 USD).

[![Dæmi um afskriftir eigna](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Til að búa til losunarfærslubók skaltu fara í **Fastar eignir \>Færslur í færslubók \> Eignabók** og veldu síðan **Línur** í aðgerðaglugganum. Veldu **Losun - rýrnun** og veldu síðan kenni fastra eigna. Til að losa eignina að fullu skaltu hvorki færa gildi í reitinn **Debet** né reitinn **Kredit**.

[![Eignabók](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Rýrnunarfærsla losunar á föstum eignum breytir reitagildi eignabókar á eftirfarandi hátt:

- Í hlutanum **Staða** er reiturinn **Staða** uppfærður í **Rýrnað**.
- Í hlutanum **Útgáfa** er reiturinn **Losunardagur** stilltur á dagsetninguna þegar eignin var rýrð.

[![Ítarupplýsingar eignabókar](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Eftirfarandi mynd sýnir stöðu fastra eigna.

[![Staða fastra eigna](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Eftirfarandi mynd sýnir fylgiskjalið sem er sent.

[![Bókað nettóvirði](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)
