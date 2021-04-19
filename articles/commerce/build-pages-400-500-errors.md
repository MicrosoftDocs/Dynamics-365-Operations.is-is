---
title: Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur
description: Þetta efnisatriði lýsir því hvernig á að búa til sérstilltar svarsíður fyrir 4xx og 5xx stöðukóðavillur með því að nota höfundarverkfæri í Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799649"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="7f275-103">Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur</span><span class="sxs-lookup"><span data-stu-id="7f275-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f275-104">Þetta efnisatriði lýsir því hvernig á að búa til sérstilltar svarsíður fyrir 4xx og 5xx stöðukóðavillur með því að nota höfundarverkfæri í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f275-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7f275-105">Ef beiðni tekst ekki, gefur þjónninn út svör við HTTP stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="7f275-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="7f275-106">404 stöðukóðinn er sóttur og skilað ef síðu er ekki að finna og 500 stöðukóðinn er sóttur og honum skilað ef villu á netþjóni kemur upp.</span><span class="sxs-lookup"><span data-stu-id="7f275-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="7f275-107">Í Dynamics 365 Commerce geta notendur forrita smíðað sérsniðnar villusvarsíður stöðukóða sem eru sýndar notendum vegna þessara villusvörunar við stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="7f275-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="7f275-108">Búðu til síðu viðbragðsstöðu við villukóða</span><span class="sxs-lookup"><span data-stu-id="7f275-108">Build a status code error response page</span></span>

<span data-ttu-id="7f275-109">Fylgdu þessum skrefum til að byrja að búa til villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="7f275-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="7f275-110">Í vafranum þínum skaltu skrá þig inn í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f275-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="7f275-111">Veldu síðuna sem þú vilt byggja upp 4xx / 5xx villusvörunarsíðu stöðukóða fyrir.</span><span class="sxs-lookup"><span data-stu-id="7f275-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="7f275-112">Búðu til sniðmátið</span><span class="sxs-lookup"><span data-stu-id="7f275-112">Build the template</span></span>

<span data-ttu-id="7f275-113">Fylgdu þessum skrefum til að byrja að búa til sniðmát fyrir villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="7f275-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="7f275-114">Farðu í **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="7f275-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="7f275-115">Veljið **Ný** til að stofna nýtt síðusniðmát.</span><span class="sxs-lookup"><span data-stu-id="7f275-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="7f275-116">Í svarglugganum **Nýtt sniðmát** undir **Heiti sniðmáts** skaltu slá inn heiti fyrir nýja sniðmátið og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7f275-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="7f275-117">Búðu til sniðmát, byggt á uppbyggingunni sem þú vilt að villusvörunarsíða stöðukóðans hafi.</span><span class="sxs-lookup"><span data-stu-id="7f275-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="7f275-118">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="7f275-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="7f275-119">Búðu til síðu viðbragðsstöðu við villukóða</span><span class="sxs-lookup"><span data-stu-id="7f275-119">Build the status code error response page</span></span>

<span data-ttu-id="7f275-120">Fylgdu þessum skrefum til að búa til villusvörunarsíðu með stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="7f275-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="7f275-121">Fara á **Síður**.</span><span class="sxs-lookup"><span data-stu-id="7f275-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="7f275-122">Veljið **Ný** til að búa til síðu.</span><span class="sxs-lookup"><span data-stu-id="7f275-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="7f275-123">Í svarglugganum **Veljið sniðmát** skal velja sniðmát og svo, undir **Síðuheiti** skal slá inn heiti fyrir svarsíð stöðukóðavillunnar.</span><span class="sxs-lookup"><span data-stu-id="7f275-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="7f275-124">Skildu reitinn **Vefslóð síðu** eftir auðann.</span><span class="sxs-lookup"><span data-stu-id="7f275-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="7f275-125">Búðu síðuna til.</span><span class="sxs-lookup"><span data-stu-id="7f275-125">Build the page.</span></span>
1. <span data-ttu-id="7f275-126">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="7f275-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="7f275-127">Þú getur búið til aðskildar svörunarsíður stöðukóða fyrir stöðukóðavillur 4xx og 5xx.</span><span class="sxs-lookup"><span data-stu-id="7f275-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="7f275-128">Að öðrum kosti er hægt að nota sömu svörunarsíðu með almennum stöðukóða fyrir báða villuflokkana.</span><span class="sxs-lookup"><span data-stu-id="7f275-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="7f275-129">Settu upp tilvísun fyrir villusvörunarsíðu stöðukóða</span><span class="sxs-lookup"><span data-stu-id="7f275-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="7f275-130">Fylgdu þessum skrefum til að setja upp framsendingu fyrir villusvörunarsíðu stöðukóða.</span><span class="sxs-lookup"><span data-stu-id="7f275-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="7f275-131">Farðu á **Vefslóðir \> Nýtt \> Nýtt auknefni** og veldu villusvörusíðu stöðukóða sem þú bjóst til fyrr.</span><span class="sxs-lookup"><span data-stu-id="7f275-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="7f275-132">Í reitinn **Auknefni** skaltu slá inn annaðhvort **sjálfgefið-4xx** eða **sjálfgefið-5xx**, allt eftir villusvörunarsíðu stöðukóða sem þú ert að setja upp framsendingu fyrir.</span><span class="sxs-lookup"><span data-stu-id="7f275-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="7f275-133">Þessi auknefni verður að birta.</span><span class="sxs-lookup"><span data-stu-id="7f275-133">These aliases must be published.</span></span> <span data-ttu-id="7f275-134">Annars virkar framsendingin ekki.</span><span class="sxs-lookup"><span data-stu-id="7f275-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="7f275-135">Velja skal **Í lagi** til að staðfesta tenginguna.</span><span class="sxs-lookup"><span data-stu-id="7f275-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="7f275-136">Ef þú ert að nota eina villusvörunarsíðu fyrir stöðukóða fyrir báða villuflokka skaltu endurtaka þessa aðferð til að tengja auknefni fyrir hinn villuflokkinn við sömu síðu.</span><span class="sxs-lookup"><span data-stu-id="7f275-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f275-137">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7f275-137">Additional resources</span></span>

[<span data-ttu-id="7f275-138">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="7f275-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="7f275-139">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="7f275-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="7f275-140">Búa til síðuvefslóð</span><span class="sxs-lookup"><span data-stu-id="7f275-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
