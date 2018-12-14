---
title: "Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (27. september 2018)"
description: "Í þessu efnisatriði er lýst nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 48e2eea2cc986edc49d5192945c3d913c3bb9756
ms.openlocfilehash: 6bd049bfe4639136276ab2f14e6310e45d1254f2
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a>Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (27. september 2018)

[!include [banner](includes/banner.md)]

**Smíði 8.1.2064**

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.


## <a name="changes"></a>Breytingar

### <a name="unable-to-create-a-note-in-case-management"></a>Ekki er hægt að búa til athugasemd í Málastjórnun

Breyting hefur verið gerð út af vandamáli þegar reynt var að breyta eða búa til athugasemd í málskladda Málastjórnunar.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Misritað orð á greiningarflipanum á vinnusvæði launa 

Breyting hefur verið gerð til að leiðrétta stafsetningu á „Ethnic Origin“ í myndriti launagreininga á vinnusvæði launa.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Vinnusvæði fyrir sjálfsafgreiðslu starfsmanns birtist ekki þegar notanda er ekki úthlutað á starfskraft 

Breyting hefur verið gerð þegar vinnusvæðið **Sjálfsafgreiðsla starfsmanns** er valið sem upphafssíða við ræsingu fyrir notanda sem ekki er úthlutaður á starfskraft. Í þessar aðstæður birtist sjálfgefna yfirlitið.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Leyfis-og fjarvistarvilla: Tilvísun hlutar ekki stillt á tilvik hlutar

Breytingar hafa verið gerðar á leyfi og fjarvistum til að leiðrétta þessa villu eftir samþykki á leyfis- og fjarvistarfærslum í listanum **Vinnuliðum úthlutað á mig**.

### <a name="unable-to-recall-an-image-workflow"></a>Ekki er hægt að afturkalla verkflæði myndar

Eftir afturköllun á verkflæði myndar verður verkflæðið stillt á „hætt við“ og hægt er að eyða núverandi beiðni á vinnusvæði fyrir sjálfsafgreiðslu starfsmanns.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Endurráðnir starfsmenn eða verktakar koma upp mörgum sinnum eftir starfslok 

Með þessari uppfærslu birtast starfsmenn, sem lokið hafa störfum en eru endurráðnir, aðeins einu sinni í listanum yfir hætta starfsmenn. 

## <a name="known-issue"></a>Þekkt vandamál

- **Vandamál**: Þegar nýtt viðhengi er bætt við starfsmann eru hnapparnir **Nýtt** og **Breyta** skyggðir. 
- **Hjáleið:** Áður en þú opnar viðhengissíðu skaltu ganga úr skugga um að FactBoxes á síðunni **Starfsmenn** séu lokaðir. Ef upplýsingareitirnir eru lokaðir þegar síðan **Starfskraftar** er hlaðið inn verða viðhengishnapparnir gerðir virkir. (Þetta vandamál verður lagað í næstu verkvangsuppfærslu.)

