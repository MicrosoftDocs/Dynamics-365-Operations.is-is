---
title: Afþakka söfnun aðgerðatilvika á vef
description: Þetta efnisatriði útskýrir hvernig hægt er að leyfa gestum á vefsvæði notanda afþakka söfnun vefnotkunar í Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791558"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="cfed9-103">Afþakka söfnun aðgerðatilvika á vef</span><span class="sxs-lookup"><span data-stu-id="cfed9-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="cfed9-104">Þetta efnisatriði útskýrir hvernig hægt er að leyfa viðskiptavinum afþakka söfnun vefnotkunar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cfed9-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cfed9-105">Dynamics 365 Commerce gerir stjórnendum vefsvæða kleift að greina vefnotkun notenda þeirra á vefsvæðum rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="cfed9-105">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="cfed9-106">Á þann hátt er hægt að skilja hvernig vefsvæði þeirra eru notuð og þeir geta fínstillt vefsvæðin til að veita bætta notendaupplifun og uppfylla markmið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="cfed9-106">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="cfed9-107">Leiðir fyrir stjórnendur til að innleiða afþökkunarupplifun</span><span class="sxs-lookup"><span data-stu-id="cfed9-107">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="cfed9-108">Stjórnendur hafa þrjár leiðir til að innleiða afþökkunarupplifun.</span><span class="sxs-lookup"><span data-stu-id="cfed9-108">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="cfed9-109">Afþakka fyrir hönd notenda</span><span class="sxs-lookup"><span data-stu-id="cfed9-109">Opt out on behalf of users</span></span>

<span data-ttu-id="cfed9-110">Í reikningsstjórnun í Commerce Headquarters (HQ) geta stjórnendur afþakkað fyrir hönd notenda.</span><span class="sxs-lookup"><span data-stu-id="cfed9-110">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="cfed9-111">Í HQ-biðlaranum, á síðunni **Allir viðskiptavinir**, skal leita að og velja viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="cfed9-111">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="cfed9-112">Á upplýsingasíðu viðskiptavinar, á **Retail** flýtiflipa, í **Persónuvernd**-hluta skal stilla **Ekki rekja vefnotkun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cfed9-112">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Öryggisstillingar](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="cfed9-114">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="cfed9-114">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="cfed9-115">Eining byggð á afþakkunarreynslu</span><span class="sxs-lookup"><span data-stu-id="cfed9-115">Module-based opt-out experience</span></span>

<span data-ttu-id="cfed9-116">Stjórnendur geta leyft sannvottuðum notendum að afþakka söfnun vefnotkunar sjálfir.</span><span class="sxs-lookup"><span data-stu-id="cfed9-116">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="cfed9-117">Til að bjóða upp á þessa afþakkunarupplifun skaltu bæta við afþakkunareiningunni fyrir notendur á prófílsíðum viðskiptavinarreiknings.</span><span class="sxs-lookup"><span data-stu-id="cfed9-117">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="cfed9-118">Sérsniðnar viðbætur</span><span class="sxs-lookup"><span data-stu-id="cfed9-118">Custom extensions</span></span>

<span data-ttu-id="cfed9-119">Stjórnendur geta búið til sínar eigin viðbætur til að stjórna afþökkunarupplifuninni fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="cfed9-119">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="cfed9-120">Fyrir frekari upplýsingar, sjá [Hringdu í smáforritaskil smásölumiðlara](e-commerce-extensibility/call-retail-server-apis.md) og [Stækkanleiki á netinu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="cfed9-120">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
