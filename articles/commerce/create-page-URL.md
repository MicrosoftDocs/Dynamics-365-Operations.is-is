---
title: Búa til síðuvefslóð
description: Þetta efni fjallar um grunnhugtök og verklagsreglur við að búa til vefslóð á síðuna þína.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98743d8948669f32d3c74e1915c7ed53db81141c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795692"
---
# <a name="create-a-page-url"></a><span data-ttu-id="48caf-103">Búa til síðuvefslóð</span><span class="sxs-lookup"><span data-stu-id="48caf-103">Create a page URL</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48caf-104">Þetta efni fjallar um grunnhugtök og verklagsreglur við að búa til vefslóð á síðuna þína.</span><span class="sxs-lookup"><span data-stu-id="48caf-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

<span data-ttu-id="48caf-105">Vefslóðin í heild eða alger sem vísar á síðu á vefsvæðinu þínu samanstendur af aðskildum hlutum.</span><span class="sxs-lookup"><span data-stu-id="48caf-105">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="48caf-106">Til dæmis slóðin hefur `https://www.contoso.com/en-us/contactus` eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="48caf-106">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="48caf-107">`https://www.contoso.com` - HTTP samskiptareglur og lén svæðisins.</span><span class="sxs-lookup"><span data-stu-id="48caf-107">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="48caf-108">`/en-us`- Tungumálaslóð vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="48caf-108">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="48caf-109">`/contactus` - Tengd slóð fyrir síðuna **Hafa samband**.</span><span class="sxs-lookup"><span data-stu-id="48caf-109">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="48caf-110">Tengd slóð er einnig þekkt sem slóð *snigill*.</span><span class="sxs-lookup"><span data-stu-id="48caf-110">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="48caf-111">Þú setur upp lén vefsvæðisins og valfrjálsa tungumálaslóð þegar þú setur vefsvæðið upp.</span><span class="sxs-lookup"><span data-stu-id="48caf-111">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="48caf-112">Þú getur bætt við fleiri lénum og tungumálaslóðum á vefsvæðið í gegnum netverslunarsíðu í stillingum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="48caf-112">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="48caf-113">Slóðarsnigill fyrir síðu er til sem sjálfstæð eining í höfundarumhverfi.</span><span class="sxs-lookup"><span data-stu-id="48caf-113">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="48caf-114">Vefslóð síðu samanstendur af tveimur hlutum: heiti sem táknar slóðarsnigil og bendil á síðu á annaðhvort vefsvæðinu eða utanaðkomandi síðu.</span><span class="sxs-lookup"><span data-stu-id="48caf-114">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="48caf-115">Einnig er hægt að stilla vefslóð síðu til að virka sem tilvísun á aðra síðu á annaðhvort vefsvæðinu eða utanaðkomandi vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="48caf-115">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="48caf-116">Búa til síðuvefslóð</span><span class="sxs-lookup"><span data-stu-id="48caf-116">Create a page URL</span></span>

<span data-ttu-id="48caf-117">Það eru tvær leiðir til að búa til vefslóðir:</span><span class="sxs-lookup"><span data-stu-id="48caf-117">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="48caf-118">Sjálfkrafa þegar þú býrð til síðu</span><span class="sxs-lookup"><span data-stu-id="48caf-118">Automatically, when you create a page</span></span>
- <span data-ttu-id="48caf-119">Handvirkt af síðunni **Vefslóðir**</span><span class="sxs-lookup"><span data-stu-id="48caf-119">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="48caf-120">Stofna vefslóð síðu þegar þú býrð til síðu</span><span class="sxs-lookup"><span data-stu-id="48caf-120">Create a page URL when you create a page</span></span>

<span data-ttu-id="48caf-121">Ef þú gefur upp heiti í reitinn **Vefslóð** þegar þú býrð til nýja síðu verður vefslóð síðu sem vísar á þá síðu sjálfkrafa stofnuð á síðunni **Vefslóðir**.</span><span class="sxs-lookup"><span data-stu-id="48caf-121">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="48caf-122">Eftir að þú hefur birt slóðina og síðuna sem hún vísar á geta notendur vefsvæða (viðskiptavinir þínir) fengið aðgang að síðunni sem er tengd slóðinni.</span><span class="sxs-lookup"><span data-stu-id="48caf-122">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="48caf-123">Ef þú birtir vefslóð án þess að birta síðuna sem hún vísar á fá notendur vefsvæðis 404-villu þegar þeir reyna að komast á síðuna.</span><span class="sxs-lookup"><span data-stu-id="48caf-123">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="48caf-124">Ef þú birtir síðu án þess að birta slóðina sem vísar á hana er ekki hægt að komast á síðuna með því að nota slóð.</span><span class="sxs-lookup"><span data-stu-id="48caf-124">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="48caf-125">Stofna síðuvefslóð handvirkt</span><span class="sxs-lookup"><span data-stu-id="48caf-125">Manually create a page URL</span></span>

<span data-ttu-id="48caf-126">Þegar þú stofnar nýjar síður þarf ekki að tilgreina vefslóð síðu.</span><span class="sxs-lookup"><span data-stu-id="48caf-126">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="48caf-127">Ef þú skilur vefslóðarreitinn eftir auðan er síðan búin til í óbundinni stöðu.</span><span class="sxs-lookup"><span data-stu-id="48caf-127">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="48caf-128">Í þessu tilfelli geta viðskiptavinir ekki fengið aðgang að síðunni, jafnvel þó að hún sé birt.</span><span class="sxs-lookup"><span data-stu-id="48caf-128">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="48caf-129">Til að gera síðuna aðgengilega verður þú að búa til slóðina handvirkt og tengja hana við síðuna.</span><span class="sxs-lookup"><span data-stu-id="48caf-129">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="48caf-130">Fylgdu þessum skrefum til að búa til síðuslóðina á handvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="48caf-130">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="48caf-131">Á síðunni **Vefslóðir** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="48caf-131">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="48caf-132">Veljið síðu á vefsvæði til að tengja við vefslóðina.</span><span class="sxs-lookup"><span data-stu-id="48caf-132">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="48caf-133">Sláðu inn slóðarsnigilinn og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="48caf-133">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="48caf-134">Á þessum tímapunkti er vefslóðin í drögum.</span><span class="sxs-lookup"><span data-stu-id="48caf-134">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="48caf-135">Það verður að birta áður en notendur vefsvæða geta nálgast viðkomandi síðu.</span><span class="sxs-lookup"><span data-stu-id="48caf-135">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="48caf-136">Uppfæra síðuvefslóð</span><span class="sxs-lookup"><span data-stu-id="48caf-136">Update a page URL</span></span>

<span data-ttu-id="48caf-137">Fylgdu þessum skrefum til að uppfæra markmiðasíðu síðuvefslóðar.</span><span class="sxs-lookup"><span data-stu-id="48caf-137">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="48caf-138">Á síðunni **Vefslóðir** velurðu slóðina sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="48caf-138">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="48caf-139">Í eiginleikaglugganum til hægri velurðu úrfellingarhnappinn (**...**) við hliðina á marksíðureitnum.</span><span class="sxs-lookup"><span data-stu-id="48caf-139">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="48caf-140">Í svarglugganum velurðu aðra síðu og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="48caf-140">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="48caf-141">Vistaðu og birtu vefslóðina.</span><span class="sxs-lookup"><span data-stu-id="48caf-141">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="48caf-142">Framsendingarslóð síðu</span><span class="sxs-lookup"><span data-stu-id="48caf-142">Redirect a page URL</span></span>

<span data-ttu-id="48caf-143">Stundum gætirðu viljað að viðskiptavinir þínir skoði aðra síðu þegar þeir biðja um sérstaka slóð.</span><span class="sxs-lookup"><span data-stu-id="48caf-143">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="48caf-144">Í þessum tilvikum er besta og auðveldasta aðferðin oft að breyta síðunni sem vefslóð síðunnar bendir á.</span><span class="sxs-lookup"><span data-stu-id="48caf-144">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="48caf-145">Hins vegar gætir þú haft réttmætar ástæður fyrir því að nota tilvísanir HTTP 301 eða 3023 til að beina beiðnum um vefslóð yfir á aðra slóð.</span><span class="sxs-lookup"><span data-stu-id="48caf-145">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="48caf-146">Fylgdu þessum skrefum til að beina vefslóðinni yfir á aðra slóð.</span><span class="sxs-lookup"><span data-stu-id="48caf-146">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="48caf-147">Á síðunni **Vefslóðir** velurðu slóðina sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="48caf-147">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="48caf-148">Í eiginleikaglugganum til hægri velurðu **Framsenda**.</span><span class="sxs-lookup"><span data-stu-id="48caf-148">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="48caf-149">Veldu áfangastað fyrir framsendinuna:</span><span class="sxs-lookup"><span data-stu-id="48caf-149">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="48caf-150">Til að benda á aðra síðu á vefsvæðinu velurðu **Innri vefslóð**, velur sporbaugshnappinn (**...**) og velur síðan slóðina sem á að framsenda á.</span><span class="sxs-lookup"><span data-stu-id="48caf-150">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="48caf-151">Til að benda á síðu á ytra vefsvæði velurðu **Ytri vefslóð** og velur síðan fulla vefslóð fyrir þá síðu.</span><span class="sxs-lookup"><span data-stu-id="48caf-151">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="48caf-152">Vertu viss um að hafa samskiptareglur með.</span><span class="sxs-lookup"><span data-stu-id="48caf-152">Be sure to include the protocol.</span></span> <span data-ttu-id="48caf-153">Til dæmis er slegið inn `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="48caf-153">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="48caf-154">Ef vefslóðin framsendir þegar á innri vefslóð verður þú að velja **Hreinsa val** áður en þú getur slegið inn ytri slóð.</span><span class="sxs-lookup"><span data-stu-id="48caf-154">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="48caf-155">Veldu framsendingargerð:</span><span class="sxs-lookup"><span data-stu-id="48caf-155">Select a redirect type:</span></span>

    - <span data-ttu-id="48caf-156">**Varanleg tilvísun (301)** - Veldu þennan valkost þegar þú veist að innihaldið er að flytja til frambúðar og mun ekki snúa aftur á fyrri slóðina.</span><span class="sxs-lookup"><span data-stu-id="48caf-156">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="48caf-157">Leitarvélar munu úthluta SEO-gildi leitarvélabestunar framsendingarslóðarinnar á vefslóðina sem framsent er á og uppfæra skrár til að sýna nýju slóðina.</span><span class="sxs-lookup"><span data-stu-id="48caf-157">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="48caf-158">**Tímabundin framsending (302)** - Veldu þennan valkost til að framsenda umferð án þess að uppfæra leitarvélar.</span><span class="sxs-lookup"><span data-stu-id="48caf-158">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="48caf-159">Þessi aðferð er venjulega notuð ef innihaldið mun brátt snúa aftur til fyrri slóðina.</span><span class="sxs-lookup"><span data-stu-id="48caf-159">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="48caf-160">Þegar þú ert tilbúin/n til að framkvæma framsendinguna skaltu vista og birta slóðina.</span><span class="sxs-lookup"><span data-stu-id="48caf-160">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48caf-161">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="48caf-161">Additional resources</span></span>

[<span data-ttu-id="48caf-162">Sérstilla yfirlit svæðis</span><span class="sxs-lookup"><span data-stu-id="48caf-162">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="48caf-163">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="48caf-163">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="48caf-164">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="48caf-164">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="48caf-165">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="48caf-165">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
