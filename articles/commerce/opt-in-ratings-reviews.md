---
title: Velja að nota einkunnir og umsagnir
description: Þetta efni útskýrir hvernig þú getur valið að nota einkunnir og umsagnir á Microsoft Dynamics 365 Commerce síðunni.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697981"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="6c0dc-103">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="6c0dc-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6c0dc-104">Þetta efni útskýrir hvernig þú getur valið að nota einkunnir og umsagnir á Microsoft Dynamics 365 Commerce síðunni.</span><span class="sxs-lookup"><span data-stu-id="6c0dc-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="6c0dc-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="6c0dc-105">Overview</span></span>

<span data-ttu-id="6c0dc-106">Einkunna- og umsagnalausnin er alhliða lausn sem þú getur gert tiltæk í Dynamics 365 Commerce með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6c0dc-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6c0dc-107">LCS er stjórnunargátt sem smásalar nota til að stjórna umhverfi sínu frá útvegun til úreldingar.</span><span class="sxs-lookup"><span data-stu-id="6c0dc-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="6c0dc-108">Ef þú vilt nota einkunna- og umsagnalausn á vefsvæðinu þínu í Commerce, verður þú fyrst að skrá þig inn.</span><span class="sxs-lookup"><span data-stu-id="6c0dc-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="6c0dc-109">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="6c0dc-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="6c0dc-110">Fylgdu þessum skrefum til að taka þátt í að nota einkunnir og umsagnir á síðuna þína.</span><span class="sxs-lookup"><span data-stu-id="6c0dc-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="6c0dc-111">Fylgdu skrefunum í [Dreifa nýja netverslunarsíðu](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="6c0dc-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="6c0dc-112">Farðu á meðan þú ert enn í LCS **Retail-uppsetning \> Aðrar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="6c0dc-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="6c0dc-113">Stilltu valkostinn **Virkja einkunna- og umsagnaþjónustu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="6c0dc-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="6c0dc-114">Í reitinn **AAD öryggishópur stjórnanda fyrir einkunnir og umsagnir (hlutakenni öryggishóps)** slærðu inn kenni Microsoft Azure Active Directory (Azure AD) öryggishópur sem inniheldur einkunnir og umsagnir stjórnenda.</span><span class="sxs-lookup"><span data-stu-id="6c0dc-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Velja að nota einkunnir og umsagnir](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="6c0dc-116">Ljúktu frumstillingarferli rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="6c0dc-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c0dc-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6c0dc-117">Additional resources</span></span>

[<span data-ttu-id="6c0dc-118">Yfirlit yfir einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="6c0dc-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="6c0dc-119">Stjórna einkunnum og umsögnum</span><span class="sxs-lookup"><span data-stu-id="6c0dc-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="6c0dc-120">Skilgreina einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="6c0dc-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="6c0dc-121">Samstilla afurðaeinkunnir í Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="6c0dc-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
