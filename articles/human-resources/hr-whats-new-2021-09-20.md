---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 20. september 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 20. september 2021.
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f4fc4768f8c96678b216709f78af6d3ddfd4132
ms.sourcegitcommit: ba8ca42e43e1a5251cbbd6ddb292566164d735dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/25/2021
ms.locfileid: "7556934"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 20. september 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Microsoft Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4464.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
|---|---|---|
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md) |
| Gera kleift að merkja starfsmenn sem tilbúna að fá greitt | [Gera kleift að merkja starfsmenn sem tilbúna að fá greitt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Tilbúið til greiðslu](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Gefa út | Lýsing |
|---|---|---|
| 619774 | Breyting á lýsingu heimilisfangs samstillist ekki við Dataverse í rauntíma. | Þegar lýsingu fyrir heimilisfang starfsmanns er breytt verður uppfærð lýsing ekki samstillt í rauntíma við Dataverse. Áskriftin í töflunni **Staðsetning vörustjórnunar** var uppfærð til að senda uppfærslu. |
| 614603| Villa á síðunni **Starfsmaður** þegar færibreytan **Starfsmannaaðgerð starfskrafts** er ekki valin. | Þegar nýr starfsmaður er ráðinn eða farið er á síðuna **Starfskraftur** sýnir eftirfarandi villa „Reitur **Gerð starfsmannaaðgerðar** verður að vera fyllt út“, jafnvel þótt slökkt sé á **Aðgerðum starfsmanns**. |
| 615367 | Flipinn **Samþykkt frí** sýnir viðvörun og birtist ekki með réttum hætti. | Ef leyfiseiningin er stillt á **Dagar** áður en eiginleikinn **Stilla leyfiseiningar fyrir hverja leyfisgerð** er virkjaður, sýnir flipinn **Samþykkt frí** ógilda viðvörun og ranga dálka. |


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
| Síðan **Skýrslufæribreytur** í **Sjálfsafgreiðslu starfsmanns** fyrir fríðindayfirlitið er röng. | Þegar farið er í **Yfirlit yfir fríðindi** í **Sjálfsafgreiðslu starfsmanns** sýnir síðan **Skýrslufæribreytur** flýtiflipana **Færslur til að taka með** og **Keyra í bakgrunni**.  Þetta þarf að fjarlægja. |
| Lokuð tímabil og næstu tímabil eru sýnd á síðunni **Skýrslufæribreyta** fyrir fríðindayfirlitið. | Þegar farið er á viðtökusíðuna **Skýrsla fríðindayfirlits** getur notandinn valið tímabil fríðindaáætlana sem eru lokuð eða dagsett fram í tímann, sem skilar af sér auðri síðu. Aðeins núverandi tímabil fríðindaáætlunar á að sjást á listanum. |
|Villa þegar skýrsla er send með tölvupósti þar sem viðtökustaður GER-skýrslu er notaður. | Hægt er að stilla fríðindayfirlitið á að nota færibreytur tölvupósts á síðunni **Viðtökustaðir GER-skýrslu**. Þegar uppsetningu og prentun skýrslunnar er lokið mun notandinn fá sniðsvillu og fríðindayfirlitið verður ekki sent.|


## <a name="coming-soon"></a>Væntanlegt

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Eiginleiki | Upplýsingar |
|---|---|
| Verkvangsuppfærsla 10.0.21 (45) | Útgáfa verkvangsuppfærslu 10.0.21 á að fara af stað í útgáfuþjónustu 4. október 2021. Frekari upplýsingar er að finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.21 af Finance and Operations-forritum (október 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Yfirlit yfir frammistöðubækur fyrir ítarlegar skýrslur | Þessi eiginleiki verður sjálfgefið virkur í næstu útgáfu. |


## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
