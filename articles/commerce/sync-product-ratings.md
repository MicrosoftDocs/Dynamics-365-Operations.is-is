---
title: Samstilla vörueinkunnagjöf í Dynamics 365 Retail
description: Þetta efni lýsir því hvernig á að samstilla vörueinkunnir í Microsoft Dynamics 365 Retail.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698166"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a><span data-ttu-id="da607-103">Samstilla vörueinkunnagjöf í Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="da607-103">Sync product ratings in Dynamics 365 Retail</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="da607-104">Þetta efni lýsir því hvernig á að samstilla vörueinkunnir í Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="da607-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="da607-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="da607-105">Overview</span></span>

<span data-ttu-id="da607-106">Til að nota afurðaeinkunnir í alhliða rásum, svo sem á sölustað (POS) og í símaverum, verður að flytja afurðareinkunnir úr einkunna- og umsagnarþjónustunni inn í gagnagrunn verslunarrásarinnar.</span><span class="sxs-lookup"><span data-stu-id="da607-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Retail channel database.</span></span> <span data-ttu-id="da607-107">Þegar afurðaeinkunnir eru gerðar aðgengilegar í alhliða rásum geta þær hjálpað viðskiptavinum óbeint við samskipti sín við söluaðila.</span><span class="sxs-lookup"><span data-stu-id="da607-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="da607-108">Þetta efni lýsir eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="da607-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="da607-109">Stilla runuvinnslu Retail til að flytja inn afurðaeinkunn.</span><span class="sxs-lookup"><span data-stu-id="da607-109">Configure a Retail batch job to import product ratings.</span></span>
1. <span data-ttu-id="da607-110">Staðfestu að runuvinnslan fyrir samstillingu afurðaeinkunna hafi gengið.</span><span class="sxs-lookup"><span data-stu-id="da607-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="da607-111">Gerðu afurðaeinkunnir tiltækar í POS.</span><span class="sxs-lookup"><span data-stu-id="da607-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a><span data-ttu-id="da607-112">Stilla runuvinnslu Retail til að flytja inn afurðaeinkunnir</span><span class="sxs-lookup"><span data-stu-id="da607-112">Configure a Retail batch job to import product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da607-113">Áður en þú hefst handa skaltu ganga úr skugga um að útgáfa 10.0.6 eða nýrri af Retail sé uppsett.</span><span class="sxs-lookup"><span data-stu-id="da607-113">Before you start, make sure that version 10.0.6 or later of Retail is installed.</span></span>

### <a name="initialize-the-retail-scheduler"></a><span data-ttu-id="da607-114">Frumstilla Retail-verkraðara</span><span class="sxs-lookup"><span data-stu-id="da607-114">Initialize the retail scheduler</span></span>

<span data-ttu-id="da607-115">Fylgið eftirfarandi skrefum til að frumstilla Retail verkraðara.</span><span class="sxs-lookup"><span data-stu-id="da607-115">To initialize the retail scheduler, follow these steps.</span></span>

1. <span data-ttu-id="da607-116">Farðu í **Retail \> Uppsetning höfuðstöðva \> Retail verkraðari \> Frumstilla Retail verkraðara**.</span><span class="sxs-lookup"><span data-stu-id="da607-116">Go to **Retail \> Headquarters setup \> Retail scheduler \> Initialize retail scheduler**.</span></span> <span data-ttu-id="da607-117">Að öðrum kosti leitarðu að „Frumstilla smásöluáætlun.“</span><span class="sxs-lookup"><span data-stu-id="da607-117">Alternatively, search for "Initialize retail scheduler."</span></span>
1. <span data-ttu-id="da607-118">Í valmyndinni **Frumstilla Retail verkraðara** skaltu ganga úr skugga um að valkosturinn **Eyða fyrirliggjandi stillingum** sé stilltur á **Nei** og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="da607-118">In the **Initialize retail scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="da607-119">Staðfestu undirvinnsluna RetailProductRating</span><span class="sxs-lookup"><span data-stu-id="da607-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="da607-120">Til að sannreyna að undirvinnslan **RetailProductRating** sé til fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="da607-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="da607-121">Farðu í **Retail \> Uppsetning höfuðstöðva \> Retail verkraðari \> Undirvinnslur verkraðara**.</span><span class="sxs-lookup"><span data-stu-id="da607-121">Go to **Retail \> Headquarters setup \> Retail scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="da607-122">Að öðrum kosti leitarðu að „Undirvinnslur verkraðara.“</span><span class="sxs-lookup"><span data-stu-id="da607-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="da607-123">Í undirvinnslulistanum finnurðu eða leitar að undirvinnslunni **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="da607-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="da607-124">Eftirfarandi mynd sýnir dæmi um undirvinnsluupplýsingar í Retail.</span><span class="sxs-lookup"><span data-stu-id="da607-124">The following illustration shows an example of the subjob details in Retail.</span></span>

![Upplýsingar um undirvinnsluna RetailProductRating](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="da607-126">Ef þú finnur ekki undirvinnsluna **RetailProductRating** gæti verið að þú hafir þegar keyrt vinnsluna **Samstilla afurðaeinkunnir** og vinnsluna **1040 CDX** áður en þú frumstilltir Retail verkraðara.</span><span class="sxs-lookup"><span data-stu-id="da607-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the retail scheduler.</span></span> <span data-ttu-id="da607-127">Í þessu tilfelli skaltu fylgja þessum skrefum til að keyra vinnsluna **Full samstilling gagna**.</span><span class="sxs-lookup"><span data-stu-id="da607-127">In this case, follow these steps to run the **Full data sync** job.</span></span>
>
> 1. <span data-ttu-id="da607-128">Farðu í **Retail \> Uppsetning höfuðstöðva \> Retail verkraðari \> Gagnagrunnur rásar**.</span><span class="sxs-lookup"><span data-stu-id="da607-128">Go to **Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span> <span data-ttu-id="da607-129">Að öðrum kosti, leitaðu að „Rásagagnagrunni.“</span><span class="sxs-lookup"><span data-stu-id="da607-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="da607-130">Veldu gagnagrunn rásarinnar sem á að samstilla.</span><span class="sxs-lookup"><span data-stu-id="da607-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="da607-131">Í aðgerðaglugganum velurðu **Samstilling allra gagna**.</span><span class="sxs-lookup"><span data-stu-id="da607-131">On the Action Pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="da607-132">Í fellivalmyndinni **Velja dreifingaráætlun** velurðu **1040 - afurðir** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="da607-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="da607-133">Endurtaktu skrefin í fyrri aðferð til að staðfesta að undirvinnslan **RetailProductRating** hafi verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="da607-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="da607-134">Flytja inn afurðareinkunnir</span><span class="sxs-lookup"><span data-stu-id="da607-134">Import product ratings</span></span>

<span data-ttu-id="da607-135">Til að flytja afurðaeinkunnir inn í Retail úr einkunna- og umsagnaþjónustunni skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="da607-135">To import product ratings into Retail from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="da607-136">Farðu í **Retail \> Uppsetning höfuðstöðva \> Retail verkraðari \> Vinnslan Samstilla afurðaeinkunnir**.</span><span class="sxs-lookup"><span data-stu-id="da607-136">Go to **Retail \> Headquarters setup \> Retail scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="da607-137">Að öðrum kosti leitarðu að „Vinnslan Samstilla afurðaeinkunnir.“</span><span class="sxs-lookup"><span data-stu-id="da607-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="da607-138">Í valmyndinni **Sækja afurðaeinkunnir**, á flýtifipanum **Keyra í bakgrunni**, velurðu **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="da607-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="da607-139">Í valmyndinni **Skilgreina endurtekningu** seturðu upp endurtekningarmynstur.</span><span class="sxs-lookup"><span data-stu-id="da607-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="da607-140">(Ráðlagt gildi er tvær klukkustundir.) Ekki tímasetja endurtekningu sem er minna en ein klukkustund.</span><span class="sxs-lookup"><span data-stu-id="da607-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="da607-141">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="da607-141">Select **OK**.</span></span>
1. <span data-ttu-id="da607-142">Stilltu valkostinn **Runuvinnsla** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="da607-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="da607-143">Þessi stilling hjálpar til við að tryggja að þú getir gert úttekt á klöddum og sannreynt stöðu runuvinnslukeyrslna.</span><span class="sxs-lookup"><span data-stu-id="da607-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="da607-144">Veldu **Í lagi** til að áætla runuvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="da607-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="da607-145">Eftirfarandi mynd sýnir dæmi um stillingar runuvinnslu í Retail.</span><span class="sxs-lookup"><span data-stu-id="da607-145">The following illustration shows an example of batch job configuration in Retail.</span></span>

![Stilling á runuvinnslunni Samstilla afurðaeinkunnir](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="da607-147">Staðfestu að runuvinnslan fyrir samstillingu afurðaeinkunna hafi gengið</span><span class="sxs-lookup"><span data-stu-id="da607-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="da607-148">Til að sannreyna að runuvinnslan **Samstilla afurðaeinkunnir** hafi tekist skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="da607-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="da607-149">Farðu í **Retail \> Kerfisstjóri \> Fyrirspurnir \> Runuvinnslur** eða, ef þú ert að nota Retail-sértæka birgðahaldseiningu (SKU), **Retail \> Fyrirspurnir og skýrslur \> Runuvinnslur** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="da607-149">Go to **Retail \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Retail-only stock keeping unit (SKU), **Retail \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="da607-150">Að öðrum kosti leitarðu að „Runuvinnslum“.</span><span class="sxs-lookup"><span data-stu-id="da607-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="da607-151">Til að skoða upplýsingar um runuvinnsluna, í runuvinnslulistanum, í dálkinum **Vinnslulýsing**, leitarðu að lýsingu sem inniheldur „Sækja afurðaeinkunnir.“</span><span class="sxs-lookup"><span data-stu-id="da607-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="da607-152">Veldu vinnslukennið til að skoða upplýsingar um runuvinnsluna, svo sem áætlaðan upphafsdag/-tíma og endurtekningatexta.</span><span class="sxs-lookup"><span data-stu-id="da607-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="da607-153">Eftirfarandi mynd sýnir dæmi um upplýsingar um runuvinnsluna í Retail þegar áætlað er að runuvinnslan gangi með tveggja tíma millibili.</span><span class="sxs-lookup"><span data-stu-id="da607-153">The following illustration shows an example of the batch job details in Retail when the batch job is scheduled to run at two-hour intervals.</span></span>

![Upplýsingar um runuvinnsluna Samstilla afurðaeinkunnir](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="da607-155">Gerðu afurðaeinkunnir tiltækar í POS</span><span class="sxs-lookup"><span data-stu-id="da607-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="da607-156">Leiðbeiningar fyrir einkunnir og umsagnir í Dynamics 365 Commerce er alhliða lausn.</span><span class="sxs-lookup"><span data-stu-id="da607-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="da607-157">Hins vegar eru afurðaeinkunnir ekki sjálfgefið sýndar í POS.</span><span class="sxs-lookup"><span data-stu-id="da607-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="da607-158">Til að hjálpa viðskiptavinum í verslunum að sjá einkunnir og umsagnir þegar þeir fá hjálp við söluaðilum verður þú að kveikja á afurðaeinkunnum í POS.</span><span class="sxs-lookup"><span data-stu-id="da607-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="da607-159">Til að kveikja á afurðaeinkunnum á sölustað skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="da607-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="da607-160">Opnið **Retail \> Uppsetning Retail \> Færibreytur \> Smásölufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="da607-160">Go to **Retail \> Retail setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="da607-161">Einnig er hægt að leita að „Smásölubreytum“.</span><span class="sxs-lookup"><span data-stu-id="da607-161">Alternatively, search for "Retail parameters."</span></span>
1. <span data-ttu-id="da607-162">Á flipanum **Stillingafæribreytur** velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="da607-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="da607-163">Sláðu inn heiti eins og **RatingsAndReviews.EnableProductRatingsForRetailStores** og stilltu gildið á **satt**.</span><span class="sxs-lookup"><span data-stu-id="da607-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="da607-164">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="da607-164">Select **Save**.</span></span>
1. <span data-ttu-id="da607-165">Farðu í **Retail \> Upplýsingatækni smásölu \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="da607-165">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span> <span data-ttu-id="da607-166">Að öðrum kosti leitarðu að „Dreifingaráætlun.“</span><span class="sxs-lookup"><span data-stu-id="da607-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="da607-167">Á vinnslulistanum velurðu **1110** (**Altækar stillingar**) og velur síðan **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="da607-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="da607-168">Þegar vinnslan hefur keyrt skaltu staðfesta að afurðaeinkunnir séu núna sýndar á sölustað.</span><span class="sxs-lookup"><span data-stu-id="da607-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="da607-169">Eftirfarandi mynd sýnir dæmi um stillingu Retail-færibreytanna til að kveikja á afurðaeinkunnum á sölustað.</span><span class="sxs-lookup"><span data-stu-id="da607-169">The following illustration shows an example of the configuration of the Retail parameters to turn on product ratings at the POS.</span></span>

![Stillingar Retail-færibreytanna fyrir afurðaeinkunnir á sölustað](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="da607-171">Eftirfarandi skýringarmynd sýnir dæmi um afurðaeinkunnir á sölustað.</span><span class="sxs-lookup"><span data-stu-id="da607-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Afurðaeinkunnir á sölustað](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="da607-173">Eftirfarandi skýringarmynd sýnir dæmi um afurðaeinkunnir á rásum símavera.</span><span class="sxs-lookup"><span data-stu-id="da607-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Afurðaeinkunnir í rás símaþjónustuvers](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="da607-175">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="da607-175">Additional resources</span></span>

[<span data-ttu-id="da607-176">Yfirlit yfir einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="da607-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="da607-177">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="da607-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="da607-178">Stjórna einkunnum og umsögnum</span><span class="sxs-lookup"><span data-stu-id="da607-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="da607-179">Skilgreina einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="da607-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
