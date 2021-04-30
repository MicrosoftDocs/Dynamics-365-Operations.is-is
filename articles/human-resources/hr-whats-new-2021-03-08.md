---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 8. mars 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 8. mars 2021.
author: marcelbf
ms.date: 03/08/2021
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
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 890d7a2e671d6365cd1f6e23e399166541c04496
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890628"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 8. mars 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4017.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks | [Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Grunnstilla færibreytur leyfis og fjarvista](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Úthreyfing |  lýsing |
| --- | --- | --- |
| 486611 | Fjarvistarleyfi er sýnt í leyfisdagatali þegar kveikt er á **Gera leyfi óvirk í öllum dagatölum** | Ef **Gera leyfi óvirk í öllum dagatölum** er virkt, birtast leyfisupplýsingar ekki lengur þegar eiginleiki viðbóta dagatals yfir leyfi og fjarvistir er virkjaður.|
| 508972 | Einingu bankafærslu leyfis og fjarvista vantar staðfestingu á skráningu | Þegar eining bankafærslu leyfis og fjarvista er notuð er ekki lengur hægt að flytja inn starfsmenn sem ekki eru skráðir í áætlun. |
| 554854 | Villa við uppfærslu dagatals í ráðningareiningu ef sjálfgefinn lögaðili í valkostum notanda er annar | Að nota ráðningareininguna til að uppfæra dagatalið fyrir starfsmann skilar ekki lengur villu ef sjálfgefinn lögaðili í valkostum notanda er annar. |
| 558347 | „Ekki er hægt að stofna færslu í skilgreiningarsniðum (FormRunConfiguration)“ birtist þegar upphafssíðan er hlaðin. | Sérstillingar valda villunni „Ekki er hægt að stofna færslu í skilgreiningarsniðum (FormRunConfiguration)“ birtist þegar upphafssíðan er hlaðin. |
| 557327 | Vinnusvæði fríðindastjórnunar: Eyða birtist fyrir ofan hnitanetið. | Vandamál varðandi upplifun notanda leyst þar sem eyða birtist óvart út við ramma hnitanetstöflunnar á vinnusvæði fríðinda. |
| 557334 | Vinnusvæði fríðindastjórnunar: Fellilistavalmyndin **Tímabil** á aðeins að birtast í flipanum **Samantekt** | Felllilistavalmynd fyrir **Tímabil** fríðinda birtist nú aðeins þegar flipinn **Samantekt** er virkur á vinnusvæði fríðinda en ekki í hlutunum **Niðurstöður vinnslu** og **Tenglar**. |
| 557336 | Vinnusvæði fríðindastjórnunar: Textinn **Opna skráningu með útskráðum áætlunum** er styttur í reitayfirlitinu | Texta breytt í reitayfirlitinu í **Útskráðar áætlanir ... opin skráning** til að forðast styttingu á nauðsynlegu samhengi. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum fyrirtækis | [Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum fyrirtækis](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Takmörkun á breytingu persónuupplýsinga](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Hæfni sem yfirmaður færir inn fyrir starfsmenn sína getur verið sjálfkrafa samþykkt af verkferlinu | Væntanlegt. |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]