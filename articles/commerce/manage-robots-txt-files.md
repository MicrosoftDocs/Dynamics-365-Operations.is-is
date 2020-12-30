---
title: Vinna með skrárnar robots.txt
description: Þetta efni lýsir hvernig á að stjórna robots.txt skrám í Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: ad87594b9c20d0c2b53e8d4e7c1170a78babe74b
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517453"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="d38b6-103">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="d38b6-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d38b6-104">Þetta efni lýsir hvernig á að stjórna robots.txt skrám í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d38b6-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d38b6-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="d38b6-105">Overview</span></span>

<span data-ttu-id="d38b6-106">Útilokunarstaðall þjarka, eða robots.txt, er staðall sem vefsíður nota til að eiga samskipti við vefþjarka.</span><span class="sxs-lookup"><span data-stu-id="d38b6-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="d38b6-107">Hann leiðbeinir vefþjörkum um öll svæði á vefsíðu sem ætti ekki að heimsækja.</span><span class="sxs-lookup"><span data-stu-id="d38b6-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="d38b6-108">Þjarkar eru oft notaðir af leitarvélum til að skrá vefsíður.</span><span class="sxs-lookup"><span data-stu-id="d38b6-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="d38b6-109">Til að útiloka þjarka frá netþjóni skaltu stofna skrá á netþjóninum.</span><span class="sxs-lookup"><span data-stu-id="d38b6-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="d38b6-110">Í þessari skrá tilgreinirðu aðgangsstefnu fyrir þjarka.</span><span class="sxs-lookup"><span data-stu-id="d38b6-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="d38b6-111">Skráin verður að vera aðgengileg með HTTP á vefslóðinni **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="d38b6-112">Robots.txt skráin hjálpar leitarvélum að skrá innihaldið á vefsíðunni.</span><span class="sxs-lookup"><span data-stu-id="d38b6-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="d38b6-113">Dynamics 365 Commerce gerir þér kleift að hlaða upp robots.txt skrá fyrir lénið þitt.</span><span class="sxs-lookup"><span data-stu-id="d38b6-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="d38b6-114">Fyrir hvert lén í viðskiptaumhverfi þínu geturðu hlaðið upp einni robots.txt skrá og tengt hana við það lén.</span><span class="sxs-lookup"><span data-stu-id="d38b6-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="d38b6-115">Frekari upplýsingar um robots.txt skrána er að finna á [Síður vefþjarka](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="d38b6-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="d38b6-116">Hlaða upp robots.txt skrá</span><span class="sxs-lookup"><span data-stu-id="d38b6-116">Upload a robots.txt file</span></span>

<span data-ttu-id="d38b6-117">Eftir að þú hefur búið til og breytt robots.txt skránni þinni í samræmi við [útilokunarstaðal þjarka](https://www.robotstxt.org/orig.html) skaltu ganga úr skugga um að skráin sé aðgengileg á tölvunni þar sem þú munt nota höfundatólin fyrir viðskipti.</span><span class="sxs-lookup"><span data-stu-id="d38b6-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="d38b6-118">Skráin verður að heita **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="d38b6-119">Til að ná sem bestum árangri verður það að vera með því sniði sem fram kemur í staðlinum.</span><span class="sxs-lookup"><span data-stu-id="d38b6-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="d38b6-120">Sérhver viðskiptavinur Commerce er ábyrgur fyrir því að staðfesta og viðhalda innihaldi robots.txt skráarinnar.</span><span class="sxs-lookup"><span data-stu-id="d38b6-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="d38b6-121">Til að hlaða upp robots.txt skrá verður þú að vera skráður inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="d38b6-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="d38b6-122">Til að hlaða upp robots.txt-skrá á síðuna þína í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d38b6-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d38b6-123">Skráðu þig inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="d38b6-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="d38b6-124">Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="d38b6-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="d38b6-125">Undir **Stillingar leigjanda** velurðu **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="d38b6-126">Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.</span><span class="sxs-lookup"><span data-stu-id="d38b6-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="d38b6-127">Veldu **Stjórna** til að hlaða upp robots.txt skrá fyrir lén í umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="d38b6-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="d38b6-128">Á valmyndinni til hægri velurðu hnappinn **Hlaða upp** (örina sem vísar upp) við hlið lénsins sem er tengt robots.txt skránni.</span><span class="sxs-lookup"><span data-stu-id="d38b6-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="d38b6-129">Gluggi skráavals birtist.</span><span class="sxs-lookup"><span data-stu-id="d38b6-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="d38b6-130">Í valglugganum skaltu fletta að og velja robots.txt-skrána sem þú vilt hlaða upp fyrir tengt lén og veldu síðan **Opna** til að ljúka uppflutningnum.</span><span class="sxs-lookup"><span data-stu-id="d38b6-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="d38b6-131">Við upphleðslu staðfestir Commerce að skjalið sé textaskrá, en það staðfestir ekki innihald skrárinnar.</span><span class="sxs-lookup"><span data-stu-id="d38b6-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="d38b6-132">Hlaða niður robots.txt skrá</span><span class="sxs-lookup"><span data-stu-id="d38b6-132">Download a robots.txt file</span></span>

<span data-ttu-id="d38b6-133">Til að hlaða niður robots.txt-skrá á síðuna þína í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d38b6-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d38b6-134">Skráðu þig inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="d38b6-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="d38b6-135">Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="d38b6-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="d38b6-136">Undir **Stillingar leigjanda** velurðu **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="d38b6-137">Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.</span><span class="sxs-lookup"><span data-stu-id="d38b6-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="d38b6-138">Veldu **Stjórna** til að hlaða niður robots.txt skrá fyrir lén í umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="d38b6-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="d38b6-139">Á valmyndinni til hægri velurðu hnappinn **Hlaða niður** (örina sem vísar niður) við hlið lénsins sem er tengt robots.txt skránni.</span><span class="sxs-lookup"><span data-stu-id="d38b6-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="d38b6-140">Gluggi skráavals birtist.</span><span class="sxs-lookup"><span data-stu-id="d38b6-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="d38b6-141">Í valglugganum skaltu fara á óskaðan stað á drifinu þínu, staðfesta eða slá inn skráarheiti og velja síðan **Vista** til að ljúka niðurflutningnum.</span><span class="sxs-lookup"><span data-stu-id="d38b6-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="d38b6-142">Þetta ferli er hægt að nota til að hlaða aðeins niður robots.txt skrám sem áður var hlaðið upp með höfundatækjum Commerce.</span><span class="sxs-lookup"><span data-stu-id="d38b6-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="d38b6-143">Eyða robots.txt skrá</span><span class="sxs-lookup"><span data-stu-id="d38b6-143">Delete a robots.txt file</span></span>

<span data-ttu-id="d38b6-144">Til að eyða robots.txt-skrá á síðunni þinni í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d38b6-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d38b6-145">Skráðu þig inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="d38b6-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="d38b6-146">Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="d38b6-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="d38b6-147">Undir **Stillingar leigjanda** velurðu **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="d38b6-148">Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.</span><span class="sxs-lookup"><span data-stu-id="d38b6-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="d38b6-149">Veldu **Stjórna** til að eyða robots.txt skrá fyrir lén í umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="d38b6-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="d38b6-150">Á valmyndinni til hægri velurðu hnappinn **Eyða** (öskutunnutáknið) við hlið lénsins sem er tengt robots.txt skránni.</span><span class="sxs-lookup"><span data-stu-id="d38b6-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="d38b6-151">Gluggi skráavals birtist.</span><span class="sxs-lookup"><span data-stu-id="d38b6-151">A file browser window appears.</span></span>
6. <span data-ttu-id="d38b6-152">Í skráavalsglugganum skaltu fletta að og velja robots.txt-skrána sem þú vilt eyða fyrir lénið og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="d38b6-153">Viðvörunarskilaboð birtast.</span><span class="sxs-lookup"><span data-stu-id="d38b6-153">A warning message box appears.</span></span>
7. <span data-ttu-id="d38b6-154">Í skilaboðaglugganum velurðu **Eyða** til að staðfesta eyðingu á robots.txt file.</span><span class="sxs-lookup"><span data-stu-id="d38b6-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="d38b6-155">Þetta ferli er hægt að nota til að eyða aðeins robots.txt skrám sem áður var hlaðið upp með höfundatækjum Commerce.</span><span class="sxs-lookup"><span data-stu-id="d38b6-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d38b6-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d38b6-156">Additional resources</span></span>

[<span data-ttu-id="d38b6-157">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="d38b6-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="d38b6-158">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="d38b6-158">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="d38b6-159">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="d38b6-159">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="d38b6-160">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="d38b6-160">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="d38b6-161">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="d38b6-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="d38b6-162">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="d38b6-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="d38b6-163">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="d38b6-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="d38b6-164">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="d38b6-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="d38b6-165">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="d38b6-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="d38b6-166">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="d38b6-166">Enable location-based store detection</span></span>](enable-store-detection.md)
