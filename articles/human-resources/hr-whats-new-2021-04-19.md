---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 19. apríl 2021
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 19. apríl 2021.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e46c5721853ebfe3b9d5955ca5f4e7a4ead570c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846301"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 19. apríl 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir eiginleikum sem eru nýir, breyttir eða koma fljótlega í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4113.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Verkvangsuppfærsla 10.0.17 (41) | -- | [Palluppfærslur fyrir útgáfu 10.0.17 af Finance and Operations forritum (apríl 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Stuðningur við sérstillta reiti í skjámyndum fríðindastjórnunar | [Stuðningur við sérstillta reiti í fríðindastjórnun](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Yfirlit fríðindastjórnunar](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þessa grein til að innihalda villuleiðréttingar sem komu inn í bygginguna eftir að þessi grein var upphaflega birt.

| Númer úthreyfingar | Gefa út |  Lýsing |
| --- | --- | --- |
| 552164 | **Vistað yfirlit** í **Sjálfsafgreiðsla starfsmanns > Opin námskeið** virkar ekki fyrir námskeið sem innihalda dagskrá | Ef vistað yfirlit er notað í opnum námskeiðum (ESS) og eitt námskeiðið er með dagskrá hengda við, þá mun yfirlitið ekki lengur sýna margar línur fyrir námskeiðið |
| 560614 | **Fríðindi > Valkostir viðburðar** sýna misræmi í fylgigögnum ábendingar og hegðun kóða. | Uppfærði ábendingar í **Valkostir viðburðar** til að sýna rétta hegðun. |
| 560616 | **Fríðindi > Valkostir viðburðar** eru breytanleg í fríðindaáætlun starfskrafts, en breytingar haldast eins. | Uppfærð hegðun á valkosti viðburðar skiptir yfir í virkt eða óvirkt, fer allt eftir tengdum valkostum, fyrir hvert fylgigagn ábendingar. |
| 565054 | Ekki er hægt að skoða innihald listans **Starfskraftar án atvinnu** þegar **Ítarlegri aðgangur** er á. | Þessi útgáfa leysir vandamálið, þegar kveikt var á **Ítarlegri aðgangur**, þar sem aðeins kerfisstjórar gátu skoðað innihald listans **Starfskraftar án atvinnu**. Þar sem þessi endurbót er öryggisbreyting þarf að velja hana í eiginleikastjórnun. Þegar eiginleikinn er virkur munu þau hlutverk sem hafa aðgang að skjámyndinni sjá innihaldið þótt kveikt sé á ítarlegum aðgangi. Frekari upplýsingar er að finna í [Starfskraftar án atvinnu](hr-personnel-workers-without-employment.md). |
| 570586 | Staðfesting leyfisbeiðni mistekst þegar starfi lýkur á undan síðustu færslu fyrir þann starfsmann yfir allar leyfisáætlanir. | Eftir að starfi lýkur mistekst staðfesting leyfisbeiðni ekki vegna leyfisfærslna starfsmanns.|
| 570783 | Með því að kveikja og slökkva á leyfi milli fyrirtækja í samnýttum færibreytum Human Resources, breytist það sem starfsmenn sem ráðnir eru í einu fyrirtæki sjá í leyfisbeiðnum. | Starfsmenn sem starfa í einu fyrirtæki sjá engar breytingar á beiðnum um frí ef færibreytan er virk eða óvirk. |
| 572343 | Nauðsynlegur ástæðukóði er ekki birtur þegar eiginleikinn fyrir leyfisyfirlit milli fyrirtækja er virkur. | Þegar leyfiseiginleiki milli fyrirtækja er virkur sýnir ástæðukóðinn nú það sem búist er við. |
| 573676 | Ekki er hægt að bæta **Tímabili** við **Fríðindastjórnun > Tenglar > Fríðindaáætlanir**. | Villur lagaðar þar sem ekki var hægt að bæta við eða uppfæra **Tímabil** í núverandi skjámynd **Fríðindaáætlunar**. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Viðbætur á upplifun verkflæðis fyrir leyfi og fjarvistir | [Viðbætur á upplifun verkflæðis fyrir leyfi og fjarvistir](https://go.microsoft.com/fwlink/?linkid=2147528) | [Biðja um frí](hr-employee-self-service-request-time-off.md)|
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Hæfni sem yfirmaður færir inn fyrir starfsmenn sína getur verið sjálfkrafa samþykkt af verkferlinu | Væntanlegt. |
| Verkvangsuppfærsla 10.0.18 (42) | Verkvangsuppfærsla 10.0.18 á að fara af stað í útgáfu 17. maí 2021. Fyrir frekari upplýsingar, sjá [Palluppfærslur fyrir útgáfu 10.0.18 af Finance and Operations forritum (maí 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Stuðningur við sérstillta reiti í hæfnireglum fríðindastjórnunar  | [Stuðningur við sérstillta reiti fyrir vinnslu á hæfni](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
