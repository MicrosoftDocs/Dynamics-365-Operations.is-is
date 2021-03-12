---
title: Velja að nota einkunnir og umsagnir
description: Þetta efni útskýrir hvernig þú getur valið að nota einkunnir og umsagnir á Microsoft Dynamics 365 Commerce síðunni.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 481a8750b2333d5dd5de2c05e175569804a6046f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985837"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Velja að nota einkunnir og umsagnir

[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig þú getur valið að nota einkunnir og umsagnir á Microsoft Dynamics 365 Commerce síðunni.

## <a name="overview"></a>Yfirlit

Einkunna- og umsagnalausnin er alhliða lausn sem þú getur gert tiltæk í Dynamics 365 Commerce með því að nota Microsoft Dynamics Lifecycle Services (LCS). LCS er stjórnunargátt sem smásalar nota til að stjórna umhverfi sínu frá útvegun til úreldingar.

Ef þú vilt nota lánshæfiseinkunnina og umsagnirnar á vefsvæði þínu í viðskiptum, verður þú að taka þátt í einkunnagjöf og umsögnum meðan þú setur netverslunarsíðuna þína á Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Velja að nota einkunnir og umsagnir

Fylgdu þessum skrefum til að taka þátt í að nota einkunnir og umsagnir á síðuna þína.

1. Fylgdu skrefunum í [Dreifa nýja netverslunarsíðu](deploy-ecommerce-site.md).
1. Farðu á meðan þú ert enn í LCS **Retail-uppsetning \> Aðrar stillingar**.
1. Stilltu valkostinn **Virkja einkunna- og umsagnaþjónustu** á **Já**.
1. Í reitinn **AAD öryggishópur stjórnanda fyrir einkunnir og umsagnir (hlutakenni öryggishóps)** slærðu inn kenni Microsoft Azure Active Directory (Azure AD) öryggishópur sem inniheldur einkunnir og umsagnir stjórnenda.

    ![Velja að nota einkunnir og umsagnir](media/LCS_RnR_Preference.png)

1. Ljúktu frumstillingarferli rafrænna viðskipta.

> [!NOTE] 
> Ef þú ert til Dynamics 365 Commerce viðskiptavinur sem þegar hefur sent frá sér e-verslunarsíðu án þess að hafa valið sér einkunnir og umsagnir og vill nú nota einkunnir og umsagnir frá Dynamics 365 Commerce pakki, vinsamlegast sendu þjónustubeiðni. Sjá upplýsingar um hvernig á að leggja fram þjónustubeiðni [Sendu inn beiðnir um þjónustu](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Skilgreina einkunnir og umsagnir](configure-ratings-reviews.md)

[Samstilla afurðaeinkunnir í Dynamics 365 Commerce](sync-product-ratings.md)


