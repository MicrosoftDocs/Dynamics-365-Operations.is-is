---
title: Stofna kostnaðareiningar
description: Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841298"
---
# <a name="create-cost-elements"></a>Stofna kostnaðareiningar 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi. Þessi verklýsing sýnir hvernig stofna á kostnaðareiningum með því að flytja inn aðallykla gegnum gagnatengi. USMF sýnifyrirtækið var notað til að stofna þetta ferli. Þetta ferli er fyrir eiginleika kostnaðarbókhalds sem var bætt við í Dynamics 365 for Operations 1611 útgáfu.


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

