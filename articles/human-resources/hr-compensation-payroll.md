---
title: Tilbúið til greiðslu
description: Í þessu efnisatriði er sýnt hvernig á að merkja starfsmann sem tilbúinn til greiðslu í Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/13/2020
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
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70b3f31db459fe021caf08fe09b2e44a597294d1992ee16a69efd8745941a4bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732418"
---
# <a name="ready-to-pay"></a>Tilbúið til greiðslu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Ef merkja á að starfsmaður sé tilbúinn til greiðslu verður fyrst að virkja virknina **(Forskoðun) Samþætting launa** í eiginleikastjórnun. Frekari upplýsingar um hvernig forskoðunareiginleikar eru virkjaðir er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).

Þessi eiginleiki gerir fagfólki í mannauðsmálum kleift að skilja hvaða starfsmenn eru tilbúnir undir launavinnslu og hvar aðgerða er þörf áður en launagreiðandi þriðja aðila notar þá.

## <a name="mark-employee-as-ready-to-pay"></a>Merkja starfsmann sem er tilbúinn fyrir launagreiðslur

Að safna saman og staðfesta upplýsingar starfsmanns getur reynst tímafrekt og villur koma gjarnan upp. Með því að bjóða upp á leið fyrir fagfólk í mannauðsmálum til að yfirfara og uppfæra upplýsingar um starfsmenn á auðveldan hátt, hjálpar Dynamics 365 Human Resources til við að minnka tímann sem fer í að undirbúa launavinnslu.

Að merkja starfsmann sem tilbúinn fyrir launagreiðslur:

1. Opnaðu **Launastjórnun**. Tveir reitir eru á vinnusvæðinu 
    - **Starfsfólk tilbúið til greiðslu**
    - **Starfsfólk ekki tilbúið til greiðslu**
    ![Vinnusvæði launastjórnunar.](./media/hr-ready-to-pay-1-workspace.png)

2. Veldu reitinn **Starfsfólk ekki tilbúið til greiðslu**.

3. Veldu starfsmenn sem á að villuleita. Í **Launaflipanum**, í flokknum **Tilbúið til greiðslu**, skal velja **Villuleita**.
    ![Villuleita starfsmenn.](./media/hr-ready-to-pay-2-validate.png)

4. Til að yfirfara niðurstöðurnar í **Launaflipanum**, í flokknum **Tilbúið til greiðslu**, skal velja **Niðurstöður**.

## <a name="validation"></a>Villuleit

Áður en starfsmaður er merktur sem tilbúinn til að greiða mun kerfið gera einfalda villuleit á því hvort notandaupplýsingar séu fullnægjandi.

![Villuleita niðurstöður.](./media/hr-ready-to-pay-3-results.png)

Eftirfarandi tafla veitir upplýsingar um allar villuleitir sem eru framkvæmdar. 

| Villuleit | Upplýsingar |
| --- | --- |
| Færibreyta tilgangs aðseturs | Sannprófar hvort kveikt sé á færibreytunni **Nota tilgang aðseturs launaskráar**. |
| Aðsetur launaskráar | Sannprófar hvort notandaupplýsingar starfsmanns séu með a.m.k. eitt aðsetur með tilganginum „Búseta fyrir launaskrá“ eða „Vinnustaðsetning fyrir launaskrá“ og að aðeins eitt aðsetur er á hvern tilgang. |
| Ráðning | Staðfestir hvort starfsmaðurinn sé með að minnsta kosti eitt starf (núverandi, áður eða fram í tímann). |
| Auðkennisnúmer | Staðfestir hvort færibreytan „Nota auðkennisgerðir í launavinnslu“ sé já og hvort gerð auðkennis sem gefin er upp í færibreytunni sé útfyllt í notandasíðu starfsmanns. |
| Fornafn og eftirnafn | Staðfestir hvort notandasíða starfsmanns sé gild, athugar hvort reitirnir **Heiti** og **Eftirnafn** sé fyllt út.|
| Staða | Staðfestu hvort starfsmaðurinn hafi úthlutaða stöðu. |
| Fæðingardagur | Staðfestir hvort notandasíða starfsmanns sé gild, athugar hvort reiturinn **Fæðingardagur** sé útfylltur. |
| Laun | Staðfestu hvort starfsmaðurinn sé skráður í launafyrirkomulag fastra launa. |

Ef ein þessara staðfestinga stenst ekki getur þú ekki merkt að starfsmaðurinn sé tilbúinn til að fá greiðslu.

Ef reiturinn **Tilbúið til greiðslu** er **Nei** er það vísbending um að þú þurfir að framkvæma aðgerð til að tryggja að lokið sé við notandasíðu starfsmanns. Þetta stöðvar ekki afhjúpun gagna í gagnaeiningum. 

## <a name="known-issues"></a>Þekkt vandamál

- Þú verður að slökkva á **Einfaldaðri starfsmannafærslu** í eiginleikastjórnun. Reitirnir á vinnusvæði launastjórnunar virka ekki sem skyldi ef þú notar þennan eiginleika.
- Í skjámynd starfsmanns er **Launaflipinn**, flokkurinn **Tilbúið til greiðslu** tiltækt í hvaða notandahlutverki sem er. 

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
