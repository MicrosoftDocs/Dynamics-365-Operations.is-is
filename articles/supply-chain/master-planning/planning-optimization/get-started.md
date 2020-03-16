---
title: Byrjaðu með hagræðingu skipulags
description: Þetta efnisatriði útskýrir hvernig skuli hefja notkun á virkninni Fínstilling skipulagningar.
author: ChristianRytt
manager: AnnBe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e64699005387adcc92e2e7c9fefad68a9de85c0
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076133"
---
# <a name="get-started-with-planning-optimization"></a>Byrjaðu með hagræðingu skipulags

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Virkni fínstillingar áætlunar styður ekki eins og er alla þá eiginleika sem eru fáanlegir í áætlunarvélinni sem er innbyggð í Microsoft Dynamics 365 Supply Chain Management. Þess vegna er mikilvægt að þú metir hvort eiginleikasettið sem nú er fáanlegt í fínstillingu skipulagsins uppfylli kröfur þínar. Sjálfgefið er að ekki er kveikt á virkni fínstillingar skipulagningar í Dynamics Lifecycle Services (LCS). Þess vegna hefurðu tækifæri til að gera úttektina áður en kveikt er á henni.

Að lokum mun fínstilling skipulagningar koma í stað núverandi innbyggðrar áætlunarvélar Supply Chain Management.

Áður en þú kveikir á fínstillingu skipulags mælum við eindregið með því að þú metir niðurstöður greiningar á fínstillingu skipulagningar. Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Leyfisveiting

Ef þú getur keyrt aðalskipulagningu með því að nota núverandi leyfi þitt þarftu ekki að kaupa viðbótarleyfi til að byrja að nota fínstillingu skipulagsins.

### <a name="install-the-add-in"></a>Setja upp innbótina

Til að nota fínstillingu skipulagningar skaltu setja upp innbótina fínstilling skipulagningar fyrir Dynamics 365 Supply Chain Management. Þú getur fengið aðgang að viðbótinni frá LCS verkinu og kveikt á virkni fínstillingar skipulagningar úr notendaviðmóti (UI) Supply Chain Management.

> [!NOTE]
> Krafan um fínstillingu áætlanagerðar er LCS-virkjað umhverfi með miklu framboði (ekki OneBox-umhverfi) með Dynamics 365 Supply Chain Management útgáfa 10.0.7 eða nýrri.

1. Skráðu þig inn á LCS og opnaðu viðkomandi umhverfi.
1. Farðu í **Fullar upplýsingar**.
1. Flettu niður að flýtiflipanum **Umhverfisinnbætur**.
1. Veldu **Setja upp nýja innbót**.
1. Veldu **Fínstillingu skipulagningar**.
1. Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.
1. Velja **Setja upp**.
1. Á flýtiflipanum **Umhverfisviðbætur** ættir þú að sjá að hagræðing skipulags er að setja upp.
1. Eftir nokkrar mínútur ætti **Setur upp** að breytast í **Uppsett** (þú gætir þurft að endurnýja síðuna). Þegar það er sett upp ertu tilbúinn til að virkja hagræðingu skipulags í Dynamics 365 Supply Chain Management.

### <a name="planning-optimization-integration"></a>Samþætting fínstillingar skipulagningar

Til að stilla hvort nota eigi innbótina fínstilling skipulagningara fyrir aðaláætlanagerð, farðu í **Aðaláætlanargerð** \> **Uppsetning** \> **Færibreytur fínstillingar skipulagningar**.

#### <a name="connection-status"></a>Staða tengingar

Staða tengingarinnar gefur til kynna núverandi stöðu tengingarinnar milli Supply Chain Management og þjónustunnar Fínstilling skipulagningar. Eftirfarandi tafla sýnir hugsanleg gildi.

| Staða tengingar | Lýsing | Er hægt að nota fínstillingu skipulagningar? |
|---|---|---|
| Tengt | Tengingu hafa verið komið á milli þjónustunnar fínstilling skipulagningar og Supply Chain Management. | Já |
| Tengir | Nú stendur yfir beiðni um að kveikja á tengingunni við þjónustuna fínstilling skipulagningar. | Nr |
| Aftengt | Engin tenging er við þjónustuna fínstilling skipulagningar. Hægt er að kveikja á tengingunni úr LCS, eins og lýst er fyrr í þessu efni. | Nr |
| Aftengir | Nú stendur yfir beiðni um að slökkva á tengingunni við þjónustuna fínstilling skipulagningar. | Nr |
| Sækir stöðu | Kerfið bíður eftir stöðuupplýsingum úr þjónustunni fínstilling skipulagningar. | Nr |

#### <a name="the-use-planning-optimization-option"></a>Valkosturinn Nota fínstillingu skipulagningar

Stilling á valkostinum **Nota fínstillingu skipulags** ákvarðar hvaða áætlunarvél er notuð við aðaláætlanagerð:

- **Já** - Fínstilling skipulags er notuð við aðaláætlungargerð.
- **Nei** - Innbyggða áætlunarvélin Supply Chain Management er notuð til aðaláætlunargerðar.

> [!NOTE]
> Ef fyrirliggjandi runuvinnslur áætlunargerðar sem voru stofnuð fyrir innbyggðu áætlunarvélina Supply Chain Management eru sett af stað á meðan valkosturinn **Nota fínstillingu skipulagningar** er stilltur á **Já** munu þær vinnslur ekki takast.

### <a name="integration-with-the-setup"></a>Samþætting við uppsetninguna

Ef kveikt er á forskoðun fínstillingar skipulags er aðaláætlunargerð gerð með því að nota viðbótaráætlun fyrir fínstillingu skipulags. Í þessu tilfelli verða niðurstöður og eiginleikar aðaláætlunargerðar fyrir áhrifum.

## <a name="related-resources"></a>Tengd tilföng

[Ákvæði og skilmálar fyrir forskoðunina](https://go.microsoft.com/fwlink/?linkid=2015274)

[Yfirlit yfir fínstillingu skipulagningar](planning-optimization-overview.md)

[Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Nota síur á áætlun](plan-filters.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)
