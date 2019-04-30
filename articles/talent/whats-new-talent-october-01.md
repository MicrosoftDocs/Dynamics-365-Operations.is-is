---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (1. október 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 15b5fd7095a62aa9b7b79ebfcada667959b756aa
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "858745"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a>Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (1. október 2018)

[!include [banner](includes/banner.md)]

**Smíði 8.1.1035.0**

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.

## <a name="turn-off-electronic-payment-validation"></a>Slökkva á villuleit rafrænnar greiðslu

Villuleit á rafrænum greiðsluupplýsingum gerist ef þú setur upp útgjöld fyrir beingreiðslu annaðhvort í gegnum vinnusvæðið **Sjálfsafgreiðsla starfsmanns** eða beint á skjámynd starfsmanns. Þessi valkostur gefur þér sveigjanleika til að fjarlægja þessa villuleit ef þú þarft ekki á henni að halda fyrir upphæðir og afgangsgildi. Þessi eiginleiki er gagnlegur ef þú samþættar við utanaðkomandi launakerfi sem hefur mismunandi kröfur.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Sjálfsafgreiðsla stjórnanda - Bættu við markmiðum fyrir hópmeðlimi í gegnum reitinn Frammistöðumarkmið hóps

Fyrir þessa útgáfu geta stjórnendur bætt markmiðum við hvern starfsmann fyrir sig í gegnum frammistöðumarkmið sem tengjast hverjum starfsmanni. Með þessari uppfærslu geta stjórnendur fengið aðgang að reitnum **Frammistaða hóps** og búið til ný markmið með því að velja einhvern af beinum undirmönnum sínum.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Sjálfsafgreiðsla stjórnanda - Bættu við umsögnum fyrir hópmeðlimi í gegnum reitinn Umsagnir um frammistöðu hóps

Fyrir þessa útgáfu geta stjórnendur bætt umsögnum við hvern starfsmann fyrir sig í gegnum umsagnirnar sem tengjast hverjum starfsmanni. Með þessari uppfærslu geta stjórnendur fengið aðgang að reitnum **Umsagnir um frammistöðu hóps** og búið til nýjar umsagnir með því að velja einhvern af beinum undirmönnum sínum.

## <a name="configure-proration-options-by-leave-plan"></a>Stilla valkosti hlutfallsskipta eftir leyfisáætlun

Fyrirtæki gefa frí á ólíkan hátt sem byggist á því hvenær starfsmenn byrja og hætta hjá fyrirtækinu. Fyrir sum fyrirtæki er starfsmönnum veitt full úthlutun á upphafsdegi þeirra á meðan aðrir hlutfallsskipta umbuninni. Boðið er upp á nýja valkost í þessari útgáfu til að velja hvernig á að hlutfallsskipta umbun og uppsöfnun fyrir þá sem hefja og hætta störfum hjá fyrirtæki. Valkostir fela í sér: Hlutfallslega skipt, Full uppsöfnun og Engin uppsöfnun.

## <a name="other-changes"></a>Aðrar breytingar

-   Starfsmannaeining uppfærð - Nú er hægt að uppfæra titilinn **Persónulegur** með Excel-innbótinni/gagnastjórnun.

-   Öryggisbreyting svo hægt sé að fjarlægja hnappana **Eyða** og **Gera óvirkt** í sjálfsafgreiðslu á greiðsluupplýsingum starfsmanns.

## <a name="known-issue"></a>Þekkt vandamál

-   **Vandamál:** Þegar nýtt viðhengi er bætt við starfsmann eru hnapparnir **Nýtt** og **Breyta** skyggðir. **Hjáleið:** Áður en þú opnar viðhengissíðu skaltu ganga úr skugga um að FactBoxes á síðunni **Starfsmenn** séu lokaðir. Ef FactBoxes eru lokaðir þegar síðan **Starfsmenn** er hlaðið inn verða hnapparnir **Viðhengi** gerðir virkir. (Þetta vandamál verður lagað í næstu verkvangsuppfærslu.)
