---
title: Notaðu JOIN gagnaheimildir í ER-líkanavörpun til að fá gögn úr mörgum töflum forrita
description: Þetta efnisatriði útskýrir hvernig hægt er að nota gagnagjafa af JOIN-gerð í rafrænni skýrslugerð (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667955"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a><span data-ttu-id="3881e-103">Notaðu JOIN gagnaheimildir til að fá gögn úr mörgum forritatöflum í líkanavörpun í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="3881e-103">Use JOIN data sources to get data from multiple application tables in Electronic reporting (ER) model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3881e-104">Við stillingu á líkanavörpun eða sniðmáta rafrænnar skýrslugerðar (ER) er hægt að [bæta við](#review) áskilins gagnagjafa af gerðinni **Join**.</span><span class="sxs-lookup"><span data-stu-id="3881e-104">While configuring Electronic reporting (ER) model mappings or formats, you can [add](#review) required data sources of the **Join** type.</span></span> <span data-ttu-id="3881e-105">Á hönnunartíma er gagnagjafi **Join** stilltur sem mengi nokkurra gagnagjafa, sem hver og einn skila lista yfir færslur.</span><span class="sxs-lookup"><span data-stu-id="3881e-105">At design time, a **Join** data source is configured as a set of several data sources each of which returns a list of records.</span></span> <span data-ttu-id="3881e-106">Fyrir hverja gagnagjafa nema þann fyrsta þarftu að skilgreina nauðsynleg skilyrði til að sameina skrár yfir núverandi og fyrri gagnaheimildir.</span><span class="sxs-lookup"><span data-stu-id="3881e-106">For every data source except the first one, you need to define necessary conditions to join records of the current and previous data sources.</span></span> <span data-ttu-id="3881e-107">Gagnagjafi af gerðinni **Join** [skilar](#executeERformat) einum sameinuðum lista yfir skrár sem innihalda reiti úr skrám með ívöfðum gagnagjöfum á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="3881e-107">At runtime, a configured data source of **Join** type [returns](#executeERformat) a single joined list of records containing fields from the records of nested data sources.</span></span>

<span data-ttu-id="3881e-108">Eftirfarandi gerðir af samtengingum eru studdar eins og er:</span><span class="sxs-lookup"><span data-stu-id="3881e-108">The following type of joins are currently supported:</span></span>

- <span data-ttu-id="3881e-109">Ytri (vinstri) samtenging:</span><span class="sxs-lookup"><span data-stu-id="3881e-109">Outer (left) join:</span></span>
    - <span data-ttu-id="3881e-110">Sameinaðu allar skrár fyrsta (vinstra) gagnagjafans og síðan allar samsvarandi í samræmi við stilltar skilyrðaskrár í síðari (hægri) gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="3881e-110">Join all records of the first (left-most) data source and then any matching in accordance to configured conditions records of the second (right-most) data source.</span></span>
- <span data-ttu-id="3881e-111">Innri (hægri) samtenging:</span><span class="sxs-lookup"><span data-stu-id="3881e-111">Inner (right) join:</span></span>
    - <span data-ttu-id="3881e-112">Sameinaðu aðeins skrár fyrsta (vinstra) gagnagjafans og aðeins skrár í síðari (hægri) gagnagjafanum sem eru samsvarandi í samræmi við stillt skilyrði.</span><span class="sxs-lookup"><span data-stu-id="3881e-112">Join only records of the first (left-most) data source and only records of the second (right-most) data source matching to each other in accordance to configured conditions.</span></span>

<span data-ttu-id="3881e-113">Í stillta gagnagjafanum **Join**, þegar allir gagnagjafar eru af gerðinni **Töflufærslur**, getur framkvæmd á Join-gagnagjafanum verið [framkvæmd á gagnagrunnsstigi](#analyze) að nota eina SQL-skipun.</span><span class="sxs-lookup"><span data-stu-id="3881e-113">In the configured **Join** data source, when all data sources are the **Table records** type, execution of the Join data source can be [performed at the database level](#analyze) using a single SQL statement.</span></span> <span data-ttu-id="3881e-114">Þetta dregur úr fjölda gagnagrunnskalla, sem bætir árangur líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="3881e-114">This reduces the number of database calls, which improves model mapping performance.</span></span> <span data-ttu-id="3881e-115">Annars er framkvæmd á **Join** gagnagjafa framkvæmd í minni.</span><span class="sxs-lookup"><span data-stu-id="3881e-115">Otherwise, execution of **Join data** source is performed in memory.</span></span>

> [!NOTE]
> <span data-ttu-id="3881e-116">Notkun á virkninni **VALUEIN** í ER-segðum sem tilgreina skilyrði fyrir sameiningu á skrám í gagnagjöfum af gerðinni Join er ekki enn studd.</span><span class="sxs-lookup"><span data-stu-id="3881e-116">Using the **VALUEIN** function in ER expressions that specify conditions for joining records in data sources of Join type is not supported yet.</span></span> <span data-ttu-id="3881e-117">Farið á síðuna [Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md) til að fá frekari upplýsingar um þessa virkni.</span><span class="sxs-lookup"><span data-stu-id="3881e-117">Visit the [Formula designer in Electronic reporting](general-electronic-reporting-formula-designer.md) page for more details about this function.</span></span>

<span data-ttu-id="3881e-118">Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka dæminu í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="3881e-118">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="example-use-join-data-sources-in-er-model-mappings"></a><span data-ttu-id="3881e-119">Dæmi: Notaðu JOIN gagnagjafa í ER-líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="3881e-119">Example: Use JOIN data sources in ER model mappings</span></span>

<span data-ttu-id="3881e-120">Eftirfarandi skref útskýra hvernig kerfisstjóri eða þróunaraðili rafrænnar skýrslugerðar getur stillt líkanavörpun rafrænnar skýrslugerðar (ER) til að sækja gögn úr mörgum forritatöflum í einu með því að nota gagnagjafa af gerðinni **Join** til að bæta afköst gagnaaðgangs.</span><span class="sxs-lookup"><span data-stu-id="3881e-120">The following steps explain how the System administrator or Electronic reporting developer can configure an Electronic reporting (ER) model mapping to get data from multiple application tables at once by using data sources of the **Join** type to improve data access performance.</span></span> <span data-ttu-id="3881e-121">Hægt er að framkvæma þessi skref fyrir eitthvert fyrirtæki Dynamics 365 Finance eða Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="3881e-121">These steps can be performed for any company of Dynamics 365 Finance or Regulatory Configuration Services (RCS).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3881e-122">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="3881e-122">Prerequisites</span></span>

<span data-ttu-id="3881e-123">Til að ljúka dæmunum í þessu efni verður þú að hafa aðgang að einu af eftirtöldu eftir því hvaða þjónusta er notuð til að ljúka þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="3881e-123">To complete the examples in this topic, you must have access to one of the following depending on what service is used to compete these steps:</span></span>

<span data-ttu-id="3881e-124">**Aðgangur að Finance fyrir eitt af eftirfarandi hlutverkum:**</span><span class="sxs-lookup"><span data-stu-id="3881e-124">**Access to Finance for one of the following roles:**</span></span>

- <span data-ttu-id="3881e-125">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="3881e-125">Electronic reporting developer</span></span>
- <span data-ttu-id="3881e-126">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="3881e-126">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="3881e-127">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="3881e-127">System administrator</span></span>

<span data-ttu-id="3881e-128">**Aðgangi RCS fyrir eitt af eftirfarandi hlutverkum:**</span><span class="sxs-lookup"><span data-stu-id="3881e-128">**Access to RCS for one of the following roles:**</span></span>

- <span data-ttu-id="3881e-129">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="3881e-129">Electronic reporting developer</span></span>
- <span data-ttu-id="3881e-130">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="3881e-130">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="3881e-131">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="3881e-131">System administrator</span></span>

<span data-ttu-id="3881e-132">Einnig verður fyrst að ljúka við skrefin í ferlinu [Stofna skilgreiningarveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3881e-132">You also must first complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

<span data-ttu-id="3881e-133">Fyrirfram verður þú einnig að sækja úr [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) og vista staðbundið eftirfarandi sýnishorn af ER-stillingarskrám:</span><span class="sxs-lookup"><span data-stu-id="3881e-133">In advance, you must also download from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) and save locally the following sample ER configuration files:</span></span>

| <span data-ttu-id="3881e-134">**Lýsing á efni**</span><span class="sxs-lookup"><span data-stu-id="3881e-134">**Content description**</span></span>  | <span data-ttu-id="3881e-135">**Skrárnafn**</span><span class="sxs-lookup"><span data-stu-id="3881e-135">**File name**</span></span>   |
|--------------------------|-----------------|
| <span data-ttu-id="3881e-136">Sýnishorn af stillingaskránni **ER-gagnalíkan** sem er notuð sem gagnagjafi fyrir dæmin.</span><span class="sxs-lookup"><span data-stu-id="3881e-136">Sample **ER data model** configuration file, which is used as the data source for the examples.</span></span>| [<span data-ttu-id="3881e-137">Model to learn JOIN data sources.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="3881e-137">Model to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="3881e-138">Sýnishorn af stillingaskránni **ER-líkanavörpun** sem innleiðir ER-gagnalíkanið fyrir dæmin.</span><span class="sxs-lookup"><span data-stu-id="3881e-138">Sample **ER model mapping** configuration file, which implements the ER data model for the examples.</span></span> | [<span data-ttu-id="3881e-139">Vörpun til að læra JOIN gagnagjafa.útgáfu.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="3881e-139">Mapping to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="3881e-140">Sýnishorn af stillingaskrá **ER-sniðs**.</span><span class="sxs-lookup"><span data-stu-id="3881e-140">Sample **ER format** configuration file.</span></span> <span data-ttu-id="3881e-141">Þessi skrá lýsir gögnum til að fylla út ER-sniðsíhlut fyrir dæmin.</span><span class="sxs-lookup"><span data-stu-id="3881e-141">This file describes the data to populate the ER format component for the examples.</span></span> | [<span data-ttu-id="3881e-142">Sniðmát til að læra JOIN gagnagjafa.útgáfu.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="3881e-142">Format to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="3881e-143">Kveikja á stillingaveitu</span><span class="sxs-lookup"><span data-stu-id="3881e-143">Activate a configurations provider</span></span>

1. <span data-ttu-id="3881e-144">Fáðu aðgang að annaðhvort Finance eða RCS í fyrstu lotu vafrans.</span><span class="sxs-lookup"><span data-stu-id="3881e-144">Access either Finance or RCS in the first session of your web browser.</span></span>
2. <span data-ttu-id="3881e-145">Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="3881e-145">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
3. <span data-ttu-id="3881e-146">Á síðunni **Skilgreiningar staðsetningar**, í kaflanum **Skilgreiningaveitur** skaltu passa að skilgreiningaveitan fyrir sýnifyrirtækið Litware, Inc. (http://www.litware.com) sé skráð og að það sé merkt sem **Virkt**.</span><span class="sxs-lookup"><span data-stu-id="3881e-146">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the configuration provider for the Litware, Inc. (http://www.litware.com) sample company is listed, and that it's marked as **Active**.</span></span> <span data-ttu-id="3881e-147">Ef þú sérð skilgreiningarveituna ekki skaltu fylgja skrefunum í ferlinu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3881e-147">If you don't see this configuration provider, follow the steps in [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

    ![Vinnusvæði rafrænnar skýrslugerðar](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a><span data-ttu-id="3881e-149">Flytja inn sýnishorn af ER-stillingaskrám</span><span class="sxs-lookup"><span data-stu-id="3881e-149">Import sample ER configuration files</span></span>

1. <span data-ttu-id="3881e-150">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-150">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="3881e-151">Flytja inn stillingarskrá ER-gagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="3881e-151">Import the ER data model configuration file.</span></span>
    1. <span data-ttu-id="3881e-152">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-152">Select **Exchange**.</span></span>
    2. <span data-ttu-id="3881e-153">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="3881e-153">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="3881e-154">Veldu **Fletta** til að finna skjalið **Model to learn JOIN data sources.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="3881e-154">Select **Browse** to find the **Model to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="3881e-155">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-155">Select **OK**.</span></span>
3. <span data-ttu-id="3881e-156">Flytja inn stillingarskrá ER-líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="3881e-156">Import the ER model mapping configuration file.</span></span>
    1. <span data-ttu-id="3881e-157">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-157">Select **Exchange**.</span></span>
    2. <span data-ttu-id="3881e-158">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="3881e-158">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="3881e-159">Veldu **Fletta** til að finna skjalið **Mapping to learn JOIN data sources.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="3881e-159">Select **Browse** to find the **Mapping to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="3881e-160">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-160">Select **OK**.</span></span>
4.  <span data-ttu-id="3881e-161">Flytja inn skilgreiningarskrá ER-sniðs.</span><span class="sxs-lookup"><span data-stu-id="3881e-161">Import the ER format configuration file.</span></span>
    1. <span data-ttu-id="3881e-162">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-162">Select **Exchange**.</span></span>
    2. <span data-ttu-id="3881e-163">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="3881e-163">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="3881e-164">Veldu **Fletta** til að finna skjalið **Format to learn JOIN data sources.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="3881e-164">Select **Browse** to find the **Format to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="3881e-165">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-165">Select **OK**.</span></span>
5.  <span data-ttu-id="3881e-166">Í skilgreiningatrénu skaltu stækka liðinn **Model to learn JOIN data sources** ásamt öðrum líkanaliðum (þegar þeir eru í boði).</span><span class="sxs-lookup"><span data-stu-id="3881e-166">In the configurations tree, expand the **Model to learn JOIN data sources** item as well as other model items (when available).</span></span>
6.  <span data-ttu-id="3881e-167">Fylgstu með lista yfir ER stillingar í trénu ásamt upplýsingum um útgáfu á flýtiflipanum **Útgáfur** - þeir verða notaðir sem gagnagjafi fyrir skýrslusýnishornið.</span><span class="sxs-lookup"><span data-stu-id="3881e-167">Observe the list of ER configurations in the tree as well as version details on the **Versions** fast tab – they will be used as the source of data for your sample report.</span></span>

    ![Síðan Skilgreiningar rafrænnar skýrslugerðar](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a><span data-ttu-id="3881e-169">Kveiktu á rakningarvalkostum framkvæmdar</span><span class="sxs-lookup"><span data-stu-id="3881e-169">Turn on execution trace options</span></span>
1.  <span data-ttu-id="3881e-170">Veldu **CONFIGURATIONS**.</span><span class="sxs-lookup"><span data-stu-id="3881e-170">Select **CONFIGURATIONS**.</span></span>
2.  <span data-ttu-id="3881e-171">Veldu **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="3881e-171">Select **User parameters**.</span></span>
3.  <span data-ttu-id="3881e-172">Stilltu rakningarfæribreytur framkvæmdar eins og sýnt er á skjámyndinni hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="3881e-172">Set execution trace parameters as shown on the screenshot below.</span></span>

    ![Síðan Færibreytur notanda rafrænnar skýrslugerðar](./media/GER-JoinDS-Parameters.PNG)

    <span data-ttu-id="3881e-174">Þegar kveikt er á þessum færibreytum verður framkvæmdarmerki myndað fyrir hverja framkvæmd á innfluttri skrá ER-sniðs.</span><span class="sxs-lookup"><span data-stu-id="3881e-174">With these parameters turned on, for every execution of the imported ER format file, the execution trace will be generated.</span></span> <span data-ttu-id="3881e-175">Með því að nota upplýsingar um myndað framkvæmdamerki er hægt að greina framkvæmd á vörpunaríhlutum ER-sniðs og ER-líkans.</span><span class="sxs-lookup"><span data-stu-id="3881e-175">Using details of generated execution trace, you can analyze the execution of ER format and ER model mapping components.</span></span> <span data-ttu-id="3881e-176">Farðu á síðuna [Rekja framkvæmd á ER-sniði til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md) til að fá frekari upplýsingar um eiginleika ER-framkvæmdamerkis.</span><span class="sxs-lookup"><span data-stu-id="3881e-176">Visit the [Trace execution of ER format to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md) page for more details about ER execution trace feature.</span></span>

### <a name="review-er-model-mapping-part-1"></a><span data-ttu-id="3881e-177">Skoðaðu vörpun ER-líkans (hluti 1)</span><span class="sxs-lookup"><span data-stu-id="3881e-177">Review ER model mapping (part 1)</span></span>

<span data-ttu-id="3881e-178">Skoðaðu stillingar á vörpunaríhluta ER-líkansins.</span><span class="sxs-lookup"><span data-stu-id="3881e-178">Review settings of the ER model mapping component.</span></span> <span data-ttu-id="3881e-179">Íhluturinn er stilltur til að fá aðgang að upplýsingum um útgáfur af ER-stillingum, upplýsingum um stillingar og stillingarveitendur án þess að nota heimildir um gerð **Join**.</span><span class="sxs-lookup"><span data-stu-id="3881e-179">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers without using data sources of the **Join** type.</span></span>

1.  <span data-ttu-id="3881e-180">Veldu skilgrieninguna **Mapping to learn JOIN data sources**.</span><span class="sxs-lookup"><span data-stu-id="3881e-180">Select **Mapping to learn JOIN data sources** configuration.</span></span>
2.  <span data-ttu-id="3881e-181">Veldu **Hönnuður** til að opna lista yfir varpanir.</span><span class="sxs-lookup"><span data-stu-id="3881e-181">Select **Designer** to open the list of mappings.</span></span>
3.  <span data-ttu-id="3881e-182">Veldu **Hönnuður** til að fara yfir upplýsingar um varpanir.</span><span class="sxs-lookup"><span data-stu-id="3881e-182">Select **Designer** to review the mapping details.</span></span> 
4.  <span data-ttu-id="3881e-183">Veljið **Sýna upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-183">Select **Show details**.</span></span>
5.  <span data-ttu-id="3881e-184">Í skilgreiningatrénu stækkarðu gagnalíkansliðina **Set1** og **Set1.Details**:</span><span class="sxs-lookup"><span data-stu-id="3881e-184">In the configurations tree, expand the **Set1** and **Set1.Details** data model items:</span></span>

    1. <span data-ttu-id="3881e-185">Bindandi **Upplýsingar: Skráalisti = Útgáfur** gefur til kynna að liðurinn **Set1.Details** vera bundinn við gagnagjafann **Útgáfur** sem skilar gögnum um töfluna **ERSolutionVersionTable**.</span><span class="sxs-lookup"><span data-stu-id="3881e-185">Binding **Details: Record list = Versions** indicates that the **Set1.Details** item is bound to the **Versions** data source returning records of the **ERSolutionVersionTable** table.</span></span> <span data-ttu-id="3881e-186">Hver skrá í þessari töflu táknar eina útgáfu af ER-stillingum.</span><span class="sxs-lookup"><span data-stu-id="3881e-186">Each record of this table represents a single version of an ER configuration.</span></span> <span data-ttu-id="3881e-187">Innihald þessarar töflu er kynnt í flýtiflipanum **Útgáfur** á síðunni **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-187">The content of this table is presented in the **Versions** fast tab on the **Configurations** page.</span></span>
    2. <span data-ttu-id="3881e-188">Bindandi **ConfigurationVersion: String = @. PublicVersionNumber** þýðir að gildi opinberu útgáfunnar af útgáfu hverrar ER-stillingar er tekið úr reitnum **PublicVersionNumber** í töflunni **ERSolutionVersionTable** og komið fyrir í liðnum **ConfigurationVersion**.</span><span class="sxs-lookup"><span data-stu-id="3881e-188">Binding **ConfigurationVersion: String = @.PublicVersionNumber** means that the value of the public version of each ER configuration’s version is taken from the **PublicVersionNumber** field of the **ERSolutionVersionTable** table and placed to the **ConfigurationVersion** item.</span></span>
    3. <span data-ttu-id="3881e-189">Bindandi **ConfigurationTitle: String = @.'>Relations'.Solution.Name** gefur til kynna að nafn ER-stillingar sé tekið úr reitnum **Heiti** í töflunni **ERSolutionTable** sem metur með því að nota mörg-við-ein tengslin (**'>Relations'**) á milli taflanna **ERSolutionVersionTable** og **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="3881e-189">Binding **ConfigurationTitle: String = @.'>Relations'.Solution.Name** indicates that the name of an ER configuration is taken from the **Name** field of the **ERSolutionTable** table assessing by using the many-to-one relation (**'>Relations'**) between the **ERSolutionVersionTable** and **ERSolutionTable** tables.</span></span> <span data-ttu-id="3881e-190">Heiti ER-stillinga núverandi forritstilviks eru sett fram í stillingatrénu á síðunni **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-190">Names of ER configurations of the current application instance are presented in the configurations tree on the **Configurations** page.</span></span>
    4. <span data-ttu-id="3881e-191">Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** þýðir að heiti skilgreiningaveitunnar sem á núverandi skilgreining er tekið úr reitnum **Heiti** í töflunni **ERVendorTable** sem metur með því að nota mörg-við-ein tengsl á milli taflanna **ERSolutionTable** og **ERVendorTable**.</span><span class="sxs-lookup"><span data-stu-id="3881e-191">Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** means that the name of the configuration provider that owns the current configuration is taken from the **Name** field of the **ERVendorTable** table assessing by using the many-to-one relation between **ERSolutionTable** and **ERVendorTable** tables.</span></span> <span data-ttu-id="3881e-192">Heiti ER-skilgreiningaveita eru sett fram í stillingatrénu á síðunni **Skilgreiningar** í síðuhaus hverrar skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="3881e-192">Names of ER configuration providers are presented in the configurations tree on the **Configurations** page on the page header for each configuration.</span></span> <span data-ttu-id="3881e-193">Finna má allan listann yfir veitendur ER-stillinga á töflusíðunni **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Veitandi skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-193">The entire list of ER configuration providers can be found on the **Organization administration \> Electronic reporting \> Configuration provider** table page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/GER-JoinDS-Set1Review.PNG)

6.  <span data-ttu-id="3881e-195">Í skilgreiningartrénu stækkarðu gagnalíkansliðinn **Set1.Summary**:</span><span class="sxs-lookup"><span data-stu-id="3881e-195">In the configurations tree, expand the **Set1.Summary** data model item:</span></span>

    1. <span data-ttu-id="3881e-196">Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** gefur til kynna að liðurinn **Set1.Summary.VersionsNumber** sé bundinn uppsöfnunarreitnum **VersionsNumber** í gagnagjafanum **VersionsSummary** af gerðinni **GroupBy** sem var skilgreindur til að skila fjölda skráa í töflunni **ERSolutionVersionTable** í gegnum gagnagjafann **Versions**.</span><span class="sxs-lookup"><span data-stu-id="3881e-196">Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** indicates that the **Set1.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **VersionsSummary** data source of the **GroupBy** type that was configured to return the number of records of the **ERSolutionVersionTable** table via the **Versions** data source.</span></span>

    ![GROUPBY færibreytusíða gagnagjafa](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  <span data-ttu-id="3881e-198">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3881e-198">Close the page.</span></span>

### <a name="review"></a><span data-ttu-id="3881e-199">Skoðaðu vörpun ER-líkans (hluti 2)</span><span class="sxs-lookup"><span data-stu-id="3881e-199">Review ER model mapping (part 2)</span></span>

<span data-ttu-id="3881e-200">Skoðaðu stillingar á vörpunaríhluta ER-líkansins.</span><span class="sxs-lookup"><span data-stu-id="3881e-200">Review settings of the ER model mapping component.</span></span> <span data-ttu-id="3881e-201">Íhluturinn er stilltur til að fá aðgang að upplýsingum um útgáfur af ER-stillingum, upplýsingum um stillingar og stillingarveitendur með notkun á gagnagjafa af gerðinni **Join**.</span><span class="sxs-lookup"><span data-stu-id="3881e-201">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers with using a data source of the **Join** type.</span></span>

1.  <span data-ttu-id="3881e-202">Í skilgreiningatrénu stækkarðu gagnalíkansliðina **Set2** og **Set2.Details**.</span><span class="sxs-lookup"><span data-stu-id="3881e-202">In the configurations tree, expand the **Set2** and **Set2.Details** data model items.</span></span> <span data-ttu-id="3881e-203">Athugaðu að bindandi **Details: Record list = Details** gefur til kynna að liðurinn **Set2.Details** er bundinn við gagnagjafann **Upplýsingar** sem er skilgreindur sem gagnagjafi af gerðinni **Join**.</span><span class="sxs-lookup"><span data-stu-id="3881e-203">Note that the binding **Details: Record list = Details** indicates that the **Set2.Details** item is bound to the **Details** data source configured as the data source of the **Join** type.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/GER-JoinDS-Set2Review.PNG)

    <span data-ttu-id="3881e-205">Hægt er að bæta gagnagjafanum **Join** við gagnaheimild með því að velja gagnagjafann **Aðgerðir\Join**:</span><span class="sxs-lookup"><span data-stu-id="3881e-205">The **Join** data source can be added by selecting the **Functions\Join** data source:</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/GER-JoinDS-AddJoinDS.PNG)

2.  <span data-ttu-id="3881e-207">Veldu gagnagjafann **Upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-207">Select **Detail**s data source.</span></span>
3.  <span data-ttu-id="3881e-208">Veldu **Breyta** í glugganum **Gagnagjafar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-208">Select **Edit** in the **Data sources** pane.</span></span>
4.  <span data-ttu-id="3881e-209">Veldu **Breyta join**.</span><span class="sxs-lookup"><span data-stu-id="3881e-209">Select **Edit join**.</span></span>
5.  <span data-ttu-id="3881e-210">Veljið **Sýna upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-210">Select **Show details**.</span></span>

    ![JOIN færibreytusíða gagnagjafa](./media/GER-JoinDS-JoinDSEditor.PNG)

    <span data-ttu-id="3881e-212">Þessi síða er notuð til að hanna áskildan gagnagjafa **Gerð Join**.</span><span class="sxs-lookup"><span data-stu-id="3881e-212">This page is used to design the required data source of the **Join type**.</span></span> <span data-ttu-id="3881e-213">Á keyrslutíma mun þessi gagnagjafi stofna einn sameinaðan lista yfir skrár úr gagnagjöfum í hnitanetinu **Sameinaður listi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-213">At runtime, this data source will create a single joined list of records from the data sources in the **Joined list** grid.</span></span> <span data-ttu-id="3881e-214">Sameining skráa hefst úr gagnagjafanum **ConfigurationProviders** sem er í hnitanetinu sem fyrsta (dálkurinn **Gerð** er auður fyrir það).</span><span class="sxs-lookup"><span data-stu-id="3881e-214">Join of records will start from the **ConfigurationProviders** data source that is in the grid as a first one (the **Type** column is blank for it).</span></span> <span data-ttu-id="3881e-215">Skrár yfir alla aðra gagnagjafa verða sameinaðar í kjölfarið við skrár í yfirgagnagjafa miðað við röð þeirra í þessu hnitaneti.</span><span class="sxs-lookup"><span data-stu-id="3881e-215">Records of every other data source will be joined consequently to records of the parent data source based on its order in this grid.</span></span> <span data-ttu-id="3881e-216">Sérhver sameiningargagnagjafi verður að vera stilltur sem gagnagjafi sem eru ívafinn undir gagnagjafa (gagnagjafinn **1Versions** er ívafinn undir **1Configurations**; gagnagjafinn **1Configurations** er ívafinn undir **ConfigurationProviders**).</span><span class="sxs-lookup"><span data-stu-id="3881e-216">Every joining data source must be configured as a data source nested under a target data source (**1Versions** data source is nested under **1Configurations** one; **1Configurations** data source is nested under **ConfigurationProviders** one).</span></span> <span data-ttu-id="3881e-217">Hver stilltur gagnagjafi verður að innihalda skilyrði fyrir sameininguna.</span><span class="sxs-lookup"><span data-stu-id="3881e-217">Each configured data source must contain the conditions for the join.</span></span> <span data-ttu-id="3881e-218">Í gagnagjafanum fyrir þetta tiltekna **Join** eru eftirfarandi sameiningar skilgreindar:</span><span class="sxs-lookup"><span data-stu-id="3881e-218">In the data source for this particular **Join**, the following joins are defined:</span></span>

    - <span data-ttu-id="3881e-219">Hver skrá í gagnagjafanum **ConfigurationProviders** (vísað til í töflunni **ERVendorTable**) er aðeins sameinuð við skrár í **1Configurations** (vísað til í töflunni **ERSolutionTable**) sem eru með sama gildi í reitunum **SolutionVendor** og **RecId**.</span><span class="sxs-lookup"><span data-stu-id="3881e-219">Each record of the **ConfigurationProviders** data source (referred to the **ERVendorTable** table) is joined with only records of the **1Configurations** one (referred to in the **ERSolutionTable** table) having the same value in the **SolutionVendor** and **RecId** fields.</span></span> <span data-ttu-id="3881e-220">Gerðin **Innra join** er notuð fyrir þessa sameininngu auk eftirfarandi skilyrða fyrir samsvarandi skrár:</span><span class="sxs-lookup"><span data-stu-id="3881e-220">The **Inner join** type is used for this join as well as the following conditions for matching records:</span></span> 

    <span data-ttu-id="3881e-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span><span class="sxs-lookup"><span data-stu-id="3881e-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span></span>

    - <span data-ttu-id="3881e-222">Hver skrá í gagnagjafanum **1Configuration** (vísað til í töflunni **ERSolutionTable**) er sameinuð við einu skrárnar í **1Versions** (vísað til í töflunni **ERSolutionVersionTable**) sem eru með sama gildi í reitunum **Solution** og **RecId**.</span><span class="sxs-lookup"><span data-stu-id="3881e-222">Each record of the **1Configurations** data source (referred to the **ERSolutionTable** table) is joined with the only records of the **1Versions** one (referred to the **ERSolutionVersionTable** table) having the same value in the **Solution** and **RecId** fields.</span></span> <span data-ttu-id="3881e-223">Gerðin **Innra join** er notuð fyrir þessa sameininngu auk eftirfarandi skilyrða fyrir samsvarandi skrár:</span><span class="sxs-lookup"><span data-stu-id="3881e-223">**Inner join** type is used for this join as well as the following conditions for matching records:</span></span>

    <span data-ttu-id="3881e-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span><span class="sxs-lookup"><span data-stu-id="3881e-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span></span>

    - <span data-ttu-id="3881e-225">Valkosturinn **Framkvæma** er stilltur sem **Fyrirspurn** sem þýðir að þessi gagnagjafi verður framkvæmdur á keyrslutíma á gagnagrunnsstigi sem beint SQL-kall.</span><span class="sxs-lookup"><span data-stu-id="3881e-225">**Execute** option is configured as **Query** meaning that this join data source will be executed at runtime on database level as a direct SQL call.</span></span>

    <span data-ttu-id="3881e-226">Athugaðu að til að sameina skrár yfir gagnagjafa sem tákna forritatöflur er hægt að tilgreina sameiningarskilyrði með því að nota önnur pör af reitum en þeim sem lýsa því sem fyrir er í AOT-tengslum milli þessara tafla.</span><span class="sxs-lookup"><span data-stu-id="3881e-226">Note that for joining records of data sources representing application tables, you can specify join conditions by using pairs of fields other than ones that describe existing in AOT relations between these tables.</span></span> <span data-ttu-id="3881e-227">Þessa tegund sameininga er einnig hægt að stilla til að framkvæma á gagnagrunnsstigi.</span><span class="sxs-lookup"><span data-stu-id="3881e-227">This type of join can be configured to execute at the database level as well.</span></span>

6.  <span data-ttu-id="3881e-228">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3881e-228">Close the page.</span></span>
7.  <span data-ttu-id="3881e-229">Veldu **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="3881e-229">Select **Cancel**.</span></span>
8.  <span data-ttu-id="3881e-230">Í skilgreiningartrénu stækkarðu gagnalíkansliðinn **Set2.Summary**:</span><span class="sxs-lookup"><span data-stu-id="3881e-230">In the configurations tree, expand the **Set2.Summary** data model item:</span></span>

    - <span data-ttu-id="3881e-231">Bindandi **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** gefur til kynna að liðurinn **Set2.Summary.VersionsNumber** sé bundinn uppsöfnunarreitnum **VersionsNumber** í gagnagjafanum **DetailsSummary** af gerðinni **GroupBy** sem var skilgreind til að skila fjölda sameinaðra skráa í gagnagjafann **Details** af gerðinni **Join**.</span><span class="sxs-lookup"><span data-stu-id="3881e-231">Binding **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** indicates that the **Set2.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **DetailsSummary** data source of the **GroupBy** type that was configured to return the number of joined records of the **Details** data source of the **Join** type.</span></span>
    - <span data-ttu-id="3881e-232">Athugaðu að staðsetningarvalkosturinn **Framkvæmd** er skilgreindur sem **Fyrirspurn** sem þýðir að þessi gagnagjafi **GroupBy** verður framkvæmdur á keyrslutíma sem beint SQL-kall á gagnastiginu.</span><span class="sxs-lookup"><span data-stu-id="3881e-232">Note that the **Execution** location option is configured as **Query** meaning that this **GroupBy** data source will be executed at runtime as a direct SQL call at the database level.</span></span> <span data-ttu-id="3881e-233">Þetta er hægt vegna þess að grunngagnagjafinn **Upplýsingar** af gerðinni **Join** er skilgreindur sem framkvæmdur á gagnagrunnsstigi.</span><span class="sxs-lookup"><span data-stu-id="3881e-233">This is possible because the base data source **Details** of the **Join** type is configured as executed at the database level.</span></span>

    ![GROUPBY færibreytusíða gagnagjafa](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  <span data-ttu-id="3881e-235">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3881e-235">Close the page.</span></span>
10. <span data-ttu-id="3881e-236">Veldu **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="3881e-236">Select **Cancel**.</span></span>

### <a name="executeERformat"></a> <span data-ttu-id="3881e-237">Framkvæma ER-snið</span><span class="sxs-lookup"><span data-stu-id="3881e-237">Execute ER format</span></span>

1.  <span data-ttu-id="3881e-238">Fáðu aðgang að Finance eða RCS í annarri lotu vafrans þíns með sömu persónuskilríkjum og fyrirtæki og í fyrstu lotunni.</span><span class="sxs-lookup"><span data-stu-id="3881e-238">Access Finance or RCS in the second session of your web browser using same credentials and company as in the first session.</span></span>
2.  <span data-ttu-id="3881e-239">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-239">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="3881e-240">Stækkaðu skilgreininguna **Model to learn JOIN data sources**.</span><span class="sxs-lookup"><span data-stu-id="3881e-240">Expand **Model to learn JOIN data sources** configuration.</span></span>
4.  <span data-ttu-id="3881e-241">Veldu skilgrieninguna **Format to learn JOIN data sources**.</span><span class="sxs-lookup"><span data-stu-id="3881e-241">Select **Format to learn JOIN data sources** configuration.</span></span>
5.  <span data-ttu-id="3881e-242">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="3881e-242">Select **Designer**.</span></span>
6.  <span data-ttu-id="3881e-243">Veljið **Sýna upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-243">Select **Show details**.</span></span>
7.  <span data-ttu-id="3881e-244">Veldu **Vörpun**.</span><span class="sxs-lookup"><span data-stu-id="3881e-244">Select **Mapping**.</span></span>
8.  <span data-ttu-id="3881e-245">Veldu **Stækka/Minnka**.</span><span class="sxs-lookup"><span data-stu-id="3881e-245">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="3881e-246">Athugaðu að þetta snið er hannað til að fylla út myndaða textaskrá með nýrri línu fyrir hverja útgáfu af ER-skilgreiningu (röð **Útgáfa**).</span><span class="sxs-lookup"><span data-stu-id="3881e-246">Note that this format is designed to populate a generated text file with a new line for every version of an ER configuration (**Version** sequence).</span></span> <span data-ttu-id="3881e-247">Hver mynda lína mun innihalda heiti stillingaraðila sem á núverandi stillingu, stillingarheitið og stillingarútgáfuna aðskilin með semíkommu.</span><span class="sxs-lookup"><span data-stu-id="3881e-247">Each generated line will contain the name of a configuration provider owning the current configuration, the configuration name and the configuration version separated by semicolon mark.</span></span> <span data-ttu-id="3881e-248">Lokalínan í myndaðri skrá mun innihalda fjölda uppgötvaðra útgáfa af ER stillingum (**Yfirlit** röð).</span><span class="sxs-lookup"><span data-stu-id="3881e-248">The final line of generated file will contain the number of discovered versions of ER configurations (**Summary** sequence).</span></span>

    ![Síða ER-sniðshönnuðar](./media/GER-JoinDS-FormatReview.PNG)

    <span data-ttu-id="3881e-250">Gagnagjafarnir **Gögn** og **Yfirlit** eru notaðir til að fylla út upplýsingar um stillingarútgáfu á myndaðri skrá:</span><span class="sxs-lookup"><span data-stu-id="3881e-250">The **Data** and **Summary** data sources are used to populate configuration version details to the generated file:</span></span>

    - <span data-ttu-id="3881e-251">Upplýsingar úr gagnalíkaninu **Set1** eru notaðar þegar þú velur gagnagjafann **Nei** fyrir **Val** á keyrslutíma í notandaglugganum þegar ER-snið er notað.</span><span class="sxs-lookup"><span data-stu-id="3881e-251">Information from the **Set1** data model is used when you choose **No** for the **Selector** data source at runtime on the user dialog page when running ER format.</span></span>
    - <span data-ttu-id="3881e-252">Upplýsingar úr gagnalíkaninu **Set2** eru notaðar þegar þú velur gagnagjafann **Já** fyrir **Val** á keyrslutíma í notandaglugganum þegar ER-snið er notað.</span><span class="sxs-lookup"><span data-stu-id="3881e-252">Information from the **Set2** data model is used when you choose **Yes** for the **Selector** data source at runtime on the user dialog page.</span></span>

    ![Síða ER-sniðshönnuðar](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  <span data-ttu-id="3881e-254">Veljið **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="3881e-254">Select **Run**.</span></span>
10. <span data-ttu-id="3881e-255">Veldu í glugganum **Nei** í reitnum **Nota JOIN gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="3881e-255">On the dialog page, select **No** in the **Use JOIN data source** field.</span></span>
11. <span data-ttu-id="3881e-256">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-256">Select **OK**.</span></span>
12. <span data-ttu-id="3881e-257">Fara yfir myndaðar skrá.</span><span class="sxs-lookup"><span data-stu-id="3881e-257">Review generated file.</span></span>

    ![ER notendagluggasíða](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><span data-ttu-id="3881e-259">Greindu framkvæmdarakningu fyrir ER snið</span><span class="sxs-lookup"><span data-stu-id="3881e-259">Analyze ER format execution trace</span></span>

1.  <span data-ttu-id="3881e-260">Í fyrstu lotu af Finance eða RCS velurðu **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="3881e-260">In the first session of Finance or RCS, select **Designer**.</span></span>
2.  <span data-ttu-id="3881e-261">Veldu **Afkastarakningu**.</span><span class="sxs-lookup"><span data-stu-id="3881e-261">Select **Performance trac**e.</span></span>
3.  <span data-ttu-id="3881e-262">Í hnitanetinu **Afkastarakningu** velurðu efstu skrána yfir nýjustu framkvæmdarmerki á ER sniði sem notaði núverandi íhlut líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="3881e-262">In the **Performance trace** grid, select the top-most record of the latest execution trace of an ER format that used the current model mapping component.</span></span>
4.  <span data-ttu-id="3881e-263">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-263">Select **OK**.</span></span>

    <span data-ttu-id="3881e-264">Athugaðu að tölfræði um framkvæmd upplýsir þig um afrit kalla í forritstöflurnar:</span><span class="sxs-lookup"><span data-stu-id="3881e-264">Note that execution statistics informs you about duplicated calls to application tables:</span></span>

    - <span data-ttu-id="3881e-265">**ERSolutionTable** hefur verið kallað eins oft og þú ert með stillingar útgáfu færslur í töflunni **ERSolutionVersionTable**, meðan fjölda slíkra kallana gæti fækkað á tímum til að bæta árangur.</span><span class="sxs-lookup"><span data-stu-id="3881e-265">**ERSolutionTable** has been called as many times as you have configuration version records in the **ERSolutionVersionTable** table, while the number of such calls could be reduced in times for performance improvement.</span></span>
    - <span data-ttu-id="3881e-266">**ERVendorTable** hefur verið kallað tvisvar fyrir hverja skilgreiningarútgáfu skráa sem var uppgötvuð í töflunni **ERSolutionVersionTable**, meðan einnig væri hægt að fækka fjölda slíkra kallana.</span><span class="sxs-lookup"><span data-stu-id="3881e-266">**ERVendorTable** has been called twice for every configuration version record that was discovered in the **ERSolutionVersionTable** table, while the number of such calls could be reduced as well.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/GER-JoinDS-Set1Run2.PNG)

5.  <span data-ttu-id="3881e-268">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3881e-268">Close the page.</span></span>

### <a name="execute-er-format"></a><span data-ttu-id="3881e-269"> Framkvæma ER-snið</span><span class="sxs-lookup"><span data-stu-id="3881e-269">Execute ER format</span></span>

1.  <span data-ttu-id="3881e-270">Skiptu yfir í flipann á vafranum þínum með seinni lotu Finance eða RCS.</span><span class="sxs-lookup"><span data-stu-id="3881e-270">Switch to your web browser tab with the second session of Finance or RCS.</span></span>
2.  <span data-ttu-id="3881e-271">Veljið **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="3881e-271">Select **Run**.</span></span>
3.  <span data-ttu-id="3881e-272">Veldu í glugganum **Já** í reitnum **Nota JOIN gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="3881e-272">On the dialog page, select **Yes** in the **Use JOIN data source** field.</span></span>
4.  <span data-ttu-id="3881e-273">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-273">Select **OK**.</span></span>
5.  <span data-ttu-id="3881e-274">Fara yfir myndaðar skrá.</span><span class="sxs-lookup"><span data-stu-id="3881e-274">Review generated file.</span></span>

    ![ER notendagluggasíða](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> <span data-ttu-id="3881e-276">Greindu framkvæmdarakningu fyrir ER snið</span><span class="sxs-lookup"><span data-stu-id="3881e-276">Analyze ER format execution trace</span></span>

1.  <span data-ttu-id="3881e-277">Í fyrstu lotu af Finance eða RCS velurðu **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="3881e-277">In the first session of Finance or RCS, select **Designer**.</span></span>
2.  <span data-ttu-id="3881e-278">Veldu **Afkastarakningu**.</span><span class="sxs-lookup"><span data-stu-id="3881e-278">Select **Performance trace**.</span></span>
3.  <span data-ttu-id="3881e-279">Í hnitanetinu **Afkastarakningu** velurðu efstu skrána yfir nýjustu framkvæmdarmerki á ER sniði sem notaði núverandi íhlut líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="3881e-279">In the **Performance trace** grid, select top-most record representing the latest execution trace of an ER format that used the current model mapping component.</span></span>
4.  <span data-ttu-id="3881e-280">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3881e-280">Select **OK**.</span></span>

    <span data-ttu-id="3881e-281">Athugaðu að tölfræði um framkvæmd upplýsir þig um eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="3881e-281">Note that execution statistics informs you about the following:</span></span>

    - <span data-ttu-id="3881e-282">Gagnasafn forrita hefur verið kallað einu sinni til að fá skrár úr töflunum **ERVendorTable**, **ERSolutionTable** og **ERSolutionVersionTable** til að fá aðgang að áskildum reitum.</span><span class="sxs-lookup"><span data-stu-id="3881e-282">Application database has been called once to get records from **ERVendorTable**, **ERSolutionTable**, and **ERSolutionVersionTable** tables to access required fields.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/GER-JoinDS-Set2Run2.PNG)

    - <span data-ttu-id="3881e-284">Forritagagnagrunnur hefur verið kallaður einu sinni til að reikna út fjölda stillingarútgáfa með því að nota sameiningar sem voru stilltar í gagnagjafanum **Upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="3881e-284">Application database has been called once to calculate the number of configuration versions by using joins that were configured in the **Details** data source.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a><span data-ttu-id="3881e-286">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3881e-286">Additional resources</span></span>

[<span data-ttu-id="3881e-287">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="3881e-287">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="3881e-288">Rekja framkvæmd á sniði rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum</span><span class="sxs-lookup"><span data-stu-id="3881e-288">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
