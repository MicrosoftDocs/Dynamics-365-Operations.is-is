---
title: Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað
description: Þetta efni veitir upplýsingar um hvernig skal nota reitagerðina Reiknað fyrir ER-gagnagjafa.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
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
ms.openlocfilehash: 3f331401f8d191243f72961333e4f1dbe84d0be5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771330"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="9e79a-103">Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað</span><span class="sxs-lookup"><span data-stu-id="9e79a-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e79a-104">Þetta efni útskýrir hvernig þú getur hannað gagnagjafa rafrænnar skýrslugerðar (ER) með því að nota gerðina **Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="9e79a-105">Þessi gagnagjafi getur innihaldið ER-segð sem, þegar hún er keyrð, er hægt að stjórna með gildum færibreytufrumbreytanna sem eru skilgreind í bindingu sem kallar þennan gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="9e79a-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="9e79a-106">Með því að skilgreina köll í færibreytur af slíkum gagnagjöfum er hægt að endurnýta staka gagnagjafa í mörgum bindingum, sem dregur úr heildarfjölda gagnagjafa sem verður að skilgreina í ER-líkanavörpunum eða ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="9e79a-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="9e79a-107">Það einfaldar einnig skilgreinda ER-íhluti, sem dregur úr viðhaldskostnaði og notkunarkostnaði annarra neytenda.</span><span class="sxs-lookup"><span data-stu-id="9e79a-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9e79a-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="9e79a-108">Prerequisites</span></span>
<span data-ttu-id="9e79a-109">Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:</span><span class="sxs-lookup"><span data-stu-id="9e79a-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="9e79a-110">Aðgangur að einu af þessum hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="9e79a-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="9e79a-111">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="9e79a-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="9e79a-112">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9e79a-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="9e79a-113">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="9e79a-113">System administrator</span></span>

- <span data-ttu-id="9e79a-114">Aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance and Operations, fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="9e79a-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="9e79a-115">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="9e79a-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="9e79a-116">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9e79a-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="9e79a-117">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="9e79a-117">System administrator</span></span>

<span data-ttu-id="9e79a-118">Úr [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) sækirðu þjappaða skrána **Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="9e79a-119">Hún inniheldur eftirfarandi ER-skilgreiningar sem verður að draga út og geyma á staðnum.</span><span class="sxs-lookup"><span data-stu-id="9e79a-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="9e79a-120">**Efni**</span><span class="sxs-lookup"><span data-stu-id="9e79a-120">**Content**</span></span>                           | <span data-ttu-id="9e79a-121">**Skrárnafn**</span><span class="sxs-lookup"><span data-stu-id="9e79a-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e79a-122">Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9e79a-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="9e79a-123">Líkan til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="9e79a-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="9e79a-124">Sýnishorn af skilgreiningu lýsigagna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9e79a-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="9e79a-125">Lýsigögn til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="9e79a-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="9e79a-126">Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9e79a-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="9e79a-127">Vörpun til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="9e79a-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="9e79a-128">Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9e79a-128">Sample ER format configuration</span></span>        | <span data-ttu-id="9e79a-129">Snimát til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="9e79a-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="9e79a-130">Skráðu þig inn á RCS tilvikið</span><span class="sxs-lookup"><span data-stu-id="9e79a-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="9e79a-131">Í þessu dæmi mun notandi stofna skilgreiningu fyrir sýnifyrirtækið Litware, Inc. Í RCS verður fyrst að ljúka skrefum ferlisins [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="9e79a-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="9e79a-132">Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="9e79a-133">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="9e79a-134">Flytja inn sóttar skilgreiningar í RCS í eftirfarandi röð: gagnalíkan, lýsigögn, vörpun líkans, snið.</span><span class="sxs-lookup"><span data-stu-id="9e79a-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="9e79a-135">Ljúktu eftirfarandi skrefum fyrir hverja ER-skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="9e79a-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="9e79a-136">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="9e79a-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="9e79a-137">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="9e79a-138">Veldu **Vafra** og veldu síðan nauðsynlega ER-skilgreiningu á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9e79a-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="9e79a-139">Veljið **Í lagi.**</span><span class="sxs-lookup"><span data-stu-id="9e79a-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="9e79a-140">Farðu yfir fyrirliggjandi ER-lausn</span><span class="sxs-lookup"><span data-stu-id="9e79a-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="9e79a-141">Farðu yfir vörpun líkans</span><span class="sxs-lookup"><span data-stu-id="9e79a-141">Review model mapping</span></span>

1. <span data-ttu-id="9e79a-142">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="9e79a-143">Veldu **Vörpun til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="9e79a-144">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-144">Select **Designer**.</span></span>
4. <span data-ttu-id="9e79a-145">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-145">Select **Designer**.</span></span>  
   
    <span data-ttu-id="9e79a-146">Þessi ER-líkanavörpun er hönnuð til að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="9e79a-146">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="9e79a-147">Sæktu lista yfir skattakóða (gagnagjafinn **Skattur**) sem er að finna í töflunni **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-147">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="9e79a-148">Sæktu lista yfir skattafærslur (gagnagjafinn **Trans**) sem er að finna í töflunni **TaxTable**:</span><span class="sxs-lookup"><span data-stu-id="9e79a-148">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="9e79a-149">Flokka lista yfir sóttar færslur (gagnagjafinn **Gr**) eftir skattakóða.</span><span class="sxs-lookup"><span data-stu-id="9e79a-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="9e79a-150">Reiknaðu fyrir flokkaðar færslur eftirfarandi uppsöfnuð gildi á hvern skattakóða:</span><span class="sxs-lookup"><span data-stu-id="9e79a-150">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="9e79a-151">Summa skattstofnsgilda.</span><span class="sxs-lookup"><span data-stu-id="9e79a-151">Sum of tax base values.</span></span>
            - <span data-ttu-id="9e79a-152">Summa skattgilda.</span><span class="sxs-lookup"><span data-stu-id="9e79a-152">Sum of tax values.</span></span>
            - <span data-ttu-id="9e79a-153">Lágmarksgildi beitts skatthlutfalls.</span><span class="sxs-lookup"><span data-stu-id="9e79a-153">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="9e79a-154">Vörpun líkansins í þessari stillingu útfærir grunngagnalíkanið fyrir hvaða ER-snið sem er búið til fyrir þetta líkan og keyrt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9e79a-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="9e79a-155">Fyrir vikið verður innihald gagnafjafanna **Tax** og **Gr** berskjaldað fyrir ER-sniðum eins og óhlutbundnum gagnagjöfum.</span><span class="sxs-lookup"><span data-stu-id="9e79a-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Hönnunarsíða fyrir líkanavörpun sem sýnir gagnagjafana Tax og Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="9e79a-157">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="9e79a-158">Lokið síðunni **Líkanavörpun**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="9e79a-159">Skoðaðu sniðmátið</span><span class="sxs-lookup"><span data-stu-id="9e79a-159">Review format</span></span>

1. <span data-ttu-id="9e79a-160">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="9e79a-161">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="9e79a-162">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-162">Select **Designer**.</span></span> <span data-ttu-id="9e79a-163">Þetta ER-sniðmát er hannað til að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="9e79a-163">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="9e79a-164">Myndaðu skattauppgjör á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9e79a-164">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="9e79a-165">Settu fram eftirfarandi stig skattheimtu í skattauppgjöri: reglulega, lækkað og ekkert.</span><span class="sxs-lookup"><span data-stu-id="9e79a-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="9e79a-166">Settu fram margar upplýsingar á hverju skattlagningarstigi, með mismunandi fjölda smáatriða í hverju stigi.</span><span class="sxs-lookup"><span data-stu-id="9e79a-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Síða sniðshönnuðar](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="9e79a-168">Veldu **Vörpun**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="9e79a-169">Stækkaðu liðina **Líkan**, **Gögn,** og **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="9e79a-170">Reiknaði reiturinn **Model.Data.Summary.Level** inniheldur segðina sem skilar kóða skattlagningarstigsins (**Venjulegur**, **Dregið úr**, **Enginn,** eða **Annað**) sem textagildi fyrir hvaða skattakóða sem hægt er að sækja úr gagnagjafanum **Model.Data.Summary** á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="9e79a-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Hönnunarsíðan sniðmáta sem sýnir upplýsingar um gagnalíkanið til að læra færibreytur á köll](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="9e79a-172">Stækkaðu liðinn **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="9e79a-173">Stækkaðu liðinn **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="9e79a-174">Gagnagjafinn **Model**.**Data2.Summary2** er stillt til að flokka færsluupplýsingar gagnagjafans **Model.Data.Summary** skattlagningarstig (skilað af reiknaða reitnum **Model.Data.Summary.Level**) og reikna uppsafnanirnar.</span><span class="sxs-lookup"><span data-stu-id="9e79a-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Hönunnarsíða sniðmáta sem sýnir upplýsingar um gagnagjafann Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="9e79a-176">Farðu yfir reiknaða reiti **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, og **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="9e79a-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="9e79a-177">Þessir reiknaðir reitir eru notaðir til að sía **Model**.**Data2.Summary2** skráningalistann og skila aðeins skrám sem tákna tiltekið skattlagningarstig.</span><span class="sxs-lookup"><span data-stu-id="9e79a-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="9e79a-178">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="9e79a-179">Stofna afleitt sniðmát</span><span class="sxs-lookup"><span data-stu-id="9e79a-179">Create a derived format</span></span>
<span data-ttu-id="9e79a-180">Þú getur bætt sniðið sem fylgir með því að bæta við einum reiknuðum reit til að sía tilskilið skattlagningarstig í stað þess að nota þrjá reiti sem fyrir eru: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** og **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="9e79a-181">Hægt er að tilgreina tilskilt skattlagningarstig á þeim stað þar sem kallað verður á þennan nýja reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="9e79a-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="9e79a-182">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="9e79a-183">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="9e79a-184">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="9e79a-185">Veldu **Sæktu frá nafni: Snið til að læra breytur símtöl, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="9e79a-186">Í reitnum **Heiti** slærðu inn **Sniðmát til að læra færibreytur á köll (sérsnið)**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="9e79a-187">Veljið **Stofna skilgreiningu.**</span><span class="sxs-lookup"><span data-stu-id="9e79a-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="9e79a-188">Stilla stika reiknaðan reit sem skilar lista yfir færslur</span><span class="sxs-lookup"><span data-stu-id="9e79a-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="9e79a-189">Byrjaðu að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9e79a-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="9e79a-190">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-190">Select **Designer**.</span></span>
2. <span data-ttu-id="9e79a-191">Veldu **Stækka/fella saman** til að stækka öll snið atriði.</span><span class="sxs-lookup"><span data-stu-id="9e79a-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="9e79a-192">Veldu **Vörpun**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="9e79a-193">Stækkaðu liðinn **Model**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="9e79a-194">Veldu liðinn **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="9e79a-195">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-195">Select **Add**.</span></span>
7. <span data-ttu-id="9e79a-196">Veldu **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="9e79a-197">Í reitinn **Heiti** skal færa inn **Stig**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="9e79a-198">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="9e79a-199">Skilgreindu færibreytu til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9e79a-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="9e79a-200">Velja **færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="9e79a-201">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-201">Select **New**.</span></span>
3. <span data-ttu-id="9e79a-202">Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="9e79a-203">Í reitnum **Gerð** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="9e79a-204">Aðeins er hægt að nota frumstæðar gagnategundir til að tilgreina gerð frumbreytu færibreytunnar.</span><span class="sxs-lookup"><span data-stu-id="9e79a-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="9e79a-205">Þess vegna er ekki hægt að nota gerðirnar **Skráalista**, **Skrá** og **Enum** í þessu skyni.</span><span class="sxs-lookup"><span data-stu-id="9e79a-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="9e79a-206">Hámarksfjöldi færibreyta sem hægt er að tilgreina fyrir einn reiknaðan reit er 8.</span><span class="sxs-lookup"><span data-stu-id="9e79a-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Upprunalisti færibreyta](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="9e79a-208">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-208">Select **OK**.</span></span>

<span data-ttu-id="9e79a-209">Með því að bæta við þessa færibreytu tilgreinirðu það skilyrði sem verður að vera til staðar til að kalla þennan reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="9e79a-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="9e79a-210">Þegar þú kallar þennan reiknaða reit þarftu að tilgreina rökin fyrir færibreytuna **Skattlagningarstig** sem gildi með sniðinu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="9e79a-211">Gakktu úr skugga um að þú skilgreinir eingöngu færibreytur fyrir þá reiknaðu reiti sem eru í gámi (annaðhvort **Skráalisti**, **Skrá**, eða **Gámur**).</span><span class="sxs-lookup"><span data-stu-id="9e79a-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="9e79a-212">Stilla breytan er fáanleg á lista yfir gagnaveitur fyrir þennan reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="9e79a-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="9e79a-213">Þú getur bætt við færibreytuna við stillta segð með því að velja **Bættu við gagnaveitu**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Gagnagjafareitir](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="9e79a-215">Skilgreindu segð til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9e79a-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="9e79a-216">Í reitinn **Formúla** skal slá inn:</span><span class="sxs-lookup"><span data-stu-id="9e79a-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="9e79a-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="9e79a-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="9e79a-218">Veldu færibreytuna **Skattlagningarstig** á lista yfir gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="9e79a-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="9e79a-219">Veldu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="9e79a-220">Í reitnum **Formúla** skal ljúka segðinni sem:</span><span class="sxs-lookup"><span data-stu-id="9e79a-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="9e79a-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="9e79a-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="9e79a-222">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-222">Select **Save**.</span></span>

    ![Upplýsingar um reit gagnaveitu](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="9e79a-224">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="9e79a-225">Ljúktu við að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9e79a-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="9e79a-226">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-226">Select **OK**.</span></span>

<span data-ttu-id="9e79a-227">Á síðunni **Sniðmátshönnuður** krefst stillanlegur reiknaður reiturinn **Stig** frumbreytunnar **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Stækkaður listi yfir reiknuð reitastig](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="9e79a-229">Notaðu stilla reiknaða reitinn til að binda sniðþætti</span><span class="sxs-lookup"><span data-stu-id="9e79a-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="9e79a-230">Veldu **Model.Data2.Levels** til að velja stilla reiknaða reitinn.</span><span class="sxs-lookup"><span data-stu-id="9e79a-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="9e79a-231">Veldu sniðmátsþáttinn **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="9e79a-232">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-232">Select **Bind**.</span></span>
4. <span data-ttu-id="9e79a-233">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level1**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum valins sniðareiningar.</span><span class="sxs-lookup"><span data-stu-id="9e79a-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="9e79a-234">Beitt bindandi hefur verið smíðað sem kall á reiknaða reitinn með breytu.</span><span class="sxs-lookup"><span data-stu-id="9e79a-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="9e79a-235">Sjálfgefið er að nafnið á bundnu sniði er notað sem rök fyrir breytu útreiknaðan reit við eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="9e79a-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="9e79a-236">Reiknaður reiturinn er stilltur til að nota eina breytu.</span><span class="sxs-lookup"><span data-stu-id="9e79a-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="9e79a-237">Gagnategund þessa færibreytu er skilgreind sem **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="9e79a-238">Þegar nafn bundins sniðsþátta er tómt er heiti gagnaheimildar þessarar frumefnis notað í beinni bindingu.</span><span class="sxs-lookup"><span data-stu-id="9e79a-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="9e79a-239">Veldu sniðmátsþáttinn **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="9e79a-240">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-240">Select **Bind**.</span></span>
7. <span data-ttu-id="9e79a-241">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level2**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum undir valinni sniðareiningu.</span><span class="sxs-lookup"><span data-stu-id="9e79a-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="9e79a-242">Veldu sniðmátsþáttinn **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="9e79a-243">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-243">Select **Bind**.</span></span>
10. <span data-ttu-id="9e79a-244">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level3**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum undir valinni sniðareiningu.</span><span class="sxs-lookup"><span data-stu-id="9e79a-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="9e79a-245">Þegar þú tilgreinir færibreytuna á útreiknaða reitinn fyrir XML frumefnið sem táknar skattheimtu (t.d. **Model.Data2.Levels(„Reduced“)** sem textagildi), þú þarft ekki að gera það sama fyrir nestta XML eiginleika - bindingar þeirra erfa sjálfkrafa gildi frumbreytunnar sem er skilgreint á yfirstigi (**Model.Data2.Levels.aggregated.Base**, ekki **Model.Data2.Levels („Minni“).aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="9e79a-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="9e79a-246">Endurtekin köll í reiknaða reiti með færibreytu eru ekki studd.</span><span class="sxs-lookup"><span data-stu-id="9e79a-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="9e79a-247">Þú getur valið **Breyta formúlu**, og breytt beitt-fyrir-vanræksröksemdum á breytubreytta reikna reitnum í valda bindingu.</span><span class="sxs-lookup"><span data-stu-id="9e79a-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="9e79a-248">Ef þess frumbreytu vantar getur það valdið villum á keyrslutíma - notendur eru upplýstir um slíkar aðstæður þegar núverandi snið er staðfest.</span><span class="sxs-lookup"><span data-stu-id="9e79a-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Tilkynning um villuviðvörun](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="9e79a-250">Skilgreindu reiknaðan reit með færibreytu til að skila skrá</span><span class="sxs-lookup"><span data-stu-id="9e79a-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="9e79a-251">Þegar reiknaður reitur með færibreytum skilar skrá þarftu að styðja við bindingu einstakra reita þessarar skráar til að forsníða þætti.</span><span class="sxs-lookup"><span data-stu-id="9e79a-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="9e79a-252">Í slíkum tilvikum verður ekki um yfirbindingu að ræða sem inniheldur gildi frumbreytu til að kalla út reiknaðan reit fyrir breytu - þetta gildi verður að vera skilgreint í bindingu reits einnar skrár.</span><span class="sxs-lookup"><span data-stu-id="9e79a-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="9e79a-253">Byrjaðu að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9e79a-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="9e79a-254">Veldu liðinn **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="9e79a-255">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-255">Select **Add**.</span></span>
3. <span data-ttu-id="9e79a-256">Veldu **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="9e79a-257">Í reitinn **Heiti** skal færa inn **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="9e79a-258">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="9e79a-259">Skilgreindu færibreytu til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9e79a-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="9e79a-260">Velja **færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="9e79a-261">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-261">Select **New**.</span></span>
3. <span data-ttu-id="9e79a-262">Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="9e79a-263">Í reitnum **Gerð** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="9e79a-264">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="9e79a-265">Skilgreindu segð til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9e79a-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="9e79a-266">Í reitnum **Formúla** skal færa inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="9e79a-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="9e79a-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="9e79a-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="9e79a-268">Veldu færibreytuna **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="9e79a-269">Veldu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="9e79a-270">Í reitnum **Formúla** skaltu bæta við **'Taxation Level'))** við það sem þú slóst inn í skref 1 til að klára segðina til:</span><span class="sxs-lookup"><span data-stu-id="9e79a-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="9e79a-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="9e79a-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="9e79a-272">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-272">Select **Save**.</span></span>
6. <span data-ttu-id="9e79a-273">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="9e79a-274">Ljúktu við að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9e79a-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="9e79a-275">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="9e79a-276">Notaðu stilla reiknaða reitinn til að binda sniðþætti</span><span class="sxs-lookup"><span data-stu-id="9e79a-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="9e79a-277">Útvíkkaðu **Model.Data2.LevelRecord** til að velja stilla reiknaða reitinn.</span><span class="sxs-lookup"><span data-stu-id="9e79a-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="9e79a-278">Útvíkkaðu gáminn **Model.Data2.LevelRecord.aggregated** í skilgreindum reiknaðum reit.</span><span class="sxs-lookup"><span data-stu-id="9e79a-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="9e79a-279">Veldu reitinn **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="9e79a-280">Veldu sniðmátsþáttinn **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="9e79a-281">Veldu **Losa**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="9e79a-282">Veldu sniðmátsþáttinn **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="9e79a-283">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-283">Select **Bind**.</span></span>
8. <span data-ttu-id="9e79a-284">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="9e79a-285">Breyta segð í **Model.Data2.LevelRecord(„None“).aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Uppfærð segð](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="9e79a-287">Fjarlægðu reiknaða reiti sem ekki eru notaðir</span><span class="sxs-lookup"><span data-stu-id="9e79a-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="9e79a-288">Veldu **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="9e79a-289">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-289">Select **Delete**.</span></span>
3. <span data-ttu-id="9e79a-290">Veldu **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="9e79a-291">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-291">Select **Delete**.</span></span>
5. <span data-ttu-id="9e79a-292">Veldu **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="9e79a-293">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-293">Select **Delete**.</span></span>
7. <span data-ttu-id="9e79a-294">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9e79a-295">Þú notaðir aftur sama reiknaða reit **Model.Data2.Levels** nokkrum sinnum í sniðbindingum.</span><span class="sxs-lookup"><span data-stu-id="9e79a-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="9e79a-296">Það er miklu auðveldara að nota og viðhalda einum reiknuðum reit í stað þess að gera þetta fyrir marga svipaða reiti.</span><span class="sxs-lookup"><span data-stu-id="9e79a-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="9e79a-297">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="9e79a-298">Fullkláruð leiðrétt útgáfa af afleiddu sniði</span><span class="sxs-lookup"><span data-stu-id="9e79a-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="9e79a-299">Á flýtflipanum **Útgáfur** velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="9e79a-300">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="9e79a-301">Flyttu út fullkláraða útgáfu af afleiddu sniði</span><span class="sxs-lookup"><span data-stu-id="9e79a-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="9e79a-302">Veldu sniðmátið **Snið til að læra færibreytur í köll (sérsniðin)** í stillingartrénu.</span><span class="sxs-lookup"><span data-stu-id="9e79a-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="9e79a-303">Í flýtiflipanum **Útgáfur** velurðu lokna útgáfu 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="9e79a-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="9e79a-304">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="9e79a-305">Veldu **Flytja út sem XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="9e79a-306">Geymdu sótta skilgreiningu á staðnum á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9e79a-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="9e79a-307">Prófa ER-snið</span><span class="sxs-lookup"><span data-stu-id="9e79a-307">Test ER formats</span></span> 
<span data-ttu-id="9e79a-308">Þú getur keyrt upphafsuppbót og endurbætt ER snið til að ganga úr skugga um að skilgreindir útreiknaðir reitir með færibreytur virki rétt.</span><span class="sxs-lookup"><span data-stu-id="9e79a-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="9e79a-309">Flytja inn rafræn skýrslugerð grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="9e79a-309">Import ER configurations</span></span>
<span data-ttu-id="9e79a-310">Þú getur flutt inn yfirfarnar stillingar úr RCS með því að nota ER-geymslu af gerðinni **RCS**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="9e79a-311">Ef þú hefur þegar gengið í gegnum skrefin í efninu, [Flytja inn rafrænar skýrslustillingar (ER) úr Regulatory Configuration Services (RCS)](rcs-download-configurations.md), notaðu stilla ER geymslu til að flytja inn stillingar sem fjallað var um áður í þessu efni til umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="9e79a-311">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="9e79a-312">Að ð öðrum kosti skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="9e79a-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="9e79a-313">Veldu fyrirtækið **DEMF** og veldu á sjálfgefna yfirlitinu **Rafræn skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="9e79a-314">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="9e79a-315">Flytja inn sóttar skilgreiningar úr Microsoft Download Center í eftirfarandi röð: gagnalíkan, vörpun líkans, snið.</span><span class="sxs-lookup"><span data-stu-id="9e79a-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="9e79a-316">Ljúktu eftirfarandi skrefum fyrir hverja ER-skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="9e79a-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="9e79a-317">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="9e79a-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="9e79a-318">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="9e79a-319">Veldu **Vafra** til að velja nauðsynlega ER-skilgreiningu á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9e79a-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="9e79a-320">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-320">Select **OK**.</span></span>

4. <span data-ttu-id="9e79a-321">Flytja út úr RCS lokið útgáfu 1.1.1 af sniðmátinu **Snið til að læra færibreytur í köll (sérsniðin)**:</span><span class="sxs-lookup"><span data-stu-id="9e79a-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="9e79a-322">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="9e79a-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="9e79a-323">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="9e79a-324">Veldu **Fletta** til að velja staðbundið vistaða skrána **Snið til að læra færibreytur á köll (sérsniðin)** á XML sniði.</span><span class="sxs-lookup"><span data-stu-id="9e79a-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="9e79a-325">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="9e79a-326">Keyra ER-snið</span><span class="sxs-lookup"><span data-stu-id="9e79a-326">Run ER formats</span></span>

1. <span data-ttu-id="9e79a-327">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="9e79a-328">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="9e79a-329">Veldu **Keyra** á efsta borðanum.</span><span class="sxs-lookup"><span data-stu-id="9e79a-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="9e79a-330">Vistaðu úttakið á staðnum.</span><span class="sxs-lookup"><span data-stu-id="9e79a-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="9e79a-331">Veldu liðinn **Snið til að læra færibreytur á köll (sérsniðin)**.</span><span class="sxs-lookup"><span data-stu-id="9e79a-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="9e79a-332">Veldu **Keyra** á efsta borðanum.</span><span class="sxs-lookup"><span data-stu-id="9e79a-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="9e79a-333">Vistaðu úttakið á staðnum.</span><span class="sxs-lookup"><span data-stu-id="9e79a-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="9e79a-334">Berðu saman innihald í mynduðu úttaki.</span><span class="sxs-lookup"><span data-stu-id="9e79a-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e79a-335">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9e79a-335">Additional resources</span></span>
[<span data-ttu-id="9e79a-336">Formúluhönnuður í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="9e79a-336">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
