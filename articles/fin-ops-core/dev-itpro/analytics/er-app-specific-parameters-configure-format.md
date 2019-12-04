---
title: Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila
description: Þetta efni útskýrir hvernig þú getur stillt ER-snið fyrir rafræna skýrslugerð til að nota færibreytur sem eru tilgreindar á lögaðila.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: d32da76ee46ff5293ae8fefb16d251564b6be21a
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694247"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="4cbbd-103">Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila</span><span class="sxs-lookup"><span data-stu-id="4cbbd-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="4cbbd-104">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4cbbd-104">Overview</span></span>

<span data-ttu-id="4cbbd-105">Í mörgum af sniðmátum rafrænnar skýrslugerðar (ER) sem þú verður að hanna verður þú að sía gögn með því að nota mengi gilda sem eru sértæk fyrir hverja lögaðila í þínu tilviki (til dæmis, sett af skattakóða til að sía skattaviðskipti).</span><span class="sxs-lookup"><span data-stu-id="4cbbd-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="4cbbd-106">Eins og er, þegar síun af þessu tagi er stillt á ER sniði, eru gildi sem eru háð lögaðilanum (til dæmis skattakóða) notuð í tjáningu á ER sniði til að tilgreina reglur um síun gagna.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="4cbbd-107">Þess vegna er ER sniðið gert sértækt fyrir lögaðila og til að mynda nauðsynlegar skýrslur verður þú að stofna afleidd afrit af upprunalegu ER sniði fyrir hvern lögaðila þar sem þú þarft að keyra ER snið.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="4cbbd-108">Breyta verður hverju afleiddu ER sniði til að koma sérstökum gildum lögaðila inn í það, endurreikna í hvert skipti sem upphaflega (grunn-) útgáfan er uppfærð, flytja úr prufuumhverfi og flytja inn í framleiðsluumhverfi þegar það verður sent til framleiðslu og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="4cbbd-109">Þess vegna er viðhald þessarar gerðar á skilgreindri ER-lausn nokkuð flókið og tímafrekt af ýmsum ástæðum:</span><span class="sxs-lookup"><span data-stu-id="4cbbd-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="4cbbd-110">Því fleiri sem lögaðilar eru, því meira verður að viðhalda skilgreiningum á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="4cbbd-111">Viðhald ER stillinga krefst þess að notendur fyrirtækja hafi ER þekkingu.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="4cbbd-112">Sértækar færibreytur fyrir ER-aðgerðir láta rafmagnsnotendur stilla gagnasíun á ER sniði þannig að hún byggist á mengi óhlutbundinna reglna.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="4cbbd-113">Hægt er að stilla þetta reglumengi til að nota gagnagjafana sem eru til á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="4cbbd-114">Notendur fyrirtækja geta síðan tilgreint raunverulegar reglur umfram ER ramma með því að nota notendaviðmótið (UI) sem er sjálfkrafa myndað út frá stillingum á samsvarandi ER sniði og núverandi lögaðilagögnum sem gagnagjafar ER sniðsins munu hafa aðgang að.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="4cbbd-115">Hægt er að flytja reglurnar sem eru tilgreindar fyrir ER snið úr núverandi lögaðila tilviksins Dynamics 365 Finance (Finance).</span><span class="sxs-lookup"><span data-stu-id="4cbbd-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="4cbbd-116">Það er síðan hægt að flytja það inn í annan lögaðila annaðhvort sama tilviks Finance eða annars tilviks sem reglumengi fyrir sama ER snið.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4cbbd-117">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="4cbbd-117">Prerequisites</span></span>

<span data-ttu-id="4cbbd-118">Til að ljúka dæmum í þessu efni verður þú að hafa aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance and Operations, fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="4cbbd-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="4cbbd-119">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="4cbbd-119">Electronic reporting developer</span></span>
- <span data-ttu-id="4cbbd-120">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="4cbbd-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="4cbbd-121">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="4cbbd-121">System administrator</span></span>

<span data-ttu-id="4cbbd-122">Við mælum með að þú klárir skrefin í efninu [Stuðningur við færibreytur kalla á ER-gagnaveitur af gerðinni REIKNAÐUR REITUR](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="4cbbd-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="4cbbd-123">Ef þú hefur þegar lokið þessum skrefum geturðu sleppt skrefunum í hlutanum **Flytja ER stillingar inn í RCS** sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="4cbbd-124">Flytja inn skilgreiningar inn í RCS</span><span class="sxs-lookup"><span data-stu-id="4cbbd-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="4cbbd-125">Úr [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448) sækirðu þjappaða skrána **Stuðningur við færibreytur kallar á ER gagnagjafa af gerðinni REIKNAÐUR REITUR**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="4cbbd-126">Þessi þjappaða skrá inniheldur eftirfarandi ER-skilgreiningar sem verður að draga út og geyma á staðnum.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="4cbbd-127">**Lýsing á efni**</span><span class="sxs-lookup"><span data-stu-id="4cbbd-127">**Content description**</span></span>                        | <span data-ttu-id="4cbbd-128">**Skrárnafn**</span><span class="sxs-lookup"><span data-stu-id="4cbbd-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4cbbd-129">Sýnishorn af skilgreiningarskránni **ER-gagnalíkan**</span><span class="sxs-lookup"><span data-stu-id="4cbbd-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="4cbbd-130">Líkan til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="4cbbd-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="4cbbd-131">Sýnishorn af skilgreiningarskrá **ER-lýsigagna**</span><span class="sxs-lookup"><span data-stu-id="4cbbd-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="4cbbd-132">Lýsigögn til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="4cbbd-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="4cbbd-133">Sýnishorn af skilgreiningu **ER-líkanavörpunar**</span><span class="sxs-lookup"><span data-stu-id="4cbbd-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="4cbbd-134">Vörpun til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="4cbbd-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="4cbbd-135">Sýnishorn af skilgreiningu **ER-sniðmáts**</span><span class="sxs-lookup"><span data-stu-id="4cbbd-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="4cbbd-136">Snimát til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="4cbbd-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="4cbbd-137">Næst skráðirðu þig inn á RCS tilvikið.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="4cbbd-138">Í þessu dæmi mun stofna skilgreiningu fyrir dæmi um sýnifyrirtæki, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="4cbbd-139">Áður en hægt er að ljúka þessu ferli verður að ljúka skrefunum í efninu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md) í RCS.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="4cbbd-140">Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="4cbbd-141">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="4cbbd-142">Flytja inn ER-skilgreiningar sem voru sóttar áður inn í RCS í eftirfarandi röð: gagnalíkan, lýsigögn, vörpun líkans og snið.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="4cbbd-143">Fyrir hverja ER-skilgreiningu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="4cbbd-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="4cbbd-144">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="4cbbd-145">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="4cbbd-146">Veljið **Vafra** til að velja skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="4cbbd-147">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="4cbbd-148">Farðu yfir þá ER-lausn sem er veitt</span><span class="sxs-lookup"><span data-stu-id="4cbbd-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="4cbbd-149">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="4cbbd-150">Veldu liðinn **Snið til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="4cbbd-151">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="4cbbd-152">Veldu **Stækka/Minnka**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="4cbbd-153">ER-sniðmátið **Snið til að læra færibreytur á köll** er hannað til að búa til skattayfirlit á XML sniði sem sýnir nokkur stig skattheimtu (venjuleg, lækkuð og engin).</span><span class="sxs-lookup"><span data-stu-id="4cbbd-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="4cbbd-154">Hvert stig hefur mismunandi fjölda smáatriða.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-154">Each level has a different number of details.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="4cbbd-156">Á flipanum **Vörpun** stækkarðu liðina **Líkan**, **Gögn** og **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="4cbbd-157">Gagnagjafinn **Model.Data.Summary** skilar lista yfir skattfærslur.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="4cbbd-158">Þessar færslur eru teknar saman eftir skattkóðum.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="4cbbd-159">Fyrir þessa gagnaheimild hefur reiknaði reiturinn **Model.Data.Summary.Level** verið stilltur til að skila kóðanum fyrir skattlagningarstig hverrar samandreginnar skráar.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="4cbbd-160">Fyrir alla skattakóða sem hægt er að sækja úr gagnagjafanum **Model.Data.Summary** á keyrslutíma skilar reiknaði reiturinn skattlagningarstigskóðanum (**Regluleg**, **Lækkuð**, **Engin** eða **Annað**) sem textagildi.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="4cbbd-161">Reiknaði reiturinn **Model.Data.Summary.Level** er notaður til að sía skrár úr gagnagjafanum **Model.Data.Summary** og slá inn síuð gögn í hvern XML-þátt sem táknar skattlagningarstig með því að nota reitina **Model.Data2.Level1**, **Model.Data2.Level2** og **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="4cbbd-163">Reiknaði reiturinn **Model.Data.Summary.Level** hefur verið stilltur þannig að hann inniheldur ER-segð.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="4cbbd-164">Athugaðu að skattakóðar (**VSK19**, **InVAT19**, **VSK7**, **InVAT7**, **THIRD** og **InVAT0**) eru harðkóðaðar í þessa stillingu.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="4cbbd-165">Þess vegna er þetta ER snið háð lögaðilanum þar sem þessir skattakóðar voru stilltir.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="4cbbd-167">Til að styðja við annað sett af skatt kóða fyrir hvern lögaðila verður þú að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="4cbbd-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="4cbbd-168">Búðu til afleidda útgáfu af ER sniði fyrir hvern lögaðila.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="4cbbd-169">Uppfæra skattakóða í reiknaða reitinn **Model.Data.Summary.Level**, byggt á stillingu lögaðila.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="4cbbd-170">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="4cbbd-171">Stofna afleitt sniðmát</span><span class="sxs-lookup"><span data-stu-id="4cbbd-171">Create a derived format</span></span>

<span data-ttu-id="4cbbd-172">Næst munt þú nota eiginleikann ER-forritasértækar færibreytur til að styðja við ólík sett af skattakóða fyrir hvern lögaðila á einu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="4cbbd-173">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="4cbbd-174">Veldu liðinn **Snið til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="4cbbd-175">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="4cbbd-176">Veldu valkostinn **Sæktu frá nafni: Snið til að læra breytur símtöl, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="4cbbd-177">Í reitnum **Heiti** slærðu inn **Sniðmát til að læra hvernig eigi að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="4cbbd-178">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="4cbbd-179">Stilla afleitt snið</span><span class="sxs-lookup"><span data-stu-id="4cbbd-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="4cbbd-180">Bæta við tölusetningu sniðs</span><span class="sxs-lookup"><span data-stu-id="4cbbd-180">Add a format enumeration</span></span>

<span data-ttu-id="4cbbd-181">Næst bætirðu við nýrri upptalningu á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="4cbbd-182">Gildi þessarar sniðupptalningar verða kynnt fyrir fyrirtækjanotendum sem munu tilgreina mengi lögaðilaháðra skattkóða fyrir hin ýmsu skattheimtustig sem notuð eru á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="4cbbd-183">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="4cbbd-184">Veldu **Tölusetningar sniða**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="4cbbd-185">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-185">Select **Add**.</span></span>
4.  <span data-ttu-id="4cbbd-186">Í reitinn **Heiti** slærðu inn **Listi yfir skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="4cbbd-187">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-187">Select **Save**.</span></span>
6.  <span data-ttu-id="4cbbd-188">Á flipaum **Gildi tölusetningar sniðs** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="4cbbd-189">Í reitinn **Heiti** slærðu inn **Regluleg skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="4cbbd-190">Veldu aftur **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="4cbbd-191">Í reitinn **Heiti** slærðu inn **Lækkuð skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="4cbbd-192">Veldu aftur **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-192">Select **Add** again.</span></span>
11. <span data-ttu-id="4cbbd-193">Í reitinn **Heiti** slærðu inn **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="4cbbd-194">Veldu aftur **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-194">Select **Add** again.</span></span>
13. <span data-ttu-id="4cbbd-195">Í reitinn **Heiti** skal færa inn **Annað**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-195">In the **Name** field, enter **Other**.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="4cbbd-197">Vegna þess að notendur fyrirtækja gætu notað mismunandi tungumál til að tilgreina skattalög sem eru háð lögaðilum, mælum við með að þú þýðir gildi þessarar talningar yfir á tungumálin sem eru stillt sem ákjósanleg tungumál fyrir þá notendur í Finance.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="4cbbd-198">Veldu skrána **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="4cbbd-199">Smelltu í reitinn **Merki**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="4cbbd-200">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-200">Select **Translate**.</span></span>
17. <span data-ttu-id="4cbbd-201">Í glugganum **Textaþýðing** í reitnum **Merkimiði** skaltu slá inn **LBL_LEVELENUM_NO**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="4cbbd-202">Í reitnum **Texti á sjálfgefnu tungumáli** slærðu inn **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="4cbbd-203">Í reitnum **Tungumál** velurðu **DE**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="4cbbd-204">Í reitinn **Þýddur texti** skal færa inn **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="4cbbd-205">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-205">Select **Translate**.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="4cbbd-207">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-207">Select **Save**.</span></span>
23. <span data-ttu-id="4cbbd-208">Lokaðu síðunni **Tölusetningar sniða**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="4cbbd-209">Bættu við nýjum gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="4cbbd-209">Add a new lookup data source</span></span>

<span data-ttu-id="4cbbd-210">Næst bætirðu við nýjum gagnagjafa til að tilgreina hvernig notendur fyrirtækja munu tilgreina reglur sem eru háðar lögaðilum til að viðurkenna rétt skattlagningarstig fyrir hvert yfirlit yfir færsluskrá.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="4cbbd-211">Á flipanum **Vörpun** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="4cbbd-212">Veldu **Format enumeration\Lookup**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="4cbbd-213">Þú varst að auðkenna að hver regla sem notendur fyrirtækja tilgreina fyrir viðurkenningu á skattaþrepum muni skila gildi upptalningar á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="4cbbd-214">Taktu eftir að gagnagjafagerðina **Uppflettingu** er hægt að nálgast undir blokkunum **Gagnalíkan** og **Dynamics 365 for Operations** til viðbótar við blokkina **Tölusetning sniðs**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="4cbbd-215">Þess vegna er hægt að nota ER-gagnalíkanatölusetningu og forritatölusetningu til að tilgreina gerð gilda sem er skilað fyrir gagnagjafa af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="4cbbd-216">Í reitinn **Heiti** skal færa inn **Val**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="4cbbd-217">Í reitinn **Tölusetning sniðs** velurðu **Listi yfir skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="4cbbd-218">Þú varst að tilgreina að fyrir hverja reglu sem er tilgreind í þessum gagnagjafa, verður viðskiptanotandi að velja eitt af gildum sniðatölusetningarinnar **Listi yfir skattlagningarstig** sem skilað gildi.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="4cbbd-219">Veldu **Breyta leit**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="4cbbd-220">Velja **Dálka**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="4cbbd-221">Stækkaðu liðinn **Model**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="4cbbd-222">Stækkaðu liðinn **Gögn**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="4cbbd-223">Stækkaðu liðinn **Skattur**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="4cbbd-224">Veldu liðinn **Model.Data.Tax.Code**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="4cbbd-225">Veldu hnappinn **Bæta við** (hægri örin).</span><span class="sxs-lookup"><span data-stu-id="4cbbd-225">Select the **Add** button (the right arrow).</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="4cbbd-227">Þú varst að tilgreina að fyrir hverja reglu sem er tilgreind í þessum gagnagjafa fyrir viðurkenningu á skattaþrepum, verður viðskiptanotandi að velja einn af skattakóðunum sem skilyrði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="4cbbd-228">Listinn yfir skattakóða sem viðskiptanotandinn getur valið verður skilað af gagnagjafanum **Model.Data.Tax**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="4cbbd-229">Vegna þess að þessi gagnaheimild inniheldur reitinn **Heiti** verður heiti skattakóðans sýnt fyrir hvert skattakóðagildi í uppflettingu sem er kynnt viðskiptanotanda.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="4cbbd-230">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-230">Select **OK**.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="4cbbd-232">Notendur fyrirtækja geta bætt við mörgum reglum sem skrám yfir þessa gagnaheimild.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="4cbbd-233">Hver skrá verður tölusett með línukóða.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="4cbbd-234">Reglur verða metnar til að auka línufjölda.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="4cbbd-235">Vegna þess að þú valdir reitinn **Skattakóði** sem skilyrði fyrir reglum í þessum gagnagjafa uppflettingar og þar sem **Skattakóði** er settur upp sem reitur af gagnagerðinni **Strengur** verður hver regla metin á keyrslutíma með því að bera saman skattakóðann sem er sendur til gagnagjafans með skattakóðanum sem er skilgreindur í þessari skrá gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="4cbbd-236">Þegar regla sem fullnægir skilgreindum skilyrðum finnst skilar þessi gagnagjafi uppflettisgildi reglunnar sem er skilgreind í reitnum **Niðurstaða uppflettingar**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="4cbbd-237">Ef engin regla finnst er undantekningu hent inn til að tilkynna notandanum að núverandi gagnagjafi geti ekki skilað réttu gildi.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="4cbbd-238">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-238">Select **Save**.</span></span>
14. <span data-ttu-id="4cbbd-239">Lokaðu síðunni **Uppflettihönnuður**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="4cbbd-240">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-240">Select **OK**.</span></span>

    <span data-ttu-id="4cbbd-241">Taktu eftir að þú bætir við nýjum gagnagjafa sem skilar skattstigi sem gildi sniðatölusetningarinnar **Listi yfir skattastig** fyrir alla skattakóða sem er sendur til gagnaheimildarinnar sem frumgildi fyrir færibreytuna **Kóði** af gagnagerðinni **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="4cbbd-243">Athugaðu að mat á stilltum reglum veltur á gagnagerð reitanna sem hafa verið valdir til að skilgreina skilyrði þessara reglna.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="4cbbd-244">Þegar þú velur reit sem er stilltur sem reitur af annaðhvort gagnagerðinni **Tölulegt** eða **Dagsetning** munu viðmiðin verða frábrugðin viðmiðunum sem lýst var áðan fyrir gagnagerðina **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="4cbbd-245">Fyrir reitina **Tölulegt** og **Dagsetning** verður að tilgreina regluna sem gildissvið.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="4cbbd-246">Skilyrði reglunnar verður síðan talið fullnægt þegar gildi sem er sent til gagnagjafans er á skilgreindu sviðinu.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="4cbbd-247">Eftirfarandi skýringarmynd sýnir dæmi um þessa gerð uppsetningar.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="4cbbd-248">Í viðbót við reitinn **Model.Data.Tax.Code** í gagnagerðinni **Strengur** er reiturinn **Model.Tax.Summary.Base** í gagnagerðinni **Rauntími** notaður til að tilgreina skilyrði fyrir uppflettingu gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="4cbbd-250">Þar sem reitirnir **Model.Data.Tax.Code** og **Model.Tax.Summary.Base** eru valdir fyrir þennan uppflettingargagnagjafa verður sérhver regla þessa gagnagjafa stillt á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="4cbbd-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="4cbbd-251">Í listanum sem er kynntur verður að velja gildi sniðatölusetningar **Listi yfir skattastil** sem skilað gildi.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="4cbbd-252">Færa verður inn skattakóðann sem skilyrði þessarar reglu.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="4cbbd-253">Aðeins skattakóðar sem veittir eru af gagnagjafanum **Model.Data.Tax** eiga við.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="4cbbd-254">Færa skal lágmarks- og hámarksgildi skattstofnupphæðar sem skilyrði þessarar reglu.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="4cbbd-255">Svona verður sérhver regla þessa gagnagjafa metin á keyrslutíma:</span><span class="sxs-lookup"><span data-stu-id="4cbbd-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="4cbbd-256">Er kóðinn í gagnagerðinni **Strengur** sem var send í þennan gagnagjafa jafnt og skattakóði reglu?</span><span class="sxs-lookup"><span data-stu-id="4cbbd-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="4cbbd-257">Fellur gildi gagnagerðarinnar **Rauntími** sem var send í þennan gagnagjafa á milli tiltekinna lágmarks- og hámarksgilda?</span><span class="sxs-lookup"><span data-stu-id="4cbbd-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="4cbbd-258">Regla verður talin eiga við þegar bæði skilyrðin eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="4cbbd-259">Þýddu merkimiða uppflettigagnagjafans sem bætt var við</span><span class="sxs-lookup"><span data-stu-id="4cbbd-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="4cbbd-260">Þar sem að fyrirtækjanotendur gætu notað mismunandi tungumál til að tilgreina lögaðilaháð mengi skattakóða mælum við með að þú þýðir merkimiða gagnagjafa uppflettinga sem þú bætir við svo að hann sé birtur á æskilegu tungumáli hvers notanda á samsvarandi síðu.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="4cbbd-261">Veldu gagnagjafann **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="4cbbd-262">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="4cbbd-263">Smelltu í reitinn **Merki**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="4cbbd-264">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="4cbbd-265">Í glugganum **Textaþýðing** í reitnum **Merkimiði** skaltu slá inn **LBL_SELECTOR_DS**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="4cbbd-266">Í reitinn **Texti á sjálfgefnu tungumáli** slærðu inn **Velja skattastig eftir skattakóða**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="4cbbd-267">Í reitnum **Tungumál** velurðu **DE**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="4cbbd-268">Í reitinn **Þýddur texti** slærðu inn **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="4cbbd-269">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-269">Select **Translate**.</span></span>
10. <span data-ttu-id="4cbbd-270">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-270">Select **OK**.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="4cbbd-272">Bættu við nýjum reit til að nota stillta uppflettingu</span><span class="sxs-lookup"><span data-stu-id="4cbbd-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="4cbbd-273">Stækkaðu liðinn **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="4cbbd-274">Veldu liðinn **Model.Data.Summary**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="4cbbd-275">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-275">Select **Add**.</span></span>
4.  <span data-ttu-id="4cbbd-276">Veldu **Aðgerðir/Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="4cbbd-277">Í reitinn **Heiti** slærðu inn **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="4cbbd-278">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="4cbbd-279">Í reitinn **Formúla** slærðu inn **Model.Selector (Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="4cbbd-280">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-280">Select **Save**.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="4cbbd-282">Lokið síðunni **Formúluritill**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="4cbbd-283">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-283">Select **OK**.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="4cbbd-285">Athugaðu að reiknaði reiturinn **LevelByLookup** sem þú bættir við mun skila skattastiginu sem gildi sniðaupptalningarinnar **Listi yfir skattastig** fyrir hverja samantekna skrá skattafærslna.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="4cbbd-286">Skattakóði skrárinnar verður sendur til uppflettigagnagjafans **Model.Selector** og reglurnar fyrir þennan gagnagjafa verða notaðar til að velja rétt skattlagningarstig.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="4cbbd-287">Bætið við nýjum sniðatölusetningarbundnum gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="4cbbd-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="4cbbd-288">Næst bætirðu við nýjum gagnagjafa sem vísar til sniðatölusetningarinnar þú bættir við fyrr.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="4cbbd-289">Gildi þessa gagnagjafa verða seinna notuð í segð á ER-sniði.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="4cbbd-290">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="4cbbd-291">Veldu **Format enumeration\Enumeration**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="4cbbd-292">Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="4cbbd-293">Í reitinn **Tölusetning sniðs** velurðu **Listi yfir skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="4cbbd-294">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="4cbbd-295">Breyttu núverandi reit til að nota leitina</span><span class="sxs-lookup"><span data-stu-id="4cbbd-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="4cbbd-296">Næst verður þú að breyta fyrirliggjandi reiknuðum reit þannig að hann notar skilgreindan uppflettingargagnagjafann til að skila réttu skattlagningargildi, allt eftir skattakóðanum.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="4cbbd-297">Veldu liðinn **Model.Data.Summary.Level**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="4cbbd-298">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="4cbbd-299">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="4cbbd-300">Taktu eftir að núverandi tjáning reitarins **Model.Data.Summary.Level** inniheldur eftirfarandi harðkóðaða skattakóða:</span><span class="sxs-lookup"><span data-stu-id="4cbbd-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="4cbbd-301">MÁL (@. Kóðinn, "VSK19", "Venjulegur", "InVAT19", "Venjulegur", "VSK7", "Minni", "InVAT7", "Minni", "ÞRIÐJA", "Enginn", "InVAT0", „Enginn“, „Annað“)</span><span class="sxs-lookup"><span data-stu-id="4cbbd-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="4cbbd-302">Í ritinn **Formúla** slærðu inn **CASE(@.LevelByLookup, TaxationLevel. 'Regular taxation', 'Regular', TaxationLevel.'Reduated taxation ',' Reduced ', TaxationLevel.'No taxation', 'None', 'Other')**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="4cbbd-304">Taktu eftir að tjáning reitarins **Model.Data.Summary.Level** mun nú skila skattastiginu, byggt á skattakóða núverandi færslu og sett reglna sem viðskiptanotandi stillir í uppflettigagnagjafa **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="4cbbd-305">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-305">Select **Save**.</span></span>
6.  <span data-ttu-id="4cbbd-306">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="4cbbd-307">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-307">Select **OK**.</span></span>
8.  <span data-ttu-id="4cbbd-308">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-308">Select **Save**.</span></span>
9.  <span data-ttu-id="4cbbd-309">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="4cbbd-310">Ljúktu uppkastsútgáfu af afleiddu sniði</span><span class="sxs-lookup"><span data-stu-id="4cbbd-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="4cbbd-311">Á flýtflipanum **Útgáfur** velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="4cbbd-312">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="4cbbd-313">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="4cbbd-314">Flyttu út fullkláraða útgáfu af breyttu sniði</span><span class="sxs-lookup"><span data-stu-id="4cbbd-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="4cbbd-315">Í stillingatrénu sniðmátið velurðu liðinn **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="4cbbd-316">Á flýtiflipanum **Útgáfur** velurðu skrána sem hefur stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="4cbbd-317">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="4cbbd-318">Veldu **Flytja út sem XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="4cbbd-319">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-319">Select **OK**.</span></span>
6.  <span data-ttu-id="4cbbd-320">Vafrinn halar niður skjalinu **Snið til að læra að fletta upp LE-gögnum.xml**.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="4cbbd-321">Geymið þessa skrá á staðnum.</span><span class="sxs-lookup"><span data-stu-id="4cbbd-321">Store this file locally.</span></span>

<span data-ttu-id="4cbbd-322">Endurtaktu skrefin í þessum hluta fyrir yfirliði sniðsins **Snið til að læra hvernig á að fletta upp LE-gögnum** og geyma eftirfarandi skrár á staðnum:</span><span class="sxs-lookup"><span data-stu-id="4cbbd-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="4cbbd-323">Sniðmát til að læra færibreytur á köll.xml</span><span class="sxs-lookup"><span data-stu-id="4cbbd-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="4cbbd-324">Veldu Vörpun til að læra færibreytur á köll.xml</span><span class="sxs-lookup"><span data-stu-id="4cbbd-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="4cbbd-325">Líkan til að læra færibreytur á köll.xml</span><span class="sxs-lookup"><span data-stu-id="4cbbd-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="4cbbd-326">Til að læra að nota skilgreint ER-snið **Snið til að læra hvernig á að fletta upp LE-gögnum** til að setja upp lögaðila sem eru háðir skattakóðum til að sía skattaviðskipti eftir mismunandi skattastigi, ljúktu við skrefin í efninu [Settu upp færibreytur ER sniðs á hvern lögaðila](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="4cbbd-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4cbbd-327">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4cbbd-327">Additional resources</span></span>

[<span data-ttu-id="4cbbd-328">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="4cbbd-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4cbbd-329">Settu upp færibreytur ER sniðs á hvern lögaðila</span><span class="sxs-lookup"><span data-stu-id="4cbbd-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
