---
title: Stofna kostnaðareiningar
description: Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779690"
---
# <a name="create-cost-elements"></a>Stofna kostnaðareiningar 

[!include [banner](../../includes/banner.md)]

Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi. Þessi verklýsing sýnir hvernig stofna á kostnaðareiningum með því að flytja inn aðallykla gegnum gagnatengi. USMF sýnifyrirtækið var notað til að stofna þetta ferli. Þetta ferli er fyrir eiginleika kostnaðarbókhalds sem var bætt við í Dynamics 365 for Operations 1611 útgáfu.


## <a name="create-new-cost-elements"></a>Stofna nýtt kostnaðareiningar
1. Fara til **Kostnaðarbókhald > Víddir > Víddir kostnaðarþáttar**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Heiti** skal slá inn gildi.
4. Í **Gagnatengi fyrir víddarmeðlimi** reit, sláðu inn eða veldu gildi.
5. Í reitinn **Lýsing** skal slá inn gildi.
6. Smelltu á **Vista**.

## <a name="configure-the-data-connector"></a>Stilla gagnatengi
1. Smellur **Stilla víddarmeðlimaveitu**.
2. Í **Reikningsyfirlit** reit, sláðu inn eða veldu gildi.
    * Veldu **Deilt** að nota sameiginlega reikningsyfirlitið.  
3. Smellt er á **Nýtt**.
4. Í listanum skal merkja valda línu.
    * Hægt er að nota síur á lykla sem uppfylla skilyrðin.  
5. Í **Af aðalreikningi** reit, sláðu inn eða veldu gildi.
6. Í **Að aðalreikningi** reit, sláðu inn eða veldu gildi.
7. Smellt er á **OK**.

## <a name="import-main-accounts"></a>Flytja inn aðallykla
1. Smellur **Flytja inn víddarmeðlimi**.
    * Aðallyklar verða fluttir inn í kostnaðarbókhald og notað sem kostnaðareiningar.  
2. Smellt er á **OK**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Skoða innflutta lykla sem kostnaðareiningar
1. Smellur **Skoða víddarmeðlimi**.
    * Lítið á innflutt fjárhagslykla sem kostnaðareiningar í fyrirtækinu sem kostnaður getur streymt inn í.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
