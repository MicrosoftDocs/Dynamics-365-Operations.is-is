---
title: Vinna með skrárnar robots.txt
description: Þetta efnisatriði lýsir hvernig á að stjórna robots.txt skrám í Microsoft Dynamics 365 Commerce.
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
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477709"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="7f11b-103">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="7f11b-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f11b-104">Þetta efnisatriði lýsir hvernig á að stjórna robots.txt skrám í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f11b-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7f11b-105">Útilokunarstaðall þjarka, eða robots.txt, er staðall sem vefsíður nota til að eiga samskipti við vefþjarka.</span><span class="sxs-lookup"><span data-stu-id="7f11b-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="7f11b-106">Hann leiðbeinir vefþjörkum um öll svæði á vefsíðu sem ætti ekki að heimsækja.</span><span class="sxs-lookup"><span data-stu-id="7f11b-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="7f11b-107">Þjarkar eru oft notaðir af leitarvélum til að skrá vefsíður.</span><span class="sxs-lookup"><span data-stu-id="7f11b-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="7f11b-108">Til að útiloka þjarka frá netþjóni skaltu stofna skrá á netþjóninum.</span><span class="sxs-lookup"><span data-stu-id="7f11b-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="7f11b-109">Í þessari skrá tilgreinirðu aðgangsstefnu fyrir þjarka.</span><span class="sxs-lookup"><span data-stu-id="7f11b-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="7f11b-110">Skráin verður að vera aðgengileg með HTTP á vefslóðinni **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7f11b-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="7f11b-111">Robots.txt skráin hjálpar leitarvélum að skrá innihaldið á vefsíðunni.</span><span class="sxs-lookup"><span data-stu-id="7f11b-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="7f11b-112">Dynamics 365 Commerce gerir þér kleift að hlaða upp robots.txt skrá fyrir lénið þitt.</span><span class="sxs-lookup"><span data-stu-id="7f11b-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="7f11b-113">Fyrir hvert lén í viðskiptaumhverfi þínu geturðu hlaðið upp einni robots.txt skrá og tengt hana við það lén.</span><span class="sxs-lookup"><span data-stu-id="7f11b-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="7f11b-114">Frekari upplýsingar um robots.txt skrána er að finna á [Síður vefþjarka](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="7f11b-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="7f11b-115">Hlaða upp robots.txt skrá</span><span class="sxs-lookup"><span data-stu-id="7f11b-115">Upload a robots.txt file</span></span>

<span data-ttu-id="7f11b-116">Eftir að þú hefur búið til og breytt robots.txt skránni þinni í samræmi við [útilokunarstaðal þjarka](https://www.robotstxt.org/orig.html) skaltu ganga úr skugga um að skráin sé aðgengileg á tölvunni þar sem þú munt nota höfundatólin fyrir viðskipti.</span><span class="sxs-lookup"><span data-stu-id="7f11b-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="7f11b-117">Skráin verður að heita **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7f11b-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="7f11b-118">Til að ná sem bestum árangri verður það að vera með því sniði sem fram kemur í staðlinum.</span><span class="sxs-lookup"><span data-stu-id="7f11b-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="7f11b-119">Sérhver viðskiptavinur Commerce er ábyrgur fyrir því að staðfesta og viðhalda innihaldi robots.txt skráarinnar.</span><span class="sxs-lookup"><span data-stu-id="7f11b-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="7f11b-120">Til að hlaða upp robots.txt skrá verður þú að vera skráður inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="7f11b-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="7f11b-121">Til að hlaða upp robots.txt-skrá á síðuna þína í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7f11b-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7f11b-122">Skráðu þig inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="7f11b-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="7f11b-123">Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="7f11b-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="7f11b-124">Undir **Stillingar leigjanda** velurðu **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7f11b-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="7f11b-125">Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.</span><span class="sxs-lookup"><span data-stu-id="7f11b-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="7f11b-126">Veldu **Stjórna** til að hlaða upp robots.txt skrá fyrir lén í umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="7f11b-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="7f11b-127">Á valmyndinni til hægri velurðu hnappinn **Hlaða upp** (örina sem vísar upp) við hlið lénsins sem er tengt robots.txt skránni.</span><span class="sxs-lookup"><span data-stu-id="7f11b-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="7f11b-128">Gluggi skráavals birtist.</span><span class="sxs-lookup"><span data-stu-id="7f11b-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="7f11b-129">Í valglugganum skaltu fletta að og velja robots.txt-skrána sem þú vilt hlaða upp fyrir tengt lén og veldu síðan **Opna** til að ljúka uppflutningnum.</span><span class="sxs-lookup"><span data-stu-id="7f11b-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="7f11b-130">Við upphleðslu staðfestir Commerce að skjalið sé textaskrá, en það staðfestir ekki innihald skrárinnar.</span><span class="sxs-lookup"><span data-stu-id="7f11b-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="7f11b-131">Hlaða niður robots.txt skrá</span><span class="sxs-lookup"><span data-stu-id="7f11b-131">Download a robots.txt file</span></span>

<span data-ttu-id="7f11b-132">Til að hlaða niður robots.txt-skrá á síðuna þína í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7f11b-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7f11b-133">Skráðu þig inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="7f11b-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="7f11b-134">Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="7f11b-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="7f11b-135">Undir **Stillingar leigjanda** velurðu **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7f11b-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="7f11b-136">Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.</span><span class="sxs-lookup"><span data-stu-id="7f11b-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="7f11b-137">Veldu **Stjórna** til að hlaða niður robots.txt skrá fyrir lén í umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="7f11b-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="7f11b-138">Á valmyndinni til hægri velurðu hnappinn **Hlaða niður** (örina sem vísar niður) við hlið lénsins sem er tengt robots.txt skránni.</span><span class="sxs-lookup"><span data-stu-id="7f11b-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="7f11b-139">Gluggi skráavals birtist.</span><span class="sxs-lookup"><span data-stu-id="7f11b-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="7f11b-140">Í valglugganum skaltu fara á óskaðan stað á drifinu þínu, staðfesta eða slá inn skráarheiti og velja síðan **Vista** til að ljúka niðurflutningnum.</span><span class="sxs-lookup"><span data-stu-id="7f11b-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="7f11b-141">Þetta ferli er hægt að nota til að hlaða aðeins niður robots.txt skrám sem áður var hlaðið upp með höfundatækjum Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f11b-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="7f11b-142">Eyða robots.txt skrá</span><span class="sxs-lookup"><span data-stu-id="7f11b-142">Delete a robots.txt file</span></span>

<span data-ttu-id="7f11b-143">Til að eyða robots.txt-skrá á síðunni þinni í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7f11b-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7f11b-144">Skráðu þig inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="7f11b-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="7f11b-145">Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="7f11b-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="7f11b-146">Undir **Stillingar leigjanda** velurðu **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7f11b-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="7f11b-147">Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.</span><span class="sxs-lookup"><span data-stu-id="7f11b-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="7f11b-148">Veldu **Stjórna** til að eyða robots.txt skrá fyrir lén í umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="7f11b-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="7f11b-149">Á valmyndinni til hægri velurðu hnappinn **Eyða** (öskutunnutáknið) við hlið lénsins sem er tengt robots.txt skránni.</span><span class="sxs-lookup"><span data-stu-id="7f11b-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="7f11b-150">Gluggi skráavals birtist.</span><span class="sxs-lookup"><span data-stu-id="7f11b-150">A file browser window appears.</span></span>
6. <span data-ttu-id="7f11b-151">Í skráavalsglugganum skaltu fletta að og velja robots.txt-skrána sem þú vilt eyða fyrir lénið og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="7f11b-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="7f11b-152">Viðvörunarskilaboð birtast.</span><span class="sxs-lookup"><span data-stu-id="7f11b-152">A warning message box appears.</span></span>
7. <span data-ttu-id="7f11b-153">Í skilaboðaglugganum velurðu **Eyða** til að staðfesta eyðingu á robots.txt file.</span><span class="sxs-lookup"><span data-stu-id="7f11b-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="7f11b-154">Þetta ferli er hægt að nota til að eyða aðeins robots.txt skrám sem áður var hlaðið upp með höfundatækjum Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f11b-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f11b-155">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7f11b-155">Additional resources</span></span>

[<span data-ttu-id="7f11b-156">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="7f11b-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7f11b-157">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="7f11b-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7f11b-158">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="7f11b-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7f11b-159">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="7f11b-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7f11b-160">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="7f11b-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7f11b-161">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="7f11b-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7f11b-162">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="7f11b-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="7f11b-163">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="7f11b-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7f11b-164">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="7f11b-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7f11b-165">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="7f11b-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
