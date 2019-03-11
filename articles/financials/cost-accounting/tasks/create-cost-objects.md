---
title: 'Stofna kostnaðarhluti  '
description: Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn Dynamics 365 for Finance and Operations Enterprise Edition fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "322675"
---
# <a name="create-cost-objects"></a>Stofna kostnaðarhluti   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn Dynamics 365 for Finance and Operations Enterprise Edition fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi. USMF sýnifyrirtækið var notað til að stofna þetta ferli. Þetta ferli er fyrir eiginleika kostnaðarbókhalds sem var bætt við í Dynamics 365 for Operations 1611 útgáfu.


## <a name="create-new-cost-objects"></a>Stofna nýjar kostnaðarhluti
1. Fara í kostnaðarbókhald > Víddir > víddir kostnaðarhlutar.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.
5. Sláið inn gildi í reitnum „Lýsing“.
6. Smellið á „Vista“.

## <a name="configure-the-data-connector"></a>Stilla gagnatengi
1. Smelltu á Skilgreina víddarstakaveitu
    * Veljið CostCenter að flytja inn víddir CostCenter í kostnaðarbókhald.  
2. Í reitnum heiti víddar skal velja kostnaðarstað.
3. Smellið á „Í lagi“.

## <a name="import-cost-centers"></a>Flytja inn kostnaðarstaði
1. Smelltu á Flytja inn víddarstök.
2. Smellið á „Í lagi“.

## <a name="view-the-imported-cost-centers"></a>Skoða innflutta kostnaðarstaði
1. Smelltu á Skoða víddarstök.

