---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 5. október 2021
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Human Resources fyrir 5. október 2021.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc8cd8616f1b82258fccbb2b41d5e72a90aaed63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845113"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 5. október 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir eiginleikum sem eru nýir, breyttir eða væntanlegar í Microsoft Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4485.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
|---|---|---|
| Verkvangsuppfærsla 10.0.21 (45) | -- | [Palluppfærslur fyrir útgáfu 10.0.21 af Finance and Operations forritum (október 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þessa grein til að innihalda villuleiðréttingar sem komu inn í bygginguna eftir að þessi grein var upphaflega birt.

| Númer úthreyfingar | Gefa út | Lýsing |
|---|---|---|
| 598896 | Starfsmannafjárhæð birtist ekki fyrr en eftir að starfsmaður hefur lokið skráningu | Á síðunni **sjálfsafgreiðsla starfsmanns** var upphæð starfsmanns fyrir fríðindi ekki sýnd. Starfsmannafjárhæðin er nú birt á síðunni **Ávinningur af sjálfsafgreiðslu**.  |
| 613440 | Ekki tókst að flytja út gögn frá **Gagnastjórnun** | Þegar gögn er flutt út fyrir verk í **gagnastjórnun** mistekst útflutningurinn óvænt. |
| 618327 | Lokuð tímabil og næstu tímabil eru sýnd á síðunni **Skýrslufæribreytur** fyrir fríðindayfirlitið | Þegar farið er í **Yfirlit yfir fríðindi** í **Sjálfsafgreiðslu starfsmanns** sýnir síðan **Skýrslufæribreytur** flýtiflipana **Færslur til að taka með** og **Keyra í bakgrunni**. Þessir hlutar voru fjarlægðir.|
| 618326 | Röng **Skýrslufæribreytur** síða birtist í **Sjálfsafgreiðslu starfsmanns** fyrir fríðindayfirlitið| Þegar farið er á viðtökusíðuna **Skýrsla fríðindayfirlits** gat notandinn valið tímabil fríðindaáætlana sem eru lokuð eða dagsett fram í tímann, sem skilar af sér auðri síðu. Aðeins núverandi tímabil fríðindaáætlunar á að sjást á listanum. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
|---|---|---|
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Sérstilltir reitir í „Hæfni“ |[Stuðningur sérstilltra reita í hæfnivinnslu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Nota sérstillta reiti í hæfnivinnslu](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Yfirlit yfir fríðindi |[Yfirlit yfir fríðindi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Yfirlit yfir fríðindi](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Fríðindayfirlýsing; þekkt vandamál

| Gefa út | Lýsing |
|---|---|
|Villa þegar skýrsla er send með tölvupósti þar sem **viðtökustaður GER-skýrslu** er notaður | Hægt er að stilla fríðindayfirlitið á að nota færibreytur tölvupósts á síðunni **Viðtökustaðir GER-skýrslu**. Þegar uppsetningu og prentun skýrslunnar er lokið mun notandinn fá sniðsvillu og fríðindayfirlitið verður ekki sent.|

## <a name="feature-management-changes"></a>Breytingar á eiginleikastjórnun

| Eiginleiki | Lýsing |
|---|---|
|Yfirlit yfir frammistöðubækur fyrir ítarlegar skýrslur | Þessi eiginleiki verður sjálfgefið virkur í þessari útgáfu. |

## <a name="coming-soon"></a>Væntanlegt

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Eiginleiki | Upplýsingar |
|---|---|
| Verkvangsuppfærsla 10.0.22 (46) | Útgáfa verkvangsuppfærslu 10.0.22 á að fara af stað í útgáfu 1. nóvember 2021. Fyrir frekari upplýsingar, sjá [Palluppfærslur fyrir útgáfu 10.0.22 af Finance and Operations forritum (nóvember 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
