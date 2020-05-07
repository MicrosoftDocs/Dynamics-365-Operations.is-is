---
title: Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur
description: Þetta efnisatriði lýsir því hvernig á að búa til sérsniðnar svarsíður fyrir villur í 4xx og 5xx stöðukóða með því að nota höfundatólin í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269545"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="03146-103">Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur</span><span class="sxs-lookup"><span data-stu-id="03146-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="03146-104">Þetta efnisatriði lýsir því hvernig á að búa til sérsniðnar svarsíður fyrir villur í 4xx og 5xx stöðukóða með því að nota höfundatólin í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="03146-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="03146-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="03146-105">Overview</span></span>

<span data-ttu-id="03146-106">Ef beiðni tekst ekki, gefur þjónninn út svör við HTTP stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="03146-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="03146-107">404 stöðukóðinn er sóttur og skilað ef síðu er ekki að finna og 500 stöðukóðinn er sóttur og honum skilað ef villu á netþjóni kemur upp.</span><span class="sxs-lookup"><span data-stu-id="03146-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="03146-108">Í Dynamics 365 Commerce geta notendur forrita smíðað sérsniðnar villusvarsíður stöðukóða sem eru sýndar notendum vegna þessara villusvörunar við stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="03146-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="03146-109">Búðu til síðu viðbragðsstöðu við villukóða</span><span class="sxs-lookup"><span data-stu-id="03146-109">Build a status code error response page</span></span>

<span data-ttu-id="03146-110">Fylgdu þessum skrefum til að byrja að búa til villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="03146-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="03146-111">Í vafranum þínum skaltu skrá þig inn í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="03146-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="03146-112">Veldu síðuna sem þú vilt byggja upp 4xx / 5xx villusvörunarsíðu stöðukóða fyrir.</span><span class="sxs-lookup"><span data-stu-id="03146-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="03146-113">Búðu til sniðmátið</span><span class="sxs-lookup"><span data-stu-id="03146-113">Build the template</span></span>

<span data-ttu-id="03146-114">Fylgdu þessum skrefum til að byrja að búa til sniðmát fyrir villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="03146-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="03146-115">Farðu í **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="03146-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="03146-116">Veljið **Ný** til að stofna nýtt síðusniðmát.</span><span class="sxs-lookup"><span data-stu-id="03146-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="03146-117">Í svarglugganum **Nýtt sniðmát** undir **Heiti sniðmáts** skaltu slá inn heiti fyrir nýja sniðmátið og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="03146-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="03146-118">Búðu til sniðmát, byggt á uppbyggingunni sem þú vilt að villusvörunarsíða stöðukóðans hafi.</span><span class="sxs-lookup"><span data-stu-id="03146-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="03146-119">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="03146-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="03146-120">Búðu til síðu viðbragðsstöðu við villukóða</span><span class="sxs-lookup"><span data-stu-id="03146-120">Build the status code error response page</span></span>

<span data-ttu-id="03146-121">Fylgdu þessum skrefum til að búa til villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="03146-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="03146-122">Fara á **Síður**.</span><span class="sxs-lookup"><span data-stu-id="03146-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="03146-123">Veljið **Ný** til að búa til síðu.</span><span class="sxs-lookup"><span data-stu-id="03146-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="03146-124">Í svarglugganum **Veljið sniðmát** skal velja sniðmát og svo, undir **Síðuheiti** skal slá inn heiti fyrir svarsíð stöðukóðavillunnar.</span><span class="sxs-lookup"><span data-stu-id="03146-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="03146-125">Skildu reitinn **Vefslóð síðu** eftir auðann.</span><span class="sxs-lookup"><span data-stu-id="03146-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="03146-126">Búðu síðuna til.</span><span class="sxs-lookup"><span data-stu-id="03146-126">Build the page.</span></span>
1. <span data-ttu-id="03146-127">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="03146-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="03146-128">Þú getur búið til aðskildar svörunarsíður stöðukóða fyrir stöðukóðavillur 4xx og 5xx.</span><span class="sxs-lookup"><span data-stu-id="03146-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="03146-129">Að öðrum kosti er hægt að nota sömu svörunarsíðu með almennum stöðukóða fyrir báða villuflokkana.</span><span class="sxs-lookup"><span data-stu-id="03146-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="03146-130">Settu upp tilvísun fyrir villusvörunarsíðu stöðukóða</span><span class="sxs-lookup"><span data-stu-id="03146-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="03146-131">Fylgdu þessum skrefum til að setja upp framsendingu fyrir villusvörunarsíðu stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="03146-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="03146-132">Farðu á **Vefslóðir \> Nýtt \> Nýtt auknefni**og veldu villusvörusíðu stöðukóða sem þú bjóst til fyrr.</span><span class="sxs-lookup"><span data-stu-id="03146-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="03146-133">Í reitinn **Auknefni** skaltu slá inn annaðhvort **sjálfgefið-4xx** eða **sjálfgefið-5xx**, allt eftir villusvörunarsíðu stöðukóða sem þú ert að setja upp framsendingu fyrir.</span><span class="sxs-lookup"><span data-stu-id="03146-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="03146-134">Þessi auknefni verður að birta.</span><span class="sxs-lookup"><span data-stu-id="03146-134">These aliases must be published.</span></span> <span data-ttu-id="03146-135">Annars virkar framsendingin ekki.</span><span class="sxs-lookup"><span data-stu-id="03146-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="03146-136">Velja skal **Í lagi** til að staðfesta tenginguna.</span><span class="sxs-lookup"><span data-stu-id="03146-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="03146-137">Ef þú ert að nota eina villusvörunarsíðu fyrir stöðukóða fyrir báða villuflokka skaltu endurtaka þessa aðferð til að tengja auknefni fyrir hinn villuflokkinn við sömu síðu.</span><span class="sxs-lookup"><span data-stu-id="03146-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03146-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="03146-138">Additional resources</span></span>

[<span data-ttu-id="03146-139">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="03146-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="03146-140">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="03146-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="03146-141">Búa til síðuvefslóð</span><span class="sxs-lookup"><span data-stu-id="03146-141">Create a page URL</span></span>](create-page-url.md)
