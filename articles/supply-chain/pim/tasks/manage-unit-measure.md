---
title: Stjórna mælieiningum
description: Þetta efnisatriði lýsir því hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921342"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="3dcfb-103">Stjórna mælieiningum</span><span class="sxs-lookup"><span data-stu-id="3dcfb-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3dcfb-104">Þetta efnisatriði lýsir því hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="3dcfb-105">Opna síðuna Einingar</span><span class="sxs-lookup"><span data-stu-id="3dcfb-105">Open the Units page</span></span>

<span data-ttu-id="3dcfb-106">Til að búa til og vinna með mælieiningar sem eru í boði í kerfinu skal fara í **Fyrirtækisstjórnun \> Uppsetning \> Einingar \> Einingar**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="3dcfb-107">Eftirfarandi hlutar þessa efnis lýsa hvað hægt er að gera á síðunni **Einingar**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="3dcfb-108">Búa til staðaleiningar og umreikninga</span><span class="sxs-lookup"><span data-stu-id="3dcfb-108">Create standard units and conversions</span></span>

<span data-ttu-id="3dcfb-109">Ef kerfið þitt inniheldur ekki nú þegar algengustu mælieiningar metrakerfisins og/eða bandaríska einingakerfisins (USCS) getur leiðsagnarforrit einingauppsetningar auðveldað þér að hefjast strax handa með grunnskilgreiningar og umreikninga á einingum.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="3dcfb-110">Til að ljúka leiðsögninni skal velja **Leiðsagnarforrit við stofnun einingar** á aðgerðasvæðinu og síðan fylgja leiðbeiningunum á skjánum.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="3dcfb-111">Stofna eða breyta mælieiningu</span><span class="sxs-lookup"><span data-stu-id="3dcfb-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="3dcfb-112">Til að búa til eða breyta mælieiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="3dcfb-113">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="3dcfb-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="3dcfb-114">Til að breyta fyrirliggjandi einingu skal velja hana í listasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="3dcfb-115">Til að stofna nýja einingu er valið **Ný** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="3dcfb-116">Í haus færslunnar skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="3dcfb-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="3dcfb-117">**Eining** – Sláið inn kennið eða tákni til að nota til að vísa í eininguna á kerfistungumálinu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="3dcfb-118">Þetta auðkenni eða tákn er venjulega algeng skammstöfun fyrir eininguna, svo sem *ea* fyrir hvert stykki eða *cm* fyrir sentimetra.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="3dcfb-119">**Lýsing** – Færið inn lýsandi nafn fyrir eininguna á kerfistungumálinu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="3dcfb-120">Þetta heiti er yfirleitt fullt heiti einingarinnar, t.d. *Hvert* eða *Sentimetri*.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="3dcfb-121">Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="3dcfb-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="3dcfb-122">**Mælieiningarflokkur** – Veldu eignina sem einingin mælir (t.d. lengd, svæði, þyngd eða magn).</span><span class="sxs-lookup"><span data-stu-id="3dcfb-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="3dcfb-123">**Einingakerfi** – Veljið mælieiningakerfið sem einingin tilheyrir (*Einingar í metrakerfi* eða *Einingar í bandaríska einingakerfinu*).</span><span class="sxs-lookup"><span data-stu-id="3dcfb-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="3dcfb-124">**Grunneining** – Stillið þennan valkost á *Já* til að nota núverandi einingu sem grunneiningu fyrir einingarflokk hennar.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="3dcfb-125">Í þessu tilfelli þarf aðeins að tilgreina umreiknistuðulinn milli grunneiningarinnar og hverrar viðbótareiningar í einingaflokknum.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="3dcfb-126">Kerfið getur síðan breytt á milli allra eininga í þeim einingaflokki.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="3dcfb-127">Því er auðveldara að setja upp umreikning.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="3dcfb-128">Til dæmis, ef gallon er grunneining fyrir einingaklasann *Rúmmál* þarf aðeins að setja upp umreiknistuðul frá lítra yfir í gallon og frá hálfpotti yfir í gallon.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="3dcfb-129">Kerfið getur þá einnig umreiknað frá lítra yfir í hálfpott.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="3dcfb-130">Aðeins er hægt að hafa eina grunneiningu í hverjum einingarflokki.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="3dcfb-131">**Kerfiseining** – Stillið þennan valkost á *Já* til að nota núverandi einingu sem væntanlega einingu fyrir allar óskilgreindar mælingar í mælieiningaflokki hennar.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="3dcfb-132">Ef til dæmis reitur sem er notaður til að færa inn magn leyfir ekki að tilgreina einingu (eða ef notandinn velur ekk einingu), notar kerfið eininguna sem er stillt sem eining kerfisins fyrir mælieiningaflokkinn *Magn*.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="3dcfb-133">Aðeins er hægt að hafa eina kerfiseiningu í hverjum einingarflokki.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="3dcfb-134">**Nákvæmni aukastafa** – Tilgreinið fjölda aukastafa sem námunda á gildi sem eru tilgreind fyrir núverandi einingu eða umbreytt í hana.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="3dcfb-135">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="3dcfb-136">Skilgreina þýðingar eininga</span><span class="sxs-lookup"><span data-stu-id="3dcfb-136">Define unit translations</span></span>

<span data-ttu-id="3dcfb-137">Til að skilgreina þýðingar fyrir auðkenni eða tákn og lýsingu fyrir mælieiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="3dcfb-138">Búa til eða velja eininguna sem á að búa til þýðingar fyrir.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="3dcfb-139">Veljið **Einingatextar** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="3dcfb-140">Síðan **Einingatextar** birtist.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="3dcfb-141">Þú notar þessa síðu til að skilgreina þýðingar fyrir kennin eða táknið fyrir valda einingu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="3dcfb-142">Þessar þýðingar er síðan hægt að nota í ytri skjölum á tungumálum tengdum viðskiptavini eða lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="3dcfb-143">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3dcfb-144">Í svæðinu **Tungumál** skal velja tungumál sem þýða á einingakenni eða tákn á yfir á.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="3dcfb-145">Í reitinn **Texti** skal færa inn þýðingu á kenni eða tákni einingarinnar á völdu tungumáli.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="3dcfb-146">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3dcfb-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-147">Close the page.</span></span>
1. <span data-ttu-id="3dcfb-148">Veljið **Aðgerðasvæðinu** skal velja **Þýddar lýsingar á einingum**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="3dcfb-149">**Þýddar lýsingar á einingum** birtast.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="3dcfb-150">Þessi síða er notuð til að skilgreina tungumálasértækar lýsingar fyrir völdu eininguna.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="3dcfb-151">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3dcfb-152">Í reitnum **Tungumál** velurðu tungumálið sem á að þýða einingarlýsinguna yfir á.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="3dcfb-153">Í reitinn **Lýsing** er færð inn þýðing á einingarlýsingunni á völdu tungumáli.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="3dcfb-154">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3dcfb-155">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="3dcfb-156">Skilgreina umreikningsreglur eininga</span><span class="sxs-lookup"><span data-stu-id="3dcfb-156">Define unit conversion rules</span></span>

<span data-ttu-id="3dcfb-157">Til að skilgreina reglur fyrir umbreytingar milli mælieininga skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="3dcfb-158">Búa til eða velja eininguna sem á að skilgreina umreikningsreglur fyrir.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="3dcfb-159">Veljið **Umreikningur eininga** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="3dcfb-160">Síðan **Umreikningur eininga** birtist.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="3dcfb-161">Þú notar þessa síðu til að skilgreina reglur til að breyta völdu einingunni í og frá öðrum einingum í einingaflokknum.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="3dcfb-162">Veljið einn af eftirfarandi flipum eftir því hvaða gerð umreiknings á að setja upp:</span><span class="sxs-lookup"><span data-stu-id="3dcfb-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="3dcfb-163">**Staðlaðir umreikningar** – Setja upp staðlaðar umreikningsreglur fyrir allar afurðir.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="3dcfb-164">**Umreikningar innan flokks** – Setja upp afurðabundnar umreikningsreglur fyrir einingar í sama einingaflokki.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="3dcfb-165">**Umreikningar á milli flokka** – Setja upp afurðabundnar umreikningsreglur fyrir einingar á milli einingaflokka.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="3dcfb-166">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="3dcfb-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="3dcfb-167">Til að stofna nýja umbreytingu skal velja **Ný** á tækjastiku.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="3dcfb-168">Til að breyta núverandi umbreytingu skal velja umbreytinguna í netinu og síðan **Breyta** á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="3dcfb-169">Í svarglugganum sem birtist, skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="3dcfb-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="3dcfb-170">**Vara** – Veljið vöruna sem umreikningurin á við um.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="3dcfb-171">Þessi reitur er aðeins í boði fyrir umreikninga innan flokks og milli flokka.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="3dcfb-172">**Útlit formúlu** – Skiljið þennan reit stilltan á *Einfalt* til að tilgreina einfaldan umreikning sem er með einn stuðul.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="3dcfb-173">Stillið hana á *Ítarlegt* til að setja upp flóknari jöfnu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="3dcfb-174">Snið fyrir ítarlegar jöfnur er breytilegt eftir einingarflokknum.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="3dcfb-175">**Frá einingu** – Í þessum reit birtist valin eining.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="3dcfb-176">Yfirleitt ætti ekki að breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-176">Usually, you should not change the value.</span></span> <span data-ttu-id="3dcfb-177">(Ef gildinu er breytt verður að opna síðuna **Umreikningur eininga** fyrir valda einingu til að skoða nýju breytinguna eftir að hún hefur verið vistuð.)</span><span class="sxs-lookup"><span data-stu-id="3dcfb-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="3dcfb-178">**Til einingar** – Velja skal eininguna sem á að umreikna í.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="3dcfb-179">**Sléttun** – Veljið hvernig á að slétta brot út frá gildinu í **Nákvæmni aukastafa** af valdri einingu (*Til næsta*, *Upp* eða *Niður*).</span><span class="sxs-lookup"><span data-stu-id="3dcfb-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="3dcfb-180">**Umbreytingarformúla** – Notið eftirstandandi reiti efst í felliglugganum til að tilgreina formúluna fyrir umreikning milli tveggja eininga.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="3dcfb-181">Reitirnir sem eru tiltækir eru breytilegir eftir því hvaða einingaflokkur og formúluuppsetning var valin.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="3dcfb-182">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-182">Select **OK**.</span></span>
1. <span data-ttu-id="3dcfb-183">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="3dcfb-184">Einnig er hægt að setja upp einingarumreikning fyrir hvert vöruafbrigði.</span><span class="sxs-lookup"><span data-stu-id="3dcfb-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="3dcfb-185">Frekari upplýsingar eru í [Umreikningur mælieiningar eftir afurðarafbrigði](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="3dcfb-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
