---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 26. júlí 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 26. júlí 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4e124655ca96e34e53723ea2608227661034d58b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694712"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 26. júlí 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4384.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Update 10.0.20 fyrir verkvang | -- | [Palluppfærslur fyrir útgáfu 10.0.20 af Finance and Operations forritum (ágúst 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Gefa út |  lýsing |
| --- | --- | --- |
| 600422 | Staðfesting á heimilisfangi launaskrár virkar ekki fyrir Tilbúið til greiðslu. | Staðfesting hefur verið uppfærð til að gera kröfu um aðeins eitt heimilisfang af gerðinni „Búseta fyrir launaskrá“ og aðeins eitt heimilisfang af gerðinni „Vinnustaðsetning fyrir launaskrá“. |
| 601226 | Vandamál varðandi gagnasamþættingu: Útflutningsverk vegna samþættingar launaskrár hefur ekki möguleikann á fullri sendingu | Samþætting launaskrár við Ceridian DayForce var að gera stigvaxandi sendingu í stað fullrar sendingar. Ceridian þarf að vera að fullu uppfært öllum stundum. Búið er að laga þetta vandamál, einingarnar í gagnaútflutningsverkinu munu ekki lengur skipta yfir í stigvaxandi sendingu. |
| 602272 | Nú vantar reiti sem bætt var við vinnusvæði starfsmanns í sjálfsafgreiðslu og ekki er lengur hægt að bæta reitum við það | Við höfum lagað vandann með sérstillinguna fyrir sjálfsafgreiðslu starfsmanns. Hægt er að bæta nýjum reitum við yfirlitið og allar fyrirliggjandi sérstillingar verða sýnilegar notendum |
| 600711 | Valreitur fyrir hálfsdags skilgreiningu virkjaður fyrir heilsdags leyfisbeiðni | Búið er að laga þetta vandamál og reitur fyrir hálfsdags skilgreiningu verður aðeins virkjaður þegar starfsmenn velja leyfisgerð með hálfsdags skilgreiningu virkjaða og hálfan dag sem valið gildi |
| 602208 | Einingar með uppsöfnuðum hraða sem sýna klukkustundir í stað daga | Nú er búið að laga þetta vandamál. Skjámyndin **Frí** mun sýna rétta leyfiseiningu (klukkustundir eða daga) fyrir dálkinn **Uppsöfnunarhraði**. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md)|
|  Virkja fjarvistarstjóra til að stjórna fríi | [Virkja fjarvistarstjóra til að stjórna fríi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Með þessari útgáfu erum við að uppfæra yfirlit vinnusvæðis fjarvistastjórnanda. Frekari upplýsingar er að finna í [Skilgreina hlutverk fjarvistastjórnanda](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  Skilgreina kröfu viðhengis á hverja leyfisgerð | [Skilgreina kröfu viðhengis á hverja leyfisgerð](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Grunnstilla gerðir leyfis og fjarvista](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Stilla leyfiseiningar fyrir hverja leyfisgerð | [Stilla leyfiseiningar fyrir hverja leyfisgerð](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Grunnstilla gerðir leyfis og fjarvista](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gera kleift að merkja starfsmenn sem tilbúna að fá greitt | [Gera kleift að merkja starfsmenn sem tilbúna að fá greitt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Tilbúið til greiðslu](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Væntanlegt

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
