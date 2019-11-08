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
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550085"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="9fb88-103">Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað</span><span class="sxs-lookup"><span data-stu-id="9fb88-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fb88-104">Þetta efni útskýrir hvernig þú getur hannað gagnagjafa rafrænnar skýrslugerðar (ER) með því að nota gerðina **Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="9fb88-105">Þessi gagnagjafi getur innihaldið ER-segð sem, þegar hún er keyrð, er hægt að stjórna með gildum færibreytufrumbreytanna sem eru skilgreind í bindingu sem kallar þennan gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="9fb88-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="9fb88-106">Með því að skilgreina köll í færibreytur af slíkum gagnagjöfum er hægt að endurnýta staka gagnagjafa í mörgum bindingum, sem dregur úr heildarfjölda gagnagjafa sem verður að skilgreina í ER-líkanavörpunum eða ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="9fb88-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="9fb88-107">Það einfaldar einnig skilgreinda ER-íhluti, sem dregur úr viðhaldskostnaði og notkunarkostnaði annarra neytenda.</span><span class="sxs-lookup"><span data-stu-id="9fb88-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9fb88-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="9fb88-108">Prerequisites</span></span>
<span data-ttu-id="9fb88-109">Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:</span><span class="sxs-lookup"><span data-stu-id="9fb88-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="9fb88-110">Aðgangur að einu af þessum hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="9fb88-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="9fb88-111">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="9fb88-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="9fb88-112">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9fb88-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="9fb88-113">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="9fb88-113">System administrator</span></span>

- <span data-ttu-id="9fb88-114">Aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance and Operations, fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="9fb88-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="9fb88-115">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="9fb88-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="9fb88-116">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9fb88-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="9fb88-117">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="9fb88-117">System administrator</span></span>

<span data-ttu-id="9fb88-118">Úr [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) sækirðu þjappaða skrána **Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="9fb88-119">Hún inniheldur eftirfarandi ER-skilgreiningar sem verður að draga út og geyma á staðnum.</span><span class="sxs-lookup"><span data-stu-id="9fb88-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="9fb88-120">**Efni**</span><span class="sxs-lookup"><span data-stu-id="9fb88-120">**Content**</span></span>                           | <span data-ttu-id="9fb88-121">**Skrárnafn**</span><span class="sxs-lookup"><span data-stu-id="9fb88-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fb88-122">Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9fb88-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="9fb88-123">Líkan til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="9fb88-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="9fb88-124">Sýnishorn af skilgreiningu lýsigagna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9fb88-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="9fb88-125">Lýsigögn til að læra breytur á calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="9fb88-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="9fb88-126">Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9fb88-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="9fb88-127">Vörpun til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="9fb88-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="9fb88-128">Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9fb88-128">Sample ER format configuration</span></span>        | <span data-ttu-id="9fb88-129">Snimát til að læra breytur á calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="9fb88-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="9fb88-130">Skráðu þig inn á RCS tilvikið</span><span class="sxs-lookup"><span data-stu-id="9fb88-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="9fb88-131">Í þessu dæmi mun notandi stofna skilgreiningu fyrir sýnifyrirtækið Litware, Inc. Í RCS verður fyrst að ljúka skrefum ferlisins [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="9fb88-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="9fb88-132">Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="9fb88-133">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="9fb88-134">Flytja inn sóttar skilgreiningar í RCS í eftirfarandi röð: gagnalíkan, lýsigögn, vörpun líkans, snið.</span><span class="sxs-lookup"><span data-stu-id="9fb88-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="9fb88-135">Ljúktu eftirfarandi skrefum fyrir hverja ER-skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="9fb88-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="9fb88-136">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="9fb88-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="9fb88-137">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="9fb88-138">Veldu **Vafra** og veldu síðan nauðsynlega ER-skilgreiningu á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9fb88-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="9fb88-139">Veljið **Í lagi.**</span><span class="sxs-lookup"><span data-stu-id="9fb88-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="9fb88-140">Farðu yfir fyrirliggjandi ER-lausn</span><span class="sxs-lookup"><span data-stu-id="9fb88-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="9fb88-141">Farðu yfir vörpun líkans</span><span class="sxs-lookup"><span data-stu-id="9fb88-141">Review model mapping</span></span>

1. <span data-ttu-id="9fb88-142">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="9fb88-143">Veldu **Vörpun til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="9fb88-144">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-144">Select **Designer**.</span></span>
4. <span data-ttu-id="9fb88-145">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="9fb88-146">Þessi ER-líkanavörpun er hönnuð til að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="9fb88-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="9fb88-147">Sæktu lista yfir skattakóða (gagnagjafinn **Skattur**) sem er að finna í töflunni   **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="9fb88-148">Sæktu lista yfir skattafærslur (gagnagjafinn **Trans**) sem er að finna í töflunni   **TaxTable**:</span><span class="sxs-lookup"><span data-stu-id="9fb88-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="9fb88-149">Flokka lista yfir sóttar færslur (gagnagjafinn **Gr**) eftir skattakóða.</span><span class="sxs-lookup"><span data-stu-id="9fb88-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="9fb88-150">Reiknaðu fyrir flokkaðar færslur eftirfarandi uppsöfnuð gildi á hvern   skattakóða:</span><span class="sxs-lookup"><span data-stu-id="9fb88-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="9fb88-151">Summa skattstofnsgilda.</span><span class="sxs-lookup"><span data-stu-id="9fb88-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="9fb88-152">Summa skattgilda.</span><span class="sxs-lookup"><span data-stu-id="9fb88-152">Sum of tax values.</span></span>
        - <span data-ttu-id="9fb88-153">Lágmarksgildi beitts skatthlutfalls.</span><span class="sxs-lookup"><span data-stu-id="9fb88-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="9fb88-154">Vörpun líkansins í þessari stillingu útfærir grunngagnalíkanið fyrir hvaða ER-snið sem er búið til fyrir þetta líkan og keyrt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fb88-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="9fb88-155">Fyrir vikið verður innihald gagnafjafanna **Tax** og **Gr** berskjaldað fyrir ER-sniðum eins og óhlutbundnum gagnagjöfum.</span><span class="sxs-lookup"><span data-stu-id="9fb88-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Hönnunarsíða fyrir líkanavörpun sem sýnir gagnagjafana Tax og Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="9fb88-157">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="9fb88-158">Lokið síðunni **Líkanavörpun**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="9fb88-159">Skoðaðu sniðmátið</span><span class="sxs-lookup"><span data-stu-id="9fb88-159">Review format</span></span>

1. <span data-ttu-id="9fb88-160">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="9fb88-161">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="9fb88-162">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-162">Select **Designer**.</span></span> <span data-ttu-id="9fb88-163">Þetta ER-sniðmát er hannað til að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="9fb88-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="9fb88-164">Myndaðu skattauppgjör á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9fb88-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="9fb88-165">Settu fram eftirfarandi stig skattheimtu í skattauppgjöri: reglulega, lækkað og ekkert.</span><span class="sxs-lookup"><span data-stu-id="9fb88-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="9fb88-166">Settu fram margar upplýsingar á hverju skattlagningarstigi, með mismunandi fjölda smáatriða í hverju stigi.</span><span class="sxs-lookup"><span data-stu-id="9fb88-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Síða sniðshönnuðar](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="9fb88-168">Veldu **Vörpun**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="9fb88-169">Stækkaðu liðina **Líkan**, **Gögn,** og **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="9fb88-170">Reiknaði reiturinn **Model.Data.Summary.Level** inniheldur segðina sem skilar kóða skattlagningarstigsins (**Venjulegur**, **Dregið úr**, **Enginn,** eða **Annað**) sem textagildi fyrir hvaða skattakóða sem hægt er að sækja úr gagnagjafanum **Model.Data.Summary** á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="9fb88-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Hönnunarsíðan sniðmáta sem sýnir upplýsingar um gagnalíkanið til að læra færibreytur á köll](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="9fb88-172">Stækkaðu liðinn **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="9fb88-173">Stækkaðu liðinn **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="9fb88-174">Gagnagjafinn **Model**.**Data2.Summary2** er stillt til að flokka færsluupplýsingar gagnagjafans **Model.Data.Summary** skattlagningarstig (skilað af reiknaða reitnum **Model.Data.Summary.Level**) og reikna uppsafnanirnar.</span><span class="sxs-lookup"><span data-stu-id="9fb88-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Hönunnarsíða sniðmáta sem sýnir upplýsingar um gagnagjafann Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="9fb88-176">Farðu yfir reiknaða reiti **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, og **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="9fb88-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="9fb88-177">Þessir reiknaðir reitir eru notaðir til að sía **Model**.**Data2.Summary2** skráningalistann og skila aðeins skrám sem tákna tiltekið skattlagningarstig.</span><span class="sxs-lookup"><span data-stu-id="9fb88-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="9fb88-178">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="9fb88-179">Stofna afleitt sniðmát</span><span class="sxs-lookup"><span data-stu-id="9fb88-179">Create a derived format</span></span>
<span data-ttu-id="9fb88-180">Þú getur bætt sniðið sem fylgir með því að bæta við einum reiknuðum reit til að sía tilskilið skattlagningarstig í stað þess að nota þrjá reiti sem fyrir eru: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** og **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="9fb88-181">Hægt er að tilgreina tilskilt skattlagningarstig á þeim stað þar sem kallað verður á þennan nýja reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="9fb88-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="9fb88-182">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="9fb88-183">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="9fb88-184">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="9fb88-185">Veldu **Sæktu frá nafni: Snið til að læra breytur símtöl, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="9fb88-186">Í reitnum **Heiti** slærðu inn **Sniðmát til að læra færibreytur á köll (sérsnið)**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="9fb88-187">Veljið **Stofna skilgreiningu.**</span><span class="sxs-lookup"><span data-stu-id="9fb88-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="9fb88-188">Stilla stika reiknaðan reit sem skilar lista yfir færslur</span><span class="sxs-lookup"><span data-stu-id="9fb88-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="9fb88-189">Byrjaðu að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9fb88-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="9fb88-190">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-190">Select **Designer**.</span></span>
2. <span data-ttu-id="9fb88-191">Veldu **Stækka/fella saman** til að stækka öll snið atriði.</span><span class="sxs-lookup"><span data-stu-id="9fb88-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="9fb88-192">Veldu **Vörpun**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="9fb88-193">Stækkaðu liðinn **Model**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="9fb88-194">Veldu liðinn **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="9fb88-195">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-195">Select **Add**.</span></span>
7. <span data-ttu-id="9fb88-196">Veldu **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="9fb88-197">Í reitinn **Heiti** skal færa inn **Stig**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="9fb88-198">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="9fb88-199">Skilgreindu færibreytu til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9fb88-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="9fb88-200">Velja **færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="9fb88-201">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-201">Select **New**.</span></span>
3. <span data-ttu-id="9fb88-202">Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="9fb88-203">Í reitnum **Gerð** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="9fb88-204">Aðeins er hægt að nota frumstæðar gagnategundir til að tilgreina gerð frumbreytu færibreytunnar.</span><span class="sxs-lookup"><span data-stu-id="9fb88-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="9fb88-205">Þess vegna er ekki hægt að nota gerðirnar **Skráalista**, **Skrá** og **Enum** í þessu skyni.</span><span class="sxs-lookup"><span data-stu-id="9fb88-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="9fb88-206">Hámarksfjöldi færibreyta sem hægt er að tilgreina fyrir einn reiknaðan reit er 8.</span><span class="sxs-lookup"><span data-stu-id="9fb88-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Upprunalisti færibreyta](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="9fb88-208">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-208">Select **OK**.</span></span>

<span data-ttu-id="9fb88-209">Með því að bæta við þessa færibreytu tilgreinirðu það skilyrði sem verður að vera til staðar til að kalla þennan reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="9fb88-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="9fb88-210">Þegar þú kallar þennan reiknaða reit þarftu að tilgreina rökin fyrir færibreytuna **Skattlagningarstig** sem gildi með sniðinu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="9fb88-211">Gakktu úr skugga um að þú skilgreinir eingöngu færibreytur fyrir þá reiknaðu reiti sem eru í gámi (annaðhvort **Skráalisti**, **Skrá**, eða **Gámur**).</span><span class="sxs-lookup"><span data-stu-id="9fb88-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="9fb88-212">Stilla breytan er fáanleg á lista yfir gagnaveitur fyrir þennan reiknaða reit.</span><span class="sxs-lookup"><span data-stu-id="9fb88-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="9fb88-213">Þú getur bætt við færibreytuna við stillta segð með því að velja **Bættu við gagnaveitu**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Gagnagjafareitir](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="9fb88-215">Skilgreindu segð til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9fb88-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="9fb88-216">Í reitinn **Formúla** skal slá inn:</span><span class="sxs-lookup"><span data-stu-id="9fb88-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="9fb88-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="9fb88-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="9fb88-218">Veldu færibreytuna **Skattlagningarstig** á lista yfir gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="9fb88-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="9fb88-219">Veldu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="9fb88-220">Í reitnum **Formúla** skal ljúka segðinni sem:</span><span class="sxs-lookup"><span data-stu-id="9fb88-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="9fb88-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="9fb88-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="9fb88-222">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-222">Select **Save**.</span></span>

    ![Upplýsingar um reit gagnaveitu](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="9fb88-224">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="9fb88-225">Ljúktu við að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9fb88-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="9fb88-226">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-226">Select **OK**.</span></span>

<span data-ttu-id="9fb88-227">Á síðunni **Sniðmátshönnuður** krefst stillanlegur reiknaður reiturinn **Stig** frumbreytunnar **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Stækkaður listi yfir reiknuð reitastig](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="9fb88-229">Notaðu stilla reiknaða reitinn til að binda sniðþætti</span><span class="sxs-lookup"><span data-stu-id="9fb88-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="9fb88-230">Veldu **Model.Data2.Levels** til að velja stilla reiknaða reitinn.</span><span class="sxs-lookup"><span data-stu-id="9fb88-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="9fb88-231">Veldu sniðmátsþáttinn **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="9fb88-232">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-232">Select **Bind**.</span></span>
4. <span data-ttu-id="9fb88-233">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level1**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum valins sniðareiningar.</span><span class="sxs-lookup"><span data-stu-id="9fb88-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="9fb88-234">Beitt bindandi hefur verið smíðað sem kall á reiknaða reitinn með breytu.</span><span class="sxs-lookup"><span data-stu-id="9fb88-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="9fb88-235">Sjálfgefið er að nafnið á bundnu sniði er notað sem rök fyrir breytu útreiknaðan reit við eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="9fb88-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="9fb88-236">Reiknaður reiturinn er stilltur til að nota eina breytu.</span><span class="sxs-lookup"><span data-stu-id="9fb88-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="9fb88-237">Gagnategund þessa færibreytu er skilgreind sem **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="9fb88-238">Þegar nafn bundins sniðsþátta er tómt er heiti gagnaheimildar þessarar frumefnis notað í beinni bindingu.</span><span class="sxs-lookup"><span data-stu-id="9fb88-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="9fb88-239">Veldu sniðmátsþáttinn **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="9fb88-240">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-240">Select **Bind**.</span></span>
7. <span data-ttu-id="9fb88-241">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level2**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum undir valinni sniðareiningu.</span><span class="sxs-lookup"><span data-stu-id="9fb88-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="9fb88-242">Veldu sniðmátsþáttinn **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="9fb88-243">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-243">Select **Bind**.</span></span>
10. <span data-ttu-id="9fb88-244">Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level3**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum undir valinni sniðareiningu.</span><span class="sxs-lookup"><span data-stu-id="9fb88-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="9fb88-245">Þegar þú tilgreinir færibreytuna á útreiknaða reitinn fyrir XML frumefnið sem táknar skattheimtu (t.d. **Model.Data2.Levels(„Reduced“)** sem textagildi), þú þarft ekki að gera það sama fyrir nestta XML eiginleika - bindingar þeirra erfa sjálfkrafa gildi frumbreytunnar sem er skilgreint á yfirstigi (**Model.Data2.Levels.aggregated.Base**, ekki **Model.Data2.Levels („Minni“).aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="9fb88-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="9fb88-246">Endurtekin köll í reiknaða reiti með færibreytu eru ekki studd.</span><span class="sxs-lookup"><span data-stu-id="9fb88-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="9fb88-247">Þú getur valið **Breyta formúlu**, og breytt beitt-fyrir-vanræksröksemdum á breytubreytta reikna reitnum í valda bindingu.</span><span class="sxs-lookup"><span data-stu-id="9fb88-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="9fb88-248">Ef þess frumbreytu vantar getur það valdið villum á keyrslutíma - notendur eru upplýstir um slíkar aðstæður þegar núverandi snið er staðfest.</span><span class="sxs-lookup"><span data-stu-id="9fb88-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Tilkynning um villuviðvörun](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="9fb88-250">Skilgreindu reiknaðan reit með færibreytu til að skila skrá</span><span class="sxs-lookup"><span data-stu-id="9fb88-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="9fb88-251">Þegar reiknaður reitur með færibreytum skilar skrá þarftu að styðja við bindingu einstakra reita þessarar skráar til að forsníða þætti.</span><span class="sxs-lookup"><span data-stu-id="9fb88-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="9fb88-252">Í slíkum tilvikum verður ekki um yfirbindingu að ræða sem inniheldur gildi frumbreytu til að kalla út reiknaðan reit fyrir breytu - þetta gildi verður að vera skilgreint í bindingu reits einnar skrár.</span><span class="sxs-lookup"><span data-stu-id="9fb88-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="9fb88-253">Byrjaðu að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9fb88-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="9fb88-254">Veldu liðinn **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="9fb88-255">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-255">Select **Add**.</span></span>
3. <span data-ttu-id="9fb88-256">Veldu **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="9fb88-257">Í reitinn **Heiti** skal færa inn **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="9fb88-258">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="9fb88-259">Skilgreindu færibreytu til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9fb88-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="9fb88-260">Velja **færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="9fb88-261">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-261">Select **New**.</span></span>
3. <span data-ttu-id="9fb88-262">Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="9fb88-263">Í reitnum **Gerð** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="9fb88-264">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="9fb88-265">Skilgreindu segð til að bæta við reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9fb88-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="9fb88-266">Í reitnum **Formúla** skal færa inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="9fb88-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="9fb88-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="9fb88-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="9fb88-268">Veldu færibreytuna **Skattlagningarstig**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="9fb88-269">Veldu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="9fb88-270">Í reitnum **Formúla** skaltu bæta við **'Taxation Level'))** við það sem þú slóst inn í skref 1 til að klára segðina til:</span><span class="sxs-lookup"><span data-stu-id="9fb88-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="9fb88-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="9fb88-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="9fb88-272">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-272">Select **Save**.</span></span>
6. <span data-ttu-id="9fb88-273">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="9fb88-274">Ljúktu við að bæta við nýjum reiknuðum reit</span><span class="sxs-lookup"><span data-stu-id="9fb88-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="9fb88-275">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="9fb88-276">Notaðu stilla reiknaða reitinn til að binda sniðþætti</span><span class="sxs-lookup"><span data-stu-id="9fb88-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="9fb88-277">Útvíkkaðu **Model.Data2.LevelRecord** til að velja stilla reiknaða reitinn.</span><span class="sxs-lookup"><span data-stu-id="9fb88-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="9fb88-278">Útvíkkaðu gáminn **Model.Data2.LevelRecord.aggregated** í skilgreindum reiknaðum reit.</span><span class="sxs-lookup"><span data-stu-id="9fb88-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="9fb88-279">Veldu reitinn **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="9fb88-280">Veldu sniðmátsþáttinn **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="9fb88-281">Veldu **Losa**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="9fb88-282">Veldu sniðmátsþáttinn **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="9fb88-283">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-283">Select **Bind**.</span></span>
8. <span data-ttu-id="9fb88-284">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="9fb88-285">Breyta segð í **Model.Data2.LevelRecord(„None“).aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Uppfærð segð](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="9fb88-287">Fjarlægðu reiknaða reiti sem ekki eru notaðir</span><span class="sxs-lookup"><span data-stu-id="9fb88-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="9fb88-288">Veldu **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="9fb88-289">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-289">Select **Delete**.</span></span>
3. <span data-ttu-id="9fb88-290">Veldu **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="9fb88-291">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-291">Select **Delete**.</span></span>
5. <span data-ttu-id="9fb88-292">Veldu **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="9fb88-293">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-293">Select **Delete**.</span></span>
7. <span data-ttu-id="9fb88-294">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9fb88-295">Þú notaðir aftur sama reiknaða reit **Model.Data2.Levels** nokkrum sinnum í sniðbindingum.</span><span class="sxs-lookup"><span data-stu-id="9fb88-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="9fb88-296">Það er miklu auðveldara að nota og viðhalda einum reiknuðum reit í stað þess að gera þetta fyrir marga svipaða reiti.</span><span class="sxs-lookup"><span data-stu-id="9fb88-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="9fb88-297">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="9fb88-298">Fullkláruð leiðrétt útgáfa af afleiddu sniði</span><span class="sxs-lookup"><span data-stu-id="9fb88-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="9fb88-299">Á flýtflipanum **Útgáfur** velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="9fb88-300">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="9fb88-301">Flyttu út fullkláraða útgáfu af afleiddu sniði</span><span class="sxs-lookup"><span data-stu-id="9fb88-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="9fb88-302">Veldu sniðmátið **Snið til að læra færibreytur í köll (sérsniðin)** í stillingartrénu.</span><span class="sxs-lookup"><span data-stu-id="9fb88-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="9fb88-303">Í flýtiflipanum **Útgáfur** velurðu lokna útgáfu 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="9fb88-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="9fb88-304">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="9fb88-305">Veldu **Flytja út sem XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="9fb88-306">Geymdu sótta skilgreiningu á staðnum á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9fb88-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="9fb88-307">Prófa ER-snið</span><span class="sxs-lookup"><span data-stu-id="9fb88-307">Test ER formats</span></span> 
<span data-ttu-id="9fb88-308">Þú getur keyrt upphafsuppbót og endurbætt ER snið til að ganga úr skugga um að skilgreindir útreiknaðir reitir með færibreytur virki rétt.</span><span class="sxs-lookup"><span data-stu-id="9fb88-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="9fb88-309">Flytja inn rafræn skýrslugerð grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="9fb88-309">Import ER configurations</span></span>
<span data-ttu-id="9fb88-310">Þú getur flutt inn yfirfarnar stillingar úr RCS með því að nota ER-geymslu af gerðinni **RCS**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="9fb88-311">Ef þú hefur þegar gengið í gegnum skrefin í efninu, [Flytja inn rafrænar skýrslustillingar frá Regulatory Configuration Services](rcs-download-configurations.md), notaðu stilla ER geymslu til að flytja inn stillingar sem fjallað var um áður í þessu efni til umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="9fb88-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="9fb88-312">Að ð öðrum kosti skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="9fb88-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="9fb88-313">Veldu fyrirtækið **DEMF** og veldu á sjálfgefna yfirlitinu **Rafræn skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="9fb88-314">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="9fb88-315">Flytja inn sóttar skilgreiningar úr Microsoft Download Center í eftirfarandi röð: gagnalíkan, vörpun líkans, snið.</span><span class="sxs-lookup"><span data-stu-id="9fb88-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="9fb88-316">Ljúktu eftirfarandi skrefum fyrir hverja ER-skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="9fb88-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="9fb88-317">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="9fb88-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="9fb88-318">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="9fb88-319">Veldu **Vafra** til að velja nauðsynlega ER-skilgreiningu á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9fb88-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="9fb88-320">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-320">Select **OK**.</span></span>

4. <span data-ttu-id="9fb88-321">Flytja út úr RCS lokið útgáfu 1.1.1 af sniðmátinu **Snið til að læra færibreytur í köll (sérsniðin)**:</span><span class="sxs-lookup"><span data-stu-id="9fb88-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="9fb88-322">Veldu **Gengi.**</span><span class="sxs-lookup"><span data-stu-id="9fb88-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="9fb88-323">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="9fb88-324">Veldu **Fletta** til að velja staðbundið vistaða skrána **Snið til að læra færibreytur á köll (sérsniðin)** á XML sniði.</span><span class="sxs-lookup"><span data-stu-id="9fb88-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="9fb88-325">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="9fb88-326">Keyra ER-snið</span><span class="sxs-lookup"><span data-stu-id="9fb88-326">Run ER formats</span></span>

1. <span data-ttu-id="9fb88-327">Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="9fb88-328">Veldu **Sniðmát til að læra færibreytur á köll**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="9fb88-329">Veldu **Keyra** á efsta borðanum.</span><span class="sxs-lookup"><span data-stu-id="9fb88-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="9fb88-330">Vistaðu úttakið á staðnum.</span><span class="sxs-lookup"><span data-stu-id="9fb88-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="9fb88-331">Veldu liðinn **Snið til að læra færibreytur á köll (sérsniðin)**.</span><span class="sxs-lookup"><span data-stu-id="9fb88-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="9fb88-332">Veldu **Keyra** á efsta borðanum.</span><span class="sxs-lookup"><span data-stu-id="9fb88-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="9fb88-333">Vistaðu úttakið á staðnum.</span><span class="sxs-lookup"><span data-stu-id="9fb88-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="9fb88-334">Berðu saman innihald í mynduðu úttaki.</span><span class="sxs-lookup"><span data-stu-id="9fb88-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fb88-335">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9fb88-335">Additional resources</span></span>
[<span data-ttu-id="9fb88-336">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="9fb88-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
