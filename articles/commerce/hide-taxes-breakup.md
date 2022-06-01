---
title: Fela upplýsingar um skattskil í samantektum pantana
description: Þetta efnisatriði lýsir því hvernig á að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, útskráningar-, pöntunarstaðfestingum og pöntunarupplýsingasíðum í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9a0bff7afaa10e49ec05f18e2b0fae7a19b5e8af
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767815"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Fela upplýsingar um skattskil í samantektum pantana

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir því hvernig á að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, útskráningar-, pöntunarstaðfestingum og pöntunarupplýsingasíðum í Microsoft Dynamics 365 Commerce.

Sjálfgefið,Dynamics 365 Commerce sýnir upplýsingar um skattaskiptingu í pöntunaryfirlitum á körfu-, útskráningar-, pöntunarstaðfestingum og pöntunarupplýsingasíðum. Frá og með útgáfu Commerce útgáfu 10.0.27, inniheldur Commerce site builder valmöguleika sem gerir þér kleift að fela upplýsingar um skattaskiptingu í pöntunarsamantektum.

Eftirfarandi mynd sýnir dæmi um tvær pöntunarsamantektir. Sá fyrri sýnir upplýsingar um skattaskiptingu og sá síðari felur þær.

![Dæmi um kerrur þar sem upplýsingar um skattaskipti eru sýndar og faldar.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Möguleikinn á að fela upplýsingar um skattaskipti í pöntunaryfirlitum er aðeins tiltækur þegar **Verð eru með söluskatti** valkostur fyrir rafræn viðskiptarás er stilltur á **Já** í höfuðstöðvum verslunar, kl **Verslun og verslun \> Rásir \> Búðir \> Allar verslanir**. 
> - Sjálfgefið er **Sýna skattaskiptingu í pöntunarsamantekt** valmöguleikinn er virkjaður í Site Builder.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Fela upplýsingar um skattskil í samantektum pantana

Fylgdu þessum skrefum til að fela upplýsingar um skattaskiptingu í pöntunaryfirlitum.

1. Í Commerce site builder, farðu á síðuna sem þú vilt uppfæra.
1. Fara til **Vefstillingar \> Viðbætur**.
1. Hreinsaðu **Sýna skattaskiptingu í pöntunarsamantekt** gátreit.

Til að sýna upplýsingar um skattaskiptingu í pöntunaryfirlitum skaltu velja **Sýna skattaskiptingu í pöntunarsamantekt** gátreit.  

Eftirfarandi mynd sýnir **Sýna skattaskiptingu í pöntunarsamantekt** gátreiturinn auðkenndur og valinn í vefsvæðisgerð.

![Sýndu skattaskiptingu í pöntunarsamantektarvalkosti í vefsíðugerð.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

> [!NOTE]
> Ef þú ert með sérsniðnar pöntunarsamantektareiningar og vilt ekki erfa virknina „fela skattaupplýsingarnar í pöntunaryfirlitum“ í Commerce útgáfu 10.0.27 eða nýrri, sjáðu [Samtala pöntunarsamantektar inniheldur ekki skatta á gjöld þegar sérsniðnar pöntunarsamantektareiningar eru notaðar](troubleshoot/summary-taxes-custom-modules-10.0.27.md#resolution).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit virðisaukaskatts](/finance/general-ledger/indirect-taxes-overview)

[Skilgreina söluskatt fyrir pantanir á netinu](sales-tax-config.md)

[Úrræðaleit: Skattar á netpantanir eru rangt reiknaðir](troubleshoot/tax-miscalculated-online-order.md)
