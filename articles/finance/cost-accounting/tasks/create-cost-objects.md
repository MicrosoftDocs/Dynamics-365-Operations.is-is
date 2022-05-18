---
title: Stofna kostnaðarhluti
description: Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734131"
---
# <a name="create-cost-objects"></a>Stofna kostnaðarhluti 

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi. USMF sýnifyrirtækið var notað til að stofna þetta ferli. 


## <a name="create-new-cost-objects"></a>Stofna nýjar kostnaðarhluti
1. Fara til **Kostnaðarbókhald > Víddir > Mál kostnaðarhluta**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Heiti** skal slá inn gildi.
4. Í **Gagnatengi fyrir víddarmeðlimi** reit, sláðu inn eða veldu gildi.
5. Í reitinn **Lýsing** skal slá inn gildi.
6. Smelltu á **Vista**.

## <a name="configure-the-data-connector"></a>Stilla gagnatengi
1. Smellur **Stilla víddarmeðlimaveitu**.
    * Veljið CostCenter að flytja inn víddir CostCenter í kostnaðarbókhald.  
2. Í **Nafn víddar** reit, veldu Kostnaðarstað.
3. Smellt er á **OK**.

## <a name="import-cost-centers"></a>Flytja inn kostnaðarstaði
1. Smellur **Flytja inn víddarmeðlimi**.
2. Smellt er á **OK**.

## <a name="view-the-imported-cost-centers"></a>Skoða innflutta kostnaðarstaði
1. Smellur **Skoða víddarmeðlimi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
