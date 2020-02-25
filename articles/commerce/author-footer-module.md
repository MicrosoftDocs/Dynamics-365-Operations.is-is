---
title: Neðanmálseining
description: Þetta efni fjallar um neðanmálseiningar og hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001153"
---
# <a name="footer-module"></a><span data-ttu-id="4e7c6-103">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="4e7c6-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="4e7c6-104">Þetta efni fjallar um neðanmálseiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4e7c6-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4e7c6-105">Overview</span></span>

<span data-ttu-id="4e7c6-106">Neðanmálseiningin er sérstakur gámur sem er notaður til að hýsa einingarnar sem birtast í síðufætinum.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="4e7c6-107">Til dæmis getur hún innihaldið tengla á ýmsar síður á vefsvæðinu, eins og síðurnar **Hafa samband** og **Stefna verslunar**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="4e7c6-108">Eiginleikar neðanmálseiningar</span><span class="sxs-lookup"><span data-stu-id="4e7c6-108">Footer module properties</span></span> 

<span data-ttu-id="4e7c6-109">Eins og flestir gámar, styður neðanmálseining eiginleika fyrir fyrirsögnina og breiddina.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="4e7c6-110">Hún styður einnig að bæta við mörgum einingum neðanmálsflokka.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="4e7c6-111">Hver eining neðanmálsflokks sem er bætt við er gerð sem dálkur í neðanmálseiningunni.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="4e7c6-112">Einingar eru fáanlegar í neðanmálseiningunni</span><span class="sxs-lookup"><span data-stu-id="4e7c6-112">Modules available in a footer module</span></span>

<span data-ttu-id="4e7c6-113">**Neðanmálsatriði** - Eining neðanmálsatriða getur innihaldið fyrirsögn, mynd og tengil.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="4e7c6-114">Hægt er að nota fyrirsögnina annaðhvort staka eða í samsetningu með mynd og tengli.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="4e7c6-115">Hægt er að stilla hvern tengil í neðanmálinu þannig að hann hafi bara texta (til dæmis tenglana „Hafðu samband“ og „Persónuvernd“), eða þannig að hann hafi bæði texta og mynd (til dæmis tengla á samfélagsmiðlum).</span><span class="sxs-lookup"><span data-stu-id="4e7c6-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="4e7c6-116">**Efst á síðu** - Einingin Efst á síðu veitir tengil fyrir fljótlega flettingu efst á síðuna.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="4e7c6-117">Áfangastaðar er krafist.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-117">A destination is required.</span></span> <span data-ttu-id="4e7c6-118">Sjálfgefið áfangastaðargildi er # sem sendir notandann efst á síðuna.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="4e7c6-119">Stofna neðanmálseiningu</span><span class="sxs-lookup"><span data-stu-id="4e7c6-119">Author a footer module</span></span>

1. <span data-ttu-id="4e7c6-120">Í leiðsagnarglugganum velurðu **Brot** og velur síðan **Nýtt síðubrot**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="4e7c6-121">Í valmyndinni **Nýtt síðubrot** velurðu neðanmálseininguna, sláðu inn heiti fyrir síðubrotið og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="4e7c6-122">Í útlínutrénu til vinstri velurðu úrfellingarhnappinn (**...**) fyrir neðanmálseininguna og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4e7c6-123">Í valmyndinni **Bæta við einingu** velurðu neðanmálsflokkseiningu og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="4e7c6-124">Í útlínutrénu velurðu úrfellingarhnappinn fyrir neðanmálsflokkseininguna og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4e7c6-125">Í valmyndinni **Bæta við einingu** velurðu neðanmálsliðareiningu og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="4e7c6-126">Í útlínutrénu velurðu neðanmálsliðareininguna.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="4e7c6-127">Síðan skaltu stilla fyrirsögnina, tengja og tengja texta og mynd eins og þú þarfnast í eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="4e7c6-128">Til að bæta við fleiri neðanmálsliðum skaltu endurtaka skref 5 til og með 7.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="4e7c6-129">Til að bæta við tenglinum „Efst á síðu“ velurðu úrfellingarhnappinn fyrir neðanmálsflokkseininguna og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4e7c6-130">Í valmyndinni **Bæta við einingu** velurðu eininguna Efst á síðu og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="4e7c6-131">Í útlínutrénu velurðu eininguna Efst á síðu.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="4e7c6-132">Síðan skaltu stilla eininguna Efst á síðu í eiginleikaglugganum til hægri eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="4e7c6-133">Vistaðu síðusagnarbrotið, skráðu það inn og gefðu það út.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="4e7c6-134">Fylgdu þessum skrefum á hvert síðusniðmát sem búið er til fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="4e7c6-135">Í hólfinu **Aðal** á sjálfgefnu síðunni, í neðanmálseiningunni skaltu bæta við neðanmálsbrotinu sem þú bjóst til.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="4e7c6-136">Vistaðu sniðmátið, athugaðu það og gefðu það út.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="4e7c6-137">Með því að bæta síðusniðinu við síðusniðmát tryggirðu að neðanmálið sé sett á hverja síðu.</span><span class="sxs-lookup"><span data-stu-id="4e7c6-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e7c6-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4e7c6-138">Additional resources</span></span>

[<span data-ttu-id="4e7c6-139">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="4e7c6-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4e7c6-140">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="4e7c6-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4e7c6-141">Kaupkassaeining</span><span class="sxs-lookup"><span data-stu-id="4e7c6-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4e7c6-142">Körfueining</span><span class="sxs-lookup"><span data-stu-id="4e7c6-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4e7c6-143">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="4e7c6-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4e7c6-144">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="4e7c6-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4e7c6-145">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="4e7c6-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4e7c6-146">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="4e7c6-146">Footer module</span></span>](author-footer-module.md)
