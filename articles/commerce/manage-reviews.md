---
title: Stjórna einkunnum og umsögnum
description: Þetta efni útskýrir hvernig á að stjórna einkunnagjöf og umsögnum með því að nota Microsoft Dynamics 365 Commerce einkunnir og umsagnir stjórnunar tól.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698027"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="401b7-103">Stjórna einkunnum og umsögnum</span><span class="sxs-lookup"><span data-stu-id="401b7-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="401b7-104">Þetta efni útskýrir hvernig á að stjórna einkunnagjöf og umsögnum með því að nota Microsoft Dynamics 365 Commerce einkunnir og umsagnir stjórnunar tól.</span><span class="sxs-lookup"><span data-stu-id="401b7-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="401b7-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="401b7-105">Overview</span></span>

<span data-ttu-id="401b7-106">Dynamics 365 Commerce notar Microsoft Azure Cognitive Services til að miðla sjálfkrafa endurskoðun texta með því að ritstýra blótsyrði.</span><span class="sxs-lookup"><span data-stu-id="401b7-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="401b7-107">Að auki geta stjórnendur notað einkunnagjafartólið og skoðað stjórnunartólið fyrir eftirfarandi handvirk verk:</span><span class="sxs-lookup"><span data-stu-id="401b7-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="401b7-108">Breyta umsögnum með því að svara þeim eða fjarlægja þær.</span><span class="sxs-lookup"><span data-stu-id="401b7-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="401b7-109">Eyða umsögnum viðskiptavinarins að beiðni viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="401b7-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="401b7-110">Flyttu inn einkunnir og umsagnir fyrir allar vörur í Microsoft Power BI-sniðmáti, svo að hægt sé að greina þróun á einkunnum og umsögnum.</span><span class="sxs-lookup"><span data-stu-id="401b7-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="401b7-111">Lesa umsögn</span><span class="sxs-lookup"><span data-stu-id="401b7-111">Read a review</span></span> 

1. <span data-ttu-id="401b7-112">Farðu í **Heim \> Umsagnir \> Breyting**.</span><span class="sxs-lookup"><span data-stu-id="401b7-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="401b7-113">Notaðu leitarreitinn efst til hægri á síðunni til að sía umsagnir sem eru sýndar með afurðakenni, vöruheiti eða umsagnartexta.</span><span class="sxs-lookup"><span data-stu-id="401b7-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="401b7-114">Viðbótarsíur gera þér kleift að takmarka umsagnir eftir tímabili, einkunn, rás eða áhyggjustöðu (tekin niður, svarað eða tilkynnt).</span><span class="sxs-lookup"><span data-stu-id="401b7-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Heimasíða breytingar](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="401b7-116">Svara umsögn</span><span class="sxs-lookup"><span data-stu-id="401b7-116">Respond to a review</span></span> 

<span data-ttu-id="401b7-117">Stundum lýsa viðskiptavinir sem keyptu vöru ánægju sinni eða óánægju, eða skilja ekki hvernig þeir nota vöruna.</span><span class="sxs-lookup"><span data-stu-id="401b7-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="401b7-118">Sem stjórnandi geturðu sent svar við gagnrýni.</span><span class="sxs-lookup"><span data-stu-id="401b7-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="401b7-119">Þetta svar birtist ásamt umsögninni á síðunni.</span><span class="sxs-lookup"><span data-stu-id="401b7-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="401b7-120">Fylgdu þessum skrefum til að svara umsögn.</span><span class="sxs-lookup"><span data-stu-id="401b7-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="401b7-121">Farðu í **Heim \> Umsagnir \> Breyting**.</span><span class="sxs-lookup"><span data-stu-id="401b7-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="401b7-122">Finndu og veldu umsögnina sem krefst svara.</span><span class="sxs-lookup"><span data-stu-id="401b7-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="401b7-123">Í eiginleikaglugganum til hægri velurðu **Bæta við svari**.</span><span class="sxs-lookup"><span data-stu-id="401b7-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="401b7-124">Sláðu inn svartexta og nafn sem ætti að sýna fyrir svarandann.</span><span class="sxs-lookup"><span data-stu-id="401b7-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="401b7-125">Sjálfgefið svar svarandsins er **Stjórnandi**.</span><span class="sxs-lookup"><span data-stu-id="401b7-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="401b7-126">Þegar því er lokið skal velja **Bóka svar**.</span><span class="sxs-lookup"><span data-stu-id="401b7-126">When you've finished, select **Post response**.</span></span>

![Svar við umsögn](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="401b7-128">Fjarlægja umsögn</span><span class="sxs-lookup"><span data-stu-id="401b7-128">Take down a review</span></span> 

<span data-ttu-id="401b7-129">Stundum er viðskiptaleg réttlæting fyrir því að stjórnendur fjarlægi umsagnir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="401b7-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="401b7-130">Til að fjarlægja umsögn fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="401b7-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="401b7-131">Farðu í **Heim \> Umsagnir \> Breyting**.</span><span class="sxs-lookup"><span data-stu-id="401b7-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="401b7-132">Finndu og veldu umsögnina sem þarf að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="401b7-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="401b7-133">Veldu eiginleikagluggann til hægri, veldu ástæðu fjarlægingar og síðan **Fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="401b7-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="401b7-134">Eyða umsögnum viðskiptavinarins að beiðni viðskiptavinarins</span><span class="sxs-lookup"><span data-stu-id="401b7-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="401b7-135">Stundum vilja viðskiptavinir að einkunna- og umsagnagögnum þeirra verði varanlega eytt af vefsíðu netverslunar.</span><span class="sxs-lookup"><span data-stu-id="401b7-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="401b7-136">Stjórnandi sem fær beiðni um flutning frá viðskiptavini getur fjarlægt gögn viðskiptavinarins með því að nota endurskoðunaraðgerðina.</span><span class="sxs-lookup"><span data-stu-id="401b7-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="401b7-137">Til að finna og eyða gögnum viðskiptavinar þarf stjórnandinn netfangið sem viðskiptavinurinn notaði til að skrá sig inn og veita umsagnir.</span><span class="sxs-lookup"><span data-stu-id="401b7-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="401b7-138">Fylgdu þessum skrefum til að finna og eyða gögnum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="401b7-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="401b7-139">Farðu í **Heim \> Umsagnir \> Eyða**.</span><span class="sxs-lookup"><span data-stu-id="401b7-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="401b7-140">Í reitnum **Leita að notendum með netfangi** slærðu inn netfang viðskiptavinarins og velur síðan **Leita**.</span><span class="sxs-lookup"><span data-stu-id="401b7-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="401b7-141">Ef viðskiptavinurinn hefur einhverjar umsagnaraðgerðir (til dæmis, endurskoða innsendingar, atkvæði um hjálpsemi umsagna annars viðskiptavinar eða athugasemdir um umsögn annars viðskiptavinar) eru niðurstöðurnar sýndar.</span><span class="sxs-lookup"><span data-stu-id="401b7-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="401b7-142">Fyrir hvern lið er hnappurinn **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="401b7-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="401b7-143">Fyrir hvert atriði sem þarf að eyða velurðu **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="401b7-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="401b7-144">Þegar þú færð kvaðningu um staðfestingu skaltu velja **Já**.</span><span class="sxs-lookup"><span data-stu-id="401b7-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Eyðing á gögnum viðskiptavinar](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="401b7-146">Það getur tekið allt að sjö daga þar til gögn eru fjarlægð að fullu úr kerfinu.</span><span class="sxs-lookup"><span data-stu-id="401b7-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="401b7-147">Stjórendur ættu að tilkynna viðskiptavinum um þessa seinkun.</span><span class="sxs-lookup"><span data-stu-id="401b7-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="401b7-148">Ef viðskiptavinir hafa breytt nafni sínu í reikningsstillingunum gætu mörg atriði birst í leitarniðurstöðum.</span><span class="sxs-lookup"><span data-stu-id="401b7-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="401b7-149">Í þessu tilfelli, til að eyða gögnum viðskiptavina að fullu verður stjórnandinn að velja **Eyða** fyrir hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="401b7-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="401b7-150">Sækja einkunna- og umsagnagögn</span><span class="sxs-lookup"><span data-stu-id="401b7-150">Download ratings and reviews data</span></span>

<span data-ttu-id="401b7-151">Stjórnendatól einkunna og umsagna gerir stjórnendum kleift að flytja inn einkunna- og umsagnagögn í magni, svo að þau geti greint leitni.</span><span class="sxs-lookup"><span data-stu-id="401b7-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="401b7-152">Power BI-sniðmát sem inniheldur grunnmælingar er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="401b7-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="401b7-153">Stjórnendur geta notað þetta snið til að tengja magninnflutt gögn og skoða stjórnborð.</span><span class="sxs-lookup"><span data-stu-id="401b7-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="401b7-154">Þeir þurfa ekki að búa til sérsniðið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="401b7-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="401b7-155">Stjórnendur geta sérsniðið Power BI-sniðmát til að mæta tilteknum þörfum sínum.</span><span class="sxs-lookup"><span data-stu-id="401b7-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="401b7-156">Fylgdu þessum skrefum til að hlaða niður einkunnagjöf og umsögnum.</span><span class="sxs-lookup"><span data-stu-id="401b7-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="401b7-157">Farðu í **Heim \> Umsagnir \> Skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="401b7-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="401b7-158">Veldu **Sækja umsagnargögn** til að sækja einkunna- og umsagnargögn í magni með kommuaðskildu gildum (CSV) sniði.</span><span class="sxs-lookup"><span data-stu-id="401b7-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="401b7-159">Skoða einkunnir og umsagnaleitni</span><span class="sxs-lookup"><span data-stu-id="401b7-159">View ratings and reviews trends</span></span>

<span data-ttu-id="401b7-160">Stjórnendur geta hlaðið niður Power BI-sniðinu svo að þeir geti skoðað leitni í stjórnborði.</span><span class="sxs-lookup"><span data-stu-id="401b7-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="401b7-161">Til að skoða einkunna- og umsagnaleitni skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="401b7-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="401b7-162">Farðu í **Heim \> Umsagnir \> Skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="401b7-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="401b7-163">Veldu **PowerBI sniðmát** til að hlaða niður sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="401b7-163">Select **PowerBI template** to download the template.</span></span>

    ![Sæki Power BI sniðmátið](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="401b7-165">Opnaðu sniðmátið sem hlaðið var niður með því að nota Power BI forritð.</span><span class="sxs-lookup"><span data-stu-id="401b7-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="401b7-166">Lokaðu glugganum **Aðgangur að vefefni** sem birtist og lokaðu síðan villunni "Endurnýja" sem birtist.</span><span class="sxs-lookup"><span data-stu-id="401b7-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="401b7-167">Farðu í **Heim**, veldu **Breyta fyrirspurnum** og veldu síðan **Stillingar gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="401b7-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="401b7-168">Í valmyndinni **Stillingar gagnagjafa** velurðu **Breyta gjafa**.</span><span class="sxs-lookup"><span data-stu-id="401b7-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="401b7-169">Í reitinn **Vefslóð** slærðu inn slóð umsagnargagnanna sem þú sóttir í fyrra ferli (til dæmis, **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="401b7-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Vefslóðareitur í svarglugganum með kommuaðgreindum gildum](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="401b7-171">Veldu **Í lagi** og veldu síðan **Beita breytingum**.</span><span class="sxs-lookup"><span data-stu-id="401b7-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="401b7-172">Það mun taka eina til tvær mínútur að nota breytingarnar á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="401b7-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="401b7-173">Veldu **Þróunarblað** til að skoða einkunnir og rifja upp þróun.</span><span class="sxs-lookup"><span data-stu-id="401b7-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Einkunna- og umsagnaþróun](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="401b7-175">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="401b7-175">Additional resources</span></span>

[<span data-ttu-id="401b7-176">Yfirlit yfir einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="401b7-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="401b7-177">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="401b7-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="401b7-178">Skilgreina einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="401b7-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="401b7-179">Samstilla afurðaeinkunnir í Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="401b7-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
