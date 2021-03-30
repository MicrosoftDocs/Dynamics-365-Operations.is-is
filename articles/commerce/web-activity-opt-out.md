---
title: Afþakka söfnun aðgerðatilvika á vef
description: Þetta efnisatriði útskýrir hvernig hægt er að leyfa gestum á vefsvæði notanda afþakka söfnun vefnotkunar í Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 244d612fa01529df4fff250df50a06526632fcf1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210924"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="19ef7-103">Afþakka söfnun aðgerðatilvika á vef</span><span class="sxs-lookup"><span data-stu-id="19ef7-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="19ef7-104">Þetta efnisatriði útskýrir hvernig hægt er að leyfa viðskiptavinum afþakka söfnun vefnotkunar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="19ef7-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="19ef7-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="19ef7-105">Overview</span></span>

<span data-ttu-id="19ef7-106">Dynamics 365 Commerce gerir stjórnendum vefsvæða kleift að greina vefnotkun notenda þeirra á vefsvæðum rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="19ef7-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="19ef7-107">Á þann hátt er hægt að skilja hvernig vefsvæði þeirra eru notuð og þeir geta fínstillt vefsvæðin til að veita bætta notendaupplifun og uppfylla markmið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="19ef7-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="19ef7-108">Leiðir fyrir stjórnendur til að innleiða afþökkunarupplifun</span><span class="sxs-lookup"><span data-stu-id="19ef7-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="19ef7-109">Stjórnendur hafa þrjár leiðir til að innleiða afþökkunarupplifun.</span><span class="sxs-lookup"><span data-stu-id="19ef7-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="19ef7-110">Afþakka fyrir hönd notenda</span><span class="sxs-lookup"><span data-stu-id="19ef7-110">Opt out on behalf of users</span></span>

<span data-ttu-id="19ef7-111">Í reikningsstjórnun í Commerce Headquarters (HQ) geta stjórnendur afþakkað fyrir hönd notenda.</span><span class="sxs-lookup"><span data-stu-id="19ef7-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="19ef7-112">Í HQ-biðlaranum, á síðunni **Allir viðskiptavinir**, skal leita að og velja viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="19ef7-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="19ef7-113">Á upplýsingasíðu viðskiptavinar, á **Retail** flýtiflipa, í **Persónuvernd**-hluta skal stilla **Ekki rekja vefnotkun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="19ef7-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Öryggisstillingar](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="19ef7-115">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="19ef7-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="19ef7-116">Eining byggð á afþakkunarreynslu</span><span class="sxs-lookup"><span data-stu-id="19ef7-116">Module-based opt-out experience</span></span>

<span data-ttu-id="19ef7-117">Stjórnendur geta leyft sannvottuðum notendum að afþakka söfnun vefnotkunar sjálfir.</span><span class="sxs-lookup"><span data-stu-id="19ef7-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="19ef7-118">Til að bjóða upp á þessa afþakkunarupplifun skaltu bæta við afþakkunareiningunni fyrir notendur á prófílsíðum viðskiptavinarreiknings.</span><span class="sxs-lookup"><span data-stu-id="19ef7-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="19ef7-119">Sérsniðnar viðbætur</span><span class="sxs-lookup"><span data-stu-id="19ef7-119">Custom extensions</span></span>

<span data-ttu-id="19ef7-120">Stjórnendur geta búið til sínar eigin viðbætur til að stjórna afþökkunarupplifuninni fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="19ef7-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="19ef7-121">Fyrir frekari upplýsingar, sjá [Hringdu í smáforritaskil smásölumiðlara](e-commerce-extensibility/call-retail-server-apis.md) og [Stækkanleiki á netinu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="19ef7-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]