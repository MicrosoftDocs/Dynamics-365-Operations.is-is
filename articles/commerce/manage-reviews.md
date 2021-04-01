---
title: Stjórna einkunnum og umsögnum
description: Þetta efnisatriði útskýrir hvernig á að stjórna einkunnum og umsögnum í Microsoft Dynamics 365 Commerce vefsmið.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8ab85605bce11934f71237ad1ef7cd24804319b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250805"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="ba865-103">Stjórna einkunnum og umsögnum</span><span class="sxs-lookup"><span data-stu-id="ba865-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba865-104">Þetta efnisatriði útskýrir hvernig á að stjórna einkunnum og umsögnum í Microsoft Dynamics 365 Commerce vefsmið.</span><span class="sxs-lookup"><span data-stu-id="ba865-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="ba865-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="ba865-105">Overview</span></span>

<span data-ttu-id="ba865-106">Dynamics 365 Commerce notar Microsoft Azure Cognitive Services til að miðla sjálfkrafa endurskoðun texta með því að ritstýra blótsyrði.</span><span class="sxs-lookup"><span data-stu-id="ba865-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="ba865-107">Auk þess geta stjórnendur notað Dynamics 365 Commerce-vefsmið til að innleiða eftirfarandi handvirk verk:</span><span class="sxs-lookup"><span data-stu-id="ba865-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="ba865-108">Breyta umsögnum með því að svara þeim eða fjarlægja þær.</span><span class="sxs-lookup"><span data-stu-id="ba865-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="ba865-109">Eyða umsögnum viðskiptavinarins að beiðni viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="ba865-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="ba865-110">Flytja inn öll gögn um einkunnir og umsagnir gagna í Microsoft Power BI sniðmát svo hægt sé að greina þau.</span><span class="sxs-lookup"><span data-stu-id="ba865-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="ba865-111">Lesa umsögn</span><span class="sxs-lookup"><span data-stu-id="ba865-111">Read a review</span></span> 

<span data-ttu-id="ba865-112">Til að lesa umsögn í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ba865-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ba865-113">Farðu í **Heim \> Umsagnir \> Breyting**.</span><span class="sxs-lookup"><span data-stu-id="ba865-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ba865-114">Notaðu leitarreitinn efst til hægri á síðunni til að sía umsagnir sem eru sýndar með afurðakenni, vöruheiti eða umsagnartexta.</span><span class="sxs-lookup"><span data-stu-id="ba865-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="ba865-115">Viðbótarsíur gera þér kleift að takmarka umsagnir eftir tímabili, einkunn, rás eða áhyggjustöðu (tekin niður, svarað eða tilkynnt).</span><span class="sxs-lookup"><span data-stu-id="ba865-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Heimasíða breytingar](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="ba865-117">Svara umsögn</span><span class="sxs-lookup"><span data-stu-id="ba865-117">Respond to a review</span></span> 

<span data-ttu-id="ba865-118">Stundum lýsa viðskiptavinir sem keyptu vöru ánægju sinni eða óánægju, eða skilja ekki hvernig þeir nota vöruna.</span><span class="sxs-lookup"><span data-stu-id="ba865-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="ba865-119">Sem stjórnandi geturðu sent svar við gagnrýni.</span><span class="sxs-lookup"><span data-stu-id="ba865-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="ba865-120">Þetta svar birtist ásamt umsögninni á síðunni.</span><span class="sxs-lookup"><span data-stu-id="ba865-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="ba865-121">Til að svara umsögn í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ba865-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ba865-122">Farðu í **Heim \> Umsagnir \> Breyting**.</span><span class="sxs-lookup"><span data-stu-id="ba865-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ba865-123">Finndu og veldu umsögnina sem krefst svara.</span><span class="sxs-lookup"><span data-stu-id="ba865-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="ba865-124">Í eiginleikaglugganum til hægri velurðu **Bæta við svari**.</span><span class="sxs-lookup"><span data-stu-id="ba865-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="ba865-125">Sláðu inn svartexta og nafn sem ætti að sýna fyrir svarandann.</span><span class="sxs-lookup"><span data-stu-id="ba865-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="ba865-126">Sjálfgefið svar svarandsins er **Stjórnandi**.</span><span class="sxs-lookup"><span data-stu-id="ba865-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="ba865-127">Þegar því er lokið skal velja **Bóka svar**.</span><span class="sxs-lookup"><span data-stu-id="ba865-127">When you've finished, select **Post response**.</span></span>

![Svar við umsögn](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="ba865-129">Fjarlægja umsögn</span><span class="sxs-lookup"><span data-stu-id="ba865-129">Take down a review</span></span> 

<span data-ttu-id="ba865-130">Stundum er viðskiptaleg réttlæting fyrir því að stjórnendur fjarlægi umsagnir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="ba865-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="ba865-131">Til að fjarlægja umsögn í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ba865-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ba865-132">Farðu í **Heim \> Umsagnir \> Breyting**.</span><span class="sxs-lookup"><span data-stu-id="ba865-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ba865-133">Finndu og veldu umsögnina sem þarf að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="ba865-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="ba865-134">Á eiginleikasvæðinu til hægri skal velja ástæðu fjarlægingar undir **Umsögn um fjarlægingu** og velja síðan **Fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="ba865-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="ba865-135">Eyða umsögnum viðskiptavinarins að beiðni viðskiptavinarins</span><span class="sxs-lookup"><span data-stu-id="ba865-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="ba865-136">Stundum vilja viðskiptavinir að einkunna- og umsagnagögnum þeirra verði varanlega eytt af vefsíðu netverslunar.</span><span class="sxs-lookup"><span data-stu-id="ba865-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="ba865-137">Stjórnandi sem fær beiðni um flutning frá viðskiptavini getur fjarlægt gögn viðskiptavinarins með því að nota endurskoðunaraðgerðina.</span><span class="sxs-lookup"><span data-stu-id="ba865-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="ba865-138">Til að finna og eyða gögnum viðskiptavinar þarf stjórnandinn netfangið sem viðskiptavinurinn notaði til að skrá sig inn og veita umsagnir.</span><span class="sxs-lookup"><span data-stu-id="ba865-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="ba865-139">Til að finna og eyða gögnum viðskiptavinar í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ba865-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ba865-140">Farðu í **Heim \> Umsagnir \> Eyða**.</span><span class="sxs-lookup"><span data-stu-id="ba865-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="ba865-141">Í glugganum **Leita að notendum eftir netfangi** skal færa inn netfang viðskiptavinar og velja síðan **Leita**.</span><span class="sxs-lookup"><span data-stu-id="ba865-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="ba865-142">Ef viðskiptavinurinn hefur einhverjar umsagnaraðgerðir (til dæmis, endurskoða innsendingar, atkvæði um hjálpsemi umsagna annars viðskiptavinar eða athugasemdir um umsögn annars viðskiptavinar) eru niðurstöðurnar sýndar.</span><span class="sxs-lookup"><span data-stu-id="ba865-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="ba865-143">Fyrir hvern lið er hnappurinn **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="ba865-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="ba865-144">Fyrir hvert atriði sem þarf að eyða velurðu **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="ba865-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="ba865-145">Þegar þú færð kvaðningu um staðfestingu skaltu velja **Já**.</span><span class="sxs-lookup"><span data-stu-id="ba865-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Eyðing á gögnum viðskiptavinar](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="ba865-147">Það getur tekið allt að sjö daga þar til gögn eru fjarlægð að fullu úr kerfinu.</span><span class="sxs-lookup"><span data-stu-id="ba865-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="ba865-148">Stjórendur ættu að tilkynna viðskiptavinum um þessa seinkun.</span><span class="sxs-lookup"><span data-stu-id="ba865-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="ba865-149">Ef viðskiptavinir hafa breytt nafni sínu í reikningsstillingunum gætu mörg atriði birst í leitarniðurstöðum.</span><span class="sxs-lookup"><span data-stu-id="ba865-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="ba865-150">Í þessu tilfelli, til að eyða gögnum viðskiptavina að fullu verður stjórnandinn að velja **Eyða** fyrir hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="ba865-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="ba865-151">Sækja einkunna- og umsagnagögn</span><span class="sxs-lookup"><span data-stu-id="ba865-151">Download ratings and reviews data</span></span>

<span data-ttu-id="ba865-152">Vefsmiður Commerce leyfir ritstjórum að flytja inn gögn einkunna og umsagna í magni, þannig að hægt sé að greina mynstur.</span><span class="sxs-lookup"><span data-stu-id="ba865-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="ba865-153">Power BI-sniðmát sem inniheldur grunnmælingar er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="ba865-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="ba865-154">Stjórnendur geta notað þetta snið til að tengja magninnflutt gögn og skoða stjórnborð.</span><span class="sxs-lookup"><span data-stu-id="ba865-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="ba865-155">Þeir þurfa ekki að búa til sérsniðið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="ba865-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="ba865-156">Stjórnendur geta sérsniðið Power BI-sniðmát til að mæta tilteknum þörfum sínum.</span><span class="sxs-lookup"><span data-stu-id="ba865-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="ba865-157">Til að sækja gögn einkunna og umsagna í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ba865-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ba865-158">Farðu í **Heim \> Umsagnir \> Skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="ba865-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="ba865-159">Veljið **Sækja umsagnargögn** til að sækja gögn einkunna og umsagna í magni í gildum aðskildum með kommu (CSV-sniði).</span><span class="sxs-lookup"><span data-stu-id="ba865-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="ba865-160">Skoða einkunnir og umsagnaleitni</span><span class="sxs-lookup"><span data-stu-id="ba865-160">View ratings and reviews trends</span></span>

<span data-ttu-id="ba865-161">Stjórnendur geta hlaðið niður Power BI-sniðinu svo að þeir geti skoðað leitni í stjórnborði.</span><span class="sxs-lookup"><span data-stu-id="ba865-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="ba865-162">Til að skoða mynstur einkunna og umsagna í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ba865-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ba865-163">Farðu í **Heim \> Umsagnir \> Skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="ba865-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="ba865-164">Veldu **PowerBI sniðmát** til að hlaða niður sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="ba865-164">Select **PowerBI template** to download the template.</span></span>

    ![Sækja Power BI-sniðmátið](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="ba865-166">Opnaðu sniðmátið sem hlaðið var niður með því að nota Power BI forritð.</span><span class="sxs-lookup"><span data-stu-id="ba865-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="ba865-167">Lokaðu glugganum **Aðgangur að vefefni** sem birtist og lokaðu síðan villunni "Endurnýja" sem birtist.</span><span class="sxs-lookup"><span data-stu-id="ba865-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="ba865-168">Farðu í **Heim**, veldu **Breyta fyrirspurnum** og veldu síðan **Stillingar gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="ba865-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="ba865-169">Í valmyndinni **Stillingar gagnagjafa** velurðu **Breyta gjafa**.</span><span class="sxs-lookup"><span data-stu-id="ba865-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="ba865-170">Í reitinn **Vefslóð** slærðu inn slóð umsagnargagnanna sem þú sóttir í fyrra ferli (til dæmis, **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="ba865-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Vefslóðareitur í svarglugganum með kommuaðgreindum gildum](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="ba865-172">Veldu **Í lagi** og veldu síðan **Beita breytingum**.</span><span class="sxs-lookup"><span data-stu-id="ba865-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="ba865-173">Það mun taka eina til tvær mínútur að nota breytingarnar á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="ba865-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="ba865-174">Veldu **Þróunarblað** til að skoða einkunnir og rifja upp þróun.</span><span class="sxs-lookup"><span data-stu-id="ba865-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Einkunna- og umsagnaþróun](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="ba865-176">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ba865-176">Additional resources</span></span>

[<span data-ttu-id="ba865-177">Yfirlit yfir einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="ba865-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="ba865-178">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="ba865-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="ba865-179">Skilgreina einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="ba865-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="ba865-180">Samstilla afurðaeinkunnir í Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="ba865-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]