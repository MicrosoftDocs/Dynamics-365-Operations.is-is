---
title: Velja að nota einkunnir og umsagnir
description: Þessi grein útskýrir hvernig á að velja að nota einkunnir og umsagnir á þínum Microsoft Dynamics 365 Commerce síða.
author: gvrmohanreddy
ms.date: 02/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 00fd30ded916cc6b587ceff67728e7d964714716
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269163"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Velja að nota einkunnir og umsagnir

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að velja að nota einkunnir og umsagnir á þínum Microsoft Dynamics 365 Commerce síða.

Einkunna- og umsagnalausnin er alhliða lausn sem þú getur gert tiltæk í Dynamics 365 Commerce með því að nota Microsoft Dynamics Lifecycle Services (LCS). LCS er stjórnunargátt sem smásalar nota til að stjórna umhverfi sínu frá útvegun til úreldingar.

Ef þú vilt nota lánshæfiseinkunnina og umsagnirnar á vefsvæði þínu í viðskiptum, verður þú að taka þátt í einkunnagjöf og umsögnum meðan þú setur netverslunarsíðuna þína á Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Velja að nota einkunnir og umsagnir

Fylgdu þessum skrefum til að taka þátt í að nota einkunnir og umsagnir á síðuna þína.

1. Fylgdu skrefunum í [Dreifa nýja netverslunarsíðu](deploy-ecommerce-site.md).
1. Farðu á meðan þú ert enn í LCS **Retail-uppsetning \> Aðrar stillingar**.
1. Stilltu valkostinn **Virkja einkunna- og umsagnaþjónustu** á **Já**.
1. Í **AAD öryggishópur fyrir einkunna- og endurskoðunarstjóra** reit, sláðu inn auðkenni Microsoft Azure Active Directory (Azure AD) öryggishópur sem inniheldur einkunna- og umsagnarstjórnendur.

    ![Velja að nota einkunnir og umsagnir.](media/LCS_RnR_Preference_2.png)

1. Ljúktu frumstillingarferli rafrænna viðskipta.

> [!NOTE] 
> Ef þú ert til Dynamics 365 Commerce viðskiptavinur sem þegar hefur sent frá sér e-verslunarsíðu án þess að hafa valið sér einkunnir og umsagnir og vill nú nota einkunnir og umsagnir frá Dynamics 365 Commerce pakki, vinsamlegast sendu þjónustubeiðni. Sjá upplýsingar um hvernig á að leggja fram þjónustubeiðni [Sendu inn beiðnir um þjónustu](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Skilgreina einkunnir og umsagnir](configure-ratings-reviews.md)

[Samstilla afurðaeinkunnir í Dynamics 365 Commerce](sync-product-ratings.md)

[Virkja handvirka birtingu einkunna og umsagna hjá stjórnanda](manual-publish-rating-reviews.md)

[Flytja einkunnir og umsagnir inn og út](import-export-reviews.md)

[Stilla sannvottun milli þjónusta](service-to-service-auth.md)

[Algengar spurningar um einkunnir og umsagnir](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
