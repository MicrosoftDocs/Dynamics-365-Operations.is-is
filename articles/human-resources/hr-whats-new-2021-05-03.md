---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 3. maí 2021
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 3. maí 2021.
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df8bd0277e4f27c23ba25c886d12f589913e5d46
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066224"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 3. maí 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir eiginleikum sem eru nýir, breyttir eða koma fljótlega í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4140.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Bæta við upplýsingastiku þegar lífsviðburðir eru stofnaðir. | - | Þegar lífsviðburður er stofnaður birtast skilaboð á upplýsingastikunni sem gefa til kynna hvers konar lífsviðburður er stofnaður.

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þessa grein til að innihalda villuleiðréttingar sem komu inn í bygginguna eftir að þessi grein var upphaflega birt.

| Númer úthreyfingar | Gefa út |  Lýsing |
| --- | --- | --- |
| 559312 |  Hæð er ekki sýnd þegar launafyrirkomulag fastra launa er búið til fyrir starfsmann. |  Þegar misræmi er á tímabelti milli tímabeltis notanda og tímabeltis fyrirtækisins er ekki hægt að lesa launastig á verkinu. Fyrirspurnin var uppfærð í að sækja miðað við UTC-tíma. |
| 573676  | Ekki er hægt að bæta nýju tímabili við á eyðublaðinu **Fríðindaáætlun**. | Uppfærði eyðublaðið þannig að hnappurinn **Nýtt** er virkjaður undir flipanum **Tímabil** í **Fríðindaáætlanir**. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Viðbætur á upplifun verkflæðis fyrir leyfi og fjarvistir | [Viðbætur á upplifun verkflæðis fyrir leyfi og fjarvistir](https://go.microsoft.com/fwlink/?linkid=2147528) | [Biðja um frí](hr-employee-self-service-request-time-off.md)|
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md)|
| Endurskoðun færslu fyrir uppsafnað leyfi | - | [Endurskoðun færslu fyrir uppsafnað leyfi](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Verkvangsuppfærsla 10.0.18 (42) | Verkvangsuppfærsla 10.0.18 á að fara af stað í útgáfu 17. maí 2021. Fyrir frekari upplýsingar, sjá [Uppfærslur á vettvangi fyrir útgáfu 10.0.18 af fjármála- og rekstrarforritum (maí 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Stuðningur við sérstillta reiti í hæfnireglum fríðindastjórnunar  | [Stuðningur við sérstillta reiti fyrir vinnslu á hæfni](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

