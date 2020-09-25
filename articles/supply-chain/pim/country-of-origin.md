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
ms.openlocfilehash: d0d93a02817bab8e188818862c1bb7f84b498fc1
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802798"
---
# <a name="country-of-origin"></a><span data-ttu-id="ede5e-105">Upprunaland</span><span class="sxs-lookup"><span data-stu-id="ede5e-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ede5e-106">Mörg fyrirtæki gefa út vottorð til lánardrottna sinna til að tryggja að afurðir uppfylli tiltekna vottunarstaðla.</span><span class="sxs-lookup"><span data-stu-id="ede5e-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="ede5e-107">Þessi vottorð eru oft háð upprunalandi.</span><span class="sxs-lookup"><span data-stu-id="ede5e-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="ede5e-108">Eiginleiki upprunalands gerir þér kleift að tengja afurð við upprunaland hennar og fylgjast með afurðarvottorðum þess.</span><span class="sxs-lookup"><span data-stu-id="ede5e-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="ede5e-109">Kveikja á eiginleika upprunalands</span><span class="sxs-lookup"><span data-stu-id="ede5e-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="ede5e-110">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="ede5e-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ede5e-111">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="ede5e-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ede5e-112">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="ede5e-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ede5e-113">**Eining:** *Afurðaupplýsingastjórnun*</span><span class="sxs-lookup"><span data-stu-id="ede5e-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="ede5e-114">**Heiti eiginleika:** *Stjórnunareiginleiki fyrir upprunaland*</span><span class="sxs-lookup"><span data-stu-id="ede5e-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="ede5e-115">Skilgreina uppruna- og viðtökuland</span><span class="sxs-lookup"><span data-stu-id="ede5e-115">Configure source and destination countries</span></span>

<span data-ttu-id="ede5e-116">Áður en hægt er að gefa út vottorð fyrir afurð verður að tengja afurðina við viðtökuland og upprunaland hennar.</span><span class="sxs-lookup"><span data-stu-id="ede5e-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="ede5e-117">Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðasamræmi \> Upprunaland \> Reglur upprunalands**.</span><span class="sxs-lookup"><span data-stu-id="ede5e-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="ede5e-118">Veldu fyrirliggjandi uppsetningu lands til að breyta henni, eða **Ný** á aðgerðasvæðinu til að búa til nýja uppsetning lands.</span><span class="sxs-lookup"><span data-stu-id="ede5e-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="ede5e-119">Stilltu eftirfarandi gildi fyrir valda landið eða nýtt land.</span><span class="sxs-lookup"><span data-stu-id="ede5e-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="ede5e-120">Svæði</span><span class="sxs-lookup"><span data-stu-id="ede5e-120">Field</span></span> | <span data-ttu-id="ede5e-121">lýsing</span><span class="sxs-lookup"><span data-stu-id="ede5e-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="ede5e-122">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="ede5e-122">Item number</span></span> | <span data-ttu-id="ede5e-123">Veldu vörunúmer Afurðarinnar.</span><span class="sxs-lookup"><span data-stu-id="ede5e-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="ede5e-124">Áfangaland</span><span class="sxs-lookup"><span data-stu-id="ede5e-124">Destination country</span></span> | <span data-ttu-id="ede5e-125">Veldu landið sem þú ert að senda afurðina til.</span><span class="sxs-lookup"><span data-stu-id="ede5e-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="ede5e-126">Upprunaland</span><span class="sxs-lookup"><span data-stu-id="ede5e-126">Origin country</span></span> | <span data-ttu-id="ede5e-127">Veljið landið sem á að afhenda afurðina frá.</span><span class="sxs-lookup"><span data-stu-id="ede5e-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="ede5e-128">Tilgangur þessarar uppsetningar er að auðvelda skýrslumyndun uppskriftar þar sem hægt er að hafa með upprunaland fyrir hvern hluta sem uppruna- og viðtökuland eru tilgreind fyrir.</span><span class="sxs-lookup"><span data-stu-id="ede5e-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="ede5e-129">Þessi skýrsla veitir heildstæðari mynd af því hvaðan hlutirnir koma og hvert þeir eru að fara.</span><span class="sxs-lookup"><span data-stu-id="ede5e-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="ede5e-130">Fylgstu með vottorðum lánardrottna</span><span class="sxs-lookup"><span data-stu-id="ede5e-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="ede5e-131">Hægt er að nota síðuna **Vottorð lánardrottins um upprunaland** til að fylgjast með vottorðum sem gefin er út til lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="ede5e-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="ede5e-132">Þú verður að ákveða hvaða vottorðsskjöl þú ert að gefa út og hvernig þú munt skrá þau til viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="ede5e-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="ede5e-133">Þessi eiginleiki hjálpar til við að fylgjast með vottorðum.</span><span class="sxs-lookup"><span data-stu-id="ede5e-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="ede5e-134">Hann gerir þér einnig kleift að velja hvort viðeigandi vottorðanúmer komi fram á reikningum, fylgiseðlum og/eða pöntunarstaðfestingum.</span><span class="sxs-lookup"><span data-stu-id="ede5e-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="ede5e-135">Til að setja upp upplýsingar um vottorð skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ede5e-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="ede5e-136">Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðasamræmi \> Upprunaland \> Vottorð lánardrottins um upprunaland**.</span><span class="sxs-lookup"><span data-stu-id="ede5e-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="ede5e-137">Veljið fyrirliggjandi uppsetningu vottorðs til að breyta henni, eða veljið **Nýtt** á aðgerðasvæðinu til að búa til nýja uppsetningu vottorðs.</span><span class="sxs-lookup"><span data-stu-id="ede5e-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="ede5e-138">Stilltu eftirfarandi stillingar fyrir valda vottorðið eða nýtt vottorð.</span><span class="sxs-lookup"><span data-stu-id="ede5e-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="ede5e-139">Svæði</span><span class="sxs-lookup"><span data-stu-id="ede5e-139">Field</span></span> | <span data-ttu-id="ede5e-140">lýsing</span><span class="sxs-lookup"><span data-stu-id="ede5e-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="ede5e-141">Lykill lánardrottins</span><span class="sxs-lookup"><span data-stu-id="ede5e-141">Vendor account</span></span> | <span data-ttu-id="ede5e-142">Veljið lánardrottininn sem vottorð var gefið út fyrir.</span><span class="sxs-lookup"><span data-stu-id="ede5e-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="ede5e-143">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="ede5e-143">Item number</span></span> | <span data-ttu-id="ede5e-144">Veljið vöruna sem vottorðið var gefið út fyrir.</span><span class="sxs-lookup"><span data-stu-id="ede5e-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="ede5e-145">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="ede5e-145">Country/region</span></span> | <span data-ttu-id="ede5e-146">Viðtökuland eða svæði þar sem þú verður að nota þetta vottorð.</span><span class="sxs-lookup"><span data-stu-id="ede5e-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="ede5e-147">Númer vottorðs</span><span class="sxs-lookup"><span data-stu-id="ede5e-147">Certificate number</span></span> | <span data-ttu-id="ede5e-148">Sláðu inn auðkennisnúmer vottorðsins sem var gefið út.</span><span class="sxs-lookup"><span data-stu-id="ede5e-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="ede5e-149">Virkt</span><span class="sxs-lookup"><span data-stu-id="ede5e-149">Effective</span></span> | <span data-ttu-id="ede5e-150">Veljið fyrstu dagsetningu þegar núgildandi vottorð er gilt.</span><span class="sxs-lookup"><span data-stu-id="ede5e-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="ede5e-151">Lok gildistíma</span><span class="sxs-lookup"><span data-stu-id="ede5e-151">Expiration</span></span> | <span data-ttu-id="ede5e-152">Veljið síðustu dagsetningu þegar núgildandi vottorð er gilt.</span><span class="sxs-lookup"><span data-stu-id="ede5e-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="ede5e-153">Prenta á reikning</span><span class="sxs-lookup"><span data-stu-id="ede5e-153">Print on invoice</span></span> | <span data-ttu-id="ede5e-154">Veljið þennan gátreit til að prenta númer vottorðs á reikningunum sem eru stílaðir á tiltekið land innan tiltekins dagsetningabils.</span><span class="sxs-lookup"><span data-stu-id="ede5e-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="ede5e-155">Prenta á fylgiseðil</span><span class="sxs-lookup"><span data-stu-id="ede5e-155">Print on packing slip</span></span> | <span data-ttu-id="ede5e-156">Veljið þennan gátreit til að prenta númer vottorðs á fylgiseðlum sem eru stílaðir á tiltekið land innan tiltekins dagsetningabils.</span><span class="sxs-lookup"><span data-stu-id="ede5e-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="ede5e-157">Prenta á sölupöntun</span><span class="sxs-lookup"><span data-stu-id="ede5e-157">Print on sales order</span></span> | <span data-ttu-id="ede5e-158">Veljið þennan gátreit til að prenta númer vottorðs á sölupöntunum sem eru stílaðar á tiltekið land innan tiltekins dagsetningabils.</span><span class="sxs-lookup"><span data-stu-id="ede5e-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="ede5e-159">Láta upprunaland fylgja með í skýrslum uppskrifta</span><span class="sxs-lookup"><span data-stu-id="ede5e-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="ede5e-160">Þegar skýrsla uppskriftar er búin til er hægt að láta upprunaland fylgja með fyrir hvern hlut sem uppruna- og viðtökuland eru tilgreind fyrir á síðunni **Reglur upprunalands**.</span><span class="sxs-lookup"><span data-stu-id="ede5e-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="ede5e-161">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ede5e-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ede5e-162">Veljið eða stofnið afurð til að opna síðuna **Upplýsingar um losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ede5e-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="ede5e-163">Á aðgerðasvæðinu, í flipanum **Hönnun**, í flokknum **Uppskrift**, skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="ede5e-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="ede5e-164">Á síðunni sem birtist, á Aðgerðasvæðinu skal smellt á **Uppskrift \> Prenta**.</span><span class="sxs-lookup"><span data-stu-id="ede5e-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="ede5e-165">Í svarglugganum **Uppskriftalínur** skal stilla reitinn **Viðtökuland** á viðtökulandið sem á að koma fram í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="ede5e-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="ede5e-166">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ede5e-166">Select **OK**.</span></span>

<span data-ttu-id="ede5e-167">Skýrsla sem sýnir upplýsingar um upprunaland hvers hluta er búin til og sýnd.</span><span class="sxs-lookup"><span data-stu-id="ede5e-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="ede5e-168">Hér er dæmi um skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="ede5e-168">Here is an example of the report.</span></span>

<span data-ttu-id="ede5e-169">![Skýrsla upprunalands](media/country-of-origin-report.png "Skýrsla upprunalands")</span><span class="sxs-lookup"><span data-stu-id="ede5e-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
