---
title: Flytja einkunnir og umsagnir inn og út
description: Þessi grein lýsir því hvernig á að flytja inn og flytja vörueinkunnir og umsagnir í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271936"
---
# <a name="import-and-export-ratings-and-reviews"></a>Flytja einkunnir og umsagnir inn og út

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að flytja inn og flytja vörueinkunnir og umsagnir í Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce tilboð [einkunnir og umsagnir](ratings-reviews-overview.md) sem alhliða lausn. Þegar þú skiptir yfir í Dynamics 365 Commerce einkunna- og umsagnarlausn, gætirðu viljað færa núverandi einkunna- og umsagnargögn yfir á viðskiptavettvanginn. Þú gætir líka viljað flytja út einkunna- og umsagnargögn frá Commerce, byggt á viðskiptaþörfum þínum. A Power Automate tengi gerir þér kleift að flytja einkunnir og umsagnir inn í Commerce og flytja þær út úr Commerce.

> [!NOTE]
> Fyrir upplýsingar um hvernig á að hefjast handa með rökfræðiflæði inn Power Automate, sjá [Búðu til skýflæði í Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Forkröfur

Áður en þú getur flutt inn og flutt út einkunnir og umsagnir þarftu að uppfylla eftirfarandi skilyrði:

- Einkunna- og endurskoðunarlausnin verður að vera virkjuð fyrir netviðskiptasíðuna þína á Commerce pallinum. Fyrir frekari upplýsingar, sjá [Veldu að nota einkunnir og umsagnir](opt-in-ratings-reviews.md).
- Dynamics 365 Ratings and Review Power App Connector verður að vera stilltur til að virkja annað hvort „senda umsagnir“ eða „flytja út umsagnir“ aðgerðir í Power Automate. Fyrir frekari upplýsingar, sjá [Dynamics 365 Commerce - Einkunnir og umsagnir (Forskoðun)](/connectors/dynamics365ratingsre/).
- Þjónustu-til-þjónustu (S2S) auðkenning verður að vera stillt til að hringja á öruggan hátt í einkunnir og endurskoðun forritunarviðmóts (API) utan viðskipta. Fyrir frekari upplýsingar, sjá [Stilla þjónustu-til-þjónustu auðkenningu](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Flytja inn einkunnir og umsagnir

Til að flytja einkunna- og umsagnargögn úr núverandi kerfi inn í Commerce þarftu að bæta við Dynamics 365 Ratings and Review Power Automate tengi við annað hvort núverandi Power Automate flæði eða nýtt. Fyrir frekari upplýsingar, sjá [Dynamics 365 Commerce - Einkunnir og umsagnir (Forskoðun)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> Áður en þú lýkur þessari aðferð verður þú [stilla S2S auðkenningu](service-to-service-auth.md).

Til að flytja einkunnir og umsagnir inn í Commerce með því að nota Dynamics 365 Ratings and Review Power Automate tengi skaltu fylgja þessum skrefum.

1. Veldu **Sendu umsögn notenda** aðgerð.
1. Komdu á tengingu með því að nota Azure Active Directory (Azure AD) forritaupplýsingar sem voru búnar til þegar þú stilltir S2S auðkenningu. Fyrir frekari upplýsingar, sjá [Stilla þjónustu-til-þjónustu auðkenningu](service-to-service-auth.md).
1. The **Sendu umsögn notenda** aðgerð tekur eina endurskoðun í einu. Þess vegna skaltu endurtaka aðgerðina. Notaðu heimildarumsagnirnar sem lista til að senda inn magndóma.
    
## <a name="export-ratings-and-reviews"></a>Flytja út einkunnir og umsagnir

Til að flytja út einkunna- og umsagnargögn frá Commerce verður þú að bæta Dynamics 365 Ratings og Review Power Automate tengi við annað hvort núverandi Power Automate flæði eða nýtt. Fyrir frekari upplýsingar, sjá [Dynamics 365 Commerce - Einkunnir og umsagnir (Forskoðun)](/connectors/dynamics365ratingsre/).

Til að flytja út einkunnir og umsagnir frá Commerce með því að nota Dynamics 365 Ratings and Review Power Automate tengi skaltu fylgja þessum skrefum.

1. Veldu **Flytja út allar umsagnir** aðgerð.
1. Ljúktu við aðgerðina. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Velja að nota einkunnir og umsagnir](opt-in-ratings-reviews.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Skilgreina einkunnir og umsagnir](configure-ratings-reviews.md)

[Samstilla afurðaeinkunnagjöf](sync-product-ratings.md)

[Virkja handvirka birtingu einkunna og umsagna hjá stjórnanda](manual-publish-rating-reviews.md)

[Stilla sannvottun milli þjónusta](service-to-service-auth.md)

[Algengar spurningar um einkunnir og umsagnir](ratings-reviews-faq.md)
