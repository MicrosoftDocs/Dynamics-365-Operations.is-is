---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 6. september 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 6. september 2021.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 314d836db9b7560c2ed95ad1b9d2eba753e39d2b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690583"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 6. september 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Microsoft Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4443.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
|---|---|---|
| Virkja fjarvistarstjóra til að stjórna fríi | [Virkja fjarvistarstjóra til að stjórna fríi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Með þessari útgáfu erum við að uppfæra yfirlit vinnusvæðis fjarvistastjórnanda. Frekari upplýsingar er að finna í [Skilgreina hlutverk fjarvistastjórnanda](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Skilgreina kröfu viðhengis á hverja leyfisgerð | [Skilgreina kröfu viðhengis á hverja leyfisgerð](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Grunnstilla gerðir leyfis og fjarvista](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Stilla leyfiseiningar fyrir hverja leyfisgerð | [Stilla leyfiseiningar fyrir hverja leyfisgerð](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Grunnstilla gerðir leyfis og fjarvista](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Gefa út | lýsing |
|---|---|---|
| 610128 | Villa við birtingu gagna þegar HcmDiscussionOverallCommentEntity var notað | Þegar gögn eru birt úr Excel-vinnubók í einingu HcmDiscussionOverralCommentEntity kemur upp eftirfarandi villa: „Get ekki fundið færslu gagnagjafa af gerðinni HcmTopicOverrall.“ |
| 589073 | EEO-1 skýrsla lítur á „Ótilgreint" og auð gildi fyrir reitinn **Kyn** sem „Kona“. | Ef **Karl** er ekki tilgreindur fyrir reitinn **Kyn** býr EEO-1 skýrslan til sjálfgefið gildi fyrir **Konu**. |
| 589617 | Staða frítímaspjalds, stöður yfir tiltækt til kaups og tiltækt til sölu birtast ekki þegar notandahlutverk takmarkast við tiltekinn lögaðila. | Ef notandinn (hlutverk starfsmanns) er takmarkað við tiltekinn lögaðila birtast stöður ekki á réttan hátt á spjaldinu **Frítími** og í reitunum **Hægt að kaupa** og **Hægt að selja**. |
| 604310 | Flipi fjarvistastjórnanda ætti að vera falinn þegar notandinn er ekki með fjarvistarstigveldið úthlutað. | Fyrir tiltekinn lögaðila ætti flipinn **Fjarvistarstjóri** að vera falinn í gátt sjálfsafgreiðslu nema færibreyta milli fyrirtækja er virkjuð og að minnsta kosti eitt fjarvistarstigveldi er tengt við notandann. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
|---|---|---|
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md) |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Gera kleift að merkja starfsmenn sem tilbúna að fá greitt | [Gera kleift að merkja starfsmenn sem tilbúna að fá greitt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Tilbúið til greiðslu](/dynamics365/human-resources/hr-compensation-payroll) |
| Sérstilltir reitir í „Hæfni“ |[Stuðningur sérstilltra reita í hæfnivinnslu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Nota sérstillta reiti í hæfnivinnslu](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Væntanlegt

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Eiginleiki | Upplýsingar |
|---|---|
| Verkvangsuppfærsla 10.0.21 (45) | Útgáfa verkvangsuppfærslu 10.0.21 á að fara af stað í útgáfuþjónustu 4. október 2021. Fyrir frekari upplýsingar, sjá [Palluppfærslur fyrir útgáfu 10.0.21 af Finance and Operations forritum (október 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Yfirlit yfir fríðindi | Yfirlit yfir fríðindi til að skoða núverandi fríðindaval starfsmanns. Frekari upplýsingar er að finna í [Yfirlit yfir fríðindi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) í skjali útgáfutímabils. |

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
