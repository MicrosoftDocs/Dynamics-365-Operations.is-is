---
title: Hlaða upp og þjóna föstum skrám
description: Þetta efnisatriði lýsir því hvernig á að hlaða upp fastri skrá í Microsoft Dynamics 365 Commerce vefsmið, og hvernig á að búa til sérstillt URL og skráarheiti sem hægt er að nota til að óska eftir skránni.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594973"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="f4586-103">Hlaða upp og þjóna föstum skrám</span><span class="sxs-lookup"><span data-stu-id="f4586-103">Upload and serve static files</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f4586-104">Þetta efnisatriði lýsir því hvernig á að hlaða upp fastri skrá í Microsoft Dynamics 365 Commerce vefsmið, og hvernig á að búa til sérstillt URL og skráarheiti sem hægt er að nota til að óska eftir skránni.</span><span class="sxs-lookup"><span data-stu-id="f4586-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="f4586-105">Sumir tenglar þriðja aðila krefjast þess að skrá sé hýst og henni sé miðlað á svæði fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="f4586-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="f4586-106">Þessir tenglar búast við því að skránni verði skilað með beiðnum á tiltekna vefslóð svarhringingar og skráarheiti.</span><span class="sxs-lookup"><span data-stu-id="f4586-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="f4586-107">Þess vegna útskýrir Þetta efnisatriði hvernig á að hlaða upp og setja upp fasta skrá sem er með URL sem notandi getur skilgreint og skráarheiti á Dynamics 365 Commerce svæði fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="f4586-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="f4586-108">Stofna vefslóð svæðis sem skilar fastri skrá</span><span class="sxs-lookup"><span data-stu-id="f4586-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="f4586-109">Til að búa til URL svæðis sem skilar fastri skrá í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f4586-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f4586-110">Farið á miðlasafn vefsvæðis og hlaðið upp skránni sem á að birtast fyrir beiðnir á URL sem er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="f4586-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="f4586-111">Ef þú hefur þegar hlaðið upp skránni geturðu sleppt þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="f4586-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="f4586-112">Opnaðu **vefslóð** fyrir vefsvæðið þitt.</span><span class="sxs-lookup"><span data-stu-id="f4586-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="f4586-113">Veljið **Nýtt \> Ný vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="f4586-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="f4586-114">Í svarglugganum **Ný vefslóð** skal velja **Miðlasafn**.</span><span class="sxs-lookup"><span data-stu-id="f4586-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="f4586-115">Í reitinn **Vefslóð** skal slá inn vefslóðina.</span><span class="sxs-lookup"><span data-stu-id="f4586-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="f4586-116">Hafðu skráarheitið með í slóðinni.</span><span class="sxs-lookup"><span data-stu-id="f4586-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="f4586-117">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="f4586-117">Select **Next**.</span></span> <span data-ttu-id="f4586-118">Miðlasafnið er opnað og sýnir allar miðlaeignir af gerðinni **skjal** sem hefur verið hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="f4586-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="f4586-119">Veljið skrána sem á að nota fyrir beiðnir á vefslóðina sem var skilgreind í skrefi 5.</span><span class="sxs-lookup"><span data-stu-id="f4586-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="f4586-120">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f4586-120">Select **Save**.</span></span>

<span data-ttu-id="f4586-121">Á þessu stigi hefur vefslóðin sem var stofnuð stöðuna drög.</span><span class="sxs-lookup"><span data-stu-id="f4586-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="f4586-122">Skránni sem vefslóðin bendir á verður ekki skilað fyrr en vefslóðin er birt.</span><span class="sxs-lookup"><span data-stu-id="f4586-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="f4586-123">Áður en vefslóðin er birt er hægt að staðfesta að hún skili réttum gögnum.</span><span class="sxs-lookup"><span data-stu-id="f4586-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="f4586-124">Villuleita og birta vefslóð</span><span class="sxs-lookup"><span data-stu-id="f4586-124">Validate and publish a URL</span></span>

<span data-ttu-id="f4586-125">Til að villuleita vefslóð áður en hún er birt skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f4586-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="f4586-126">Opnaðu **vefslóð** fyrir svæðið þitt og veldu vefslóðina sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="f4586-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="f4586-127">Á eiginleikasvæðinu hægra megin, fyrir neðan hnappinn **Breyta**, skal velja réttan tengil ULR.</span><span class="sxs-lookup"><span data-stu-id="f4586-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="f4586-128">Nýr vafragluggi opnast og villan 404 ætti að birtast.</span><span class="sxs-lookup"><span data-stu-id="f4586-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="f4586-129">Bætið við **?preview=inprogress** fyrirspurnarstrengnum á URL (til dæmis `https://yoursite.com/callback.html?preview=inprogress`) og endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="f4586-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="f4586-130">Skráin sem var hlaðið upp í miðlasafnið ætti að vera skilað í svarinu.</span><span class="sxs-lookup"><span data-stu-id="f4586-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="f4586-131">Þegar vefslóð hefur verið staðfest er hægt að birta hana.</span><span class="sxs-lookup"><span data-stu-id="f4586-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="f4586-132">Opnaðu **vefslóð** fyrir svæðið þitt og veldu vefslóðina.</span><span class="sxs-lookup"><span data-stu-id="f4586-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="f4586-133">Á skipanastikunni skal velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="f4586-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="f4586-134">Uppfærið skrána sem vefslóðin bendir á</span><span class="sxs-lookup"><span data-stu-id="f4586-134">Update the file that a URL points to</span></span>

<span data-ttu-id="f4586-135">Eftir að vefslóðin hefur verið birt er hægt að uppfæra hana þannig að hún vísar í aðra skrá.</span><span class="sxs-lookup"><span data-stu-id="f4586-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="f4586-136">Að öðrum kosti er hægt að uppfæra vefslóðina þannig að hún bendir á aðra gerð tilfanga, eins og lýst er í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="f4586-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="f4586-137">Til dæmis er hægt að láta vefslóð vísa á innri síðu eða framsendingu.</span><span class="sxs-lookup"><span data-stu-id="f4586-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="f4586-138">Til að uppfæra skrána sem vefslóðin bendir á skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f4586-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="f4586-139">Farið á **Vefslóð** fyrir svæðið og veljið vefslóðina sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="f4586-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="f4586-140">Í eiginleikastikunni hægra megin skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="f4586-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="f4586-141">Undir **Úthlutun vefslóðar** skal velja reitinn **Skref 2** og síðan velja nýtt skjal úr miðlasafninu.</span><span class="sxs-lookup"><span data-stu-id="f4586-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="f4586-142">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f4586-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="f4586-143">Uppfæra eignagerðina sem vefslóðin bendir á</span><span class="sxs-lookup"><span data-stu-id="f4586-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="f4586-144">Einnig er hægt að uppfæra vefslóðin þannig að hún vísar í aðra gerð eignar (tilfang), t.d. innri síðu eða framsendingu.</span><span class="sxs-lookup"><span data-stu-id="f4586-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="f4586-145">Til að uppfæra eignagerð sem vefslóðin bendir á skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f4586-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="f4586-146">Farið á **Vefslóð** fyrir svæðið og veljið vefslóðina sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="f4586-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="f4586-147">Í eiginleikastikunni hægra megin skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="f4586-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="f4586-148">Undir **Úthlutun vefslóðar**, undir **Skref 1**, skal velja aðra eignagerð.</span><span class="sxs-lookup"><span data-stu-id="f4586-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="f4586-149">Veljið gátreitinn **Skref 2** og veljið síðan nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="f4586-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="f4586-150">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f4586-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="f4586-151">Breyta vefslóð</span><span class="sxs-lookup"><span data-stu-id="f4586-151">Change the URL path</span></span>

<span data-ttu-id="f4586-152">Þegar búið er að stofna vefslóð er ekki hægt að breyta slóð hennar.</span><span class="sxs-lookup"><span data-stu-id="f4586-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="f4586-153">Ef nauðsynlegt er að breyta vefslóð sem þjónar skrá eða öðrum gerðum tilfanga þarf að stofna nýja vefslóð, varpa henni á fyrirliggjandi skrá eða önnur tilföng, taka hana úr birtingu og eyða svo gömlu vefslóðinni.</span><span class="sxs-lookup"><span data-stu-id="f4586-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="f4586-154">Til að breyta vefslóð skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f4586-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="f4586-155">Til að búa til nýtt URL og varpa því á fyrirliggjandi skrá eða annað tilfang skal fylgja leiðbeiningunum í hlutanum [Stofna vefslóð svæðis sem skilar fastri skrá](#create-a-site-url-that-returns-a-static-file) fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="f4586-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="f4586-156">Velja skal nýju vefslóðina og velja **Birta** á skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="f4586-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="f4586-157">Nýja vefslóðin er birt.</span><span class="sxs-lookup"><span data-stu-id="f4586-157">The new URL is published.</span></span>
1. <span data-ttu-id="f4586-158">Til að opna gömlu vefslóðina skal velja hana og velja svo **Taka úr birtingu** á skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="f4586-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="f4586-159">Nú er hægt að eyða eldri vefslóð ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="f4586-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4586-160">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f4586-160">Additional resources</span></span>

[<span data-ttu-id="f4586-161">Yfirlit stjórnunar stafrænna eigna</span><span class="sxs-lookup"><span data-stu-id="f4586-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="f4586-162">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="f4586-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="f4586-163">Hlaða upp myndskeiðum</span><span class="sxs-lookup"><span data-stu-id="f4586-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="f4586-164">Hlaða upp skrám öðrum en myndum og myndböndum</span><span class="sxs-lookup"><span data-stu-id="f4586-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="f4586-165">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="f4586-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="f4586-166">Sérstilla áherslupunkta myndar</span><span class="sxs-lookup"><span data-stu-id="f4586-166">Customize image focal points</span></span>](dam-custom-focal-point.md)
