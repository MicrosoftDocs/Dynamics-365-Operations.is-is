---
title: Fela upplýsingar um skattskil í samantektum pantana
description: Þessi grein lýsir því hvernig á að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, útskráningar-, pöntunarstaðfestingum og pöntunarupplýsingasíðum í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 669534a6611860ac73439460afedce341310cc7d
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027336"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Fela upplýsingar um skattskil í samantektum pantana

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, útskráningar-, pöntunarstaðfestingum og pöntunarupplýsingasíðum í Microsoft Dynamics 365 Commerce.

Sjálfgefið,Dynamics 365 Commerce sýnir upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, kassa-, pöntunarstaðfestingum og pöntunarupplýsingasíðum. Frá og með útgáfu Commerce útgáfu 10.0.27 inniheldur Commerce site builder valmöguleika sem gerir þér kleift að fela upplýsingar um skattaskiptingu í pöntunarsamantektum.

Eftirfarandi mynd sýnir dæmi um tvær pöntunarsamantektir. Sá fyrri sýnir upplýsingar um skattaskiptingu og sá síðari felur þær.

![Dæmi um kerrur þar sem upplýsingar um skattaskipti eru sýndar og faldar.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Möguleikinn á að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum er aðeins tiltækur þegar **Verð eru með söluskatti** valkostur fyrir rafræn viðskiptarás er stilltur á **Já** í höfuðstöðvum verslunar, kl **Verslun og verslun \> Rásir \> Búðir \> Allar verslanir**. 
> - Sjálfgefið er **Sýna skattaskiptingu í pöntunarsamantekt** valmöguleikinn er virkur í vefsmiði.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Fela upplýsingar um skattskil í samantektum pantana

Fylgdu þessum skrefum til að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum.

1. Í Commerce site builder, farðu á síðuna sem þú vilt uppfæra.
1. Fara til **Vefstillingar \> Viðbætur**.
1. Hreinsaðu **Sýna skattaskiptingu í pöntunarsamantekt** gátreit.

Til að sýna upplýsingar um skattaskiptingu í pöntunarsamantektum skaltu velja **Sýna skattaskiptingu í pöntunarsamantekt** gátreit.  

Eftirfarandi mynd sýnir **Sýna skattaskiptingu í pöntunarsamantekt** gátreiturinn auðkenndur og valinn í vefsvæðisgerð.

![Sýna skattaskiptingu í pöntunarsamantektarvalkosti í vefsíðugerð.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

> [!NOTE]
> Ef þú ert með sérsniðnar pöntunarsamantektareiningar og vilt ekki erfa virknina „fela skattaupplýsingarnar í pöntunarsamantektum“ í Commerce útgáfu 10.0.27 eða nýrri, sjáðu [Samtala pöntunarsamantektar inniheldur ekki skatta á gjöld þegar sérsniðnar pöntunarsamantektareiningar eru notaðar](troubleshoot/summary-taxes-custom-modules-10.0.27.md#resolution).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit virðisaukaskatts](/finance/general-ledger/indirect-taxes-overview)

[Skilgreina söluskatt fyrir pantanir á netinu](sales-tax-config.md)

[Úrræðaleit: Skattar á netpantanir eru rangt reiknaðir](troubleshoot/tax-miscalculated-online-order.md)
