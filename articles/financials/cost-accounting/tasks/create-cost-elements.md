--- 
title: "Stofna kostnaðareiningar  "
description: "Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e665fc53455e457a2488f4ec28ebb5b715d90eb
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-elements"></a>Stofna kostnaðareiningar   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi. Þessi verklýsing sýnir hvernig stofna á kostnaðareiningum með því að flytja inn aðallykla gegnum gagnatengi. USMF sýnifyrirtækið var notað til að stofna þetta ferli. Þetta ferli er fyrir Kostnaðarbókhald eiginleika sem var bætt við í Dynamics 365 for Operations útgáfu 1611.


## <a name="create-new-cost-elements"></a>Stofna nýtt kostnaðareiningar
1. Fara í kostnaðarbókhald > Víddir > Víddir kostnaðareininga.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.
5. Sláið inn gildi í reitnum „Lýsing“.
6. Smellið á „Vista“.

## <a name="configure-the-data-connector"></a>Stilla gagnatengi
1. Smelltu á Skilgreina víddarstakaveitu
2. Sláið inn eða veljið gildi í reitnum Bókhaldslykill.
    * Velja samnýtt til að nota samnýttar bókhaldslykla.  
3. Smellið á „Nýtt“.
4. Í listanum skal merkja valda línu.
    * Hægt er að nota síur á lykla sem uppfylla skilyrðin.  
5. Sláið inn eða veljið gildi í reitnum úr aðallykli.
6. Sláið inn eða veljið gildi í reitnum Til aðallykils.
7. Smellið á „Í lagi“.

## <a name="import-main-accounts"></a>Flytja inn aðallykla
1. Smelltu á Flytja inn víddarstök.
    * Aðallyklar verða fluttir inn í kostnaðarbókhald og notað sem kostnaðareiningar.  
2. Smellið á „Í lagi“.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Skoða innflutta lykla sem kostnaðareiningar
1. Smelltu á Skoða víddarstök.
    * Lítið á innflutt fjárhagslykla sem kostnaðareiningar í fyrirtækinu sem kostnaður getur streymt inn í.  


