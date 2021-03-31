---
title: Kveikja á og grunnstilla sjálfvirk gjöld eftir rás
description: Þetta efnisatriði lýsir hvernig er kveikt á og grunnstillt sjálfvirk gjöld eftir rás í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 834d90c8ec8515c6bced2d8a4fabc79b4e4e4c3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211274"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="b1a71-103">Kveikja á og grunnstilla sjálfvirk gjöld eftir rás</span><span class="sxs-lookup"><span data-stu-id="b1a71-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="b1a71-104">Þetta efnisatriði útskýrir hvernig á að virkja og grunnstilla sjálfvirk gjöld (sjálfvirk gjöld) eftir rásum í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b1a71-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b1a71-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b1a71-105">Overview</span></span>

<span data-ttu-id="b1a71-106">Þú gætir haft atburðarás þar sem nota þarf endurvinnslugjöld eða önnur gjöld fyrir hóp af vörum sem eru seldar í öllum eða sumum verslunum í tilteknu ríki (til dæmis í Kaliforníu).</span><span class="sxs-lookup"><span data-stu-id="b1a71-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="b1a71-107">Eiginleikinn **Kveikja á síun sjálfvirkra gjalda eftir rás** í Commerce gerir þér kleift að tilgreina sjálfvirka gjaldtöku eftir rás (til dæmis ákveðin verslunarrás).</span><span class="sxs-lookup"><span data-stu-id="b1a71-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="b1a71-108">Þessi eiginleiki er tiltækur í Dynamics 365 Commerce útgáfa 10.0.10 og síðar.</span><span class="sxs-lookup"><span data-stu-id="b1a71-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="b1a71-109">Til að virkja og stilla sjálfvirkt gjald eftir rás verður þú að klára eftirfarandi verkefni:</span><span class="sxs-lookup"><span data-stu-id="b1a71-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="b1a71-110">Kveiktu á eiginleikanum **Kveikja á síun sjálfvirkra gjalda eftir rás**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="b1a71-111">Grunnstilltu tilgang fyrir stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="b1a71-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="b1a71-112">Skilgreina sjálfvirkt gjald eftir rás.</span><span class="sxs-lookup"><span data-stu-id="b1a71-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="b1a71-113">Eiginleikinn **Kveikja á síun sjálfvirkra gjalda eftir rás** virkar aðeins ef einnig er kveikt á ítarlegum sjálfvirkum gjaldaeiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="b1a71-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="b1a71-114">Nánari upplýsingar um hvernig á að kveikja á háþróaðri sjálfvirkri gjaldtöku er að finna í [Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="b1a71-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="b1a71-115">Kveiktu á eiginleikanum Kveikja á síun sjálfvirkra gjalda eftir rás</span><span class="sxs-lookup"><span data-stu-id="b1a71-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="b1a71-116">Fylgdu þessum skrefum til að virkja sjálfvirka gjaldtöku eftir rás í Commerce.</span><span class="sxs-lookup"><span data-stu-id="b1a71-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b1a71-117">Farðu í **Kerfisstjóri \> Vinnusvæði \> Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="b1a71-118">Á flipanum **Ekki gert virkt**, á listanum **Heiti eiginleika**, finnurðu og velur **Kveikja á síun sjálfvirkra gjalda eftir rás**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="b1a71-119">Neðst í hægra horninu velurðu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="b1a71-120">Þegar kveikt hefur verið á eiginleikanum birtist hann á listanum á flipanum **Allt**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="b1a71-121">Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b1a71-122">Í vinstri glugganum finnurðu og velur vinnsluna **1110** (**Altækar stillingar**).</span><span class="sxs-lookup"><span data-stu-id="b1a71-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="b1a71-123">Í aðgerðaglugganum velurðu **Keyra núna** til að breiða út stillingarbreytingarnar.</span><span class="sxs-lookup"><span data-stu-id="b1a71-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="b1a71-124">Ef þú slekkur á eiginleikanum **Kveikja á síun sjálfvirkra gjalda eftir rás** þegar þú hefur þegar notað hann birtist reiturinn **Tengsl smásölurásar** undir **Sjálfvirk gjöld** ekki lengur og þú tapar öllum núverandi stillingum.</span><span class="sxs-lookup"><span data-stu-id="b1a71-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="b1a71-125">Ef fjarlæging á stillingum **Tengsla smásölurásar** valda tvíritun á reglum um sjálfvirkt gjald mun tilraun til að slökkva á eiginleikanum ekki takast.</span><span class="sxs-lookup"><span data-stu-id="b1a71-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="b1a71-126">Passaðu að fara yfir allar reglur um gjöld fyrir sjálfvirk gjöld og gera nauðsynlegar breytingar áður en slökkt er á eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="b1a71-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="b1a71-127">Grunnstilltu tilgang fyrir stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="b1a71-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="b1a71-128">Nýr tilgangur stigveldisskipulags sem nefndur er **Sjálfvirkt gjald í Retail** hefur verið stofnað til að stjórna stigveldinu fyrir sjálfvirka gjaldtöku eftir rás.</span><span class="sxs-lookup"><span data-stu-id="b1a71-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="b1a71-129">Fylgdu þessum skrefum til að tengja sjálfgefið stigveldi við skipulag stigveldis í Commerce.</span><span class="sxs-lookup"><span data-stu-id="b1a71-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="b1a71-130">Farðu í **Fyrirtækisstjórnun \> Fyrirtæki \> Tilgangur stigveldis fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="b1a71-131">Veldu á vinstri glugganum **Sjálfvirkt gjald í Retail**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="b1a71-132">Undir **Úthlutuð stigveldi** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="b1a71-133">Í valmyndinni **Stigveldi fyrirtækis** velurðu stigveldi fyrirtækis (til dæmis, **Smásöluverslnair eftir svæðum**) og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="b1a71-134">Undir **Úthlutuð stigveldi** velurðu **Setja sem sjálfgildi**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="b1a71-135">Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b1a71-136">Í vinstri glugganum finnurðu og velur vinnsluna **1040** (**Afurðir**).</span><span class="sxs-lookup"><span data-stu-id="b1a71-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="b1a71-137">Í aðgerðarúðunni velurðu **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="b1a71-138">Endurtaktu tvö síðustu skref til að keyra vinnslurnar **1070** (**Stilling rásar**) og **1110** (**Altækar stillingar**).</span><span class="sxs-lookup"><span data-stu-id="b1a71-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Stillingar tilgangs gjalda stigveldis fyrirtækis í Retail](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="b1a71-140">Skilgreina sjálfvirkt gjald eftir rás</span><span class="sxs-lookup"><span data-stu-id="b1a71-140">Define auto charges by channel</span></span>

<span data-ttu-id="b1a71-141">Þegar þú hefur kveikt á eiginleikanum **Kveikja á síun sjálfvirkra gjalda eftir rás** og stillt tilgang fyrirtækjastigveldis **Sjálfvirkt gjald í Retail** er hægt að skilgreina sjálfvirk gjöld eftir rás á annaðhvort hausstigi raðar eða línustigi raðar.</span><span class="sxs-lookup"><span data-stu-id="b1a71-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="b1a71-142">Fylgdu þessum skrefum til að skilgreina sjálfvirka gjaldtöku eftir rás í Commerce.</span><span class="sxs-lookup"><span data-stu-id="b1a71-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b1a71-143">Farðu í **Viðskiptakröfur \> Uppsetning gjalda \> Sjálfvirk gjöld**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="b1a71-144">Í vinstri glugganum, í reitnum **Stig**, velurðu annaðhvort **Haus** eða **Lína**, eftir því hverjar viðskiptakröfur þínar eru.</span><span class="sxs-lookup"><span data-stu-id="b1a71-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="b1a71-145">Í reitnum **Númer smásölurásar** velurðu viðeigandi rásakóða (til dæmis, **Tafla** eða **Hópur**).</span><span class="sxs-lookup"><span data-stu-id="b1a71-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="b1a71-146">Ef sjálfgefin stilling, **Allt**, er notuð eru gjaldareglur notaðar á allar rásir.</span><span class="sxs-lookup"><span data-stu-id="b1a71-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="b1a71-147">Ef þú velur **Hópur** skaltu passa að gjaldtökuhópur smásölurásar sé stofnaður í **Retail og Commerce \> Uppsetning rásar \> Gjöld \> Gjaldhópar smásölurásar**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="b1a71-148">Ef þú velur **Tafla** geturðu valið ákveðna rás (til dæmis, **San Fransiskó**) í reitnum **Tengsl smásölurásar**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="b1a71-149">Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b1a71-150">Í vinstri glugganum finnurðu og velur vinnsluna **1040** (**Afurðir**).</span><span class="sxs-lookup"><span data-stu-id="b1a71-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="b1a71-151">Í aðgerðarúðunni velurðu **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="b1a71-152">Endurtaktu tvö síðustu skref til að keyra vinnslurnar **1070** (**Stilling rásar**) og **1110** (**Altækar stillingar**).</span><span class="sxs-lookup"><span data-stu-id="b1a71-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Sjálfvirk gjöld skilgreind eftir rás](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="b1a71-154">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b1a71-154">Example scenario</span></span>

<span data-ttu-id="b1a71-155">Eftirfarandi dæmi sýnir skrefin sem þarf til að stilla vöru þannig að endurvinnslugjöld eru innheimt þegar varan er seld á verslunarrás í San Francisco.</span><span class="sxs-lookup"><span data-stu-id="b1a71-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="b1a71-156">Dæmið sýnir einnig hvernig sjálfvirka gjaldið birtist í POS-forritinu í Commerce.</span><span class="sxs-lookup"><span data-stu-id="b1a71-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="b1a71-157">Fyrirtækið skilgreinir gjaldakóða sem nefndur er **ENDURVINNA** eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="b1a71-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![Gjaldakóðinn ENDURVINNA](media/Auto-charges-charge-code.png)

<span data-ttu-id="b1a71-159">Sjálfvirkt gjald er stofnað á línustiginu.</span><span class="sxs-lookup"><span data-stu-id="b1a71-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="b1a71-160">Það hefur eftirfarandi stillingu:</span><span class="sxs-lookup"><span data-stu-id="b1a71-160">It has the following configuration:</span></span>

- <span data-ttu-id="b1a71-161">Reiturinn **Kóði lykils** er stilltur á **Allt**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="b1a71-162">Reiturinn **Kóði vöru** er stilltur á **Tafla**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="b1a71-163">Reiturinn **Vöruvensl** er stilltur á afurðakennið **91001**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="b1a71-164">Reiturinn **Kóði afhendingarmáta** er stilltur á **Allt**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="b1a71-165">Reiturinn **Kóði smásölurásar** er stilltur á **Tafla**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="b1a71-166">Reiturinn **Tengsl smásölurásar** er stilltur á verslunina í **San Fransiskó**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="b1a71-167">Sjálfvirk gjaldalína er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="b1a71-167">An auto charges line is created.</span></span> <span data-ttu-id="b1a71-168">Það hefur eftirfarandi stillingu:</span><span class="sxs-lookup"><span data-stu-id="b1a71-168">It has the following configuration:</span></span>

- <span data-ttu-id="b1a71-169">Reiturinn **Gjaldmiðill** er stilltur **USD**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="b1a71-170">Reiturinn **Kóði gjalda** er stilltur á **ENDURVINNA**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="b1a71-171">Reiturinn **Flokkur** er stilltur **Fast**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="b1a71-172">Reiturinn **Gjöld** er stilltur á **$6,25**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-172">The **Charges** field is set to **$6.25**.</span></span>

![Stillingar sjálfvirku gjaldalínunnar og sjálfvirku gjaldalínunnar](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="b1a71-174">Í POS-forritinu er sölupöntun stofnuð í verslunarrásinni í **San Fransiskó**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="b1a71-175">Línan **Gjöld** sýnir endurvinnslugjald upp á **$6,25**.</span><span class="sxs-lookup"><span data-stu-id="b1a71-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="b1a71-176">Með því að velja **Færslukosti \> Gjöld \> Stjórna gjöldum** í POS-forritinu geturðu skoðað gjaldakóðann og lýsingu fyrir endurvinnslugjaldið.</span><span class="sxs-lookup"><span data-stu-id="b1a71-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Endurvinnslugjald í POS-forritinu](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="b1a71-178">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b1a71-178">Additional resources</span></span>

[<span data-ttu-id="b1a71-179">Ítarleg sjálfvirk gjöld fyrir omni-rás</span><span class="sxs-lookup"><span data-stu-id="b1a71-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="b1a71-180">Skipta gjöldum í haus í hlutfalli við samsvarandi sölulínur</span><span class="sxs-lookup"><span data-stu-id="b1a71-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]