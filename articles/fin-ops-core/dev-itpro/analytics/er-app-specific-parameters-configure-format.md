---
title: Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila
description: Þetta efni útskýrir hvernig þú getur stillt ER-snið fyrir rafræna skýrslugerð til að nota færibreytur sem eru tilgreindar á lögaðila.
author: NickSelin
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 3802675b2fe0615f4c2ad682462a233c67f18f1a
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853494"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="6da27-103">Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila</span><span class="sxs-lookup"><span data-stu-id="6da27-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="6da27-104">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="6da27-104">Overview</span></span>

<span data-ttu-id="6da27-105">Í mörgum af sniðmátum rafrænnar skýrslugerðar (ER) sem þú verður að hanna verður þú að sía gögn með því að nota mengi gilda sem eru sértæk fyrir hverja lögaðila í þínu tilviki (til dæmis, sett af skattakóða til að sía skattaviðskipti).</span><span class="sxs-lookup"><span data-stu-id="6da27-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="6da27-106">Eins og er, þegar síun af þessu tagi er stillt á ER sniði, eru gildi sem eru háð lögaðilanum (til dæmis skattakóða) notuð í tjáningu á ER sniði til að tilgreina reglur um síun gagna.</span><span class="sxs-lookup"><span data-stu-id="6da27-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="6da27-107">Þess vegna er ER sniðið gert sértækt fyrir lögaðila og til að mynda nauðsynlegar skýrslur verður þú að stofna afleidd afrit af upprunalegu ER sniði fyrir hvern lögaðila þar sem þú þarft að keyra ER snið.</span><span class="sxs-lookup"><span data-stu-id="6da27-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="6da27-108">Breyta þarf hverju afleiddu sniði rafrænnar skýrslugerðar til fá gildi ákveðins lögaðila inn í það, endurreiknað í hvert sinn sem upprunaleg (grunn)útgáfan hefur verið uppfærð, flutt úr prófunarumhverfi og flutt inn í vinnsluumhverfi þegar nota þarf það í framleiðsluskyni og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="6da27-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment, and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="6da27-109">Því er vinna við þessa gerð af skilgreindri lausn rafrænnar skýrslugerðar flókin og tímafrek af ýmsum ástæðum:</span><span class="sxs-lookup"><span data-stu-id="6da27-109">Therefore, maintenance of this type of configured ER solution is complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="6da27-110">Því fleiri sem lögaðilar eru, því meira verður að viðhalda skilgreiningum á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6da27-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="6da27-111">Viðhald ER stillinga krefst þess að notendur fyrirtækja hafi ER þekkingu.</span><span class="sxs-lookup"><span data-stu-id="6da27-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="6da27-112">Sértækar færibreytur fyrir ER-aðgerðir láta rafmagnsnotendur stilla gagnasíun á ER sniði þannig að hún byggist á mengi óhlutbundinna reglna.</span><span class="sxs-lookup"><span data-stu-id="6da27-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="6da27-113">Hægt er að stilla þetta reglumengi til að nota gagnagjafana sem eru til á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6da27-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="6da27-114">Notendur fyrirtækja geta síðan tilgreint raunverulegar reglur umfram ER ramma með því að nota notendaviðmótið (UI) sem er sjálfkrafa myndað út frá stillingum á samsvarandi ER sniði og núverandi lögaðilagögnum sem gagnagjafar ER sniðsins munu hafa aðgang að.</span><span class="sxs-lookup"><span data-stu-id="6da27-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="6da27-115">Hægt er að flytja reglurnar sem eru tilgreindar fyrir ER snið úr núverandi lögaðila tilviksins Dynamics 365 Finance (Finance).</span><span class="sxs-lookup"><span data-stu-id="6da27-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="6da27-116">Það er síðan hægt að flytja það inn í annan lögaðila annaðhvort sama tilviks Finance eða annars tilviks sem reglumengi fyrir sama ER snið.</span><span class="sxs-lookup"><span data-stu-id="6da27-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6da27-117">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="6da27-117">Prerequisites</span></span>

<span data-ttu-id="6da27-118">Til að ljúka dæmum í þessu efni verður þú að hafa aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance and Operations, fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="6da27-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="6da27-119">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="6da27-119">Electronic reporting developer</span></span>
- <span data-ttu-id="6da27-120">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6da27-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="6da27-121">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="6da27-121">System administrator</span></span>

<span data-ttu-id="6da27-122">Við mælum með að þú klárir skrefin í efninu [Stuðningur við færibreytur kalla á ER-gagnaveitur af gerðinni REIKNAÐUR REITUR](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="6da27-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="6da27-123">Ef þú hefur þegar lokið þessum skrefum geturðu sleppt skrefunum í hlutanum **Flytja ER stillingar inn í RCS** sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="6da27-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="6da27-124">Flytja inn skilgreiningar inn í RCS</span><span class="sxs-lookup"><span data-stu-id="6da27-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="6da27-125">Einnig verður að sækja og geyma staðbundið eftirfarandi skilgreiningar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="6da27-125">Download and locally store the following ER configurations.</span></span>

| <span data-ttu-id="6da27-126">**Lýsing á efni**</span><span class="sxs-lookup"><span data-stu-id="6da27-126">**Content description**</span></span>                        | <span data-ttu-id="6da27-127">**Skrárnafn**</span><span class="sxs-lookup"><span data-stu-id="6da27-127">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6da27-128">Sýnishorn af skilgreiningarskránni **ER-gagnalíkan**</span><span class="sxs-lookup"><span data-stu-id="6da27-128">Sample **ER data model** configuration file</span></span>    | [<span data-ttu-id="6da27-129">Líkan til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="6da27-129">Model to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| <span data-ttu-id="6da27-130">Sýnishorn af skilgreiningarskrá **ER-lýsigagna**</span><span class="sxs-lookup"><span data-stu-id="6da27-130">Sample **ER metadata** configuration file</span></span>      | [<span data-ttu-id="6da27-131">Lýsigögn til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="6da27-131">Metadata to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| <span data-ttu-id="6da27-132">Sýnishorn af skilgreiningu **ER-líkanavörpunar**</span><span class="sxs-lookup"><span data-stu-id="6da27-132">Sample **ER model mapping** configuration file</span></span> | [<span data-ttu-id="6da27-133">Vörpun til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="6da27-133">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| <span data-ttu-id="6da27-134">Sýnishorn af skilgreiningu **ER-sniðmáts**</span><span class="sxs-lookup"><span data-stu-id="6da27-134">Sample **ER format** configuration</span></span>             | [<span data-ttu-id="6da27-135">Snimát til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="6da27-135">Format to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

<span data-ttu-id="6da27-136">Næst skráðirðu þig inn á RCS tilvikið.</span><span class="sxs-lookup"><span data-stu-id="6da27-136">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="6da27-137">Í þessu dæmi mun stofna skilgreiningu fyrir dæmi um sýnifyrirtæki, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6da27-137">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="6da27-138">Áður en hægt er að ljúka þessu ferli verður að ljúka skrefunum í efninu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md) í RCS.</span><span class="sxs-lookup"><span data-stu-id="6da27-138">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="6da27-139">Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="6da27-139">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="6da27-140">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="6da27-140">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="6da27-141">Flytja inn ER-skilgreiningar sem voru sóttar áður inn í RCS í eftirfarandi röð: gagnalíkan, lýsigögn, vörpun líkans og snið.</span><span class="sxs-lookup"><span data-stu-id="6da27-141">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="6da27-142">Fyrir hverja ER-skilgreiningu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="6da27-142">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="6da27-143">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-143">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="6da27-144">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="6da27-144">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="6da27-145">Veljið **Vafra** til að velja skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="6da27-145">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="6da27-146">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-146">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="6da27-147">Farðu yfir þá ER-lausn sem er veitt</span><span class="sxs-lookup"><span data-stu-id="6da27-147">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="6da27-148">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="6da27-148">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="6da27-149">Veldu liðinn **Snið til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="6da27-149">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="6da27-150">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6da27-150">Select **Designer**.</span></span>
4.  <span data-ttu-id="6da27-151">Veldu **Stækka/Minnka**.</span><span class="sxs-lookup"><span data-stu-id="6da27-151">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="6da27-152">ER-sniðmátið **Snið til að læra færibreytur á köll** er hannað til að búa til skattayfirlit á XML sniði sem sýnir nokkur stig skattheimtu (venjuleg, lækkuð og engin).</span><span class="sxs-lookup"><span data-stu-id="6da27-152">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="6da27-153">Hvert stig hefur mismunandi fjölda smáatriða.</span><span class="sxs-lookup"><span data-stu-id="6da27-153">Each level has a different number of details.</span></span>

    ![Mörg stig af sniði rafrænnar skýrslugerðar, snið til að læra færibreytusímtöl](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="6da27-155">Á flipanum **Vörpun** stækkarðu liðina **Líkan**, **Gögn** og **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="6da27-155">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="6da27-156">Gagnagjafinn **Model.Data.Summary** skilar lista yfir skattfærslur.</span><span class="sxs-lookup"><span data-stu-id="6da27-156">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="6da27-157">Þessar færslur eru teknar saman eftir skattkóðum.</span><span class="sxs-lookup"><span data-stu-id="6da27-157">These transactions are summarized by tax code.</span></span> <span data-ttu-id="6da27-158">Fyrir þessa gagnaheimild hefur reiknaði reiturinn **Model.Data.Summary.Level** verið stilltur til að skila kóðanum fyrir skattlagningarstig hverrar samandreginnar skráar.</span><span class="sxs-lookup"><span data-stu-id="6da27-158">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="6da27-159">Fyrir alla skattakóða sem hægt er að sækja úr gagnagjafanum **Model.Data.Summary** á keyrslutíma skilar reiknaði reiturinn skattlagningarstigskóðanum (**Regluleg**, **Lækkuð**, **Engin** eða **Annað**) sem textagildi.</span><span class="sxs-lookup"><span data-stu-id="6da27-159">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="6da27-160">Reiknaði reiturinn **Model.Data.Summary.Level** er notaður til að sía skrár úr gagnagjafanum **Model.Data.Summary** og slá inn síuð gögn í hvern XML-þátt sem táknar skattlagningarstig með því að nota reitina **Model.Data2.Level1**, **Model.Data2.Level2** og **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="6da27-160">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![Model.Data.Summary listi gagnaveitu skattfærsla](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="6da27-162">Reiknaði reiturinn **Model.Data.Summary.Level** hefur verið stilltur þannig að hann inniheldur ER-segð.</span><span class="sxs-lookup"><span data-stu-id="6da27-162">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="6da27-163">Skattkóðar (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** og **InVAT0**) eru harðkóðaðir í þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="6da27-163">Tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="6da27-164">Þess vegna er þetta ER snið háð lögaðilanum þar sem þessir skattakóðar voru stilltir.</span><span class="sxs-lookup"><span data-stu-id="6da27-164">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![Model.Data.Summary.Level útreiknaður reitur með harðkóðuðum skattkóðum](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="6da27-166">Til að styðja við annað sett af skatt kóða fyrir hvern lögaðila verður þú að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="6da27-166">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="6da27-167">Búðu til afleidda útgáfu af ER sniði fyrir hvern lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6da27-167">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="6da27-168">Uppfæra skattakóða í reiknaða reitinn **Model.Data.Summary.Level**, byggt á stillingu lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6da27-168">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="6da27-169">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6da27-169">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="6da27-170">Stofna afleitt sniðmát</span><span class="sxs-lookup"><span data-stu-id="6da27-170">Create a derived format</span></span>

<span data-ttu-id="6da27-171">Næst munt þú nota eiginleikann ER-forritasértækar færibreytur til að styðja við ólík sett af skattakóða fyrir hvern lögaðila á einu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6da27-171">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="6da27-172">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="6da27-172">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="6da27-173">Veldu liðinn **Snið til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="6da27-173">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="6da27-174">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6da27-174">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="6da27-175">Veldu valkostinn **Sæktu frá nafni: Snið til að læra breytur símtöl, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="6da27-175">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="6da27-176">Í reitnum **Heiti** slærðu inn **Sniðmát til að læra hvernig eigi að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="6da27-176">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="6da27-177">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6da27-177">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="6da27-178">Stilla afleitt snið</span><span class="sxs-lookup"><span data-stu-id="6da27-178">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="6da27-179">Bæta við tölusetningu sniðs</span><span class="sxs-lookup"><span data-stu-id="6da27-179">Add a format enumeration</span></span>

<span data-ttu-id="6da27-180">Næst bætirðu við nýrri upptalningu á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6da27-180">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="6da27-181">Gildi þessarar sniðupptalningar verða kynnt fyrir fyrirtækjanotendum sem munu tilgreina mengi lögaðilaháðra skattkóða fyrir hin ýmsu skattheimtustig sem notuð eru á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6da27-181">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="6da27-182">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6da27-182">Select **Designer**.</span></span>
2.  <span data-ttu-id="6da27-183">Veldu **Tölusetningar sniða**.</span><span class="sxs-lookup"><span data-stu-id="6da27-183">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="6da27-184">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6da27-184">Select **Add**.</span></span>
4.  <span data-ttu-id="6da27-185">Í reitinn **Heiti** slærðu inn **Listi yfir skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="6da27-185">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="6da27-186">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6da27-186">Select **Save**.</span></span>
6.  <span data-ttu-id="6da27-187">Á flipaum **Gildi tölusetningar sniðs** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6da27-187">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="6da27-188">Í reitinn **Heiti** slærðu inn **Regluleg skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="6da27-188">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="6da27-189">Veldu aftur **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6da27-189">Select **Add** again.</span></span>
9.  <span data-ttu-id="6da27-190">Í reitinn **Heiti** slærðu inn **Lækkuð skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="6da27-190">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="6da27-191">Veldu aftur **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6da27-191">Select **Add** again.</span></span>
11. <span data-ttu-id="6da27-192">Í reitinn **Heiti** slærðu inn **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="6da27-192">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="6da27-193">Veldu aftur **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6da27-193">Select **Add** again.</span></span>
13. <span data-ttu-id="6da27-194">Í reitinn **Heiti** skal færa inn **Annað**.</span><span class="sxs-lookup"><span data-stu-id="6da27-194">In the **Name** field, enter **Other**.</span></span>

    ![Ný færsla á síðunni tölusetningar sniðs](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="6da27-196">Vegna þess að notendur fyrirtækja gætu notað mismunandi tungumál til að tilgreina skattalög sem eru háð lögaðilum, mælum við með að þú þýðir gildi þessarar talningar yfir á tungumálin sem eru stillt sem ákjósanleg tungumál fyrir þá notendur í Finance.</span><span class="sxs-lookup"><span data-stu-id="6da27-196">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="6da27-197">Veldu skrána **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="6da27-197">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="6da27-198">Smelltu í reitinn **Merki**.</span><span class="sxs-lookup"><span data-stu-id="6da27-198">Click in the **Label** field.</span></span>
16. <span data-ttu-id="6da27-199">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="6da27-199">Select **Translate**.</span></span>
17. <span data-ttu-id="6da27-200">Á **Textaþýðing** svæðinu í **Kenni merkis** reitinn skal slá inn **LBL_LEVELENUM_NO**.</span><span class="sxs-lookup"><span data-stu-id="6da27-200">In the **Text translation** pane, in the **Label ID** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="6da27-201">Í reitnum **Texti á sjálfgefnu tungumáli** slærðu inn **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="6da27-201">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="6da27-202">Í reitnum **Tungumál** velurðu **DE**.</span><span class="sxs-lookup"><span data-stu-id="6da27-202">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="6da27-203">Í reitinn **Þýddur texti** skal færa inn **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="6da27-203">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="6da27-204">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="6da27-204">Select **Translate**.</span></span>

    ![Textaþýðingar renna út](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="6da27-206">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6da27-206">Select **Save**.</span></span>
23. <span data-ttu-id="6da27-207">Lokaðu síðunni **Tölusetningar sniða**.</span><span class="sxs-lookup"><span data-stu-id="6da27-207">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="6da27-208">Bættu við nýjum gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="6da27-208">Add a new lookup data source</span></span>

<span data-ttu-id="6da27-209">Næst bætirðu við nýjum gagnagjafa til að tilgreina hvernig notendur fyrirtækja munu tilgreina reglur sem eru háðar lögaðilum til að viðurkenna rétt skattlagningarstig fyrir hvert yfirlit yfir færsluskrá.</span><span class="sxs-lookup"><span data-stu-id="6da27-209">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="6da27-210">Á flipanum **Vörpun** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6da27-210">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="6da27-211">Veldu **Format enumeration\Lookup**.</span><span class="sxs-lookup"><span data-stu-id="6da27-211">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="6da27-212">Þú varst að auðkenna að hver regla sem notendur fyrirtækja tilgreina fyrir viðurkenningu á skattaþrepum muni skila gildi upptalningar á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6da27-212">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="6da27-213">Taktu eftir að gagnagjafagerðina **Uppflettingu** er hægt að nálgast undir blokkunum **Gagnalíkan** og **Dynamics 365 for Operations** til viðbótar við blokkina **Tölusetning sniðs**.</span><span class="sxs-lookup"><span data-stu-id="6da27-213">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="6da27-214">Því er hægt að nota tölusetningar fyrir gagnalíkan rafrænnar skýrslugerðar og tölusetningar forrits til að tilgreina gerð gilda sem skilað er fyrir gagnagjafa af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="6da27-214">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that are returned for data sources of that type.</span></span> <span data-ttu-id="6da27-215">Frekari upplýsingar um gagnagjafana **Uppfletting** er að finna í [Skilgreina gagnagjafa uppflettingar til að nota eiginleika fyrir færibreytur forrits í rafrænni skýrslugerð](er-lookup-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="6da27-215">To learn more about the **Lookup** data sources, see [Configure Lookup data sources to use the ER application-specific parameters feature](er-lookup-data-sources.md).</span></span>
    
3.  <span data-ttu-id="6da27-216">Í reitinn **Heiti** skal færa inn **Val**.</span><span class="sxs-lookup"><span data-stu-id="6da27-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="6da27-217">Í reitinn **Tölusetning sniðs** velurðu **Listi yfir skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="6da27-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="6da27-218">Þú tilgreindir að fyrir hverja reglu sem er tilgreind í þessum gagnagjafa þurfi að velja eitt af gildunum í tölusetningarsniðinu **Listi yfir skattstig** sem skiluðu gildi.</span><span class="sxs-lookup"><span data-stu-id="6da27-218">You specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="6da27-219">Veldu **Breyta leit**.</span><span class="sxs-lookup"><span data-stu-id="6da27-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="6da27-220">Velja **Dálka**.</span><span class="sxs-lookup"><span data-stu-id="6da27-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="6da27-221">Stækkaðu liðinn **Model**.</span><span class="sxs-lookup"><span data-stu-id="6da27-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="6da27-222">Stækkaðu liðinn **Gögn**.</span><span class="sxs-lookup"><span data-stu-id="6da27-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="6da27-223">Stækkaðu liðinn **Skattur**.</span><span class="sxs-lookup"><span data-stu-id="6da27-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="6da27-224">Veldu liðinn **Model.Data.Tax.Code**.</span><span class="sxs-lookup"><span data-stu-id="6da27-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="6da27-225">Veldu hnappinn **Bæta við** (hægri örin).</span><span class="sxs-lookup"><span data-stu-id="6da27-225">Select the **Add** button (the right arrow).</span></span>

    ![Dálkar renna út](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="6da27-227">Þú varst að tilgreina að fyrir hverja reglu sem er tilgreind í þessum gagnagjafa fyrir viðurkenningu á skattaþrepum, verður viðskiptanotandi að velja einn af skattakóðunum sem skilyrði.</span><span class="sxs-lookup"><span data-stu-id="6da27-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="6da27-228">Listinn yfir skattakóða sem viðskiptanotandinn getur valið verður skilað af gagnagjafanum **Model.Data.Tax**.</span><span class="sxs-lookup"><span data-stu-id="6da27-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="6da27-229">Vegna þess að þessi gagnaheimild inniheldur reitinn **Heiti** verður heiti skattakóðans sýnt fyrir hvert skattakóðagildi í uppflettingu sem er kynnt viðskiptanotanda.</span><span class="sxs-lookup"><span data-stu-id="6da27-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="6da27-230">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-230">Select **OK**.</span></span>

    ![Hönnunarsíða leitar](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="6da27-232">Notendur fyrirtækja geta bætt við mörgum reglum sem skrám yfir þessa gagnaheimild.</span><span class="sxs-lookup"><span data-stu-id="6da27-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="6da27-233">Hver skrá verður tölusett með línukóða.</span><span class="sxs-lookup"><span data-stu-id="6da27-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="6da27-234">Reglur verða metnar til að auka línufjölda.</span><span class="sxs-lookup"><span data-stu-id="6da27-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="6da27-235">Vegna þess að þú valdir reitinn **Skattakóði** sem skilyrði fyrir reglum í þessum gagnagjafa uppflettingar og þar sem **Skattakóði** er settur upp sem reitur af gagnagerðinni **Strengur** verður hver regla metin á keyrslutíma með því að bera saman skattakóðann sem er sendur til gagnagjafans með skattakóðanum sem er skilgreindur í þessari skrá gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6da27-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="6da27-236">Þegar regla sem fullnægir skilgreindum skilyrðum finnst skilar þessi gagnagjafi uppflettisgildi reglunnar sem er skilgreind í reitnum **Niðurstaða uppflettingar**.</span><span class="sxs-lookup"><span data-stu-id="6da27-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="6da27-237">Ef engin regla finnst er undantekningu hent inn til að tilkynna notandanum að núverandi gagnagjafi geti ekki skilað réttu gildi.</span><span class="sxs-lookup"><span data-stu-id="6da27-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="6da27-238">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6da27-238">Select **Save**.</span></span>
14. <span data-ttu-id="6da27-239">Lokaðu síðunni **Uppflettihönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6da27-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="6da27-240">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-240">Select **OK**.</span></span>

    <span data-ttu-id="6da27-241">Taktu eftir að þú bætir við nýjum gagnagjafa sem skilar skattstigi sem gildi sniðatölusetningarinnar **Listi yfir skattastig** fyrir alla skattakóða sem er sendur til gagnaheimildarinnar sem frumgildi fyrir færibreytuna **Kóði** af gagnagerðinni **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="6da27-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![Sniðshönnuðarsíða með nýrri gagnaveitu](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="6da27-243">Mat á skilgreindum reglum fer eftir gagnagerð reitanna sem hafa verið valdir til að skilgreina skilyrði þessara reglna.</span><span class="sxs-lookup"><span data-stu-id="6da27-243">The evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="6da27-244">Þegar þú velur reit sem er stilltur sem reitur af annaðhvort gagnagerðinni **Tölulegt** eða **Dagsetning** munu viðmiðin verða frábrugðin viðmiðunum sem lýst var áðan fyrir gagnagerðina **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="6da27-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="6da27-245">Fyrir reitina **Tölulegt** og **Dagsetning** verður að tilgreina regluna sem gildissvið.</span><span class="sxs-lookup"><span data-stu-id="6da27-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="6da27-246">Skilyrði reglunnar verður síðan talið fullnægt þegar gildi sem er sent til gagnagjafans er á skilgreindu sviðinu.</span><span class="sxs-lookup"><span data-stu-id="6da27-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="6da27-247">Eftirfarandi skýringarmynd sýnir dæmi um þessa gerð uppsetningar.</span><span class="sxs-lookup"><span data-stu-id="6da27-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="6da27-248">Í viðbót við reitinn **Model.Data.Tax.Code** í gagnagerðinni **Strengur** er reiturinn **Model.Tax.Summary.Base** í gagnagerðinni **Rauntími** notaður til að tilgreina skilyrði fyrir uppflettingu gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6da27-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![Hönnunarsíða leitar með viðbótardálkum](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="6da27-250">Þar sem reitirnir **Model.Data.Tax.Code** og **Model.Tax.Summary.Base** eru valdir fyrir þennan uppflettingargagnagjafa verður sérhver regla þessa gagnagjafa stillt á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="6da27-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="6da27-251">Í listanum sem er kynntur verður að velja gildi sniðatölusetningar **Listi yfir skattastil** sem skilað gildi.</span><span class="sxs-lookup"><span data-stu-id="6da27-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="6da27-252">Færa verður inn skattakóðann sem skilyrði þessarar reglu.</span><span class="sxs-lookup"><span data-stu-id="6da27-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="6da27-253">Aðeins skattakóðar sem veittir eru af gagnagjafanum **Model.Data.Tax** eiga við.</span><span class="sxs-lookup"><span data-stu-id="6da27-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="6da27-254">Færa skal lágmarks- og hámarksgildi skattstofnupphæðar sem skilyrði þessarar reglu.</span><span class="sxs-lookup"><span data-stu-id="6da27-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="6da27-255">Svona verður sérhver regla þessa gagnagjafa metin á keyrslutíma:</span><span class="sxs-lookup"><span data-stu-id="6da27-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="6da27-256">Er kóðinn í gagnagerðinni **Strengur** sem var send í þennan gagnagjafa jafnt og skattakóði reglu?</span><span class="sxs-lookup"><span data-stu-id="6da27-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="6da27-257">Fellur gildi gagnagerðarinnar **Rauntími** sem var send í þennan gagnagjafa á milli tiltekinna lágmarks- og hámarksgilda?</span><span class="sxs-lookup"><span data-stu-id="6da27-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="6da27-258">Regla verður talin eiga við þegar bæði skilyrðin eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="6da27-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="6da27-259">Þýddu merkimiða uppflettigagnagjafans sem bætt var við</span><span class="sxs-lookup"><span data-stu-id="6da27-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="6da27-260">Þar sem að fyrirtækjanotendur gætu notað mismunandi tungumál til að tilgreina lögaðilaháð mengi skattakóða mælum við með að þú þýðir merkimiða gagnagjafa uppflettinga sem þú bætir við svo að hann sé birtur á æskilegu tungumáli hvers notanda á samsvarandi síðu.</span><span class="sxs-lookup"><span data-stu-id="6da27-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="6da27-261">Veldu gagnagjafann **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="6da27-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="6da27-262">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6da27-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="6da27-263">Smelltu í reitinn **Merki**.</span><span class="sxs-lookup"><span data-stu-id="6da27-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="6da27-264">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="6da27-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="6da27-265">Á **Textaþýðing** svæðinu í **Kenni merkis** reitinn skal slá inn **LBL_SELECTOR_DS**.</span><span class="sxs-lookup"><span data-stu-id="6da27-265">In the **Text translation** pane, in the **Label ID** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="6da27-266">Í reitinn **Texti á sjálfgefnu tungumáli** slærðu inn **Velja skattastig eftir skattakóða**.</span><span class="sxs-lookup"><span data-stu-id="6da27-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="6da27-267">Í reitnum **Tungumál** velurðu **DE**.</span><span class="sxs-lookup"><span data-stu-id="6da27-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="6da27-268">Í reitinn **Þýddur texti** slærðu inn **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="6da27-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="6da27-269">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="6da27-269">Select **Translate**.</span></span>
10. <span data-ttu-id="6da27-270">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-270">Select **OK**.</span></span>

    ![Eiginleiki gagnagjafa, renna út](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="6da27-272">Bættu við nýjum reit til að nota stillta uppflettingu</span><span class="sxs-lookup"><span data-stu-id="6da27-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="6da27-273">Stækkaðu liðinn **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="6da27-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="6da27-274">Veldu liðinn **Model.Data.Summary**.</span><span class="sxs-lookup"><span data-stu-id="6da27-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="6da27-275">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6da27-275">Select **Add**.</span></span>
4.  <span data-ttu-id="6da27-276">Veldu **Aðgerðir/Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="6da27-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="6da27-277">Í reitinn **Heiti** slærðu inn **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="6da27-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="6da27-278">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="6da27-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="6da27-279">Í reitinn **Formúla** slærðu inn **Model.Selector (Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="6da27-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="6da27-280">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6da27-280">Select **Save**.</span></span>

    ![Adding Model.Selector(Model.Data.Summary.Code) á síðu Formúluhönnuðarins](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="6da27-282">Lokið síðunni **Formúluritill**.</span><span class="sxs-lookup"><span data-stu-id="6da27-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="6da27-283">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-283">Select **OK**.</span></span>

    ![Sniðshönnuður með nýrri viðbættri formúlu](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="6da27-285">Athugaðu að reiknaði reiturinn **LevelByLookup** sem þú bættir við mun skila skattastiginu sem gildi sniðaupptalningarinnar **Listi yfir skattastig** fyrir hverja samantekna skrá skattafærslna.</span><span class="sxs-lookup"><span data-stu-id="6da27-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="6da27-286">Skattakóði skrárinnar verður sendur til uppflettigagnagjafans **Model.Selector** og reglurnar fyrir þennan gagnagjafa verða notaðar til að velja rétt skattlagningarstig.</span><span class="sxs-lookup"><span data-stu-id="6da27-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="6da27-287">Bætið við nýjum sniðatölusetningarbundnum gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="6da27-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="6da27-288">Næst bætirðu við nýjum gagnagjafa sem vísar til sniðatölusetningarinnar þú bættir við fyrr.</span><span class="sxs-lookup"><span data-stu-id="6da27-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="6da27-289">Gildi þessa gagnagjafa verða seinna notuð í segð á ER-sniði.</span><span class="sxs-lookup"><span data-stu-id="6da27-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="6da27-290">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="6da27-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="6da27-291">Veldu **Format enumeration\Enumeration**.</span><span class="sxs-lookup"><span data-stu-id="6da27-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="6da27-292">Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="6da27-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="6da27-293">Í reitinn **Tölusetning sniðs** velurðu **Listi yfir skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="6da27-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="6da27-294">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6da27-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="6da27-295">Breyttu núverandi reit til að nota leitina</span><span class="sxs-lookup"><span data-stu-id="6da27-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="6da27-296">Næst verður þú að breyta fyrirliggjandi reiknuðum reit þannig að hann notar skilgreindan uppflettingargagnagjafann til að skila réttu skattlagningargildi, allt eftir skattakóðanum.</span><span class="sxs-lookup"><span data-stu-id="6da27-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="6da27-297">Veldu liðinn **Model.Data.Summary.Level**.</span><span class="sxs-lookup"><span data-stu-id="6da27-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="6da27-298">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6da27-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="6da27-299">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="6da27-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="6da27-300">Taktu eftir að núverandi tjáning reitarins **Model.Data.Summary.Level** inniheldur eftirfarandi harðkóðaða skattakóða:</span><span class="sxs-lookup"><span data-stu-id="6da27-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="6da27-301">MÁL (@. Kóðinn, "VSK19", "Venjulegur", "InVAT19", "Venjulegur", "VSK7", "Minni", "InVAT7", "Minni", "ÞRIÐJA", "Enginn", "InVAT0", „Enginn“, „Annað“)</span><span class="sxs-lookup"><span data-stu-id="6da27-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="6da27-302">Í ritinn **Formúla** slærðu inn **CASE(@.LevelByLookup, TaxationLevel. 'Regular taxation', 'Regular', TaxationLevel.'Reduated taxation ',' Reduced ', TaxationLevel.'No taxation', 'None', 'Other')**.</span><span class="sxs-lookup"><span data-stu-id="6da27-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![Síða ER-aðgerðahönnuður](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="6da27-304">Takið eftir að segð reitsins **Model.Data.Summary.Level** mun nú skila skattlagningarstiginu út frá skattkóða gildandi færslu og reglusafni sem viðskiptanotandi skilgreinir í uppflettingargagnagjafa **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="6da27-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="6da27-305">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6da27-305">Select **Save**.</span></span>
6.  <span data-ttu-id="6da27-306">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6da27-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="6da27-307">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-307">Select **OK**.</span></span>
8.  <span data-ttu-id="6da27-308">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6da27-308">Select **Save**.</span></span>
9.  <span data-ttu-id="6da27-309">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6da27-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="6da27-310">Ljúktu uppkastsútgáfu af afleiddu sniði</span><span class="sxs-lookup"><span data-stu-id="6da27-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="6da27-311">Á flýtiflipanum **Útgáfur** skal velja **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="6da27-311">On the **Versions** FastTab, select **Change status**.</span></span>
2.  <span data-ttu-id="6da27-312">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="6da27-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="6da27-313">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="6da27-314">Flyttu út fullkláraða útgáfu af breyttu sniði</span><span class="sxs-lookup"><span data-stu-id="6da27-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="6da27-315">Í skilgreiningatrénu skal velja atriðið **Snið til að læra hvernig á að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="6da27-315">In the configuration tree, select the **Format to learn how to look up LE data** item.</span></span>
2.  <span data-ttu-id="6da27-316">Í flýtiflipanum **Útgáfur** skal velja færsluna sem er með stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="6da27-316">On the **Versions** FastTab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="6da27-317">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="6da27-318">Veldu **Flytja út sem XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="6da27-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="6da27-319">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6da27-319">Select **OK**.</span></span>
6.  <span data-ttu-id="6da27-320">Vafrinn sækir skrána **Snið til að læra hvernig á að fletta upp LE data.xml**.</span><span class="sxs-lookup"><span data-stu-id="6da27-320">The web browser downloads a **Format to learn how to look up LE data.xml** file.</span></span> <span data-ttu-id="6da27-321">Geymið þessa skrá á staðnum.</span><span class="sxs-lookup"><span data-stu-id="6da27-321">Store this file locally.</span></span>

<span data-ttu-id="6da27-322">Endurtakið skrefin í þessum hluta fyrir yfirvörur á sniðinu **Snið til að læra hvernig á að fletta upp LE-gögnum** og geymið eftirfarandi skrár staðbundið:</span><span class="sxs-lookup"><span data-stu-id="6da27-322">Repeat steps in this section for parent items of the **Format to learn how to look up LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="6da27-323">Sniðmát til að læra færibreytur á köll.xml</span><span class="sxs-lookup"><span data-stu-id="6da27-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="6da27-324">Veldu Vörpun til að læra færibreytur á köll.xml</span><span class="sxs-lookup"><span data-stu-id="6da27-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="6da27-325">Líkan til að læra færibreytur á köll.xml</span><span class="sxs-lookup"><span data-stu-id="6da27-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="6da27-326">Til að læra hvernig á að nota skilgreinda rafræna skýrslugerðarsniðið **Snið til að læra hvernig á að fletta upp LE-gögnum** til að setja upp sett af skattkóðum sem tengjast lögaðila til að sía skattfærslur eftir mismunandi skattlagningarstigum, skal ljúka skrefunum í efnisatriðinu [Setja upp færibreytur rafræns skýrslugerðarsniðs fyrir hvern lögaðila](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="6da27-326">To learn how to use the configured **Format to learn how to look up LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6da27-327">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6da27-327">Additional resources</span></span>

[<span data-ttu-id="6da27-328">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="6da27-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="6da27-329">Setja upp færibreytur á sniði rafrænnar skýrslugerðar fyrir hvern lögaðila</span><span class="sxs-lookup"><span data-stu-id="6da27-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)

[<span data-ttu-id="6da27-330">Skilgreina gagnaveitu uppflettingar til að nota eiginleikann fyrir færibreytur sem eru sértækar fyrir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="6da27-330">Configure Lookup data sources to use the ER application-specific parameters feature</span></span>](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
