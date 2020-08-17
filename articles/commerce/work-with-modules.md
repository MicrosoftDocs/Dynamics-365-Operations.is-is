---
title: Vinna með einingar
description: Þetta efni lýsir því hvernig og hvenær á að nota einingar í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: da430857801d8007244c04aadd325e99c0b882c5
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646016"
---
# <a name="work-with-modules"></a><span data-ttu-id="c9a91-103">Vinna með einingar</span><span class="sxs-lookup"><span data-stu-id="c9a91-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c9a91-104">Þetta efni lýsir því hvernig og hvenær á að nota einingar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9a91-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c9a91-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c9a91-105">Overview</span></span>

<span data-ttu-id="c9a91-106">Einingar eru rökréttir byggingarreitir sem mynda síðuuppbyggingu þína og þau hafa ýmsan tilgang og gildissvið.</span><span class="sxs-lookup"><span data-stu-id="c9a91-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="c9a91-107">Sumir einingar eru hástigs gámar og eini tilgangur þeirra er að halda og skipuleggja aðrar einingar (undireiningar).</span><span class="sxs-lookup"><span data-stu-id="c9a91-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="c9a91-108">Aðrar einingar, svo sem einföld myndstaðsetningareining, hafa mjög sérstakan tilgang.</span><span class="sxs-lookup"><span data-stu-id="c9a91-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="c9a91-109">Aðrar einingar, svo sem hringekjueining, falla einhvers staðar á milli þessara tveggja flokka.</span><span class="sxs-lookup"><span data-stu-id="c9a91-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="c9a91-110">Sjálfgefið er svæði þitt í Dynamics 365 Commerce inniheldur byrjunarbúnaðareiningasafn sem gerir þér kleift að ná flestum grundvallaratriðum fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="c9a91-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="c9a91-111">Þú ættir að geta smíðað vefsvæði frá einni verslun til annarrar með því að nota þessar einingar.</span><span class="sxs-lookup"><span data-stu-id="c9a91-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="c9a91-112">Hins vegar gætirðu líka viljað aðlaga þessa einingar eða smíða nýjar sérsniðnar einingar fyrir sérstakar þarfir.</span><span class="sxs-lookup"><span data-stu-id="c9a91-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="c9a91-113">Ef þú vilt smíða sérsniðnar einingar er hugbúnaðarþróunarbúnaður (SDK) í boði til að hjálpa þér að búa til sérsniðið einingasafn.</span><span class="sxs-lookup"><span data-stu-id="c9a91-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="c9a91-114">Gámaeiningar og -hólf</span><span class="sxs-lookup"><span data-stu-id="c9a91-114">Container modules and slots</span></span>

<span data-ttu-id="c9a91-115">Eins og áður var getið eru sumar einingar hannaðar til að innihalda undireiningar.</span><span class="sxs-lookup"><span data-stu-id="c9a91-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="c9a91-116">Þessar einingar eru þekktar sem *gámar* og þær gera ráð fyrir stigveldum ívafinna eininga.</span><span class="sxs-lookup"><span data-stu-id="c9a91-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="c9a91-117">Gámaeiningar innihalda *hólf*.</span><span class="sxs-lookup"><span data-stu-id="c9a91-117">Container modules include *slots*.</span></span> <span data-ttu-id="c9a91-118">Hólf eru notuð til að takast á við skipulag og tilgang undireininga í gámnum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="c9a91-119">Dæmi um það er grunnsíðugámaeining (efsta stigs eining fyrir hverja síðu) sem skilgreinir nokkur mikilvæg hólf:</span><span class="sxs-lookup"><span data-stu-id="c9a91-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="c9a91-120">Fyrirsagnarhólf</span><span class="sxs-lookup"><span data-stu-id="c9a91-120">A header slot</span></span>
- <span data-ttu-id="c9a91-121">Undirfyrirsagnarhólf</span><span class="sxs-lookup"><span data-stu-id="c9a91-121">A sub-header slot</span></span>
- <span data-ttu-id="c9a91-122">Aðalhólf</span><span class="sxs-lookup"><span data-stu-id="c9a91-122">A main slot</span></span>
- <span data-ttu-id="c9a91-123">Síðufótarhólf</span><span class="sxs-lookup"><span data-stu-id="c9a91-123">A footer slot</span></span>
- <span data-ttu-id="c9a91-124">Undirsíðufótarhólf</span><span class="sxs-lookup"><span data-stu-id="c9a91-124">A sub-footer slot</span></span>

<span data-ttu-id="c9a91-125">Þróunaraðili einingarinnar skilgreinir þessi hólf og ákvarðar hvaða undireiningar og hversu margar undireiningar má setja beint í þau.</span><span class="sxs-lookup"><span data-stu-id="c9a91-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="c9a91-126">Til dæmis gæti fyrirsagnarhólfið aðeins stutt eina einingu af gerðinni **Fyrirsagnareining** en meginmálshólfið gæti stutt ótakmarkaðan fjölda eininga af hvaða gerð sem er (nema aðrar gámaeiningar á síðunni).</span><span class="sxs-lookup"><span data-stu-id="c9a91-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="c9a91-127">Í höfundatækjunum þurfa síðuhöfundar ekki að vita fyrirfram hvaða einingar er hægt og ekki hægt að setja í hvert hólf.</span><span class="sxs-lookup"><span data-stu-id="c9a91-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="c9a91-128">Þegar síðuhöfundar velja hólf og reyna síðan að velja einingu til að bæta við það sjá þeir síaða mynd af gerðum eininga sem eru studdar fyrir það hólf.</span><span class="sxs-lookup"><span data-stu-id="c9a91-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="c9a91-129">Innihaldseiningar</span><span class="sxs-lookup"><span data-stu-id="c9a91-129">Content modules</span></span>

<span data-ttu-id="c9a91-130">Innihaldseiningar innihalda efni og fjölmiðlaþætti, svo sem texta (til dæmis fyrirsagnir, málsgreinar og krækjur) eða tilvísanir í eignir (til dæmis myndir, myndskeið og PDF skjöl).</span><span class="sxs-lookup"><span data-stu-id="c9a91-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="c9a91-131">Dæmigerðar gerðir efniseininga innihalda efnisbálk, textabálk og einingar tilboðsborða.</span><span class="sxs-lookup"><span data-stu-id="c9a91-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="c9a91-132">Einingar af þessum þremur gerðum geta innihaldið texta eða miðla og þeir þurfa ekki neinar undireiningar til að gera eitthvað sýnilegt á síðu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="c9a91-133">Meirihluti dæmigerðra, daglegra síðu- og efnisskriftaaðgerða fela í sér efniseiningar, fyrst og fremst vegna þess að þessar einingar skilgreina raunverulegt innihald sem birt er í yfirgámaeiningum þeirra.</span><span class="sxs-lookup"><span data-stu-id="c9a91-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="c9a91-134">Margar efniseiningar eru í boði og þessar einingar eru venjulega síðustu verkin sem þú bætir við stigveldi síðunnar með ívöfðum einingum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="c9a91-135">Eftirfarandi mynd sýnir hvernig einingar eru ívafðar innan í einingahólfum yfirgáms.</span><span class="sxs-lookup"><span data-stu-id="c9a91-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Ívafðar einingar](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="c9a91-137">Bæta við eða fjarlægja einingar</span><span class="sxs-lookup"><span data-stu-id="c9a91-137">Add or remove modules</span></span>

<span data-ttu-id="c9a91-138">Eftirfarandi aðferðir lýsa því hvernig á að bæta við og fjarlægja einingar.</span><span class="sxs-lookup"><span data-stu-id="c9a91-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="c9a91-139">Bæta við einingu</span><span class="sxs-lookup"><span data-stu-id="c9a91-139">Add a module</span></span>

<span data-ttu-id="c9a91-140">Til að bæta einingu við hólf eða gám á síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-141">Á yfirlitssvæðinu vinstra megin eða beint á aðalvinnusvæðinu skal velja svæði eða hólf þar sem bæta á undireiningu við.</span><span class="sxs-lookup"><span data-stu-id="c9a91-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9a91-142">Einingahönnuðurinn skilgreinir listann yfir gerðir eininga sem hægt er að bæta við tiltekið hólf fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="c9a91-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="c9a91-143">Sniðmátshöfundar geta þá fínstillt leyfilega valkosti eininga til að hjálpa til við að tryggja stöðuga leitarvélabestun og skilvirkni höfundarverks fyrir allar síðurnar sem búnar til samkvæmt tilteknu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="c9a91-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="c9a91-144">Þegar einingu er bætt við hólf, er svarglugginn **Bæta við einingu** sjálfkrafa síaður þannig að hann sýni aðeins einingar sem eru studdar í völdu svæði eða hólfi.</span><span class="sxs-lookup"><span data-stu-id="c9a91-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="c9a91-145">Þessi listi yfir leyfðar einingar ákvarðast af sniðmáti síðunnar eða skilgreiningu svæðiseiningar.</span><span class="sxs-lookup"><span data-stu-id="c9a91-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="c9a91-146">Ef yfirlitssvæðið er notað skal velja úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="c9a91-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="c9a91-147">Ef stýringarnar eru notaðar beint innan vinnusvæðisins skal velja plúsmerkið (**+**) í auðu hólfi eða samliggjandi við valda einingu, og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="c9a91-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9a91-148">Ef gámur eða hólf styður ekki nýjar undireiningar er valkosturinn **Bæta við einingu** er ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="c9a91-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="c9a91-149">Í svarglugganum **Bæta við einingu** skal velja einingu til að bæta við síðuna þína.</span><span class="sxs-lookup"><span data-stu-id="c9a91-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="c9a91-150">**Efnisbálkur** er góð einingagerð fyrir byrjendur til að vinna með.</span><span class="sxs-lookup"><span data-stu-id="c9a91-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="c9a91-151">Veldu **Í lagi** til að bæta valinni einingu við valinn gám eða hólf á síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="c9a91-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="c9a91-152">Fjarlægja einingu</span><span class="sxs-lookup"><span data-stu-id="c9a91-152">Remove a module</span></span>

<span data-ttu-id="c9a91-153">Til að fjarlægja einingu úr hólfi eða gámi á síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-154">Á yfirlitssvæðinu vinstra megin skal velja úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar sem á að fjarlægja og síðan velja ruslakörfutáknið.</span><span class="sxs-lookup"><span data-stu-id="c9a91-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="c9a91-155">Einnig er hægt í aðalvinnusvæðinu að velja ruslakörfutáknið í tækjastiku valdrar einingar.</span><span class="sxs-lookup"><span data-stu-id="c9a91-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="c9a91-156">Þegar beðið er um að staðfesta að ætlunin sé að fjarlægja eininguna, skal velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c9a91-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="c9a91-157">Færa einingu á nýjan stað</span><span class="sxs-lookup"><span data-stu-id="c9a91-157">Move a module to a new position</span></span>

<span data-ttu-id="c9a91-158">Til að færa einingu yfir á nýjan stað innan síðunnar, skal nota eina af eftirfarandi aðferðum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="c9a91-159">Færa einingu með yfirlitssvæðinu</span><span class="sxs-lookup"><span data-stu-id="c9a91-159">Move a module using the outline pane</span></span>

<span data-ttu-id="c9a91-160">Til að færa einingu með yfirlitssvæðinu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-161">Veljið og haldið einingunni sem á að færa á yfirlitssvæðinu, dragið síðan eininguna yfir á nýja staðsetningu í yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="c9a91-162">Bláa línan í yfirlitinu og á vinnusvæðinu sýnir hvar hægt er að staðsetja eininguna.</span><span class="sxs-lookup"><span data-stu-id="c9a91-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="c9a91-163">Sleppið einingunni til að fella hana inn í nýja staðinn.</span><span class="sxs-lookup"><span data-stu-id="c9a91-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="c9a91-164">Færa einingu beint innan vinnusvæðisins</span><span class="sxs-lookup"><span data-stu-id="c9a91-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="c9a91-165">Til að færa einingu beint innan vinnusvæðisins skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-166">Veljið eininguna sem á að færa innan vinnusvæðisins.</span><span class="sxs-lookup"><span data-stu-id="c9a91-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="c9a91-167">Veljið annaðhvort örvatákn sem vísar upp eða niður í tækjastiku einingarinnar og dragið síðan örina yfir á nýjan stað á síðunni.</span><span class="sxs-lookup"><span data-stu-id="c9a91-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="c9a91-168">Bláa línan á vinnusvæðinu og í yfirlitinu sýnir hvar hægt er að staðsetja eininguna.</span><span class="sxs-lookup"><span data-stu-id="c9a91-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="c9a91-169">Ef ekki er hægt að færa einingu upp eða niður, verður örvartáknið skyggt.</span><span class="sxs-lookup"><span data-stu-id="c9a91-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="c9a91-170">Sleppið einingunni til að fella hana inn í nýja staðinn.</span><span class="sxs-lookup"><span data-stu-id="c9a91-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="c9a91-171">Færa einingu með úrfellingarvalmyndinni</span><span class="sxs-lookup"><span data-stu-id="c9a91-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="c9a91-172">Til að færa einingu með úrfellingarvalmyndinni skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-173">Veljið einingu í annaðhvort yfirlitinu eða vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="c9a91-174">Veljið úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar á yfirlitssvæðinu eða í tækjastiku einingarinnar á vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="c9a91-175">Ef hægt er að færa eininguna upp eða niður innan svæðis eða hólfs birtast valmöguleikar fyrir **Færa upp** eða **Færa niður**.</span><span class="sxs-lookup"><span data-stu-id="c9a91-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="c9a91-176">Veljið æskilegan færsluvalkost til að færa eininguna upp eða niður miðað við aðrar einingar.</span><span class="sxs-lookup"><span data-stu-id="c9a91-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="c9a91-177">Skilgreina einingar</span><span class="sxs-lookup"><span data-stu-id="c9a91-177">Configure modules</span></span>

<span data-ttu-id="c9a91-178">Eftirfarandi aðferðir lýsa því hvernig á að skilgreina efnis- og gámaeiningar.</span><span class="sxs-lookup"><span data-stu-id="c9a91-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="c9a91-179">Stilla innihaldseiningu</span><span class="sxs-lookup"><span data-stu-id="c9a91-179">Configure a content module</span></span>

<span data-ttu-id="c9a91-180">Fylgdu þessum skrefum til að stilla efniseiningu á síðu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-181">Á yfirlitssvæðinu vinstra megin skal útvíkka tréð og velja einhverja efniseiningu (til dæmis **Efnisbálkur**).</span><span class="sxs-lookup"><span data-stu-id="c9a91-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="c9a91-182">Einnig er hægt að velja eininguna á aðalvinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="c9a91-183">Á eiginleikasvæði einingarinnar hægra megin skal færa inn eiginleika fyrir eiginleikastýringar sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c9a91-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="c9a91-184">Á skipanastikunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c9a91-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="c9a91-185">Þetta mun einnig endurnýja forskoðunardúkinn.</span><span class="sxs-lookup"><span data-stu-id="c9a91-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="c9a91-186">Breyta textaeiginleikum einingar</span><span class="sxs-lookup"><span data-stu-id="c9a91-186">Edit module text properties</span></span>

<span data-ttu-id="c9a91-187">Textaeiginleikar einingar sem ekki eru skrifvarðar er hægt að breyta á vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="c9a91-188">Til að breyta textaeiginleikum einingar skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-189">Veljið textastýringuna á vinnusvæðinu og farið með bendilinn þangað sem á að breyta texta.</span><span class="sxs-lookup"><span data-stu-id="c9a91-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="c9a91-190">Sláið inn textann.</span><span class="sxs-lookup"><span data-stu-id="c9a91-190">Enter your text content.</span></span>
1. <span data-ttu-id="c9a91-191">Veljið hvar sem er fyrir utan textaefnið til að halda áfram að breyta öðru efni.</span><span class="sxs-lookup"><span data-stu-id="c9a91-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="c9a91-192">Innfellt val myndar</span><span class="sxs-lookup"><span data-stu-id="c9a91-192">Inline image selection</span></span>

<span data-ttu-id="c9a91-193">Myndaeiningar sem ekki eru skrifvarðar er hægt að breyta á vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="c9a91-194">Til að velja nýja mynd fyrir efniseiningu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-195">Á vinnusvæðinu skal tvísmella á myndina.</span><span class="sxs-lookup"><span data-stu-id="c9a91-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="c9a91-196">Þá kemur upp gluggi fyrir val á miðli.</span><span class="sxs-lookup"><span data-stu-id="c9a91-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="c9a91-197">Finnið og veljið nýja mynd sem á að nota og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c9a91-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="c9a91-198">Nýja myndin er nú sýnd á vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="c9a91-199">Stillla gámaeiningu</span><span class="sxs-lookup"><span data-stu-id="c9a91-199">Configure a container module</span></span>

<span data-ttu-id="c9a91-200">Fylgdu þessum skrefum til að stilla gámaeiningu á síðu.</span><span class="sxs-lookup"><span data-stu-id="c9a91-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="c9a91-201">Veldu gámaeiningu á síðunni (til dæmis hringekju- eða vökvagámaeiningu).</span><span class="sxs-lookup"><span data-stu-id="c9a91-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="c9a91-202">Í eiginleikaglugganum til hægri skaltu stækka ívafðar stýringarnar með því að velja hausana og stilla öll nauðsynleg stjórnunargildi.</span><span class="sxs-lookup"><span data-stu-id="c9a91-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="c9a91-203">Í útlínuglugganum til vinstri velurðu úrfellingarhnappinn við hliðina á heiti annaðhvort gámsins eða hólfa innan í gámnum og síðan velurðu **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="c9a91-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="c9a91-204">Bættu síðan undireiningum við valinn gám.</span><span class="sxs-lookup"><span data-stu-id="c9a91-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="c9a91-205">Fyrir frekari upplýsingar, sjá hlutann [Vinna með einingar](#add-a-module) fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="c9a91-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="c9a91-206">Ef margar undireiningar eru til sem systkini í yfirgámi geturðu breytt skjápöntun þeirra í yfirgámnum.</span><span class="sxs-lookup"><span data-stu-id="c9a91-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="c9a91-207">Veldu úrfellingarhnappinn fyrir eininguna og notaðu síðan upp örina og örvatakkana.</span><span class="sxs-lookup"><span data-stu-id="c9a91-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9a91-208">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c9a91-208">Additional resources</span></span>

[<span data-ttu-id="c9a91-209">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="c9a91-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="c9a91-210">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="c9a91-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="c9a91-211">Vinna með forstillt útlit</span><span class="sxs-lookup"><span data-stu-id="c9a91-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="c9a91-212">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="c9a91-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="c9a91-213">Bæta gámaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="c9a91-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="c9a91-214">Vinna með birtingarhópa</span><span class="sxs-lookup"><span data-stu-id="c9a91-214">Work with publish groups</span></span>](publish-groups.md)

