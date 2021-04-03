---
title: Tengill innskráningar framsendir aftur á svæði rafrænna viðskipta
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar innskráningartengill framsendir aftur á svæði rafrænna viðskipta í stað þess að fara á innskráningarsíðuna.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585367"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="8240b-103">Tengill innskráningar framsendir aftur á svæði rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="8240b-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8240b-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar innskráningartengill framsendir aftur á svæði rafrænna viðskipta í stað þess að fara á innskráningarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="8240b-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="8240b-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="8240b-105">Description</span></span>

<span data-ttu-id="8240b-106">Þegar búið er að skilgreina nýjan Microsoft Azure Active Directory B2C-leigjanda (Azure AD B2C) í vefsmið Commerce eru notendur sem velja tengilinn **Innskráning** framsendir á aðallendingarsíðu rafrænna viðskipta án þess að fara á innskráningarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="8240b-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="8240b-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="8240b-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="8240b-108">Staðfesta að svarvefslóð sé rétt skilgreind í forriti Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8240b-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="8240b-109">Til að staðfesta að svarvefslóð sé rétt skilgreind í forriti Azure AD B2C skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8240b-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="8240b-110">Opna [Azure-gáttina](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="8240b-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="8240b-111">Veljið forrit Azure AD B2C sem var búið til fyrir aðgang að svæðinu.</span><span class="sxs-lookup"><span data-stu-id="8240b-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="8240b-112">Veljið forritið sem var búið til við uppsetningu Azure AD B2C uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="8240b-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="8240b-113">Undir **Svarslóð** skal ganga úr skugga um listinn innihaldi færslur fyrir bæði vefslóð svæðisins og vefslóð sem rafræn viðskipti mynda eins og sýnt er í dæminu á eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="8240b-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Færslur svarslóðar Azure AD B2C](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="8240b-115">Bæði vefslóð svæðisins og mynduð vefslóð rafrænna viðskipta verða að vera á gildu sniði vefslóðar sem inniheldur ekki línubil fyrir framan og aftan.</span><span class="sxs-lookup"><span data-stu-id="8240b-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8240b-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8240b-116">Additional resources</span></span>

[<span data-ttu-id="8240b-117">Skrá vefforrit í Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="8240b-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="8240b-118">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="8240b-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
