---
title: Flytja inn skrár á XML-sniði með valeigindum
description: Þetta umræðuefni veitir upplýsingar um að uppsetningu á ER-sniðum sem tilgreina XML-eiginleika til að þátta komandi rafræn skjöl í XML-sniði.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14b14dd609805a7cf9331427012b991791698cfd
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686662"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="5707e-103">Flytja inn skrár á XML-sniði með valeigindum</span><span class="sxs-lookup"><span data-stu-id="5707e-103">Import files in XML format with optional attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5707e-104">Hægt er að setja upp snið rafrænnar skýrslugerðar (ER) til að þátta skjöl á innleið í XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="5707e-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="5707e-105">Hægt er að tilgreina ákveðna eiginleika XML-eininga í uppsettu ER-sniði sem valfrjálsa.</span><span class="sxs-lookup"><span data-stu-id="5707e-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="5707e-106">Það mun gera þér kleift að meðhöndla skrár á innleið og án slíkra XML-eiginleika rétt.</span><span class="sxs-lookup"><span data-stu-id="5707e-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="5707e-107">Síðan er hægt að nota efnið úr þessum skrám til að uppfæra hugbúnaðargögn.</span><span class="sxs-lookup"><span data-stu-id="5707e-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="5707e-108">Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka skrefunum í efninu [(RCS) Flytja inn skrár á XML-sniði með valkvæðum eiginleikum](tasks/import-files-xml-format-optional-attributes.md), sem er hluti af viðskiptaferlinu 7.5.4.3 Acquire/Develop IT þjónusta/lausnarhluti (10677).</span><span class="sxs-lookup"><span data-stu-id="5707e-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="5707e-109">Hægt er að sækja þessar verkleiðbeiningarnar og tengdar sýnisskrár úr [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="5707e-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="5707e-110">Lýsing á efni</span><span class="sxs-lookup"><span data-stu-id="5707e-110">Content description</span></span>       | <span data-ttu-id="5707e-111">Skrá</span><span class="sxs-lookup"><span data-stu-id="5707e-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5707e-112">Sýnisskrá á XML-sniði</span><span class="sxs-lookup"><span data-stu-id="5707e-112">Sample file in XML format</span></span> | <span data-ttu-id="5707e-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="5707e-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="5707e-114">verkefnaleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="5707e-114">Task guide</span></span>                | <span data-ttu-id="5707e-115">RCS Flytja inn skrár á XML-sniði með valkvæðum attributes.axtr</span><span class="sxs-lookup"><span data-stu-id="5707e-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="5707e-116">Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp ER-skilgreiningarsnið til að flytja inn skrár á XML-sniði sem innihalda valkvæðar eigindir.</span><span class="sxs-lookup"><span data-stu-id="5707e-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="5707e-117">Til að ljúka þessum skrefum verður fyrst að ljúka skrefunum í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5707e-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="5707e-118">Áður en þú hefst handa skaltu sækja og vista staðbundið skrána IncomingDocumentToLearnHowToHandleOptionalAttributes.xml frá Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span><span class="sxs-lookup"><span data-stu-id="5707e-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="5707e-119">Farðu í **Fyrirtækisstjórnun** > **Vinnusvæði** > **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="5707e-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="5707e-120">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="5707e-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="5707e-121">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5707e-121">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="5707e-122">Smellið á **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="5707e-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="5707e-123">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="5707e-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="5707e-124">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5707e-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="5707e-125">Í reitnum **Heiti** ritarðu „Líkan til að flytja inn XML-skrá“.</span><span class="sxs-lookup"><span data-stu-id="5707e-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="5707e-126">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="5707e-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="5707e-127">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5707e-127">Click **Designer**.</span></span>
5. <span data-ttu-id="5707e-128">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5707e-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="5707e-129">Í reitnum **Heiti** skaltu færa inn „Rót“.</span><span class="sxs-lookup"><span data-stu-id="5707e-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="5707e-130">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="5707e-130">Click **Add**.</span></span>
8. <span data-ttu-id="5707e-131">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5707e-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="5707e-132">Í reitnum **Heiti** skaltu færa inn „Listi“.</span><span class="sxs-lookup"><span data-stu-id="5707e-132">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="5707e-133">Í reitnum **Gerð vöru** velurðu **Skráalisti**.</span><span class="sxs-lookup"><span data-stu-id="5707e-133">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="5707e-134">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="5707e-134">Click **Add**.</span></span>
12.    <span data-ttu-id="5707e-135">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5707e-135">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="5707e-136">Í reitnum **Heiti** skal færa inn „kóða“.</span><span class="sxs-lookup"><span data-stu-id="5707e-136">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="5707e-137">Í reitnum **Gerð vöru** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="5707e-137">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="5707e-138">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="5707e-138">Click **Add**.</span></span>
16.    <span data-ttu-id="5707e-139">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5707e-139">Click **Save**.</span></span>
17.    <span data-ttu-id="5707e-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5707e-140">Close the page.</span></span>
18.    <span data-ttu-id="5707e-141">Smelltu á **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="5707e-141">Click **Change status**.</span></span>
19.    <span data-ttu-id="5707e-142">Smelltu á **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="5707e-142">Click **Complete**.</span></span>
20.    <span data-ttu-id="5707e-143">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="5707e-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="5707e-144">Stofnaðu snið fyrir gagnaflutning</span><span class="sxs-lookup"><span data-stu-id="5707e-144">Create a format for data import</span></span>
1. <span data-ttu-id="5707e-145">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5707e-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="5707e-146">Í reitnum **Nýtt** skaltu færa inn „Snið byggir á gagnalíkani Líkan til að flytja inn xml-skrá“.</span><span class="sxs-lookup"><span data-stu-id="5707e-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="5707e-147">Í reitnum **Heiti** ritarðu „Sníða til að flytja inn XML-skrá“.</span><span class="sxs-lookup"><span data-stu-id="5707e-147">In the **Nam** e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="5707e-148">Veldu **Já** í reitnum **Styður gagnainnflutning**.</span><span class="sxs-lookup"><span data-stu-id="5707e-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="5707e-149">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="5707e-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="5707e-150">Settu upp snið til að þátta komandi skrá í xml-sniði</span><span class="sxs-lookup"><span data-stu-id="5707e-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="5707e-151">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5707e-151">Click **Designer**.</span></span>
2. <span data-ttu-id="5707e-152">Smellið á **Bæta við rót** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5707e-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="5707e-153">Í trénu skal velja **XML/Element**.</span><span class="sxs-lookup"><span data-stu-id="5707e-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="5707e-154">Í reitnum **Heiti** skaltu færa inn „rót“.</span><span class="sxs-lookup"><span data-stu-id="5707e-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="5707e-155">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="5707e-155">Click **OK**.</span></span>
6. <span data-ttu-id="5707e-156">Smellið á **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5707e-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="5707e-157">Í trénu skal velja **XML/Element**.</span><span class="sxs-lookup"><span data-stu-id="5707e-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="5707e-158">Í reitnum **Heiti** skaltu færa inn „skjal“.</span><span class="sxs-lookup"><span data-stu-id="5707e-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="5707e-159">Í reitnum **Margfeldi** skaltu velja **Einn margir**.</span><span class="sxs-lookup"><span data-stu-id="5707e-159">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="5707e-160">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="5707e-160">Click **OK**.</span></span>
11.    <span data-ttu-id="5707e-161">Í trénu velurðu **rót\skjal**.</span><span class="sxs-lookup"><span data-stu-id="5707e-161">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="5707e-162">Smellið á **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5707e-162">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="5707e-163">Í trénu skal velja **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="5707e-163">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="5707e-164">Í reitinn **Heiti** ritarðu „kenni“.</span><span class="sxs-lookup"><span data-stu-id="5707e-164">In the **Name** field, type 'id'.</span></span>
15.    <span data-ttu-id="5707e-165">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="5707e-165">Click **OK**.</span></span>
16.    <span data-ttu-id="5707e-166">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5707e-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="5707e-167">Settu upp sniðvörpun til að vista þáttaðar upplýsingar í gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="5707e-167">Design a format mapping to save parsed information to data model</span></span>
1.    <span data-ttu-id="5707e-168">Smelltu á **Varpa sniði á líkan**.</span><span class="sxs-lookup"><span data-stu-id="5707e-168">Click **Map format to model**.</span></span>
2.    <span data-ttu-id="5707e-169">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5707e-169">Click **New**.</span></span>
3.    <span data-ttu-id="5707e-170">Í reitnum **Skilgreining** skaltu slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5707e-170">In the **Definition** field, enter or select a value.</span></span>
4.    <span data-ttu-id="5707e-171">Í reitnum **Heiti** skaltu færa inn „Vörpun“.</span><span class="sxs-lookup"><span data-stu-id="5707e-171">In the **Name** field, type 'Mapping'.</span></span>
5.    <span data-ttu-id="5707e-172">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5707e-172">Click **Save**.</span></span>
6.    <span data-ttu-id="5707e-173">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5707e-173">Click **Designer**.</span></span>
7.    <span data-ttu-id="5707e-174">Í trénu skal víkka út **snið**.</span><span class="sxs-lookup"><span data-stu-id="5707e-174">In the tree, expand **format**.</span></span>
8.    <span data-ttu-id="5707e-175">Í trénu skal útvíkka **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="5707e-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.    <span data-ttu-id="5707e-176">Í trénu skal velja \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="5707e-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5707e-177">(fylgiskjal)\*\*.</span><span class="sxs-lookup"><span data-stu-id="5707e-177">(document)\*\*.</span></span>
10.    <span data-ttu-id="5707e-178">Smelltu á **Binda**.</span><span class="sxs-lookup"><span data-stu-id="5707e-178">Click **Bind**.</span></span>
11.    <span data-ttu-id="5707e-179">Í trénu skal útvíkka \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="5707e-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5707e-180">(fylgiskjal)\*\*.</span><span class="sxs-lookup"><span data-stu-id="5707e-180">(document)\*\*.</span></span>
12.    <span data-ttu-id="5707e-181">Í trénu skal velja \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="5707e-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5707e-182">(fylgiskjal)\kenni\*\*.</span><span class="sxs-lookup"><span data-stu-id="5707e-182">(document)\id\*\*.</span></span>
13.    <span data-ttu-id="5707e-183">Í trénu skaltu stækka **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="5707e-183">In the tree, expand **List = format.root.document**.</span></span>
14.    <span data-ttu-id="5707e-184">Í trénu skaltu velja **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="5707e-184">In the tree, select **List = format.root.document\Code**.</span></span>
15.    <span data-ttu-id="5707e-185">Smelltu á **Binda**.</span><span class="sxs-lookup"><span data-stu-id="5707e-185">Click **Bind**.</span></span>
16.    <span data-ttu-id="5707e-186">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5707e-186">Click **Save**.</span></span>
17.    <span data-ttu-id="5707e-187">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5707e-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="5707e-188">Keyra sniðsvörpun</span><span class="sxs-lookup"><span data-stu-id="5707e-188">Run format mapping</span></span>
1. <span data-ttu-id="5707e-189">Smelltu á **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="5707e-189">Click **Run**.</span></span>
2. <span data-ttu-id="5707e-190">Smelltu á **Fletta** og veldu skrána **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="5707e-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="5707e-191">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="5707e-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="5707e-192">Valin skrá hefur ekki verið flutt inn þar sem sniðhönnunin gerir ráð fyrir að eigindin „kenni“ sé til staðar fyrir eininguna „skjal“, en innflutt skrá inniheldur engar slíkar eigindir.</span><span class="sxs-lookup"><span data-stu-id="5707e-192">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="5707e-193">Breyta sniðsskipulagi til að meðhöndla xml-eigindi sem valfrjáls</span><span class="sxs-lookup"><span data-stu-id="5707e-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="5707e-194">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5707e-194">Close the page.</span></span>
2. <span data-ttu-id="5707e-195">Í trénu stækkarðu **rót\skjal**.</span><span class="sxs-lookup"><span data-stu-id="5707e-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="5707e-196">Í trénu velurðu **rót\skjal\kenni**.</span><span class="sxs-lookup"><span data-stu-id="5707e-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="5707e-197">Í reitnum **Tómur strengur fyrir eigind sem vantar** velurðu **Já**.</span><span class="sxs-lookup"><span data-stu-id="5707e-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="5707e-198">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5707e-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="5707e-199">Keyra sniðvörpun til að prófa breytingar</span><span class="sxs-lookup"><span data-stu-id="5707e-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="5707e-200">Smelltu á **Varpa sniði á líkan**.</span><span class="sxs-lookup"><span data-stu-id="5707e-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="5707e-201">Smelltu á **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="5707e-201">Click **Run**.</span></span>
3. <span data-ttu-id="5707e-202">Smelltu á **Fletta** og veldu skrána **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="5707e-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="5707e-203">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="5707e-203">Click **OK**.</span></span>
5. <span data-ttu-id="5707e-204">Yfirfara myndaða skrá.</span><span class="sxs-lookup"><span data-stu-id="5707e-204">Review the generated file.</span></span> <span data-ttu-id="5707e-205">Athugaðu að sama skrá hefur verið flutt inn þar sem sniðshönnunin telur nú að eigindin „kenni“ fyrir eininguna „fylgiskjal“ sé valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="5707e-205">Note that same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>
