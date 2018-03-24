---
title: "Skoða og flytja út svæðalýsingar"
description: "Þessi grein er lýst hvernig á að skoða lýsingar á svæðum og hvernig á að nota síðuna lýsingar Svæðið til að flytja út lýsingar."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: cfe5126841905248d0ab04ed9a718098c11bbd22
ms.contentlocale: is-is
ms.lasthandoff: 03/23/2018

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="a5478-103">Skoða og flytja út svæðalýsingar</span><span class="sxs-lookup"><span data-stu-id="a5478-103">View and export field descriptions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a5478-104">Þessi grein er lýst hvernig á að skoða lýsingar á svæðum og hvernig á að nota síðuna lýsingar Svæðið til að flytja út lýsingar.</span><span class="sxs-lookup"><span data-stu-id="a5478-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="a5478-105">Microsoft Dynamics 365 for Finance and Operations er með lýsingar á sumum af flóknarði reitunum.</span><span class="sxs-lookup"><span data-stu-id="a5478-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="a5478-106">Lýsingar á þessum birtist þegar þú músabendil yfir svæði.</span><span class="sxs-lookup"><span data-stu-id="a5478-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="a5478-107">Í **Lýsingar svæðis** síðunni geturðu skoðað og flutt út lýsingar.</span><span class="sxs-lookup"><span data-stu-id="a5478-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="a5478-108">Ekki eru allar síður með lýsingum.</span><span class="sxs-lookup"><span data-stu-id="a5478-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="a5478-109">Við viljum aðeins veita lýsingu fyrir flóknari svæði og ekki þau þar sem notkun svæðisins er augljós.</span><span class="sxs-lookup"><span data-stu-id="a5478-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="a5478-110">Þess vegna sumar síður hafa engar lýsingum sumar síður hafa nokkrar lýsingar og sumar flóknari síðum, eins og margar síður færibreytur hafa margar lýsingar.</span><span class="sxs-lookup"><span data-stu-id="a5478-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="a5478-111">Ef þú hefur aðgang að þróunarumhverfinu í Microsoft Dynamics 365 Finance and Operations geturðu bætt við eigin reitalýsingum og sérsniðið eldri lýsingar.</span><span class="sxs-lookup"><span data-stu-id="a5478-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="a5478-112">Til dæmis er hægt að bæta upplýsingum bundin tilteknu fyrirtæki í lýsing svæðis.</span><span class="sxs-lookup"><span data-stu-id="a5478-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="a5478-113">Nánari upplýsingar eru í svæðahjálpinni í [svæðahjálpinni](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="a5478-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="a5478-114">Sjá svæðislýsingar í notendaviðmótinu</span><span class="sxs-lookup"><span data-stu-id="a5478-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="a5478-115">Hægt er að skoða lýsingar á svæðum með halda yfir á svæðið.</span><span class="sxs-lookup"><span data-stu-id="a5478-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="a5478-116">Sé engin lýsing tiltæk, er hægt að sjá heiti svæðis þegar þú setur músabendil yfir svæðið.</span><span class="sxs-lookup"><span data-stu-id="a5478-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="a5478-117">(Athugasemd: Í Dynamics AX 7.0 (Febrúar 2016) er aðeins hægt að skoða svæðislýsingar á **Svæðið lýsingar** síðu.) Eftirfarandi skýringarmynd sýnir lýsingu sem birtist þegar þú setur músabendil yfir **Læsa vörum á meðan á talningu stendur** svæði.</span><span class="sxs-lookup"><span data-stu-id="a5478-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="a5478-118">[![Dæmi um svæðislýsingu](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="a5478-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="a5478-119">Notið Svæðið lýsingar síðu til þess að skoða og flytja út svæðið hjálp</span><span class="sxs-lookup"><span data-stu-id="a5478-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="a5478-120">Í **Lýsingar svæðis** síðunni geturðu skoðað og flutt út reitalýsingar.</span><span class="sxs-lookup"><span data-stu-id="a5478-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="a5478-121">Hægt er að finna lýsingar sem eru tiltækar fyrir eina síðu í einu.</span><span class="sxs-lookup"><span data-stu-id="a5478-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="a5478-122">Skoða lýsingar á síðu</span><span class="sxs-lookup"><span data-stu-id="a5478-122">View the descriptions for a page</span></span>

<span data-ttu-id="a5478-123">Til að skoða lýsingar fyrir síðu skaltu fylgja þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="a5478-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="a5478-124">Í svæðið **velja síðu** skal færa inn heiti síðunnar.</span><span class="sxs-lookup"><span data-stu-id="a5478-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="a5478-125">Einnig er hægt að smella á örina til að opna lista yfir allar síður, og síðan flett eða sía lista.</span><span class="sxs-lookup"><span data-stu-id="a5478-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="a5478-126">Hægt er að nota heiti síðunnar sem er sýnt í Notendaviðmóti, (til dæmis **Viðskiptavini**)eða kóðanafn (AOT-heiti) sem er tiltæk með því að hægrismella á síðu, (til dæmis **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="a5478-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="a5478-127">Upplýsingar um mismunandi aðferðir til að sía lista yfir síður, sjá hlutann „Leit fyrir síðu" síðar í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="a5478-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="a5478-128">Ef stilltur er **Hafa svæði án lýsingar** valkostur á **Já** birtast öll svæði á síðunni, óháð því hvort þeir hafa lýsing svæðis.</span><span class="sxs-lookup"><span data-stu-id="a5478-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="a5478-129">Flytja út lýsingar á síðu</span><span class="sxs-lookup"><span data-stu-id="a5478-129">Export the descriptions for a page</span></span>

<span data-ttu-id="a5478-130">Til að flytja út lýsingar fyrir síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a5478-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="a5478-131">Velja síðu á **Velja síðu** reitnum.</span><span class="sxs-lookup"><span data-stu-id="a5478-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="a5478-132">Smellið á **Opna í Microsoft Office** hnappinn í hægra efra horninu og smellið á **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="a5478-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="a5478-133">Leita að síðu</span><span class="sxs-lookup"><span data-stu-id="a5478-133">Searching for a page</span></span>

<span data-ttu-id="a5478-134">Nokkrar leiðir eru til að leita að síðu í reitnum **Velja síðu**.</span><span class="sxs-lookup"><span data-stu-id="a5478-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="a5478-135">Í mörgum tilvikum þarf að smella á örina í **Velja síðu** reitnum til að opna fellilistinn og velja úr síaða lista yfir síður.</span><span class="sxs-lookup"><span data-stu-id="a5478-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="a5478-136">Færið inn hluta úr nafni, þá svo skal opna fellilistann til að velja úr lista yfir síaðar síður.</span><span class="sxs-lookup"><span data-stu-id="a5478-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="a5478-137">Opna fellilistinn og smella á annaðhvort titilinn **Síðuheiti** efst á listanum eða **AOT-heiti síðu** titill.</span><span class="sxs-lookup"><span data-stu-id="a5478-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="a5478-138">Þetta opnar svarglugga þar sem hægt er að nota ítarlega síunarvalkosti, eins og **Síðuheiti hefst á**.</span><span class="sxs-lookup"><span data-stu-id="a5478-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="a5478-139">Sláðu inn fullt nafn síðunanr.</span><span class="sxs-lookup"><span data-stu-id="a5478-139">Type the full name of the page.</span></span> <span data-ttu-id="a5478-140">Þegar þessi valkostur er notaður er best að opna fellilistinn og sjá hvað annað er á listanum, jafnvel þótt lýsingum eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="a5478-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="a5478-141">Ef einn nákvæm samsvörun heiti er til staðar birtist lýsing fyrir þá síðu.</span><span class="sxs-lookup"><span data-stu-id="a5478-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="a5478-142">Ef fleiri en einn nákvæm samsvörun er engin lýsingar sýndar.</span><span class="sxs-lookup"><span data-stu-id="a5478-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="a5478-143">Þú verður að Opna í fellilistanum og veljið síðan sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="a5478-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="a5478-144">Ef heiti sem slegið er inn er hluta á nafni á aðra síðu sérðu lýsingu á síðunni.</span><span class="sxs-lookup"><span data-stu-id="a5478-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="a5478-145">Hins vegar ef á fellilistann er opnuð, er að sjá aðrar síður sem innihalda nafninu.</span><span class="sxs-lookup"><span data-stu-id="a5478-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="a5478-146">Til dæmis ekkert lýsingar eru sýnd þegar færa **Talning** í ****Velja síðu ****svæði.</span><span class="sxs-lookup"><span data-stu-id="a5478-146">For example, no descriptions are shown when you type **Counting** in the ****Select a page**** field.</span></span> <span data-ttu-id="a5478-147">Ef opnað er á fellilistanum sést að það eru tvær síður með heitið **"Talning"** auk nokkrum síða sem innihalda orðið "Talning“ í nafni.</span><span class="sxs-lookup"><span data-stu-id="a5478-147">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="a5478-148">Ef valin er síða með AOT-heiti **"InventJournalCount"** birtast svæðislýsingar fyrir þá síðu.</span><span class="sxs-lookup"><span data-stu-id="a5478-148">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="a5478-149">Hins vegar ef fellilistinn er opnuð aftur, sést að listinn inniheldur allar síður sem hafa "InventJournalCount" sem hluti af þeirra AOT-heiti.</span><span class="sxs-lookup"><span data-stu-id="a5478-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="a5478-150">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="a5478-150">Troubleshooting</span></span>
<span data-ttu-id="a5478-151">Eftirfarandi kaflar veita upplýsingar við úrræðaleit vegna vandamála sem koma upp við notkun á svæðislýsingum.</span><span class="sxs-lookup"><span data-stu-id="a5478-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="a5478-152">Ég finn ekki svæðislýsingu</span><span class="sxs-lookup"><span data-stu-id="a5478-152">I can't find a field description</span></span>

<span data-ttu-id="a5478-153">Við höfum verið að bæta við lýsingar fyrir flóknari reitum.</span><span class="sxs-lookup"><span data-stu-id="a5478-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="a5478-154">Ef þú þarft hjálp vegna tiltekins svæðis, skaltu láta okkur vita með því að bæta við athugasemd um þetta efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="a5478-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="a5478-155">Svæðislýsingin er ekki gagnleg</span><span class="sxs-lookup"><span data-stu-id="a5478-155">The field description isn't helpful</span></span>

<span data-ttu-id="a5478-156">Láttu okkur vita með því að bæta við athugasemd um þetta efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="a5478-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="a5478-157">Ef hægt er, lýsa viðbótarupplýsingar sem þarf.</span><span class="sxs-lookup"><span data-stu-id="a5478-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="a5478-158">Ég finnur ekki svæðið á síðunni Svæði lýsingar</span><span class="sxs-lookup"><span data-stu-id="a5478-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="a5478-159">Til að sýna alla reiti á síðu skal stilla valkostinn **Hafa með reiti án lýsingar** á **Já.**</span><span class="sxs-lookup"><span data-stu-id="a5478-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="a5478-160">Smellið á **Velja síðu** svæði til að staðfesta er valin rétt síðu.</span><span class="sxs-lookup"><span data-stu-id="a5478-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="a5478-161">Ef heiti sem fært er inn er hluti af annarri svæðisheiti gæti hafa verið valdar síðu sem hefur lengra heiti.</span><span class="sxs-lookup"><span data-stu-id="a5478-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="a5478-162">Ég finnur ekki svæðið á síðunni Svæði lýsingar</span><span class="sxs-lookup"><span data-stu-id="a5478-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="a5478-163">Upplýsingar um mismunandi aðferðir til að finna síður, sjá hlutann „Leit fyrir síðu" fyrr í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="a5478-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="a5478-164">Ef nákvæmt heiti síðunnar hefur verið fært inn, kunna lýsingar á svæðum ekki að vera sýndar ef er meira en eina síða er með sama heiti.</span><span class="sxs-lookup"><span data-stu-id="a5478-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="a5478-165">Smella á örina í kassanum **Velja síðu** til að opna síaða lista yfir tiltækar síður.</span><span class="sxs-lookup"><span data-stu-id="a5478-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="see-also"></a><span data-ttu-id="a5478-166">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a5478-166">See also</span></span>
--------

[<span data-ttu-id="a5478-167">Sérsníða reit hjálp</span><span class="sxs-lookup"><span data-stu-id="a5478-167">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)





