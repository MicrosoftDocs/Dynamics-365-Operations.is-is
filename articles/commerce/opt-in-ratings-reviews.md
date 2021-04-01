---
title: Velja að nota einkunnir og umsagnir
description: Þetta efnisatriði lýsir því hvernig á að velja að nota einkunnir og umsagnir á Microsoft Dynamics 365 Commerce svæðinu þínu.
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
ms.openlocfilehash: 6c54a8fa01badb6a383c41dc979e71d82a25ef97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251236"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="9994c-103">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="9994c-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9994c-104">Þetta efnisatriði lýsir því hvernig á að velja að nota einkunnir og umsagnir á Microsoft Dynamics 365 Commerce svæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="9994c-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="9994c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="9994c-105">Overview</span></span>

<span data-ttu-id="9994c-106">Einkunna- og umsagnalausnin er alhliða lausn sem þú getur gert tiltæk í Dynamics 365 Commerce með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9994c-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9994c-107">LCS er stjórnunargátt sem smásalar nota til að stjórna umhverfi sínu frá útvegun til úreldingar.</span><span class="sxs-lookup"><span data-stu-id="9994c-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="9994c-108">Ef þú vilt nota lánshæfiseinkunnina og umsagnirnar á vefsvæði þínu í viðskiptum, verður þú að taka þátt í einkunnagjöf og umsögnum meðan þú setur netverslunarsíðuna þína á Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9994c-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="9994c-109">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="9994c-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="9994c-110">Fylgdu þessum skrefum til að taka þátt í að nota einkunnir og umsagnir á síðuna þína.</span><span class="sxs-lookup"><span data-stu-id="9994c-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="9994c-111">Fylgdu skrefunum í [Dreifa nýja netverslunarsíðu](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="9994c-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="9994c-112">Farðu á meðan þú ert enn í LCS **Retail-uppsetning \> Aðrar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="9994c-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="9994c-113">Stilltu valkostinn **Virkja einkunna- og umsagnaþjónustu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="9994c-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="9994c-114">Í reitinn **AAD öryggishópur stjórnanda fyrir einkunnir og umsagnir (hlutakenni öryggishóps)** slærðu inn kenni Microsoft Azure Active Directory (Azure AD) öryggishópur sem inniheldur einkunnir og umsagnir stjórnenda.</span><span class="sxs-lookup"><span data-stu-id="9994c-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Velja að nota einkunnir og umsagnir](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="9994c-116">Ljúktu frumstillingarferli rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="9994c-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="9994c-117">Ef þú ert til Dynamics 365 Commerce viðskiptavinur sem þegar hefur sent frá sér e-verslunarsíðu án þess að hafa valið sér einkunnir og umsagnir og vill nú nota einkunnir og umsagnir frá Dynamics 365 Commerce pakki, vinsamlegast sendu þjónustubeiðni.</span><span class="sxs-lookup"><span data-stu-id="9994c-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="9994c-118">Sjá upplýsingar um hvernig á að leggja fram þjónustubeiðni [Sendu inn beiðnir um þjónustu](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="9994c-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9994c-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9994c-119">Additional resources</span></span>

[<span data-ttu-id="9994c-120">Yfirlit yfir einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="9994c-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="9994c-121">Stjórna einkunnum og umsögnum</span><span class="sxs-lookup"><span data-stu-id="9994c-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="9994c-122">Skilgreina einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="9994c-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="9994c-123">Samstilla afurðaeinkunnir í Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9994c-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]