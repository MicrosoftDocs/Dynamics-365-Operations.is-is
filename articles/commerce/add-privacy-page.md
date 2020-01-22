---
title: Bæt við síðu persónuverndarstefnu
description: Þetta efni lýsir því hvernig á að bæta síðu persónuverndarstefnu við á vefsvæði í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946031"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="f4d2b-103">Bæt við síðu persónuverndarstefnu</span><span class="sxs-lookup"><span data-stu-id="f4d2b-103">Add a privacy policy page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f4d2b-104">Þetta efni lýsir því hvernig á að bæta síðu persónuverndarstefnu við á vefsvæði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f4d2b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f4d2b-105">Overview</span></span>

<span data-ttu-id="f4d2b-106">Fylgni við friðhelgi einkalífsins felur í sér skipulagsaðgerðir sem upplýsa notendur vefsins um hvernig gögnum þeirra er safnað og meðhöndlað.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="f4d2b-107">Notendur geta síðan ákveðið hvernig þeir vilja að farið verði með persónuupplýsingar sínar og gripið til viðeigandi ráðstafana.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="f4d2b-108">Lestu yfirlýsingu Microsoft um persónuvernd í Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f4d2b-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="f4d2b-109">Til að fara yfir persónuverndaryfirlýsingu Microsoft meðan þú ert innskráð/ur í Dynamics 365 Commerce höfundatól, veldu hnappinn **Hjálp** (**?**) efst í hægra horninu og veldu síðan **Persónuvernd og kökur**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="f4d2b-110">Nýr flipi er opnaður sem hefur tengil á [Persónuverndaryfirlýsingu Microsoft](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="f4d2b-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="f4d2b-111">Búðu til síðu með persónuverndarstefnu fyrir síðuna þína</span><span class="sxs-lookup"><span data-stu-id="f4d2b-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="f4d2b-112">Í Dynamics 365 Commerce eru nokkrar leiðir til að veita notendum vefsvæðisins aðgang að persónuverndarstefnu þinni.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="f4d2b-113">Þessi hluti sýnir hvernig á að byggja upp persónuverndarstefnusíðu og vísa síðan á síðuna með því að nota síðufótarbrot.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="f4d2b-114">Leiðbeiningarnar sem fylgja eru dæmi sem sýnir hvernig á að smíða almenna persónuverndarstefnusíðu fyrir viðskiptasíðu.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="f4d2b-115">Þú berð ábyrgð á því að hanna og útfæra lausn á persónuverndarstefnu sem best uppfyllir lagalegar kröfur fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="f4d2b-116">Til að hefjast handa skaltu í höfundatækjunum fara á síðuna sem þú vilt byggja upp persónuverndarstefnusíðu fyrir.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="f4d2b-117">Búa til sniðmát</span><span class="sxs-lookup"><span data-stu-id="f4d2b-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="f4d2b-118">Ef sniðmát sem hægt er að nota fyrir persónuverndarstefnusíðuna hefur þegar verið stofnað skaltu fara beint áfram í kaflann [Búa til síðu með persónuverndarstefnu](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="f4d2b-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="f4d2b-119">Fylgið eftirfarandi skrefum til að stofna sniðmát.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="f4d2b-120">Farðu í **Sniðmát \> Nýtt sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="f4d2b-121">Sláðu inn heiti sniðmáts og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="f4d2b-122">Í sniðmátinu skaltu bæta við þeim einingum sem þarf í þar til gerð hólf á síðunni.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="f4d2b-123">Til leiðbeiningar skaltu halda músabendlinum yfir rauðu upphrópunarmerkjunum.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="f4d2b-124">Til dæmis kann hólfið **HTML-haus** að krefjast einingarinnar **Sjálfvirk ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="f4d2b-125">Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="f4d2b-126">Í einingunni **Sjálfgefin síða**, í hólfinu **Aðal**, skaltu bæta við einingunni **Bálkur með fjölbreyttu efni**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="f4d2b-127">Í einingunni **Bálkur með fjölbreyttu efni** skaltu bæta við einingunni **Bálkaliður með fjölbreyttu efni**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="f4d2b-128">Skráðu sniðmátið inn og birtu það.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="f4d2b-129">Byggja upp síðu persónuverndarstefnu</span><span class="sxs-lookup"><span data-stu-id="f4d2b-129">Build a privacy policy page</span></span>

<span data-ttu-id="f4d2b-130">Fylgdu þessum skrefum til að byggja upp persónuverndarstefnusíðu.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="f4d2b-131">Farðu á **Síður \> Ný síða**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="f4d2b-132">Veldu sniðmát fyrir persónuverndarstefnusíðuna.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="f4d2b-133">Sláðu inn heiti og slóð síðu og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="f4d2b-134">Í hólfinu **Aðal** á síðunni bætirðu við einingunni **Bálkur með fjölbreyttu efni**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="f4d2b-135">Í einingunni **Bálkur með fjölbreyttu efni** skaltu bæta við einingunni **Bálkaliður með fjölbreyttu efni**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="f4d2b-136">Í eiginleikaglugganum fyrir eininguna **Bálkur með fjölbreyttu efni** velurðu **Bæta við gagnagjafa** og velur síðan **RTF-efni**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="f4d2b-137">Sláðu inn innihaldið fyrir persónuverndarstefnusíðuna í RTF-ritlinum.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="f4d2b-138">Stækkaðu textaritilinn í fulla skjástillingu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="f4d2b-139">Þegar þú hefur lokið við að slá inn efni skaltu velja **Forskoðun** til að forskoða síðuna í vafranum.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="f4d2b-140">Ljúktu öllu eftirstandandi viðbætum við síðuna og einingareiginleikana.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="f4d2b-141">Skráðu persónuverndarsíðuna inn og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="f4d2b-142">Til að birta slóðina fyrir persónuverndarstefnusíðuna skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="f4d2b-143">Farðu á **Vefslóðir** og veldu slóðina fyrir persónuverndarstefnusíðuna.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="f4d2b-144">Birtu valda slóð.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="f4d2b-145">Búðu til tengil á persónuverndarstefnusíðu í síðufæti</span><span class="sxs-lookup"><span data-stu-id="f4d2b-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="f4d2b-146">Þú getur bætt krækju á persónuverndarstefnusíðuna við brot.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="f4d2b-147">Á þennan hátt er hægt að deila hlekknum og uppfæra hann á mörgum vefsíðum með því að vísa í brotið.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="f4d2b-148">Þetta dæmi sýnir hvernig á að bæta við tengli á persónuverndarstefnusíðuna við síðufótarbrot.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="f4d2b-149">Til að bæta tengli við síðufótarbrot skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="f4d2b-150">Farðu í **Síðubrot \> Ný síðubrot**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="f4d2b-151">Veldu eininguna **Síðufótur** og sláðu síðan inn heiti í reitinn **Heiti blaðbrots**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="f4d2b-152">Í hólfinu **Síðufótaflokkur** bætirði við einingunni **Neðanmálsatriði**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="f4d2b-153">Í eiginleikaglugganum til hægri velurðu **Tengja texta**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="f4d2b-154">Í glugganum **Tengja texta** skal slá inn tenglatextinn og tengja mark persónuverndarstefnunnar og smella síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="f4d2b-155">Til að fá slóðina á persónuverndarstefnusíðuna ferðu á **Síður**, farðu svo á persónuverndarstefnusíðuna og afritaðu slóðina úr eignarrúðunni.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="f4d2b-156">Vistaðu brotið, skráðu það inn og gefðu það út.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="f4d2b-157">Forskoðaðu brotið og prófaðu hlekkinn á persónuverndarstefnusíðuna.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="f4d2b-158">Nú er hægt að vísa í brotið í sniðmátinu fyrir aðrar vefsíður.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="f4d2b-159">Þegar vísað er í þetta brot í einingunni **Síðufótur** í sniðmáti mun tilvísun tengilsins birtast á öllum síðum sem eru smíðaðar með því sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="f4d2b-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4d2b-160">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f4d2b-160">Additional resources</span></span>

[<span data-ttu-id="f4d2b-161">Yfirlit yfir samræmi</span><span class="sxs-lookup"><span data-stu-id="f4d2b-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="f4d2b-162">Aðgengiseiginleikar og -geta</span><span class="sxs-lookup"><span data-stu-id="f4d2b-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="f4d2b-163">Kökusamræmi</span><span class="sxs-lookup"><span data-stu-id="f4d2b-163">Cookie compliance</span></span>](cookie-compliance.md)
