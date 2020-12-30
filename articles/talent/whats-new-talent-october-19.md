---
title: Nýjungar eða breytingar í Dynamics 365 Talent - Core HR (16. október 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461492"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Nýjungar eða breytingar í Dynamics 365 Talent - Core HR (16. október 2018)

**Smíði 8.1.1067**

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.

## <a name="allow-managers-to-update-time-off-requests"></a>Leyfa stjórnendum að uppfæra beiðnir um frí

Hugsanlega verður að uppfæra beiðnir um frí frá starfsmönnum þegar þeir eru samþykktir í gegnum vinnuflæði. Í mörgum tilvikum framkvæmir stjórnandi þessar uppfærslur fyrir hönd starfsmannsins. Þessi nýi eiginleiki veitir stjórnendum kleift að uppfæra beiðnir um frí eða hætta við beiðnir um frí fyrir hönd starfsmanna sinna. Þessum eiginleika er stjórnað af **Störf fyrir hönd annarra** færibreytu sem hægt er að stilla á **Mannauðsfæribreytum** síðu. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>Leyfa mannauði að uppfæra beiðnir um frí

Líkt og eiginleikinn hér að framan, kann mannauður að þurfa að uppfæra beiðnir starfsmanna um frí eftir að þær hafa verið samþykktar í gegnum vinnuflæði. Þessi eiginleiki gerir mannauðsnotendum kleift að uppfæra beiðnir um frí. Eiginleikinn er virkjaður í **Starfsfólk** vinnumiðstöðinni og á **Starfskraftur** síðunni, með nýjum valkosti sem heitir **Skoða frí**. Á þessum síðum geta mannauðsnotendur skoðað beiðnir og uppfært beiðnir um frí, svipað og hvernig stjórnendur geta framkvæmt þessar aðgerðir.

Öryggisskyldan sem stjórnar aðgangi að þessari virkni er:
- Skylda: Vinna með leyfis- og fjarvistaferla tiltekinna starfsmanna.
- Réttindi: Vinna með leyfis- og fjarvistabeiðnir fyrir allt starfsfólk.

## <a name="other-changes"></a>Aðrar breytingar
Eftirfarandi uppfærslur hafa verið gerðar í þessari útgáfu:
- Breytingar á aðgerðum starfsmannaráðninga þannig að þeir séu ekki lengur „fastir“ í **Verkflæði lokið** ástandi.
- Starfsferilsskrá er nú hægt að búa til án upphafsdags atvinnu.
- Dynamics 365 Talent skráningardegi fyrir námskeið sem er sýnt í sjálfsafgreiðslusíðum starfsmanna gildir nú tímabeltið á móti þeim degi.
- Excel-skrár geta verið fluttar inn mörgum sinnum villulaust með **Starfsmannaeiningu**.

## <a name="known-issue"></a>Þekkt vandamál

- **Vandamál**: Þegar nýtt viðhengi er bætt við starfsmann eru hnapparnir **Nýtt** og **Breyta** skyggðir. 
- **Hjáleið:** Áður en þú opnar viðhengissíðu skaltu ganga úr skugga um að FactBoxes á síðunni **Starfsmenn** séu lokaðir. Ef upplýsingareitirnir eru lokaðir þegar síðan **Starfskraftar** er hlaðið inn verða viðhengishnapparnir gerðir virkir. (Þetta vandamál verður lagað í næstu verkvangsuppfærslu.)
