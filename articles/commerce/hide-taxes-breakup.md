---
title: Fela upplýsingar um skattaskiptingu í pöntunaryfirlitum
description: Þetta efnisatriði lýsir því hvernig á að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, útskráningar-, pöntunarstaðfestingum og pöntunarupplýsingasíðum í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648134"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Fela upplýsingar um skattaskiptingu í pöntunaryfirlitum

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir því hvernig á að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, útskráningar-, pöntunarstaðfestingum og pöntunarupplýsingasíðum í Microsoft Dynamics 365 Commerce.

Sjálfgefið,Dynamics 365 Commerce sýnir upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, útskráningar-, pöntunarstaðfestingum og pöntunarupplýsingasíðum. Frá og með útgáfu Commerce útgáfu 10.0.27 inniheldur Commerce site builder valmöguleika sem gerir þér kleift að fela upplýsingar um skattaskiptingu í pöntunarsamantektum.

Eftirfarandi mynd sýnir dæmi um tvær pöntunarsamantektir. Sá fyrri sýnir upplýsingar um skattaskiptingu og sá síðari felur þær.

![Dæmi um kerrur þar sem upplýsingar um skattaskipti eru sýndar og faldar.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Möguleikinn á að fela upplýsingar um skattaskipti í pöntunaryfirlitum er aðeins tiltækur þegar **Verð eru með söluskatti** valkostur fyrir rafræn viðskiptarás er stilltur á **Já** í höfuðstöðvum verslunar, kl **Verslun og verslun \> Rásir \> Búðir \> Allar verslanir**. 
> - Sjálfgefið er **Sýna skattaskiptingu í pöntunarsamantekt** valmöguleikinn er virkur í vefsvæðisgerðinni.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Fela upplýsingar um skattaskiptingu í pöntunaryfirlitum

Fylgdu þessum skrefum til að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum.

1. Í Commerce site builder, farðu á síðuna sem þú vilt uppfæra.
1. Fara til **Vefstillingar \> Viðbætur**.
1. Hreinsaðu **Sýna skattaskiptingu í pöntunarsamantekt** gátreit.

Til að sýna upplýsingar um skattaskiptingu í pöntunaryfirlitum skaltu velja **Sýna skattaskiptingu í pöntunarsamantekt** gátreit.  

Eftirfarandi mynd sýnir **Sýna skattaskiptingu í pöntunarsamantekt** gátreiturinn auðkenndur og valinn í vefsvæðisgerð.

![Sýndu skattaskiptingu í pöntunarsamantektarvalkosti í vefsíðugerð.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit virðisaukaskatts](/finance/general-ledger/indirect-taxes-overview)

[Skilgreina söluskatt fyrir pantanir á netinu](sales-tax-config.md)

[Úrræðaleit: Skattar á netpantanir eru rangt reiknaðir](troubleshoot/tax-miscalculated-online-order.md)
