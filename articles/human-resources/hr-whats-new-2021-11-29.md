---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 19. nóvember 2021
description: Þetta efnisatriði lýsir eiginleikum sem eru annað hvort nýir eða breyttir í sjálfstæðu Microsoft Dynamics 365 Human Resources fyrir 19. nóvember 2021.
author: marcelbf
ms.date: 12/03/2021
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
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 618d90f95637002f444b334e16d3fef466dda65e
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087475"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 19. nóvember 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Microsoft Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Fyrir frekari upplýsingar um nýja eiginleika og væntanlegar almennar tiltækar dagsetningar, sjá [Dynamics 365 Human Resources 2021 útgáfubylgja 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa inniheldur eftirfarandi villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4591.

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Gefa út | Lýsing |
|---|---|---|
| 626178 | Leiðsögn vantar á verkamannaflísarnar inn **Sjálfsafgreiðslustjóri** | Nú er búið að laga þetta vandamál. Leiðsögnin er tiltæk til að sjá skýrsluupplýsingarnar í **Sjálfsafgreiðslustjóri**. |
| 632573 | Það er engin staðfestingarvilla þegar þú vistar a **Námskeið** | Nú er búið að laga þetta vandamál. Þegar þú býrð til námskeið með **Lágmarksfjöldi þátttakenda** að meira en 0 var samt leyft að vera vistað jafnvel þegar **Hámarksfjöldi þátttakenda** er 0. |
| 615955 | Villa "Field **Tilgangur** verður að fylla út þegar ný ráðningarbeiðni er stofnuð. | Þegar þú býrð til heimilisfang fyrir nýjan staðsetningarbeiðni fyrir ráðningarbeiðni, færðu villuna: "Field 'Tilgangur' verður að fylla út." Hins vegar er **Tilgangur** reiturinn er ekki tiltækur á síðunni. |
| 620797 | Autt **Kyn** reitvilla er villandi | Þegar kyn er ekki slegið inn fyrir persónulegan tengilið sýnir skýrslan „Smelltu eða pikkaðu hér til að slá inn texta“ – Það er villandi þar sem ekkert er hægt að slá inn í reitinn. |
| 620800 | Hlekkur yfirlýsingu um kosti er falinn | Fríðindayfirlit er ekki sjálfgefið sýnilegt í **Sjálfsafgreiðsla starfsmanna**.  Tengli var bætt við hægra megin á **Sjálfsafgreiðsla starfsmanna** undir **Tenglar** kafla |
| 629778 | Afköst vandamál með CDS samþættingu. | Heimildartengd beiðni olli frammistöðuvandamálum. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
|---|---|---|
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Væntanlegt
Fyrir heildarlista yfir fyrirhugaða eiginleika og áætlaða útgáfu þeirra, sjá [Dynamics 365 og iðnaðarský: 2021 útgáfubylgja 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
