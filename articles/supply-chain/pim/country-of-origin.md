---
title: Upprunaland
description: Mörg fyrirtæki gefa út vottorð til lánardrottna sinna til að tryggja að afurðir uppfylli tiltekna vottunarstaðla. Þessi vottorð eru oft háð upprunalandi. Í þessu efnisatriði er að finna upplýsingar um eiginleika upprunalands, sem gerir þér kleift að tengja afurð við upprunaland hennar og fylgjast með afurðarvottorðum þess.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596242"
---
# <a name="country-of-origin"></a><span data-ttu-id="95069-105">Upprunaland</span><span class="sxs-lookup"><span data-stu-id="95069-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95069-106">Mörg fyrirtæki gefa út vottorð til lánardrottna sinna til að tryggja að afurðir uppfylli tiltekna vottunarstaðla.</span><span class="sxs-lookup"><span data-stu-id="95069-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="95069-107">Þessi vottorð eru oft háð upprunalandi.</span><span class="sxs-lookup"><span data-stu-id="95069-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="95069-108">Eiginleiki upprunalands gerir þér kleift að tengja afurð við upprunaland hennar og fylgjast með afurðarvottorðum þess.</span><span class="sxs-lookup"><span data-stu-id="95069-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="95069-109">Skilgreina uppruna- og viðtökuland</span><span class="sxs-lookup"><span data-stu-id="95069-109">Configure source and destination countries</span></span>

<span data-ttu-id="95069-110">Áður en hægt er að gefa út vottorð fyrir afurð verður að tengja afurðina við viðtökuland og upprunaland hennar.</span><span class="sxs-lookup"><span data-stu-id="95069-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="95069-111">Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðasamræmi \> Upprunaland \> Reglur upprunalands**.</span><span class="sxs-lookup"><span data-stu-id="95069-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="95069-112">Veldu fyrirliggjandi uppsetningu lands til að breyta henni, eða **Ný** á aðgerðasvæðinu til að búa til nýja uppsetning lands.</span><span class="sxs-lookup"><span data-stu-id="95069-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="95069-113">Stilltu eftirfarandi gildi fyrir valda landið eða nýtt land.</span><span class="sxs-lookup"><span data-stu-id="95069-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="95069-114">Svæði</span><span class="sxs-lookup"><span data-stu-id="95069-114">Field</span></span> | <span data-ttu-id="95069-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="95069-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="95069-116">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="95069-116">Item number</span></span> | <span data-ttu-id="95069-117">Veldu vörunúmer Afurðarinnar.</span><span class="sxs-lookup"><span data-stu-id="95069-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="95069-118">Áfangaland</span><span class="sxs-lookup"><span data-stu-id="95069-118">Destination country</span></span> | <span data-ttu-id="95069-119">Veldu landið sem þú ert að senda afurðina til.</span><span class="sxs-lookup"><span data-stu-id="95069-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="95069-120">Upprunaland</span><span class="sxs-lookup"><span data-stu-id="95069-120">Origin country</span></span> | <span data-ttu-id="95069-121">Veljið landið sem á að afhenda afurðina frá.</span><span class="sxs-lookup"><span data-stu-id="95069-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="95069-122">Tilgangur þessarar uppsetningar er að auðvelda skýrslumyndun uppskriftar þar sem hægt er að hafa með upprunaland fyrir hvern hluta sem uppruna- og viðtökuland eru tilgreind fyrir.</span><span class="sxs-lookup"><span data-stu-id="95069-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="95069-123">Þessi skýrsla veitir heildstæðari mynd af því hvaðan hlutirnir koma og hvert þeir eru að fara.</span><span class="sxs-lookup"><span data-stu-id="95069-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="95069-124">Fylgstu með vottorðum lánardrottna</span><span class="sxs-lookup"><span data-stu-id="95069-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="95069-125">Hægt er að nota síðuna **Vottorð lánardrottins um upprunaland** til að fylgjast með vottorðum sem gefin er út til lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="95069-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="95069-126">Þú verður að ákveða hvaða vottorðsskjöl þú ert að gefa út og hvernig þú munt skrá þau til viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="95069-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="95069-127">Þessi eiginleiki hjálpar til við að fylgjast með vottorðum.</span><span class="sxs-lookup"><span data-stu-id="95069-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="95069-128">Hann gerir þér einnig kleift að velja hvort viðeigandi vottorðanúmer komi fram á reikningum, fylgiseðlum og/eða pöntunarstaðfestingum.</span><span class="sxs-lookup"><span data-stu-id="95069-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="95069-129">Til að setja upp upplýsingar um vottorð skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="95069-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="95069-130">Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðasamræmi \> Upprunaland \> Vottorð lánardrottins um upprunaland**.</span><span class="sxs-lookup"><span data-stu-id="95069-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="95069-131">Veljið fyrirliggjandi uppsetningu vottorðs til að breyta henni, eða veljið **Nýtt** á aðgerðasvæðinu til að búa til nýja uppsetningu vottorðs.</span><span class="sxs-lookup"><span data-stu-id="95069-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="95069-132">Stilltu eftirfarandi stillingar fyrir valda vottorðið eða nýtt vottorð.</span><span class="sxs-lookup"><span data-stu-id="95069-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="95069-133">Svæði</span><span class="sxs-lookup"><span data-stu-id="95069-133">Field</span></span> | <span data-ttu-id="95069-134">lýsing</span><span class="sxs-lookup"><span data-stu-id="95069-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="95069-135">Lykill lánardrottins</span><span class="sxs-lookup"><span data-stu-id="95069-135">Vendor account</span></span> | <span data-ttu-id="95069-136">Veljið lánardrottininn sem vottorð var gefið út fyrir.</span><span class="sxs-lookup"><span data-stu-id="95069-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="95069-137">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="95069-137">Item number</span></span> | <span data-ttu-id="95069-138">Veljið vöruna sem vottorðið var gefið út fyrir.</span><span class="sxs-lookup"><span data-stu-id="95069-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="95069-139">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="95069-139">Country/region</span></span> | <span data-ttu-id="95069-140">Viðtökuland eða svæði þar sem þú verður að nota þetta vottorð.</span><span class="sxs-lookup"><span data-stu-id="95069-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="95069-141">Númer vottorðs</span><span class="sxs-lookup"><span data-stu-id="95069-141">Certificate number</span></span> | <span data-ttu-id="95069-142">Sláðu inn auðkennisnúmer vottorðsins sem var gefið út.</span><span class="sxs-lookup"><span data-stu-id="95069-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="95069-143">Virkt</span><span class="sxs-lookup"><span data-stu-id="95069-143">Effective</span></span> | <span data-ttu-id="95069-144">Veljið fyrstu dagsetningu þegar núgildandi vottorð er gilt.</span><span class="sxs-lookup"><span data-stu-id="95069-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="95069-145">Lok gildistíma</span><span class="sxs-lookup"><span data-stu-id="95069-145">Expiration</span></span> | <span data-ttu-id="95069-146">Veljið síðustu dagsetningu þegar núgildandi vottorð er gilt.</span><span class="sxs-lookup"><span data-stu-id="95069-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="95069-147">Prenta á reikning</span><span class="sxs-lookup"><span data-stu-id="95069-147">Print on invoice</span></span> | <span data-ttu-id="95069-148">Veljið þennan gátreit til að prenta númer vottorðs á reikningunum sem eru stílaðir á tiltekið land innan tiltekins dagsetningabils.</span><span class="sxs-lookup"><span data-stu-id="95069-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="95069-149">Prenta á fylgiseðil</span><span class="sxs-lookup"><span data-stu-id="95069-149">Print on packing slip</span></span> | <span data-ttu-id="95069-150">Veljið þennan gátreit til að prenta númer vottorðs á fylgiseðlum sem eru stílaðir á tiltekið land innan tiltekins dagsetningabils.</span><span class="sxs-lookup"><span data-stu-id="95069-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="95069-151">Prenta á sölupöntun</span><span class="sxs-lookup"><span data-stu-id="95069-151">Print on sales order</span></span> | <span data-ttu-id="95069-152">Veljið þennan gátreit til að prenta númer vottorðs á sölupöntunum sem eru stílaðar á tiltekið land innan tiltekins dagsetningabils.</span><span class="sxs-lookup"><span data-stu-id="95069-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="95069-153">Láta upprunaland fylgja með í skýrslum uppskrifta</span><span class="sxs-lookup"><span data-stu-id="95069-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="95069-154">Þegar skýrsla uppskriftar er búin til er hægt að láta upprunaland fylgja með fyrir hvern hlut sem uppruna- og viðtökuland eru tilgreind fyrir á síðunni **Reglur upprunalands**.</span><span class="sxs-lookup"><span data-stu-id="95069-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="95069-155">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="95069-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="95069-156">Veljið eða stofnið afurð til að opna síðuna **Upplýsingar um losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="95069-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="95069-157">Á aðgerðasvæðinu, í flipanum **Hönnun**, í flokknum **Uppskrift**, skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="95069-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="95069-158">Á síðunni sem birtist, á Aðgerðasvæðinu skal smellt á **Uppskrift \> Prenta**.</span><span class="sxs-lookup"><span data-stu-id="95069-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="95069-159">Í svarglugganum **Uppskriftalínur** skal stilla reitinn **Viðtökuland** á viðtökulandið sem á að koma fram í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="95069-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="95069-160">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95069-160">Select **OK**.</span></span>

<span data-ttu-id="95069-161">Skýrsla sem sýnir upplýsingar um upprunaland hvers hluta er búin til og sýnd.</span><span class="sxs-lookup"><span data-stu-id="95069-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="95069-162">Hér er dæmi um skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="95069-162">Here is an example of the report.</span></span>

<span data-ttu-id="95069-163">![Skýrsla upprunalands](media/country-of-origin-report.png "Skýrsla upprunalands")</span><span class="sxs-lookup"><span data-stu-id="95069-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
