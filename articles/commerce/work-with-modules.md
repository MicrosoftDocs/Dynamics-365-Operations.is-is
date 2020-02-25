---
title: Vinna með einingar
description: Þetta efni lýsir því hvernig og hvenær á að nota einingar í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025880"
---
# <a name="work-with-modules"></a><span data-ttu-id="f2f91-103">Vinna með einingar</span><span class="sxs-lookup"><span data-stu-id="f2f91-103">Work with modules</span></span>

<span data-ttu-id="f2f91-104">Þetta efni lýsir því hvernig og hvenær á að nota einingar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2f91-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>


[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="f2f91-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f2f91-105">Overview</span></span>

<span data-ttu-id="f2f91-106">Einingar eru rökréttir byggingarreitir sem mynda síðuuppbyggingu þína og þau hafa ýmsan tilgang og gildissvið.</span><span class="sxs-lookup"><span data-stu-id="f2f91-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="f2f91-107">Sumir einingar eru hástigs gámar og eini tilgangur þeirra er að halda og skipuleggja aðrar einingar (undireiningar).</span><span class="sxs-lookup"><span data-stu-id="f2f91-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="f2f91-108">Aðrar einingar, svo sem einföld myndstaðsetningareining, hafa mjög sérstakan tilgang.</span><span class="sxs-lookup"><span data-stu-id="f2f91-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="f2f91-109">Aðrar einingar, svo sem hringekjueining, falla einhvers staðar á milli þessara tveggja flokka.</span><span class="sxs-lookup"><span data-stu-id="f2f91-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="f2f91-110">Sjálfgefið er svæði þitt í Dynamics 365 Commerce inniheldur byrjunarbúnaðareiningasafn sem gerir þér kleift að ná flestum grundvallaratriðum fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="f2f91-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="f2f91-111">Þú ættir að geta smíðað vefsvæði frá einni verslun til annarrar með því að nota þessar einingar.</span><span class="sxs-lookup"><span data-stu-id="f2f91-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="f2f91-112">Hins vegar gætirðu líka viljað aðlaga þessa einingar eða smíða nýjar sérsniðnar einingar fyrir sérstakar þarfir.</span><span class="sxs-lookup"><span data-stu-id="f2f91-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="f2f91-113">Ef þú vilt smíða sérsniðnar einingar er hugbúnaðarþróunarbúnaður (SDK) í boði til að hjálpa þér að búa til sérsniðið einingasafn.</span><span class="sxs-lookup"><span data-stu-id="f2f91-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="f2f91-114">Gámaeiningar og -hólf</span><span class="sxs-lookup"><span data-stu-id="f2f91-114">Container modules and slots</span></span>

<span data-ttu-id="f2f91-115">Eins og áður var getið eru sumar einingar hannaðar til að innihalda undireiningar.</span><span class="sxs-lookup"><span data-stu-id="f2f91-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="f2f91-116">Þessar einingar eru þekktar sem *gámar* og þær gera ráð fyrir stigveldum ívafinna eininga.</span><span class="sxs-lookup"><span data-stu-id="f2f91-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="f2f91-117">Gámaeiningar innihalda *hólf*.</span><span class="sxs-lookup"><span data-stu-id="f2f91-117">Container modules include *slots*.</span></span> <span data-ttu-id="f2f91-118">Hólf eru notuð til að takast á við skipulag og tilgang undireininga í gámnum.</span><span class="sxs-lookup"><span data-stu-id="f2f91-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="f2f91-119">Dæmi um það er grunnsíðugámaeining (efsta stigs eining fyrir hverja síðu) sem skilgreinir nokkur mikilvæg hólf:</span><span class="sxs-lookup"><span data-stu-id="f2f91-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="f2f91-120">Fyrirsagnarhólf</span><span class="sxs-lookup"><span data-stu-id="f2f91-120">A header slot</span></span>
- <span data-ttu-id="f2f91-121">Meginmálshólf</span><span class="sxs-lookup"><span data-stu-id="f2f91-121">A body slot</span></span>
- <span data-ttu-id="f2f91-122">Síðufótarhólf</span><span class="sxs-lookup"><span data-stu-id="f2f91-122">A footer slot</span></span>

<span data-ttu-id="f2f91-123">Þróunaraðili einingarinnar skilgreinir þessi hólf og ákvarðar hvaða undireiningar og hversu margar undireiningar má setja beint í þau.</span><span class="sxs-lookup"><span data-stu-id="f2f91-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="f2f91-124">Til dæmis gæti fyrirsagnarhólfið aðeins stutt eina einingu af gerðinni **Fyrirsagnareining** en meginmálshólfið gæti stutt ótakmarkaðan fjölda eininga af hvaða gerð sem er (nema aðrar gámaeiningar á síðunni).</span><span class="sxs-lookup"><span data-stu-id="f2f91-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="f2f91-125">Í höfundatækjunum þurfa síðuhöfundar ekki að vita fyrirfram hvaða einingar er hægt og ekki hægt að setja í hvert hólf.</span><span class="sxs-lookup"><span data-stu-id="f2f91-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="f2f91-126">Þegar síðuhöfundar velja hólf og reyna síðan að velja einingu til að bæta við það sjá þeir síaða mynd af gerðum eininga sem eru studdar fyrir það hólf.</span><span class="sxs-lookup"><span data-stu-id="f2f91-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="f2f91-127">Innihaldseiningar</span><span class="sxs-lookup"><span data-stu-id="f2f91-127">Content modules</span></span>

<span data-ttu-id="f2f91-128">Innihaldseiningar innihalda efni og fjölmiðlaþætti, svo sem texta (til dæmis fyrirsagnir, málsgreinar og krækjur) eða tilvísanir í eignir (til dæmis myndir, myndskeið og PDF skjöl).</span><span class="sxs-lookup"><span data-stu-id="f2f91-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="f2f91-129">Dæmi um dæmigerðar gerðir innihaldseininga eru **Hetja**, **Eiginleiki** og **Borði**.</span><span class="sxs-lookup"><span data-stu-id="f2f91-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="f2f91-130">Einingar af þessum þremur gerðum geta innihaldið texta eða miðla og þeir þurfa ekki neinar undireiningar til að gera eitthvað sýnilegt á síðu.</span><span class="sxs-lookup"><span data-stu-id="f2f91-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="f2f91-131">Meirihluti dæmigerðra, daglegra síðu- og efnisskriftaaðgerða fela í sér efniseiningar, fyrst og fremst vegna þess að þessar einingar skilgreina raunverulegt innihald sem birt er í yfirgámaeiningum þeirra.</span><span class="sxs-lookup"><span data-stu-id="f2f91-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="f2f91-132">Margar efniseiningar eru í boði og þessar einingar eru venjulega síðustu verkin sem þú bætir við stigveldi síðunnar með ívöfðum einingum.</span><span class="sxs-lookup"><span data-stu-id="f2f91-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="f2f91-133">Eftirfarandi mynd sýnir hvernig einingar eru ívafðar innan í einingahólfum yfirgáms.</span><span class="sxs-lookup"><span data-stu-id="f2f91-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Ívafðar einingar](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="f2f91-135">Bæta við eða fjarlægja einingar</span><span class="sxs-lookup"><span data-stu-id="f2f91-135">Add or remove modules</span></span>

<span data-ttu-id="f2f91-136">Eftirfarandi aðferðir lýsa því hvernig á að bæta við og fjarlægja einingar.</span><span class="sxs-lookup"><span data-stu-id="f2f91-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="f2f91-137">Bæta við einingu</span><span class="sxs-lookup"><span data-stu-id="f2f91-137">Add a module</span></span>

<span data-ttu-id="f2f91-138">Til að bæta einingu við hólf eða gám á síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f2f91-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="f2f91-139">Veldu útlínugluggann til vinstri til að velja gám eða hólf sem hægt er að bæta undireiningunni við.</span><span class="sxs-lookup"><span data-stu-id="f2f91-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2f91-140">Einingahönnuðurinn skilgreinir listann yfir gerðir eininga sem hægt er að bæta við tiltekið hólf fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="f2f91-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="f2f91-141">Höfundar sniðmáts geta síðan fínstillt leyfða einingavalkosti til að tryggja stöðuga leitarvélabestun (SEO) og höfundarvirkni fyrir allar síðurnar sem eru smíðaðar úr ákveðnu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="f2f91-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="f2f91-142">Veldu úrfellingarhnappinn (**...**) fyrir eininguna og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="f2f91-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="f2f91-143">Valmyndin **Bæta við einingu** birtist.</span><span class="sxs-lookup"><span data-stu-id="f2f91-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="f2f91-144">Þessi gluggi er sjálfvirkt síaður þannig að hann sýnir aðeins einingar sem eru studdar í völdum gámi eða hólfi.</span><span class="sxs-lookup"><span data-stu-id="f2f91-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="f2f91-145">Listinn yfir einingar ræðst af sniðmáti síðunnar eða skilgreiningu gámaeiningar.</span><span class="sxs-lookup"><span data-stu-id="f2f91-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2f91-146">Ef gámur eða hólf styður ekki nýjar undireiningar er valkosturinn **Bæta við einingu** er ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="f2f91-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="f2f91-147">Leitaðu að og veldu einingu til að bæta við síðuna í valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="f2f91-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="f2f91-148">**Eiginleiki** og **Hetja** eru góðar einingagerðir fyrir byrjendur að vinna með.</span><span class="sxs-lookup"><span data-stu-id="f2f91-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="f2f91-149">Veldu **Í lagi** til að bæta valinni einingu við valinn gám eða hólf á síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="f2f91-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="f2f91-150">Fjarlægja einingu</span><span class="sxs-lookup"><span data-stu-id="f2f91-150">Remove a module</span></span>

<span data-ttu-id="f2f91-151">Til að fjarlægja einingu úr hólfi eða gámi á síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f2f91-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="f2f91-152">Veldu útlínuhnappinn við hliðina á nafni einingarinnar sem á að fjarlægja í yfirlitsrúðunni til vinstri og veldu síðan ruslatunnuhnappinn.</span><span class="sxs-lookup"><span data-stu-id="f2f91-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="f2f91-153">Þegar þú færð kvaðningu um að staðfesta að þú viljir fjarlægja eininguna skaltu velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f2f91-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="f2f91-154">Skilgreina einingar</span><span class="sxs-lookup"><span data-stu-id="f2f91-154">Configure modules</span></span>

<span data-ttu-id="f2f91-155">Eftirfarandi aðferðir lýsa því hvernig á að skilgreina efnis- og gámaeiningar.</span><span class="sxs-lookup"><span data-stu-id="f2f91-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="f2f91-156">Stilla innihaldseiningu</span><span class="sxs-lookup"><span data-stu-id="f2f91-156">Configure a content module</span></span>

<span data-ttu-id="f2f91-157">Fylgdu þessum skrefum til að stilla efniseiningu á síðu.</span><span class="sxs-lookup"><span data-stu-id="f2f91-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="f2f91-158">Veldu útlínugluggann til vinstri stækkarðu tréð og velur einhverja eininga fyrir efni (til dæmis, **Eiginleiki**, **Hetja** eða **Borði**).</span><span class="sxs-lookup"><span data-stu-id="f2f91-158">In the outline pane on the left, expand the tree and select any content module (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="f2f91-159">Finndu innihald og stillingarstýringar einingarinnar á eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="f2f91-159">In the properties pane on the right, find the module's content and settings controls.</span></span>
1. <span data-ttu-id="f2f91-160">Sláðu inn eiginleika fyrir allar viðeigandi einingarstýringar.</span><span class="sxs-lookup"><span data-stu-id="f2f91-160">Enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="f2f91-161">Veldu **Vista** í skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="f2f91-161">Select **Save** in the command bar.</span></span> <span data-ttu-id="f2f91-162">Þetta mun einnig endurnýja forskoðunardúkinn.</span><span class="sxs-lookup"><span data-stu-id="f2f91-162">This will also refresh the preview canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="f2f91-163">Stillla gámaeiningu</span><span class="sxs-lookup"><span data-stu-id="f2f91-163">Configure a container module</span></span>

<span data-ttu-id="f2f91-164">Fylgdu þessum skrefum til að stilla gámaeiningu á síðu.</span><span class="sxs-lookup"><span data-stu-id="f2f91-164">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="f2f91-165">Veldu gámaeiningu á síðunni (til dæmis hringekju- eða vökvagámaeiningu).</span><span class="sxs-lookup"><span data-stu-id="f2f91-165">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="f2f91-166">Í eiginleikaglugganum til hægri skaltu stækka ívafðar stýringarnar með því að velja hausana og stilla öll nauðsynleg stjórnunargildi.</span><span class="sxs-lookup"><span data-stu-id="f2f91-166">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="f2f91-167">Í útlínuglugganum til vinstri velurðu úrfellingarhnappinn við hliðina á heiti annaðhvort gámsins eða hólfa innan í gámnum og síðan velurðu **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="f2f91-167">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="f2f91-168">Bættu síðan undireiningum við valinn gám.</span><span class="sxs-lookup"><span data-stu-id="f2f91-168">Then, add child modules to the selected container.</span></span> <span data-ttu-id="f2f91-169">Fyrir frekari upplýsingar, sjá hlutann [Vinna með einingar](#add-a-module) fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="f2f91-169">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="f2f91-170">Ef margar undireiningar eru til sem systkini í yfirgámi geturðu breytt skjápöntun þeirra í yfirgámnum.</span><span class="sxs-lookup"><span data-stu-id="f2f91-170">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="f2f91-171">Veldu úrfellingarhnappinn fyrir eininguna og notaðu síðan upp örina og örvatakkana.</span><span class="sxs-lookup"><span data-stu-id="f2f91-171">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2f91-172">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f2f91-172">Additional resources</span></span>

[<span data-ttu-id="f2f91-173">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="f2f91-173">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f2f91-174">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="f2f91-174">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="f2f91-175">Vinna með forstillt útlit</span><span class="sxs-lookup"><span data-stu-id="f2f91-175">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="f2f91-176">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="f2f91-176">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="f2f91-177">Bæta gámaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="f2f91-177">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="f2f91-178">Vinna með birtingarhópa</span><span class="sxs-lookup"><span data-stu-id="f2f91-178">Work with publish groups</span></span>](publish-groups.md)

