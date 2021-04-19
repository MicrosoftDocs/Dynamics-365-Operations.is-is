---
title: Takmarka aðgang að netverslun við prófun eða þróun
description: Þetta efnisatriði útskýrir hvernig á að takmarka aðgang að Microsoft Dynamics 365 Commerce-netverslun á meðan innri prófun eða þróun er í gangi.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f5cba6b7ff3aa65441c932e72fa458bda0d0fc69
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801532"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="a4b58-103">Takmarka aðgang að netverslun við prófun eða þróun</span><span class="sxs-lookup"><span data-stu-id="a4b58-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4b58-104">Þetta efnisatriði útskýrir hvernig á að takmarka aðgang að Microsoft Dynamics 365 Commerce-netverslun á meðan innri prófun eða þróun er í gangi.</span><span class="sxs-lookup"><span data-stu-id="a4b58-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="a4b58-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="a4b58-105">Description</span></span>

<span data-ttu-id="a4b58-106">Á meðan innri prófun eða virk þróun er í gangi gæti verið sniðugt að takmarka aðgang að svæðinu til að koma í veg fyrir aðgang ytri notenda að virkum netverslunarsíðum.</span><span class="sxs-lookup"><span data-stu-id="a4b58-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="a4b58-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="a4b58-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="a4b58-108">Setja upp Azure AD B2C með því að nota hefðbundið notandastreymi</span><span class="sxs-lookup"><span data-stu-id="a4b58-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="a4b58-109">Upplýsingar um hvernig á að skilgreina Azure Active Directory B2C (Azure AD B2C) fyrir svæði rafrænna viðskipta er að finna í [Setja upp B2C-leigjanda í Commerce](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="a4b58-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="a4b58-110">Takmarka aðgang notanda að síðum netverslunar og loka á stofnun nýrra notenda</span><span class="sxs-lookup"><span data-stu-id="a4b58-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="a4b58-111">Til að takmarka aðgang að síðum netverslunar í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a4b58-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a4b58-112">Opnið svæðið ykkar.</span><span class="sxs-lookup"><span data-stu-id="a4b58-112">Go to your site.</span></span>
1. <span data-ttu-id="a4b58-113">Veljið **Síður** og veljið því næst síðuna þar sem á að takmarka aðgang notanda.</span><span class="sxs-lookup"><span data-stu-id="a4b58-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="a4b58-114">Veljið hólf einingar eða síðubrots og veljið því næst **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a4b58-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="a4b58-115">Í eiginleikaglugganum skal velja **Krefst innskráningar?** og því næst velja **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="a4b58-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="a4b58-116">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="a4b58-116">Select **Publish**.</span></span>

<span data-ttu-id="a4b58-117">Til að loka á stofnun nýrra notenda í Azure AD skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a4b58-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="a4b58-118">Opna [Azure-gáttina](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="a4b58-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="a4b58-119">Veljið forrit Azure AD B2C sem var búið til fyrir aðgang að svæðinu.</span><span class="sxs-lookup"><span data-stu-id="a4b58-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="a4b58-120">Í vinstri flettingunni skal velja **Notandastreymi**.</span><span class="sxs-lookup"><span data-stu-id="a4b58-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="a4b58-121">Efst á síðunni **Notandastreymi** skal velja **Nýtt notandastreymi**.</span><span class="sxs-lookup"><span data-stu-id="a4b58-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="a4b58-122">Á síðunni **Velja gerð notandastreymis** skal velja **Forskoða**.</span><span class="sxs-lookup"><span data-stu-id="a4b58-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="a4b58-123">Fyrir miðju síðunnar skal velja **Skrá inn v2**.</span><span class="sxs-lookup"><span data-stu-id="a4b58-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="a4b58-124">Síðan skal fylgja skrefunum í [Setja upp B2C-leigjanda í Commerce](../set-up-b2c-tenant.md) til að skilgreina streymið sem hefðbundið notandastreymi svæðisins fyrir Azure AD B2C á meðan prófun og þróun er í gangi.</span><span class="sxs-lookup"><span data-stu-id="a4b58-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4b58-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a4b58-125">Additional resources</span></span>

[<span data-ttu-id="a4b58-126">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="a4b58-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="a4b58-127">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="a4b58-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
