---
title: (RCS) Flytja inn skrár á XML-sniði með valkvæmum eigindum
description: Þetta efni veitir upplýsingar um hvernig notandi getur sett upp skilgreiningu ER-sniðs til að flytja inn skrár á XML-sniði sem inniheldur valkvæð eigindi.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc28e9a2170929c6cd8daafd7eae54713cec36ff
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143201"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="d0490-103">(RCS) Flytja inn skrár á XML-sniði með valkvæmum eigindum</span><span class="sxs-lookup"><span data-stu-id="d0490-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0490-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp ER-skilgreiningarsnið til að flytja inn skrár á XML-sniði sem innihalda valkvæðar eigindir.</span><span class="sxs-lookup"><span data-stu-id="d0490-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="d0490-105">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="d0490-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="d0490-106">Áður en þú hefst handa skaltu sækja og vista staðbundið skrána IncomingDocumentToLearnHowToHandleOptionalAttributes.xml frá [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="d0490-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="d0490-107">Farðu í **Öll vinnusvæði** > **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="d0490-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="d0490-108">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="d0490-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="d0490-109">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d0490-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="d0490-110">Smellið á **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="d0490-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="d0490-111">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="d0490-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="d0490-112">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d0490-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="d0490-113">Í reitnum **Heiti** ritarðu „Líkan til að flytja inn XML-skrá“.</span><span class="sxs-lookup"><span data-stu-id="d0490-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="d0490-114">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="d0490-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="d0490-115">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="d0490-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="d0490-116">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d0490-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="d0490-117">Í reitnum **Heiti** skaltu færa inn „Rót“.</span><span class="sxs-lookup"><span data-stu-id="d0490-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="d0490-118">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="d0490-118">Click **Add**.</span></span>
8.    <span data-ttu-id="d0490-119">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d0490-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="d0490-120">Í reitnum **Heiti** skaltu færa inn „Listi“.</span><span class="sxs-lookup"><span data-stu-id="d0490-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="d0490-121">Í reitnum **Gerð vöru** velurðu **Skráalisti**.</span><span class="sxs-lookup"><span data-stu-id="d0490-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="d0490-122">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="d0490-122">Click **Add**.</span></span>
12.    <span data-ttu-id="d0490-123">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d0490-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="d0490-124">Í reitnum **Heiti** skal færa inn „kóða“.</span><span class="sxs-lookup"><span data-stu-id="d0490-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="d0490-125">Í reitnum **Gerð vöru** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="d0490-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="d0490-126">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="d0490-126">Click **Add**.</span></span>
16.    <span data-ttu-id="d0490-127">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d0490-127">Click **Save**.</span></span>
17.    <span data-ttu-id="d0490-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d0490-128">Close the page.</span></span>
18.    <span data-ttu-id="d0490-129">Smelltu á **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="d0490-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="d0490-130">Smelltu á **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="d0490-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="d0490-131">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0490-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="d0490-132">Stofnaðu snið fyrir gagnaflutning</span><span class="sxs-lookup"><span data-stu-id="d0490-132">Create a format for data import</span></span>
1.    <span data-ttu-id="d0490-133">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d0490-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="d0490-134">Í reitnum **Nýtt** skaltu færa inn „Snið byggir á gagnalíkani Líkan til að flytja inn xml-skrá“.</span><span class="sxs-lookup"><span data-stu-id="d0490-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="d0490-135">Í reitnum **Heiti** ritarðu „Sníða til að flytja inn XML-skrá“.</span><span class="sxs-lookup"><span data-stu-id="d0490-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="d0490-136">Veldu **Já** í reitnum **Styður gagnainnflutning**.</span><span class="sxs-lookup"><span data-stu-id="d0490-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="d0490-137">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="d0490-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="d0490-138">Settu upp snið til að þátta komandi skrá í xml-sniði</span><span class="sxs-lookup"><span data-stu-id="d0490-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="d0490-139">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="d0490-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="d0490-140">Smellið á **Bæta við rót** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d0490-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="d0490-141">Í trénu skal velja **XML/Element**.</span><span class="sxs-lookup"><span data-stu-id="d0490-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="d0490-142">Í reitnum **Heiti** skaltu færa inn „rót“.</span><span class="sxs-lookup"><span data-stu-id="d0490-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="d0490-143">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0490-143">Click **OK**.</span></span>
6.    <span data-ttu-id="d0490-144">Smellið á **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d0490-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="d0490-145">Í trénu skal velja **XML/Element**.</span><span class="sxs-lookup"><span data-stu-id="d0490-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="d0490-146">Í reitnum **Heiti** skaltu færa inn „skjal“.</span><span class="sxs-lookup"><span data-stu-id="d0490-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="d0490-147">Í reitnum **Margfeldi** skaltu velja **Einn margir**.</span><span class="sxs-lookup"><span data-stu-id="d0490-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="d0490-148">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0490-148">Click **OK**.</span></span>
11.    <span data-ttu-id="d0490-149">Í trénu velurðu **rót\skjal**.</span><span class="sxs-lookup"><span data-stu-id="d0490-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="d0490-150">Smellið á **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d0490-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="d0490-151">Í trénu skal velja **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="d0490-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="d0490-152">Í reitinn **Heiti** ritarðu „Kenni“.</span><span class="sxs-lookup"><span data-stu-id="d0490-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="d0490-153">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0490-153">Click **OK**.</span></span>
16.    <span data-ttu-id="d0490-154">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d0490-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="d0490-155">Settu upp sniðvörpun til að vista þáttaðar upplýsingar í gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="d0490-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="d0490-156">Smelltu á **Varpa sniði á líkan**.</span><span class="sxs-lookup"><span data-stu-id="d0490-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="d0490-157">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d0490-157">Click **New**.</span></span>
3. <span data-ttu-id="d0490-158">Í reitnum **Skilgreining** skaltu slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d0490-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="d0490-159">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d0490-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d0490-160">Í reitnum **Heiti** skaltu færa inn „Vörpun“.</span><span class="sxs-lookup"><span data-stu-id="d0490-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="d0490-161">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d0490-161">Click **Save**.</span></span>
7. <span data-ttu-id="d0490-162">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="d0490-162">Click **Designer**.</span></span>
8. <span data-ttu-id="d0490-163">Í trénu skal víkka út **snið**.</span><span class="sxs-lookup"><span data-stu-id="d0490-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="d0490-164">Í trénu skal útvíkka **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="d0490-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="d0490-165">Í trénu skal velja \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="d0490-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="d0490-166">(fylgiskjal)\*\*.</span><span class="sxs-lookup"><span data-stu-id="d0490-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="d0490-167">Smelltu á **Binda**.</span><span class="sxs-lookup"><span data-stu-id="d0490-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="d0490-168">Í trénu skal útvíkka \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="d0490-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="d0490-169">(fylgiskjal)\*\*.</span><span class="sxs-lookup"><span data-stu-id="d0490-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="d0490-170">Í trénu skal velja \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="d0490-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="d0490-171">(fylgiskjal)\kenni\*\*.</span><span class="sxs-lookup"><span data-stu-id="d0490-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="d0490-172">Í trénu skaltu stækka **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="d0490-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="d0490-173">Í trénu skaltu velja **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="d0490-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="d0490-174">Smelltu á **Binda**.</span><span class="sxs-lookup"><span data-stu-id="d0490-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="d0490-175">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d0490-175">Click **Save**.</span></span>
18.    <span data-ttu-id="d0490-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d0490-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="d0490-177">Keyra sniðsvörpun</span><span class="sxs-lookup"><span data-stu-id="d0490-177">Run format mapping</span></span>
1. <span data-ttu-id="d0490-178">Smelltu á **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="d0490-178">Click **Run**.</span></span>
2. <span data-ttu-id="d0490-179">Smelltu á **Fletta** og veldu **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="d0490-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="d0490-180">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0490-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="d0490-181">Valin skrá hefur ekki verið flutt inn þar sem sniðhönnunin gerir ráð fyrir að eigindin „kenni“ sé til staðar fyrir eininguna „skjal“, en innflutt skrá inniheldur engar slíkar eigindir.</span><span class="sxs-lookup"><span data-stu-id="d0490-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="d0490-182">Breyta sniðsskipulagi til að meðhöndla xml-eigindi sem valfrjáls</span><span class="sxs-lookup"><span data-stu-id="d0490-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="d0490-183">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d0490-183">Close the page.</span></span>
2. <span data-ttu-id="d0490-184">Í trénu stækkarðu **rót\skjal**.</span><span class="sxs-lookup"><span data-stu-id="d0490-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="d0490-185">Í trénu velurðu **rót\skjal\kenni**.</span><span class="sxs-lookup"><span data-stu-id="d0490-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="d0490-186">Veldu **Já** í reitnum **Tómur strengur fyrir eigind sem vantar**.</span><span class="sxs-lookup"><span data-stu-id="d0490-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="d0490-187">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d0490-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="d0490-188">Keyra sniðvörpun til að prófa breytingar</span><span class="sxs-lookup"><span data-stu-id="d0490-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="d0490-189">Smelltu á **Varpa sniði á líkan**.</span><span class="sxs-lookup"><span data-stu-id="d0490-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="d0490-190">Smelltu á **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="d0490-190">Click **Run**.</span></span>
3. <span data-ttu-id="d0490-191">Smelltu á **Fletta** og veldu skrána **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="d0490-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="d0490-192">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0490-192">Click **OK**.</span></span>
5. <span data-ttu-id="d0490-193">Yfirfara myndaða skrá.</span><span class="sxs-lookup"><span data-stu-id="d0490-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="d0490-194">Sama skrá hefur verið flutt inn þar sem sniðshönnunin telur nú að eigindin „kenni“ fyrir eininguna „fylgiskjal“ sé valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="d0490-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>
