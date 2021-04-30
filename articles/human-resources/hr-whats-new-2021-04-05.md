---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 5. apríl 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 5. apríl 2021.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ffb1d8966cb7e41a7032c6d4449b9e332c0e4703
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890602"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 5. apríl 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4074.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum fyrirtækis | [Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum fyrirtækis](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Takmarka breytingu persónulegra upplýsinga](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Úthreyfing |  lýsing |
| --- | --- | --- |
| 550852 | Hnappurinn **Samþykki** staðfestir ekki með áskilda reiti stillta í skjámyndinni **Yfirfara**. | Þegar reitur er stilltur sem áskilinn í skjámyndinni **Yfirfara** og breytingar eru gefnar út fyrir stjórnandahlutverkið, staðfestir skjámyndin ekki eins og búist er við. |
| 559564 | Gamlar aðgerðir starfsmanns fyrir breytingu á föstum launum sýna villu fyrir hætta notendur. | Aðgerð starfsmanns vegna launa starfsmanns sem er hættur sýnir villu. Þegar starfsmanni er sagt upp sýnir starfsmannaaðgerð stöðuhækkunar á undan uppsögn villu. |
| 560074 | Fellilisti starfsflokks síar ekki **Gerð starfsmanns** og sýnir flokka fyrir starfsmenn og verktaka. | Í skjámyndinni **Starfsmaður** ætti fellilistinn **Starfsflokkur** að sýna annaðhvort starfsmanna- eða verktakaflokk samkvæmt starfsmannagerð starfsmannsins. |
| 567388 | Sumar upplýsingar um nýstofnaða starfsmenn samstillast ekki strax við töfluna **cdm_worker** í Dataverse. | Þegar ný starfsmannafærsla er búin til ætti nýja færslan að samstillast við töfluna **cdm_worker** í Dataverse en ekki allir eiginleikar myndu vera teknir með í Dataverse færsluna. |
| 563837 | Eiginleikar sem eru ekki tiltækir í Human Resources birtast. | Ýmsir eiginleikar sem eiga ekki við um Human Resources birtast í eiginleikastjórnun. Þessir eiginleikar eru nú fjarlægðir af lista yfir eiginleika sem hægt er að virkja í Human Resources. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Hæfni sem yfirmaður færir inn fyrir starfsmenn sína getur verið sjálfkrafa samþykkt af verkferlinu | Væntanlegt. |
| Verkvangsuppfærsla 10.0.17 (41) | Verkvangsuppfærsla 10.0.17 á að fara af stað í næstu útgáfu 19. apríl 2021. Frekari upplýsingar er að finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.17 fyrir Finance and Operations-forrit (apríl 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]