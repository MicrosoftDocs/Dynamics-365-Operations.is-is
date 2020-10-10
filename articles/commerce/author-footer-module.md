---
title: Neðanmálseining
description: Þetta efni fjallar um neðanmálseiningar og hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 42a71ea9498461febca80952acc3158517918332
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816962"
---
# <a name="footer-module"></a><span data-ttu-id="5ade9-103">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="5ade9-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ade9-104">Þetta efni fjallar um neðanmálseiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5ade9-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5ade9-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5ade9-105">Overview</span></span>

<span data-ttu-id="5ade9-106">Neðanmálseiningin er sérstakur gámur sem er notaður til að hýsa einingarnar sem birtast í síðufætinum.</span><span class="sxs-lookup"><span data-stu-id="5ade9-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="5ade9-107">Til dæmis getur hún innihaldið tengla á ýmsar síður á vefsvæðinu, eins og síðurnar **Hafa samband** og **Stefna verslunar**.</span><span class="sxs-lookup"><span data-stu-id="5ade9-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="5ade9-108">Eftirfarandi mynd sýnir dæmi um neðanmálseiningu á síðu svæðis.</span><span class="sxs-lookup"><span data-stu-id="5ade9-108">The following image shows an example of a footer module on a site page.</span></span>

![Dæmi um neðanmálseiningu](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="5ade9-110">Eiginleikar neðanmálseiningar</span><span class="sxs-lookup"><span data-stu-id="5ade9-110">Footer module properties</span></span> 

<span data-ttu-id="5ade9-111">Eins og á við um flesta gáma, styður neðanmálseiningin eiginleika fyrir fyrirsögnina og breiddina.</span><span class="sxs-lookup"><span data-stu-id="5ade9-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="5ade9-112">Hún styður einnig að bæta við mörgum einingum neðanmálsflokka.</span><span class="sxs-lookup"><span data-stu-id="5ade9-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="5ade9-113">Hver eining neðanmálsflokks sem er bætt við er gerð sem dálkur í neðanmálseiningunni.</span><span class="sxs-lookup"><span data-stu-id="5ade9-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="5ade9-114">Einingar eru fáanlegar í neðanmálseiningunni</span><span class="sxs-lookup"><span data-stu-id="5ade9-114">Modules available in a footer module</span></span>

<span data-ttu-id="5ade9-115">**Neðanmálsatriði** - Eining neðanmálsatriða getur innihaldið fyrirsögn, mynd og tengil.</span><span class="sxs-lookup"><span data-stu-id="5ade9-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="5ade9-116">Hægt er að nota fyrirsögnina annaðhvort staka eða í samsetningu með mynd og tengli.</span><span class="sxs-lookup"><span data-stu-id="5ade9-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="5ade9-117">Hægt er að stilla hvern tengil í neðanmálinu þannig að hann hafi bara texta (til dæmis tenglana „Hafðu samband“ og „Persónuvernd“), eða þannig að hann hafi bæði texta og mynd (til dæmis tengla á samfélagsmiðlum).</span><span class="sxs-lookup"><span data-stu-id="5ade9-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="5ade9-118">**Efst á síðu** - Einingin Efst á síðu veitir tengil fyrir fljótlega flettingu efst á síðuna.</span><span class="sxs-lookup"><span data-stu-id="5ade9-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="5ade9-119">Áfangastaðar er krafist.</span><span class="sxs-lookup"><span data-stu-id="5ade9-119">A destination is required.</span></span> <span data-ttu-id="5ade9-120">Sjálfgefið gildi áfangastaðar er \#, sem fer með notandann efst á síðuna.</span><span class="sxs-lookup"><span data-stu-id="5ade9-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="5ade9-121">Búa til neðanmálseiningu</span><span class="sxs-lookup"><span data-stu-id="5ade9-121">Create a footer module</span></span>

1. <span data-ttu-id="5ade9-122">Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="5ade9-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="5ade9-123">Í glugganum **Nýtt brot** skal velja eininguna **Hólf**, slá inn heiti fyrir brotið og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5ade9-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="5ade9-124">Í hólfinu **Sjálfgefið hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="5ade9-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5ade9-125">Í glugganum **Bæta við einingu** skal velja eininguna **Neðanmálsflokkur** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5ade9-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5ade9-126">Í hólfinu **Neðanmálsflokkur** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="5ade9-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5ade9-127">Í glugganum **Bæta við einingu** skal velja eininguna **Neðanmálsatriði** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5ade9-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5ade9-128">Veldu hólfið **Neðanmálsatriði** og síðan, hægra megin á eiginleikasvæðinu, skal stilla fyrirsögnina, tengil og texta tengils og mynd eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="5ade9-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="5ade9-129">Til að bæta við fleiri neðanmálsatriðum skal endurtaka skref 5 til 7.</span><span class="sxs-lookup"><span data-stu-id="5ade9-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="5ade9-130">Til að bæta tenglinum „efst á síðu“ í neðanmáli skal velja úrfellingarmerkið (**...**) í hólfinu **Neðanmálsflokkur** og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="5ade9-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="5ade9-131">Í glugganum **Bæta við einingu** skal velja eininguna **Efst á síðu** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5ade9-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5ade9-132">Veldu hólfið **Efst á síðu** og síðan, hægra megin á eiginleikasvæðinu, skal stilla textann og aðrar eiginleikaeiningar eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="5ade9-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="5ade9-133">Veldu **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="5ade9-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="5ade9-134">Til að tryggja að haus birtist á hverri síðu, fylgdu þessum skrefum á hverju síðusniðmáti sem er búið til fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="5ade9-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="5ade9-135">Í hólfinu **Neðanmál** í einingunni **Sjálfgefin síða** skal bæta við neðanmálsbrotinu sem var búið til.</span><span class="sxs-lookup"><span data-stu-id="5ade9-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="5ade9-136">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="5ade9-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="5ade9-137">Með því að bæta broti við síðusniðmát hjálpar þú til við að tryggja að fóturinn birtist á hverri síðu.</span><span class="sxs-lookup"><span data-stu-id="5ade9-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ade9-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5ade9-138">Additional resources</span></span>

[<span data-ttu-id="5ade9-139">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="5ade9-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5ade9-140">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="5ade9-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5ade9-141">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="5ade9-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5ade9-142">Körfueining</span><span class="sxs-lookup"><span data-stu-id="5ade9-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5ade9-143">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="5ade9-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5ade9-144">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="5ade9-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5ade9-145">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="5ade9-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5ade9-146">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="5ade9-146">Footer module</span></span>](author-footer-module.md)
