---
title: Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað
description: Þetta efni veitir upplýsingar um hvernig skal nota reitagerðina Reiknað fyrir ER-gagnagjafa.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 02d53f4326d8f31abf6ec7404575728837954bef
ms.sourcegitcommit: c9baf9a3b4552f0317b5ec87d252834f52df1b98
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665611"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="5805d-103">Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað</span><span class="sxs-lookup"><span data-stu-id="5805d-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5805d-104">Þetta efni útskýrir hvernig þú getur hannað gagnagjafa rafrænnar skýrslugerðar (ER) með því að nota gerðina **Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="5805d-105">Þessi gagnagjafi getur innihaldið ER-segð sem, þegar hún er keyrð, er hægt að stjórna með gildum færibreytufrumbreytanna sem eru skilgreind í bindingu sem kallar þennan gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="5805d-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="5805d-106">Með því að skilgreina köll í færibreytur af slíkum gagnagjöfum er hægt að endurnýta staka gagnagjafa í mörgum bindingum, sem dregur úr heildarfjölda gagnagjafa sem verður að skilgreina í ER-líkanavörpunum eða ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="5805d-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="5805d-107">Það einfaldar einnig skilgreinda ER-íhluti, sem dregur úr viðhaldskostnaði og notkunarkostnaði annarra neytenda.</span><span class="sxs-lookup"><span data-stu-id="5805d-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5805d-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="5805d-108">Prerequisites</span></span>
<span data-ttu-id="5805d-109">Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:</span><span class="sxs-lookup"><span data-stu-id="5805d-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="5805d-110">Aðgangur að einu af þessum hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="5805d-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="5805d-111">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="5805d-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="5805d-112">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5805d-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5805d-113">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="5805d-113">System administrator</span></span>

- <span data-ttu-id="5805d-114">Aðgangur að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutaður fyrir sama leigjandann sem Finance and Operations fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="5805d-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="5805d-115">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="5805d-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="5805d-116">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5805d-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5805d-117">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="5805d-117">System administrator</span></span>

<span data-ttu-id="5805d-118">Einnig verður að sækja og geyma staðbundið eftirfarandi skrár.</span><span class="sxs-lookup"><span data-stu-id="5805d-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="5805d-119">**Efni**</span><span class="sxs-lookup"><span data-stu-id="5805d-119">**Content**</span></span>                           | <span data-ttu-id="5805d-120">**Skrárnafn**</span><span class="sxs-lookup"><span data-stu-id="5805d-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5805d-121">Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5805d-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="5805d-122">Líkan til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="5805d-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="5805d-123">Sýnishorn af skilgreiningu lýsigagna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5805d-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="5805d-124">Lýsigögn til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="5805d-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="5805d-125">Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5805d-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="5805d-126">Vörpun til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="5805d-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="5805d-127">Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5805d-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="5805d-128">Snimát til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="5805d-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="5805d-129">Skráðu þig inn á RCS tilvikið</span><span class="sxs-lookup"><span data-stu-id="5805d-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="5805d-130">Í þessu dæmi mun notandi stofna skilgreiningu fyrir sýnifyrirtækið Litware, Inc. Í RCS verður fyrst að ljúka skrefum ferlisins [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="5805d-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="5805d-131">Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="5805d-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="5805d-132">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="5805d-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="5805d-133">Flytja inn sóttar skilgreiningar í RCS í eftirfarandi röð: gagnalíkan, lýsigögn, vörpun líkans, snið.</span><span class="sxs-lookup"><span data-stu-id="5805d-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="5805d-134">Ljúktu eftirfarandi skrefum fyrir hverja ER-skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="5805d-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="5805d-135">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="5805d-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5805d-136">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="5805d-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5805d-137">Veldu **Vafra** og veldu síðan nauðsynlega ER-skilgreiningu á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="5805d-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="5805d-138">Veljið **Í lagi.**</span><span class="sxs-lookup"><span data-stu-id="5805d-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="5805d-139">Farðu yfir fyrirliggjandi ER-lausn</span><span class="sxs-lookup"><span data-stu-id="5805d-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="5805d-140">Farðu yfir vörpun líkans</span><span class="sxs-lookup"><span data-stu-id="5805d-140">Review model mapping</span></span>

1. <span data-ttu-id="5805d-141">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="5805d-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5805d-142">Veldu **Vörpun til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="5805d-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5805d-143">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5805d-143">Select **Designer**.</span></span>
4. <span data-ttu-id="5805d-144">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5805d-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="5805d-145">Þessi ER-líkanavörpun er hönnuð til að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="5805d-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="5805d-146">Sæktu lista yfir skattakóða (gagnagjafinn **Skattur**) sem er að finna í töflunni **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="5805d-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="5805d-147">Sæktu lista yfir skattafærslur (gagnagjafinn **Trans**) sem er að finna í töflunni **TaxTable**:</span><span class="sxs-lookup"><span data-stu-id="5805d-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="5805d-148">Flokka lista yfir sóttar færslur (gagnagjafinn **Gr**) eftir skattakóða.</span><span class="sxs-lookup"><span data-stu-id="5805d-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="5805d-149">Reiknaðu fyrir flokkaðar færslur eftirfarandi uppsöfnuð gildi á hvern skattakóða:</span><span class="sxs-lookup"><span data-stu-id="5805d-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="5805d-150">Summa skattstofnsgilda.</span><span class="sxs-lookup"><span data-stu-id="5805d-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="5805d-151">Summa skattgilda.</span><span class="sxs-lookup"><span data-stu-id="5805d-151">Sum of tax values.</span></span>
            - <span data-ttu-id="5805d-152">Lágmarksgildi beitts skatthlutfalls.</span><span class="sxs-lookup"><span data-stu-id="5805d-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="5805d-153">Líkanavörpun í þessari skilgreiningu innleiðir grunngagnalíkanið fyrir eitthvert snið rafrænnar skýrslugerðar sem búið var til fyrir þetta líkan og keyrt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5805d-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="5805d-154">Fyrir vikið verður innihald gagnafjafanna **Tax** og **Gr** berskjaldað fyrir ER-sniðum eins og óhlutbundnum gagnagjöfum.</span><span class="sxs-lookup"><span data-stu-id="5805d-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Hönnunarsíða fyrir líkanavörpun sem sýnir gagnagjafana Tax og Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="5805d-156">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="5805d-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="5805d-157">Lokið síðunni **Líkanavörpun**.</span><span class="sxs-lookup"><span data-stu-id="5805d-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="5805d-158">Skoðaðu sniðmátið</span><span class="sxs-lookup"><span data-stu-id="5805d-158">Review format</span></span>

1. <span data-ttu-id="5805d-159">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="5805d-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5805d-160">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="5805d-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5805d-161">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5805d-161">Select **Designer**.</span></span> <span data-ttu-id="5805d-162">Þetta ER-sniðmát er hannað til að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="5805d-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="5805d-163">Myndaðu skattauppgjör á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="5805d-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="5805d-164">Settu fram eftirfarandi stig skattheimtu í skattauppgjöri: reglulega, lækkað og ekkert.</span><span class="sxs-lookup"><span data-stu-id="5805d-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="5805d-165">Settu fram margar upplýsingar á hverju skattlagningarstigi, með mismunandi fjölda smáatriða í hverju stigi.</span><span class="sxs-lookup"><span data-stu-id="5805d-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Síða sniðshönnuðar](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="5805d-167">Veldu **Vörpun**.</span><span class="sxs-lookup"><span data-stu-id="5805d-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="5805d-168">Stækkaðu liðina **Líkan**, **Gögn,** og **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="5805d-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="5805d-169">Reiknaði reiturinn **Model.Data.Summary.Level** inniheldur segðina sem skilar kóða skattlagningarstigsins (**Venjulegur**, **Dregið úr**, **Enginn,** eða **Annað**) sem textagildi fyrir hvaða skattakóða sem hægt er að sækja úr gagnagjafanum **Model.Data.Summary** á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="5805d-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Hönnunarsíðan sniðmáta sem sýnir upplýsingar um gagnalíkanið til að læra færibreytur á köll](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="5805d-171">Stækkaðu liðinn **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="5805d-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="5805d-172">Stækkaðu liðinn **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="5805d-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="5805d-173">Gagnagjafinn **Model**.**Data2.Summary2** er stillt til að flokka færsluupplýsingar gagnagjafans **Model.Data.Summary** skattlagningarstig (skilað af reiknaða reitnum **Model.Data.Summary.Level**) og reikna uppsafnanirnar.</span><span class="sxs-lookup"><span data-stu-id="5805d-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Hönunnarsíða sniðmáta sem sýnir upplýsingar um gagnagjafann Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="5805d-175">Farðu yfir reiknaða reiti **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, og **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="5805d-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="5805d-176">Þessir reiknaðir reitir eru notaðir til að sía **Model**.**Data2.Summary2** skráningalistann og skila aðeins skrám sem tákna tiltekið skattlagningarstig.</span><span class="sxs-lookup"><span data-stu-id="5805d-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="5805d-177">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5805d-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="5805d-178">Stofna afleitt sniðmát</span><span class="sxs-lookup"><span data-stu-id="5805d-178">Create a derived format</span></span>
<span data-ttu-id="5805d-179">Þú getur bætt sniðið sem fylgir með því að bæta við einum reiknuðum reit til að sía tilskilið skattlagningarstig í stað þess að nota þrjá reiti sem fyrir eru: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** og **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="5805d-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="5805d-180">Hægt er að tilgreina tilskilt skattlagningarstig á þeim stað þar sem kallað verður á þennan nýja reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="5805d-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="5805d-181">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="5805d-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5805d-182">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="5805d-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5805d-183">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="5805d-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="5805d-184">Veldu **Sæktu frá nafni: Snið til að læra breytur símtöl, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="5805d-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="5805d-185">Í reitnum **Heiti** slærðu inn **Sniðmát til að læra færibreytur á köll (sérsnið)**.</span><span class="sxs-lookup"><span data-stu-id="5805d-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="5805d-186">Veljið **Stofna skilgreiningu.**</span><span class="sxs-lookup"><span data-stu-id="5805d-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="5805d-187">Stilla stika reiknaðan reit sem skilar lista yfir færslur</span><span class="sxs-lookup"><span data-stu-id="5805d-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="5805d-188">Byrjaðu að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="5805d-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="5805d-189">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5805d-189">Select **Designer**.</span></span>
2. <span data-ttu-id="5805d-190">Veldu **Stækka/fella saman** til að stækka öll snið atriði.</span><span class="sxs-lookup"><span data-stu-id="5805d-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="5805d-191">Veldu **Vörpun**.</span><span class="sxs-lookup"><span data-stu-id="5805d-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="5805d-192">Stækkaðu liðinn **Model**.</span><span class="sxs-lookup"><span data-stu-id="5805d-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="5805d-193">Veldu liðinn **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="5805d-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="5805d-194">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="5805d-194">Select **Add**.</span></span>
7. <span data-ttu-id="5805d-195">Veldu **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="5805d-196">Í reitinn **Heiti** skal færa inn **Stig**.</span><span class="sxs-lookup"><span data-stu-id="5805d-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="5805d-197">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="5805d-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="5805d-198">Skilgreindu færibreytu til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="5805d-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="5805d-199">Velja **færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="5805d-200">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5805d-200">Select **New**.</span></span>
3. <span data-ttu-id="5805d-201">Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="5805d-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="5805d-202">Í reitnum **Gerð** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="5805d-203">Aðeins er hægt að nota frumstæðar gagnategundir til að tilgreina gerð frumbreytu færibreytunnar.</span><span class="sxs-lookup"><span data-stu-id="5805d-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="5805d-204">Þess vegna er ekki hægt að nota gerðirnar **Skráalista**, **Skrá** og **Enum** í þessu skyni.</span><span class="sxs-lookup"><span data-stu-id="5805d-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="5805d-205">Hámarksfjöldi færibreyta sem hægt er að tilgreina fyrir einn reiknaðan reit er 8.</span><span class="sxs-lookup"><span data-stu-id="5805d-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Upprunalisti færibreyta](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="5805d-207">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5805d-207">Select **OK**.</span></span>

<span data-ttu-id="5805d-208">Með því að bæta við þessa færibreytu tilgreinirðu það skilyrði sem verður að vera til staðar til að kalla þennan reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="5805d-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="5805d-209">Þegar þú kallar þennan reiknaða reit þarftu að tilgreina rökin fyrir færibreytuna **Skattlagningarstig** sem gildi með sniðinu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="5805d-210">Gakktu úr skugga um að þú skilgreinir eingöngu færibreytur fyrir þá reiknaðu reiti sem eru í gámi (annaðhvort **Skráalisti**, **Skrá**, eða **Gámur**).</span><span class="sxs-lookup"><span data-stu-id="5805d-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="5805d-211">Stilla breytan er fáanleg á lista yfir gagnaveitur fyrir þennan reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="5805d-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="5805d-212">Þú getur bætt við færibreytuna við stillta segð með því að velja **Bættu við gagnaveitu**.</span><span class="sxs-lookup"><span data-stu-id="5805d-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Gagnagjafareitir](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="5805d-214">Skilgreindu segð til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="5805d-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="5805d-215">Í reitinn **Formúla** skal slá inn:</span><span class="sxs-lookup"><span data-stu-id="5805d-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="5805d-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="5805d-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="5805d-217">Veldu færibreytuna **Skattlagningarstig** á lista yfir gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="5805d-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="5805d-218">Veldu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="5805d-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="5805d-219">Í reitnum **Formúla** skal ljúka segðinni sem:</span><span class="sxs-lookup"><span data-stu-id="5805d-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="5805d-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="5805d-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="5805d-221">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5805d-221">Select **Save**.</span></span>

    ![Upplýsingar um reit gagnaveitu](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="5805d-223">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5805d-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="5805d-224">Ljúktu við að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="5805d-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="5805d-225">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5805d-225">Select **OK**.</span></span>

<span data-ttu-id="5805d-226">Á síðunni **Sniðmátshönnuður** krefst stillanlegur reiknaður reiturinn **Stig** frumbreytunnar **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Stækkaður listi yfir reiknuð reitastig](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="5805d-228">Notaðu stilla reiknaða reitinn til að binda sniðþætti</span><span class="sxs-lookup"><span data-stu-id="5805d-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="5805d-229">Veldu **Model.Data2.Levels** til að velja stilla reiknaða reitinn.</span><span class="sxs-lookup"><span data-stu-id="5805d-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="5805d-230">Veldu sniðmátsþáttinn **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="5805d-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="5805d-231">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="5805d-231">Select **Bind**.</span></span>
4. <span data-ttu-id="5805d-232">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level1**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum valins sniðareiningar.</span><span class="sxs-lookup"><span data-stu-id="5805d-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="5805d-233">Beitt bindandi hefur verið smíðað sem kall á reiknaða reitinn með breytu.</span><span class="sxs-lookup"><span data-stu-id="5805d-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="5805d-234">Sjálfgefið er að nafnið á bundnu sniði er notað sem rök fyrir breytu útreiknaðan reit við eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="5805d-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="5805d-235">Reiknaður reiturinn er stilltur til að nota eina breytu.</span><span class="sxs-lookup"><span data-stu-id="5805d-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="5805d-236">Gagnategund þessa færibreytu er skilgreind sem **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="5805d-237">Þegar nafn bundins sniðsþátta er tómt er heiti gagnaheimildar þessarar frumefnis notað í beinni bindingu.</span><span class="sxs-lookup"><span data-stu-id="5805d-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="5805d-238">Veldu sniðmátsþáttinn **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="5805d-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="5805d-239">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="5805d-239">Select **Bind**.</span></span>
7. <span data-ttu-id="5805d-240">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level2**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum undir valinni sniðareiningu.</span><span class="sxs-lookup"><span data-stu-id="5805d-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="5805d-241">Veldu sniðmátsþáttinn **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="5805d-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="5805d-242">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="5805d-242">Select **Bind**.</span></span>
10. <span data-ttu-id="5805d-243">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level3**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum undir valinni sniðareiningu.</span><span class="sxs-lookup"><span data-stu-id="5805d-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="5805d-244">Þegar þú tilgreinir færibreytuna á útreiknaða reitinn fyrir XML frumefnið sem táknar skattheimtu (t.d. **Model.Data2.Levels(„Reduced“)** sem textagildi), þú þarft ekki að gera það sama fyrir nestta XML eiginleika - bindingar þeirra erfa sjálfkrafa gildi frumbreytunnar sem er skilgreint á yfirstigi (**Model.Data2.Levels.aggregated.Base**, ekki **Model.Data2.Levels („Minni“).aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="5805d-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="5805d-245">Endurtekin köll í reiknaða reiti með færibreytu eru ekki studd.</span><span class="sxs-lookup"><span data-stu-id="5805d-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="5805d-246">Þú getur valið **Breyta formúlu**, og breytt beitt-fyrir-vanræksröksemdum á breytubreytta reikna reitnum í valda bindingu.</span><span class="sxs-lookup"><span data-stu-id="5805d-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="5805d-247">Ef þess frumbreytu vantar getur það valdið villum á keyrslutíma - notendur eru upplýstir um slíkar aðstæður þegar núverandi snið er staðfest.</span><span class="sxs-lookup"><span data-stu-id="5805d-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Tilkynning um villuviðvörun](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="5805d-249">Skilgreindu reiknaðan reit með færibreytu til að skila skrá</span><span class="sxs-lookup"><span data-stu-id="5805d-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="5805d-250">Þegar reiknaður reitur með færibreytum skilar skrá þarftu að styðja við bindingu einstakra reita þessarar skráar til að forsníða þætti.</span><span class="sxs-lookup"><span data-stu-id="5805d-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="5805d-251">Í slíkum tilvikum verður ekki um yfirbindingu að ræða sem inniheldur gildi frumbreytu til að kalla út reiknaðan reit fyrir breytu - þetta gildi verður að vera skilgreint í bindingu reits einnar skrár.</span><span class="sxs-lookup"><span data-stu-id="5805d-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="5805d-252">Byrjaðu að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="5805d-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="5805d-253">Veldu liðinn **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="5805d-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="5805d-254">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="5805d-254">Select **Add**.</span></span>
3. <span data-ttu-id="5805d-255">Veldu **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="5805d-256">Í reitinn **Heiti** skal færa inn **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="5805d-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="5805d-257">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="5805d-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="5805d-258">Skilgreindu færibreytu til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="5805d-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="5805d-259">Velja **færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="5805d-260">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5805d-260">Select **New**.</span></span>
3. <span data-ttu-id="5805d-261">Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="5805d-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="5805d-262">Í reitnum **Gerð** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="5805d-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="5805d-263">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5805d-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="5805d-264">Skilgreindu segð til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="5805d-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="5805d-265">Í reitnum **Formúla** skal færa inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="5805d-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="5805d-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="5805d-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="5805d-267">Veldu færibreytuna **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="5805d-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="5805d-268">Veldu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="5805d-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="5805d-269">Í reitnum **Formúla** skaltu bæta við **'Taxation Level'))** við það sem þú slóst inn í skref 1 til að klára segðina til:</span><span class="sxs-lookup"><span data-stu-id="5805d-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="5805d-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="5805d-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="5805d-271">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5805d-271">Select **Save**.</span></span>
6. <span data-ttu-id="5805d-272">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5805d-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="5805d-273">Ljúktu við að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="5805d-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="5805d-274">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5805d-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="5805d-275">Notaðu stilla reiknaða reitinn til að binda sniðþætti</span><span class="sxs-lookup"><span data-stu-id="5805d-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="5805d-276">Útvíkkaðu **Model.Data2.LevelRecord** til að velja stilla reiknaða reitinn.</span><span class="sxs-lookup"><span data-stu-id="5805d-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="5805d-277">Útvíkkaðu gáminn **Model.Data2.LevelRecord.aggregated** í skilgreindum reiknaðum reit.</span><span class="sxs-lookup"><span data-stu-id="5805d-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="5805d-278">Veldu reitinn **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="5805d-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="5805d-279">Veldu sniðmátsþáttinn **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="5805d-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="5805d-280">Veldu **Losa**.</span><span class="sxs-lookup"><span data-stu-id="5805d-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="5805d-281">Veldu sniðmátsþáttinn **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="5805d-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="5805d-282">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="5805d-282">Select **Bind**.</span></span>
8. <span data-ttu-id="5805d-283">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="5805d-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="5805d-284">Breyta segð í **Model.Data2.LevelRecord(„None“).aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="5805d-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Uppfærð segð](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="5805d-286">Fjarlægðu reiknaða reiti sem ekki eru notaðir</span><span class="sxs-lookup"><span data-stu-id="5805d-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="5805d-287">Veldu **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="5805d-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="5805d-288">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="5805d-288">Select **Delete**.</span></span>
3. <span data-ttu-id="5805d-289">Veldu **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="5805d-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="5805d-290">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="5805d-290">Select **Delete**.</span></span>
5. <span data-ttu-id="5805d-291">Veldu **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="5805d-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="5805d-292">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="5805d-292">Select **Delete**.</span></span>
7. <span data-ttu-id="5805d-293">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5805d-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5805d-294">Þú notaðir aftur sama reiknaða reit **Model.Data2.Levels** nokkrum sinnum í sniðbindingum.</span><span class="sxs-lookup"><span data-stu-id="5805d-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="5805d-295">Það er miklu auðveldara að nota og viðhalda einum reiknuðum reit í stað þess að gera þetta fyrir marga svipaða reiti.</span><span class="sxs-lookup"><span data-stu-id="5805d-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="5805d-296">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5805d-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="5805d-297">Fullkláruð leiðrétt útgáfa af afleiddu sniði</span><span class="sxs-lookup"><span data-stu-id="5805d-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="5805d-298">Á flýtflipanum **Útgáfur** velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="5805d-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="5805d-299">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="5805d-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="5805d-300">Flyttu út fullkláraða útgáfu af afleiddu sniði</span><span class="sxs-lookup"><span data-stu-id="5805d-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="5805d-301">Veldu sniðmátið **Snið til að læra færibreytur í köll (sérsniðin)** í stillingartrénu.</span><span class="sxs-lookup"><span data-stu-id="5805d-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="5805d-302">Í flýtiflipanum **Útgáfur** velurðu lokna útgáfu 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="5805d-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="5805d-303">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="5805d-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="5805d-304">Veldu **Flytja út sem XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="5805d-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="5805d-305">Geymdu sótta skilgreiningu á staðnum á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="5805d-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="5805d-306">Prófa ER-snið</span><span class="sxs-lookup"><span data-stu-id="5805d-306">Test ER formats</span></span> 
<span data-ttu-id="5805d-307">Þú getur keyrt upphafsuppbót og endurbætt ER snið til að ganga úr skugga um að skilgreindir útreiknaðir reitir með færibreytur virki rétt.</span><span class="sxs-lookup"><span data-stu-id="5805d-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="5805d-308">Flytja inn rafræn skýrslugerð grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="5805d-308">Import ER configurations</span></span>
<span data-ttu-id="5805d-309">Þú getur flutt inn yfirfarnar stillingar úr RCS með því að nota ER-geymslu af gerðinni **RCS**.</span><span class="sxs-lookup"><span data-stu-id="5805d-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="5805d-310">Ef þú hefur þegar gengið í gegnum skrefin í efninu, [Flytja inn rafrænar skýrslustillingar (ER) úr Regulatory Configuration Services (RCS)](rcs-download-configurations.md), notaðu stilla ER geymslu til að flytja inn stillingar sem fjallað var um áður í þessu efni til umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="5805d-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="5805d-311">Að ð öðrum kosti skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="5805d-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="5805d-312">Veldu fyrirtækið **DEMF** og veldu á sjálfgefna yfirlitinu **Rafræn skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="5805d-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="5805d-313">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="5805d-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="5805d-314">Flytja inn sóttar skilgreiningar úr Microsoft Download Center í eftirfarandi röð: gagnalíkan, vörpun líkans, snið.</span><span class="sxs-lookup"><span data-stu-id="5805d-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="5805d-315">Ljúktu eftirfarandi skrefum fyrir hverja ER-skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="5805d-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="5805d-316">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="5805d-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5805d-317">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="5805d-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5805d-318">Veldu **Vafra** til að velja nauðsynlega ER-skilgreiningu á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="5805d-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="5805d-319">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5805d-319">Select **OK**.</span></span>

4. <span data-ttu-id="5805d-320">Flytja út úr RCS lokið útgáfu 1.1.1 af sniðmátinu **Snið til að læra færibreytur í köll (sérsniðin)**:</span><span class="sxs-lookup"><span data-stu-id="5805d-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="5805d-321">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="5805d-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5805d-322">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="5805d-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5805d-323">Veldu **Fletta** til að velja staðbundið vistaða skrána **Snið til að læra færibreytur á köll (sérsniðin)** á XML sniði.</span><span class="sxs-lookup"><span data-stu-id="5805d-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="5805d-324">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5805d-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="5805d-325">Keyra ER-snið</span><span class="sxs-lookup"><span data-stu-id="5805d-325">Run ER formats</span></span>

1. <span data-ttu-id="5805d-326">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="5805d-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5805d-327">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="5805d-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5805d-328">Veldu **Keyra** á efsta borðanum.</span><span class="sxs-lookup"><span data-stu-id="5805d-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="5805d-329">Vistaðu úttakið á staðnum.</span><span class="sxs-lookup"><span data-stu-id="5805d-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="5805d-330">Veldu liðinn **Snið til að læra færibreytur á köll (sérsniðin)**.</span><span class="sxs-lookup"><span data-stu-id="5805d-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="5805d-331">Veldu **Keyra** á efsta borðanum.</span><span class="sxs-lookup"><span data-stu-id="5805d-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="5805d-332">Vistaðu úttakið á staðnum.</span><span class="sxs-lookup"><span data-stu-id="5805d-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="5805d-333">Berðu saman innihald í mynduðu úttaki.</span><span class="sxs-lookup"><span data-stu-id="5805d-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5805d-334">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5805d-334">Additional resources</span></span>
[<span data-ttu-id="5805d-335">Formúluhönnuður í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="5805d-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
