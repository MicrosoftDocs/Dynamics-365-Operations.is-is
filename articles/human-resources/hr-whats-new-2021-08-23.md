---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 23. ágúst 2021.
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 23. ágúst 2021.
author: marcelbf
ms.date: 08/23/2021
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
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c9ee0206bd77a8a2ec42501d64e83077baef09
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441676"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 23. ágúst 2021.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Microsoft Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4419.

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Gefa út | lýsing |
| --- | --- | --- |
| 594066 | Ekki hægt að eyða samskiptaupplýsingum | Þegar valið er að eyða færslum samskiptaupplýsinga fyrir starfsmann er annarri færslu samskiptaupplýsinga eytt í staðinn. |
| 611339 | Að bæta sérstillingu við leiðir til þess að bankareikningur hunsar síu og sækir fyrstu færsluna | Að bæta við sérstillingu veldur því að bankareikningslistinn keyrir fyrirspurn sérstillingar eftir að gagnasafnsfyrirspurnin keyrir, sem leiðir til þess að fyrirspurnin sækir efstu færsluna án tillits til þess starfsmanns sem verið er að skoða upplýsingarnar fyrir. |
| 591806 | Innleiðing verka vegna gjalddaga eru reiknuð út á rangan hátt | Gjalddagar eru ranglega reiknaðir þegar eftirfarandi skilyrði eru fyrir hendi: Gátlistarnir sem eru búnir til nota dagatal sem notar stækkað tímabil (til dæmis frá 2005 til 2050) og kjörstillingar notandans nota annað tímabelti en CST. |   
| 592749 | Leyfisstaða er röng í **Sjálfsafgreiðslu starfsmanns** | Ef starfsmaðurinn er í starfi hjá fleiri en einum lögaðila og leyfisyfirlit milli fyrirtækja er virkjað gæti leyfisstaðan verið röng. |
| 603133 | Óvænt viðvörun þegar óskað er eftir fríi | Þegar óskað er eftir fríi kemur upp óvænt viðvörun þegar fyllt er út í reitinn **Hálfur dagur** áður en reiturinn **Magn** er fylltur út. |
| 606546 | Valinn reitur ekki sýnilegur í samþykktu fríi | Gátreiturinn til að velja margar samþykktar leyfisbeiðnir var ekki sýnilegur. |
| 597059 | Starfsmaður ekki sýnilegur í **Fyrirtækjadagatal fyrir leyfi og fjarvistir** | Starfsmaður er ekki sýnilegur í **Fyrirtækjadagatal fyrir leyfi og fjarvistir** ef notað dagsetningabil inniheldur einhvern dag þar sem leyfisbeiðni hefur verið hafnað. |


## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md)|
| Virkja fjarvistarstjóra til að stjórna fríi | [Virkja fjarvistarstjóra til að stjórna fríi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Með þessari útgáfu erum við að uppfæra yfirlit vinnusvæðis fjarvistastjórnanda. Frekari upplýsingar er að finna í [Skilgreina hlutverk fjarvistastjórnanda](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Skilgreina kröfu viðhengis á hverja leyfisgerð | [Skilgreina kröfu viðhengis á hverja leyfisgerð](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Grunnstilla gerðir leyfis og fjarvista](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Stilla leyfiseiningar fyrir hverja leyfisgerð | [Stilla leyfiseiningar fyrir hverja leyfisgerð](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Grunnstilla gerðir leyfis og fjarvista](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gera kleift að merkja starfsmenn sem tilbúna að fá greitt | [Gera kleift að merkja starfsmenn sem tilbúna að fá greitt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Tilbúið til greiðslu](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Væntanlegt

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Eiginleiki | Upplýsingar |
| --- | --- |
| Verkvangsuppfærsla 10.0.21 (45) | Útgáfa verkvangsuppfærslu 10.0.21 á að fara af stað í útgáfuþjónustu 4. október 2021. Frekari upplýsingar er að finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.21 af Finance and Operations-forritum (október 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
