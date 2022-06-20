---
title: Tilbúið til greiðslu
description: Þessi grein sýnir hvernig á að merkja starfsmann sem tilbúinn til að greiða inn Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 81c73584e3567d620292227ce4a24c3c0945fa96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862860"
---
# <a name="ready-to-pay"></a>Tilbúið til greiðslu


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> Ef merkja á að starfsmaður sé tilbúinn til greiðslu verður fyrst að virkja virknina **(Forskoðun) Samþætting launa** í eiginleikastjórnun. Frekari upplýsingar um hvernig forskoðunareiginleikar eru virkjaðir er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).

Þessi eiginleiki gerir fagfólki í mannauðsmálum kleift að skilja hvaða starfsmenn eru tilbúnir undir launavinnslu og hvar aðgerða er þörf áður en launagreiðandi þriðja aðila notar þá.

## <a name="mark-employee-as-ready-to-pay"></a>Merkja starfsmann sem er tilbúinn fyrir launagreiðslur

Að safna saman og staðfesta upplýsingar starfsmanns getur reynst tímafrekt og villur koma gjarnan upp. Með því að bjóða upp á leið fyrir fagfólk í mannauðsmálum til að yfirfara og uppfæra upplýsingar um starfsmenn á auðveldan hátt, hjálpar Dynamics 365 Human Resources til við að minnka tímann sem fer í að undirbúa launavinnslu.

Að merkja starfsmann sem tilbúinn fyrir launagreiðslur:

1. Opnaðu **Launastjórnun**. Tveir reitir eru á vinnusvæðinu: 
    - **Starfsfólk tilbúið til greiðslu**
    - **Starfsfólk ekki tilbúið til greiðslu**
    ![Vinnusvæði launastjórnunar.](./media/hr-ready-to-pay-1-workspace.png)

2. Veldu reitinn **Starfsfólk ekki tilbúið til greiðslu**.

3. Veldu starfsmenn sem á að villuleita. Í **Launaflipanum**, í flokknum **Tilbúið til greiðslu**, skal velja **Villuleita**.
    ![Villuleita starfsmenn.](./media/hr-ready-to-pay-2-validate.png)

4. Til að yfirfara niðurstöðurnar í **Launaflipanum**, í flokknum **Tilbúið til greiðslu**, skal velja **Niðurstöður**.

## <a name="validation"></a>Villuleit

Áður en starfsmaður er merktur sem reiðubúinn til að greiða verður staðfest hvort prófíll starfsmanns sé fullkláraður.

![Villuleita niðurstöður.](./media/hr-ready-to-pay-3-results.png)

| Villuleit | Upplýsingar |
| --- | --- |
| **Færibreyta tilgangs aðseturs** | Staðfestir að færibreytan **Nota tilgang aðseturs launaskráar** sé valin. |
| **Aðsetur launaskráar** | Sannprófar hvort notandaupplýsingar starfsmanns séu með a.m.k. eitt aðsetur með tilganginum **Búseta fyrir launaskrá** eða **Vinnustaðsetning fyrir launaskrá** og að aðeins eitt aðsetur er á hvern tilgang. |
| **Ráðning** | Staðfestir hvort starfsmaðurinn sé með að minnsta kosti eitt starf (núverandi, áður eða fram í tímann). |
| **Auðkennisnúmer** | Staðfestir að reiturinn **Nota auðkennisgerðir í launavinnslu** sé **Já** á síðunni **Færibreytur Human Resources** og hvort auðkennisgerðin sem gefin er upp í færibreytunni sé fyllt út í prófíl starfsmanns. |
| **Fornafn og eftirnafn** | Staðfestir að reitirnir **Fornafn** og **Eftirnafn** séu fylltir út.|
| **Staða** | Staðfestir hvort starfsmaðurinn hafi úthlutaða stöðu. |
| **Fæðingardagur** | Staðfestir að reiturinn **Fæðingardagur** sé útfylltur. |
| **Laun** | Staðfestir hvort starfsmaðurinn sé skráður í launafyrirkomulag fastra launa. |

Ef ein þessara staðfestinga stenst ekki getur þú ekki merkt að starfsmaðurinn sé tilbúinn til að fá greiðslu.

Ef reiturinn **Tilbúið til greiðslu** er **Nei** er það vísbending um að þú þurfir að framkvæma aðgerð til að tryggja að lokið sé við notandasíðu starfsmanns. Þetta stöðvar ekki afhjúpun gagna í gagnaeiningum. 

## <a name="process-automation"></a>Sjálfvirkni ferlis

Þú getur gert staðfestingu allra starfsmanna sjálfvirka með því að nota [Sjálfvirkni ferlis](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation). Í vinnusvæðinu **Launastjórnun** skal fara í **Tenglar** \> **Færibreytur** \> **Sjálfvirkni ferlis**.

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
