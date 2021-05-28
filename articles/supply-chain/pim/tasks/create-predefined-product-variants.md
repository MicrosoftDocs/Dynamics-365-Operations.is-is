---
title: Stofna forskilgreind afurðarafbrigði
description: Þetta ferli fer í gegnum stofnun afurðarafbrigða fyrir afurðarsniðmát með samsetningum fyrir afurðavíddir.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f78441445baecba279f96eb3935d9ebbb4ff03f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021909"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="49956-103">Fyrirframskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="49956-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="49956-104">Sýnidæmi: Stofna fyrirframskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="49956-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="49956-105">Þetta sýnidæmi sýnir hvernig á að stofna afurðarafbrigði fyrir afurðarsniðmát með því að nota samsetningar af afurðarafbrigðum.</span><span class="sxs-lookup"><span data-stu-id="49956-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="49956-106">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="49956-106">Make demo data available</span></span>

<span data-ttu-id="49956-107">Til að fylgja þessari atburðarás með gögnunum sem mælt er með hér, verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann *USMF*.</span><span class="sxs-lookup"><span data-stu-id="49956-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="49956-108">Skref 1: Stofna afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="49956-108">Step 1: Create a product master</span></span>

<span data-ttu-id="49956-109">Til að stofna afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="49956-109">To create a product master:</span></span>

1. <span data-ttu-id="49956-110">Fara í **Upplýsingastjórnun afurða > Afurðir > Afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="49956-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="49956-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="49956-111">Select **New**.</span></span>
1. <span data-ttu-id="49956-112">Ef reiturinn **Afurðarnúmer** sýnir ekki númer nú þegar skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="49956-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="49956-113">Þetta er aðeins nauðsynlegt ef engin númeraröð hefur verið sett upp fyrir þennan reit.</span><span class="sxs-lookup"><span data-stu-id="49956-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="49956-114">Færið inn heiti í reitinn **Afurðarheiti**.</span><span class="sxs-lookup"><span data-stu-id="49956-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="49956-115">Í reitinn **Afurðavíddaflokkur** skal velja afurðavíddaflokkinn *SizeCol* (stærð og litur).</span><span class="sxs-lookup"><span data-stu-id="49956-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="49956-116">Veljið **Í lagi** til að stofna og opna nýtt afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="49956-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="49956-117">Skref 2: Bæta við afurðarvíddum</span><span class="sxs-lookup"><span data-stu-id="49956-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="49956-118">Þetta dæmi sýnir hvernig á að færa inn afurðarvíddir handvirkt.</span><span class="sxs-lookup"><span data-stu-id="49956-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="49956-119">Einnig er hægt að velja stærð, lit eða stílflokk sem inniheldur afurðarvíddargildi sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="49956-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="49956-120">Til að bæta við afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="49956-120">To add product dimensions:</span></span>

1. <span data-ttu-id="49956-121">Með nýja afurðarsniðmátið enn opið skal velja **Afurðarvíddir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="49956-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="49956-122">Opnið flipann **Stærð** og veljið **Ný** á tækjastikunni til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="49956-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="49956-123">Gerið eftirfarandi stillingar fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="49956-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="49956-124">**Stærð:** Veljið stærðargildi.</span><span class="sxs-lookup"><span data-stu-id="49956-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="49956-125">**Heiti:** Færið inn heiti fyrir stærðina.</span><span class="sxs-lookup"><span data-stu-id="49956-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="49956-126">Veljið **Ný** á tækjastikunni og bætið annarri stærð við hnitanetið með nýrri **Stærð** og **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="49956-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="49956-127">Opnið flipann **Litir** og veljið **Nýr** á tækjastikunni til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="49956-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="49956-128">Gerið eftirfarandi stillingar fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="49956-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="49956-129">**Litur:** Veljið litargildi.</span><span class="sxs-lookup"><span data-stu-id="49956-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="49956-130">**Heiti:** Færið inn heiti fyrir litinn.</span><span class="sxs-lookup"><span data-stu-id="49956-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="49956-131">Veljið **Nýr** á tækjastikunni og bætið öðrum lit við hnitanetið með nýjum **Lit** og **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="49956-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="49956-132">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="49956-132">Select **Save**.</span></span>
1. <span data-ttu-id="49956-133">Lokið síðunni til að fara aftur á nýja afurðarsniðmátið.</span><span class="sxs-lookup"><span data-stu-id="49956-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="49956-134">Skref 3: Búa til afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="49956-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="49956-135">Þessi hluti lýsir því hvernig búa á til afurðarafbrigði þegar eiginleikinn *Endurbætur á tillögusíðu afbrigðis* er ekki virkur.</span><span class="sxs-lookup"><span data-stu-id="49956-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="49956-136">Frekari upplýsingar um hvernig á að búa til afurðarafbrigði þegar þessi eiginleiki er í boði er að finna í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="49956-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="49956-137">Til að stofna afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="49956-137">To generate product variants:</span></span>

1. <span data-ttu-id="49956-138">Með nýja afurðarsniðmátið enn opið skal velja **Afurðarafbrigði** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="49956-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="49956-139">Veljið **Tillögur um afbrigði** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="49956-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="49956-140">Kerfið býr til lista með öllum mögulegum samsetningum stærða og lita sem þú skilgreindir fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="49956-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="49956-141">Veljið **Veljið allt** á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="49956-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="49956-142">Í þessu dæmi skal velja öll möguleg afbrigði.</span><span class="sxs-lookup"><span data-stu-id="49956-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="49956-143">Ef eingöngu á að nota undirsafn af mögulegum samsetningum afurðarvídda skal velja áskildu gátreitina eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="49956-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="49956-144">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="49956-144">Select **Create**.</span></span>
1. <span data-ttu-id="49956-145">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="49956-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="49956-146">Bættar tillögur um afbrigði</span><span class="sxs-lookup"><span data-stu-id="49956-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="49956-147">Eiginleikinn *Endurbætur á tillögusíðu afbrigðis* bætir síðuna **Tillögur um afbrigði** til að takast á við vandamál varðandi afköst og notagildi fyrir fyrirtæki sem eru með mikinn fjölda af samsetningum á afurðarvíddum.</span><span class="sxs-lookup"><span data-stu-id="49956-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="49956-148">Bætt ferli til að velja afurðarvíddargildin þar sem á að búa til tillögur um afbrigði gerir það fljótlegra og auðveldara að bera kennsl á og gefa út viðeigandi safn af afurðarafbrigðum.</span><span class="sxs-lookup"><span data-stu-id="49956-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="49956-149">Eftirfarandi endurbótum er bætt við af þessum eiginleika:</span><span class="sxs-lookup"><span data-stu-id="49956-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="49956-150">**Frestun á myndun afurðartillagna:** Síðan **Tillögur um afbrigði** sýnir ekki lengur tillögur þegar hún er opnuð í fyrsta skipti.</span><span class="sxs-lookup"><span data-stu-id="49956-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="49956-151">Þess í stað þarf sérstaklega að velja hvaða gildi þarf og velja svo hnappinn **Leggðu til** til að mynda samsetningarnar.</span><span class="sxs-lookup"><span data-stu-id="49956-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="49956-152">Þetta gerir ferlið sýnilegra og gagnvirkara.</span><span class="sxs-lookup"><span data-stu-id="49956-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="49956-153">**Val víddargilda:** Þegar mörg víddargildi eru til staðar vill notandi yfirleitt búa til tillögur að afbrigðum sem taka aðeins nokkrar þeirra til greina (t.d. þegar nýir litir eða stílbrigði eru tekin í notkun).</span><span class="sxs-lookup"><span data-stu-id="49956-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="49956-154">Með endurbættri hönnun er hægt að velja víddargildin fyrir það sem búa á tillögur að afurðarafbrigðum fyrir.</span><span class="sxs-lookup"><span data-stu-id="49956-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="49956-155">Þetta eykur vægi þeirra afbrigða sem stungið er upp á og bætir bæði afköst kerfis og skilvirkni notanda.</span><span class="sxs-lookup"><span data-stu-id="49956-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="49956-156">Kveikja á eiginleika vegna endurbóta á tillögusíðu afurða</span><span class="sxs-lookup"><span data-stu-id="49956-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="49956-157">Áður en hægt er að nota eiginleikann *Endurbætur á tillögusíðu afbrigðis* þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="49956-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="49956-158">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="49956-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="49956-159">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="49956-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="49956-160">**Eining:** *Afurðaupplýsingastjórnun*</span><span class="sxs-lookup"><span data-stu-id="49956-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="49956-161">**Heiti eiginleika:** *Endurbætur á tillögusíðu afbrigðis*</span><span class="sxs-lookup"><span data-stu-id="49956-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="49956-162">Unnið með endurbætur á tillögum afbrigðis</span><span class="sxs-lookup"><span data-stu-id="49956-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="49956-163">Til að búa til tillögur um afurðarafbrigði þegar kveikt er á eiginleikanum *Endurbætur á tillögusíðu afbrigðis*:</span><span class="sxs-lookup"><span data-stu-id="49956-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="49956-164">Opnið eða búið til afurðarsniðmát og bætið nauðsynlegum afurðarvíddum við það eins og lýst er í hlutanum hér á undan.</span><span class="sxs-lookup"><span data-stu-id="49956-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="49956-165">Með afurðarsniðmátið opið skal velja **Afurðarafbrigði** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="49956-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="49956-166">Veljið **Tillögur um afbrigði** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="49956-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="49956-167">Veljið gildin sem ætlunin er að nota fyrir hverja vídd fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="49956-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="49956-168">Á efri tækjastikunni skal velja **Leggja til**.</span><span class="sxs-lookup"><span data-stu-id="49956-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="49956-169">Kerfið býr til lista með öllum mögulegum samsetningum stærða og lita sem voru valdar.</span><span class="sxs-lookup"><span data-stu-id="49956-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="49956-170">Í flýtiflipanum **Afbrigði sem stungið er upp á** skal velja gátreitinn fyrir hverja samsetningu afurðarvíddar sem ætlunin er að nota eða velja **Velja allar** á tækjastikunni til að velja þær allar.</span><span class="sxs-lookup"><span data-stu-id="49956-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="49956-171">Veljið **Búa til** til að bæta afbrigðunum við núverandi afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="49956-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
