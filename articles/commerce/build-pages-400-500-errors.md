---
title: Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur
description: Þetta efnisatriði lýsir því hvernig á að búa til sérsniðnar svarsíður fyrir villur í 4xx og 5xx stöðukóða með því að nota höfundatólin í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001131"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="ac51a-103">Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur</span><span class="sxs-lookup"><span data-stu-id="ac51a-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ac51a-104">Þetta efnisatriði lýsir því hvernig á að búa til sérsniðnar svarsíður fyrir villur í 4xx og 5xx stöðukóða með því að nota höfundatólin í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ac51a-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ac51a-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="ac51a-105">Overview</span></span>

<span data-ttu-id="ac51a-106">Ef beiðni tekst ekki, gefur þjónninn út svör við HTTP stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="ac51a-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="ac51a-107">404 stöðukóðinn er sóttur og skilað ef síðu er ekki að finna og 500 stöðukóðinn er sóttur og honum skilað ef villu á netþjóni kemur upp.</span><span class="sxs-lookup"><span data-stu-id="ac51a-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="ac51a-108">Í Dynamics 365 Commerce geta notendur forrita smíðað sérsniðnar villusvarsíður stöðukóða sem eru sýndar notendum vegna þessara villusvörunar við stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="ac51a-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="ac51a-109">Búðu til síðu viðbragðsstöðu við villukóða</span><span class="sxs-lookup"><span data-stu-id="ac51a-109">Build a status code error response page</span></span>

<span data-ttu-id="ac51a-110">Fylgdu þessum skrefum til að byrja að búa til villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="ac51a-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ac51a-111">Í vafranum þínum skaltu skrá þig inn í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ac51a-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="ac51a-112">Veldu síðuna sem þú vilt byggja upp 4xx / 5xx villusvörunarsíðu stöðukóða fyrir.</span><span class="sxs-lookup"><span data-stu-id="ac51a-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="ac51a-113">Búðu til sniðmátið</span><span class="sxs-lookup"><span data-stu-id="ac51a-113">Build the template</span></span>

<span data-ttu-id="ac51a-114">Fylgdu þessum skrefum til að byrja að búa til sniðmát fyrir villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="ac51a-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ac51a-115">Farðu í **Sniðmát \> Nýtt sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="ac51a-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="ac51a-116">Gefðu nýja sniðmátinu heiti.</span><span class="sxs-lookup"><span data-stu-id="ac51a-116">Name the new template.</span></span>
1. <span data-ttu-id="ac51a-117">Búðu til sniðmát, byggt á uppbyggingunni sem þú vilt að villusvörunarsíða stöðukóðans hafi.</span><span class="sxs-lookup"><span data-stu-id="ac51a-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="ac51a-118">Skráðu sniðmátið inn og birtu það.</span><span class="sxs-lookup"><span data-stu-id="ac51a-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="ac51a-119">Búðu til síðu viðbragðsstöðu við villukóða</span><span class="sxs-lookup"><span data-stu-id="ac51a-119">Build the status code error response page</span></span>

<span data-ttu-id="ac51a-120">Fylgdu þessum skrefum til að búa til villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="ac51a-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ac51a-121">Farðu á **Síður \> Ný síða**.</span><span class="sxs-lookup"><span data-stu-id="ac51a-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="ac51a-122">Nefndu villusvörusíðu stöðukóða, en stilltu **ekki** reitinn **Vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="ac51a-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="ac51a-123">Búðu síðuna til.</span><span class="sxs-lookup"><span data-stu-id="ac51a-123">Build the page.</span></span>
1. <span data-ttu-id="ac51a-124">Skráðu síðuna inn og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="ac51a-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="ac51a-125">Þú getur búið til aðskildar svörunarsíður stöðukóða fyrir stöðukóðavillur 4xx og 5xx.</span><span class="sxs-lookup"><span data-stu-id="ac51a-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="ac51a-126">Að öðrum kosti er hægt að nota sömu svörunarsíðu með almennum stöðukóða fyrir báða villuflokkana.</span><span class="sxs-lookup"><span data-stu-id="ac51a-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="ac51a-127">Settu upp tilvísun fyrir villusvörunarsíðu stöðukóða</span><span class="sxs-lookup"><span data-stu-id="ac51a-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="ac51a-128">Fylgdu þessum skrefum til að setja upp framsendingu fyrir villusvörunarsíðu stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="ac51a-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ac51a-129">Farðu á **Vefslóðir \> Nýtt \> Nýtt auknefni**og veldu villusvörusíðu stöðukóða sem þú bjóst til fyrr.</span><span class="sxs-lookup"><span data-stu-id="ac51a-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="ac51a-130">Í reitinn **Auknefni** skaltu slá inn annaðhvort **sjálfgefið-4xx** eða **sjálfgefið-5xx**, allt eftir villusvörunarsíðu stöðukóða sem þú ert að setja upp framsendingu fyrir.</span><span class="sxs-lookup"><span data-stu-id="ac51a-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="ac51a-131">Þessi auknefni verður að birta.</span><span class="sxs-lookup"><span data-stu-id="ac51a-131">These aliases must be published.</span></span> <span data-ttu-id="ac51a-132">Annars virkar framsendingin ekki.</span><span class="sxs-lookup"><span data-stu-id="ac51a-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="ac51a-133">Velja skal **Í lagi** til að staðfesta tenginguna.</span><span class="sxs-lookup"><span data-stu-id="ac51a-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="ac51a-134">Ef þú ert að nota eina villusvörunarsíðu fyrir stöðukóða fyrir báða villuflokka skaltu endurtaka þessa aðferð til að tengja auknefni fyrir hinn villuflokkinn við sömu síðu.</span><span class="sxs-lookup"><span data-stu-id="ac51a-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac51a-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ac51a-135">Additional resources</span></span>

[<span data-ttu-id="ac51a-136">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="ac51a-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="ac51a-137">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="ac51a-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ac51a-138">Búa til síðuvefslóð</span><span class="sxs-lookup"><span data-stu-id="ac51a-138">Create a page URL</span></span>](create-page-url.md)
