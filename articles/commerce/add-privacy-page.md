---
title: Bæt við síðu persónuverndarstefnu
description: Þetta efnisatriði lýsir því hvernig á að bæta síðu með persónuverndarstefnu við svæði í Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797528"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="3365a-103">Bæta við persónuverndarstefnusíðu</span><span class="sxs-lookup"><span data-stu-id="3365a-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3365a-104">Þetta efnisatriði lýsir því hvernig á að bæta síðu með persónuverndarstefnu við svæði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3365a-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3365a-105">Fylgni við friðhelgi einkalífsins felur í sér skipulagsaðgerðir sem upplýsa notendur vefsins um hvernig gögnum þeirra er safnað og meðhöndlað.</span><span class="sxs-lookup"><span data-stu-id="3365a-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="3365a-106">Notendur geta síðan ákveðið hvernig þeir vilja að farið verði með persónuupplýsingar sínar og gripið til viðeigandi ráðstafana.</span><span class="sxs-lookup"><span data-stu-id="3365a-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="3365a-107">Lestu yfirlýsingu Microsoft um persónuvernd í Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3365a-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="3365a-108">Til að fara yfir persónuverndaryfirlýsingu Microsoft meðan þú ert innskráð/ur í Dynamics 365 Commerce höfundatól, veldu hnappinn **Hjálp** (**?**) efst í hægra horninu og veldu síðan **Persónuvernd og kökur**.</span><span class="sxs-lookup"><span data-stu-id="3365a-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="3365a-109">Nýr flipi er opnaður sem hefur tengil á [Persónuverndaryfirlýsingu Microsoft](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="3365a-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="3365a-110">Búðu til síðu með persónuverndarstefnu fyrir síðuna þína</span><span class="sxs-lookup"><span data-stu-id="3365a-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="3365a-111">Í Dynamics 365 Commerce eru nokkrar leiðir til að veita notendum vefsvæðisins aðgang að persónuverndarstefnu þinni.</span><span class="sxs-lookup"><span data-stu-id="3365a-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="3365a-112">Þessi hluti sýnir hvernig á að byggja upp persónuverndarstefnusíðu og vísa síðan á síðuna með því að nota síðufótarbrot.</span><span class="sxs-lookup"><span data-stu-id="3365a-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="3365a-113">Leiðbeiningarnar sem fylgja eru dæmi sem sýnir hvernig á að smíða almenna persónuverndarstefnusíðu fyrir viðskiptasíðu.</span><span class="sxs-lookup"><span data-stu-id="3365a-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="3365a-114">Þú berð ábyrgð á því að hanna og útfæra lausn á persónuverndarstefnu sem best uppfyllir lagalegar kröfur fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="3365a-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="3365a-115">Til að hefjast handa skaltu í höfundatækjunum fara á síðuna sem þú vilt byggja upp persónuverndarstefnusíðu fyrir.</span><span class="sxs-lookup"><span data-stu-id="3365a-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="3365a-116">Búa til sniðmát</span><span class="sxs-lookup"><span data-stu-id="3365a-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="3365a-117">Ef sniðmát sem hægt er að nota fyrir persónuverndarstefnusíðuna hefur þegar verið stofnað skaltu fara beint áfram í kaflann [Búa til síðu með persónuverndarstefnu](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="3365a-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="3365a-118">Fylgið eftirfarandi skrefum til að stofna sniðmát.</span><span class="sxs-lookup"><span data-stu-id="3365a-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="3365a-119">Farðu í **Sniðmát** og veldu síðan **Nýtt** til að búa til síðusniðmát.</span><span class="sxs-lookup"><span data-stu-id="3365a-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="3365a-120">Í svarglugganum **Nýtt sniðmát** undir **Heiti sniðmáts** skaltu slá inn **Sniðmát tilboðsborða** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3365a-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="3365a-121">Í sniðmátinu skaltu bæta við þeim einingum sem þarf í þar til gerð hólf á síðunni.</span><span class="sxs-lookup"><span data-stu-id="3365a-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="3365a-122">Til leiðbeiningar skaltu halda músabendlinum yfir rauðu upphrópunarmerkjunum.</span><span class="sxs-lookup"><span data-stu-id="3365a-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="3365a-123">(Til dæmis gæti hólfið **HTML-haus** þurft eininguna **Sjálfgefin ytri forskrift**.)</span><span class="sxs-lookup"><span data-stu-id="3365a-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="3365a-124">Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.</span><span class="sxs-lookup"><span data-stu-id="3365a-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="3365a-125">Í einingunni **Sjálfgefin síða**, í hólfinu **Aðal**, skaltu bæta við einingunni **Bálkur með fjölbreyttu efni**.</span><span class="sxs-lookup"><span data-stu-id="3365a-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="3365a-126">Í einingunni **Bálkur með fjölbreyttu efni** skaltu bæta við einingunni **Bálkaliður með fjölbreyttu efni**.</span><span class="sxs-lookup"><span data-stu-id="3365a-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="3365a-127">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="3365a-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="3365a-128">Byggja upp síðu persónuverndarstefnu</span><span class="sxs-lookup"><span data-stu-id="3365a-128">Build a privacy policy page</span></span>

<span data-ttu-id="3365a-129">Fylgdu þessum skrefum til að byggja upp persónuverndarstefnusíðu.</span><span class="sxs-lookup"><span data-stu-id="3365a-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="3365a-130">Farðu á **Síður** og veldu **Ný** til að búa til síðu.</span><span class="sxs-lookup"><span data-stu-id="3365a-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="3365a-131">Í svarglugganum **Velja sniðmát** skal velja sniðmátið fyrir síðu persónuverndarstefnu.</span><span class="sxs-lookup"><span data-stu-id="3365a-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="3365a-132">Sláðu inn síðuheiti og vefslóð síðu og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3365a-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="3365a-133">Í hólfinu **Aðal** á síðunni bætirðu við einingunni **Bálkur með fjölbreyttu efni**.</span><span class="sxs-lookup"><span data-stu-id="3365a-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="3365a-134">Í einingunni **Bálkur með fjölbreyttu efni** skaltu bæta við einingunni **Bálkaliður með fjölbreyttu efni**.</span><span class="sxs-lookup"><span data-stu-id="3365a-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="3365a-135">Í eiginleikaglugganum fyrir eininguna **Bálkur með fjölbreyttu efni** velurðu **Bæta við gagnagjafa** og velur síðan **RTF-efni**.</span><span class="sxs-lookup"><span data-stu-id="3365a-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="3365a-136">Sláðu inn innihaldið fyrir persónuverndarstefnusíðuna í RTF-ritlinum.</span><span class="sxs-lookup"><span data-stu-id="3365a-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="3365a-137">Stækkaðu textaritilinn í fulla skjástillingu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="3365a-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="3365a-138">Þegar þú hefur lokið við að slá inn efni skaltu velja **Forskoðun** til að forskoða síðuna í vafranum.</span><span class="sxs-lookup"><span data-stu-id="3365a-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="3365a-139">Ljúktu öllu eftirstandandi viðbætum við síðuna og einingareiginleikana.</span><span class="sxs-lookup"><span data-stu-id="3365a-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="3365a-140">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="3365a-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="3365a-141">Til að birta slóðina fyrir persónuverndarstefnusíðuna skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3365a-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="3365a-142">Farðu á **Vefslóðir** og veldu slóðina fyrir persónuverndarstefnusíðuna.</span><span class="sxs-lookup"><span data-stu-id="3365a-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="3365a-143">Veldu **Birta** til að birta valda vefslóð.</span><span class="sxs-lookup"><span data-stu-id="3365a-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="3365a-144">Búðu til tengil á persónuverndarstefnusíðu í síðufæti</span><span class="sxs-lookup"><span data-stu-id="3365a-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="3365a-145">Þú getur bætt krækju á persónuverndarstefnusíðuna við brot.</span><span class="sxs-lookup"><span data-stu-id="3365a-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="3365a-146">Á þennan hátt er hægt að deila hlekknum og uppfæra hann á mörgum vefsíðum með því að vísa í brotið.</span><span class="sxs-lookup"><span data-stu-id="3365a-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="3365a-147">Þetta dæmi sýnir hvernig á að bæta við tengli á persónuverndarstefnusíðuna við síðufótarbrot.</span><span class="sxs-lookup"><span data-stu-id="3365a-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="3365a-148">Til að bæta tengli við síðufótarbrot skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3365a-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="3365a-149">Farðu í **Brot** og veldu síðan **Nýtt** til að búa til síðubrot.</span><span class="sxs-lookup"><span data-stu-id="3365a-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="3365a-150">Í svarglugganum **Nýtt brot** skal velja eininguna **Síðufótur**.</span><span class="sxs-lookup"><span data-stu-id="3365a-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="3365a-151">Undir **Heiti brots** skal slá inn heiti brotsins og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3365a-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3365a-152">Í hólfinu **Síðufótaflokkur** bætirði við einingunni **Neðanmálsatriði**.</span><span class="sxs-lookup"><span data-stu-id="3365a-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="3365a-153">Í eiginleikaglugganum til hægri velurðu **Tengja texta**.</span><span class="sxs-lookup"><span data-stu-id="3365a-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="3365a-154">Í glugganum **Tengja texta** skal slá inn tenglatextinn og tengja mark persónuverndarstefnunnar og smella síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3365a-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="3365a-155">Til að fá slóðina á persónuverndarstefnusíðuna ferðu á **Síður**, farðu svo á persónuverndarstefnusíðuna og afritaðu slóðina úr eignarrúðunni.</span><span class="sxs-lookup"><span data-stu-id="3365a-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="3365a-156">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="3365a-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3365a-157">Forskoðaðu brotið og prófaðu hlekkinn á persónuverndarstefnusíðuna.</span><span class="sxs-lookup"><span data-stu-id="3365a-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="3365a-158">Nú er hægt að vísa í brotið í sniðmátinu fyrir aðrar vefsíður.</span><span class="sxs-lookup"><span data-stu-id="3365a-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="3365a-159">Þegar vísað er í þetta brot í einingunni **Síðufótur** í sniðmáti mun tilvísun tengilsins birtast á öllum síðum sem eru smíðaðar með því sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="3365a-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3365a-160">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3365a-160">Additional resources</span></span>

[<span data-ttu-id="3365a-161">Yfirlit yfir samræmi</span><span class="sxs-lookup"><span data-stu-id="3365a-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="3365a-162">Aðgengiseiginleikar og -geta</span><span class="sxs-lookup"><span data-stu-id="3365a-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="3365a-163">Reglufylgni köku</span><span class="sxs-lookup"><span data-stu-id="3365a-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="3365a-164">Skipta um notandakenni sem tengjast röktum efnisbreytingum</span><span class="sxs-lookup"><span data-stu-id="3365a-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
