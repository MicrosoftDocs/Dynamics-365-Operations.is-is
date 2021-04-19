---
title: Bættu frammistöðu rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum með reiknaða reiti með færibreytum
description: Þetta efnisatriði útskýrir hvernig hægt er að auka afköst rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum reiknaðra reita með færibreytum.
author: NickSelin
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 299570d6a94b0f9e7ee7cf490d4c1aeeb86d5716
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749514"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="2497d-103">Bættu frammistöðu rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum með reiknaða reiti með færibreytum</span><span class="sxs-lookup"><span data-stu-id="2497d-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2497d-104">Þetta efnisatriði útskýrir hvernig hægt er að taka [afkastarakningu](trace-execution-er-troubleshoot-perf.md) af sniðum [Rafrænnar skýrslugerðar](general-electronic-reporting.md) sem eru keyrðar og síðan nota upplýsingarnar úr þessum rakningum til að bæta afköst með því að stilla gagnagjafa **Reiknaðra reita** með færibreytum.</span><span class="sxs-lookup"><span data-stu-id="2497d-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="2497d-105">Sem hluti af hönnunarferlinu fyrir skilgreiningar rafrænnar skýrslugerðar til að búa til viðskiptaskjöl, skilgreinir þú aðferðina sem er notuð til að ná í gögn úr forritinu og færa þau inn í úttak sem er myndað.</span><span class="sxs-lookup"><span data-stu-id="2497d-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="2497d-106">Með því að hanna gagnagjafa með færibreytum fyrir rafræna skýrslugerð af gerðinni **Reiknaður reitur**, er hægt að draga úr fjölda gagnagrunnskalla og draga umtalsvert úr tíma og kostnaði sem fer í að safna saman upplýsingum um framkvæmd rafræns skýrslugerðarsniðs.</span><span class="sxs-lookup"><span data-stu-id="2497d-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2497d-107">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="2497d-107">Prerequisites</span></span>

- <span data-ttu-id="2497d-108">Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa aðgang að einu af eftirfarandi [hlutverkum](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="2497d-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="2497d-109">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="2497d-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="2497d-110">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2497d-111">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="2497d-111">System administrator</span></span>

- <span data-ttu-id="2497d-112">Stilla verður fyrirtæki á **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="2497d-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="2497d-113">Fylgja skal leiðbeiningunum í [Viðauka 1](#appendix1) í þessu efnisatriði til að sækja þætti fyrir dæmi um rafræna skýrslugerðarlausna Microsoft sem nauðsynlegir eru til að ljúka dæmunum í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="2497d-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="2497d-114">Fylgja skal leiðbeiningunum í [Viðauka 2](#appendix2) í þessu efnisatriði til að skilgreina lágmarkssafn af færibreytum rafrænnar skýrslugerðar sem er nauðsynlegt til að nota umgjörð rafrænnar skýrslugerðar til að bæta afköstin í dæminu um rafræna skýrslugerðarlausn Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2497d-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="2497d-115">Flytja inn dæmið um rafræna skýrslugerðarlausn</span><span class="sxs-lookup"><span data-stu-id="2497d-115">Import the sample ER solution</span></span>

<span data-ttu-id="2497d-116">Ímyndaðu þér að þú þurfir að hanna rafræna skýrslugerðarlausn til að búa til nýja skýrslu sem sýnir lánardrottnafærslur.</span><span class="sxs-lookup"><span data-stu-id="2497d-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="2497d-117">Eins og er geturðu fundið færslurnar fyrir valinn lánardrottin á síðunni **Lánardrottnafærslur** síðunni (farðu á **Viðskiptaskuldir** \> **Lánardrottnar** \> **Allir lánardrottnar**, veldu lánardrottin og síðan, í aðgerðarúðunni, í flipanum **Lánardrottinn** í **Færslur** hópnum velurðu **Færslur**).</span><span class="sxs-lookup"><span data-stu-id="2497d-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="2497d-118">Hins vegar viltu hafa allar lánardrottnafærslur saman í einu rafrænu skjali á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="2497d-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="2497d-119">Þessi lausn mun samanstanda af nokkrum skilgreiningum rafrænnar skýrslugerðar sem innihalda nauðsynlegt gagnalíkan, líkanavörpun og sniðseiningar.</span><span class="sxs-lookup"><span data-stu-id="2497d-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="2497d-120">Fyrsta skrefið er að flytja inn dæmið um rafræna skýrslugerðarlausn til að búa til skýrslu um lánardrottnafærslu.</span><span class="sxs-lookup"><span data-stu-id="2497d-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="2497d-121">Skráðu þig inn í tilvikið af Microsoft Dynamics 365 Finance sem fyrirtækinu þínu er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="2497d-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="2497d-122">Í þessu efnisatriði býrðu til og breytir skilgreiningum fyrir sýnifyrirtækið **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="2497d-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="2497d-123">Gakktu því úr skugga um að þessari skilgreiningarveitu hafi verið bætt við Finance-tilvikið þitt og verið merkt sem virk.</span><span class="sxs-lookup"><span data-stu-id="2497d-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="2497d-124">Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2497d-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="2497d-125">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="2497d-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="2497d-126">Á síðunni **Skilgreiningar**, skal flytja inn skilgreiningar rafrænnar skýrslugerðar sem voru sóttar sem forkröfur í Finance, í eftirfarandi röð: gagnalíkan, líkanavörpun, snið.</span><span class="sxs-lookup"><span data-stu-id="2497d-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="2497d-127">Fyrir hverja skilgreiningu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2497d-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="2497d-128">Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="2497d-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="2497d-129">Veljið **Vafra** til að velja viðeigandi skrá fyrir skilgreiningu rafrænnar skýrslugerðar á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="2497d-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="2497d-130">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-130">Select **OK**.</span></span>

![Skilgreiningar fluttar inn á síðunni Skilgreiningar](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="2497d-132">Yfirfara dæmi um rafræna skýrslugerðarlausn</span><span class="sxs-lookup"><span data-stu-id="2497d-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="2497d-133">Fara yfir líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="2497d-133">Review the model mapping</span></span>

1. <span data-ttu-id="2497d-134">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal stækka **Líkan aukinna afkasta** og velja **Vörpun aukinna afkasta**.</span><span class="sxs-lookup"><span data-stu-id="2497d-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="2497d-135">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="2497d-136">Á síðunni **Líkanavörpun á gagnagjafa**, á aðgerðasvæðinu, skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="2497d-137">Þessi líkanavörpun rafrænnar skýrslugerðar er hönnuð til að framkvæma eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="2497d-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="2497d-138">Sækja listann yfir lánardrottnafærslur sem eru geymdar í töflunni VendTrans (**Trans** gagnagjafi).</span><span class="sxs-lookup"><span data-stu-id="2497d-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="2497d-139">Fyrir hverja færslu skal sækja úr VendTable-töflunni færslu lánardrottins sem færslan hefur verið bókuð fyrir (**\#Vend** gagnagjafi).</span><span class="sxs-lookup"><span data-stu-id="2497d-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="2497d-140">**\#Vend** gagnagjafinn er stilltur til að sækja samsvarandi lánardrottnafærslu með því að nota fyrirliggjandi tengslin „margar við eina“ **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="2497d-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="2497d-141">Líkanavörpunin í þessari skilgreiningu innleiðir grunngagnalíkanið fyrir eitthvert snið rafrænnar skýrslugerðar sem búið var til fyrir þetta líkan og keyrt í Finance.</span><span class="sxs-lookup"><span data-stu-id="2497d-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="2497d-142">Þess vegna er efnið í gagnagjafanum **Trans** opið fyrir rafrænum skýrslugerðarsniðum á borð við útdrátt af **líkani** gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="2497d-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Trans-gagnagjafi á hönnunarsíðu líkanavörpunar](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="2497d-144">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="2497d-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="2497d-145">Lokið síðunni **Líkanavörpun á gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="2497d-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="2497d-146">Skoðaðu sniðmátið</span><span class="sxs-lookup"><span data-stu-id="2497d-146">Review format</span></span>

1. <span data-ttu-id="2497d-147">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal stækka **Líkan aukinna afkasta** og velja **Snið aukinna afkasta**.</span><span class="sxs-lookup"><span data-stu-id="2497d-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="2497d-148">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="2497d-149">Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, skal velja **Stækka/fella saman**.</span><span class="sxs-lookup"><span data-stu-id="2497d-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="2497d-150">Stækkið **Líkanið**, **Gögnin** og **Færsluna**.</span><span class="sxs-lookup"><span data-stu-id="2497d-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="2497d-151">Þetta snið rafrænnar skýrslugerðar er hannað til að mynda skýrslu um lánardrottnafærslur á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="2497d-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Snið gagnagjafa og skilgreindar bindingar á sniðseiningum á síðu sniðshönnuðar](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="2497d-153">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="2497d-154">Keyra dæmi um lausn rafrænnar skýrslugerðar til að rekja framkvæmd</span><span class="sxs-lookup"><span data-stu-id="2497d-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="2497d-155">Ímyndum okkur að þú hafir lokið við að hanna fyrstu útgáfu af lausn rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="2497d-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="2497d-156">Núna viltu prófa hana í Finance-tilviki og greina afköst keyrslunnar.</span><span class="sxs-lookup"><span data-stu-id="2497d-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="2497d-157">Kveikja á afkastarakningu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="2497d-158">Veldu fyrirtækið **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="2497d-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="2497d-159">Fylgdu leiðbeiningunum í [Kveikja á afkastarakningu rafrænnar skýrslugerðar](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) til að búa til afkastarakningu á meðan snið rafrænnar skýrslugerðar er keyrt.</span><span class="sxs-lookup"><span data-stu-id="2497d-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Svarglugginn Notandafæribreytur](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="2497d-161">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-161">Run the ER format</span></span>

1. <span data-ttu-id="2497d-162">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="2497d-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2497d-163">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið aukinna afkasta**.</span><span class="sxs-lookup"><span data-stu-id="2497d-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="2497d-164">Í aðgerðarúðunni skal velja **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="2497d-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="2497d-165">Nota afkastarakningu til að greina afköst líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="2497d-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="2497d-166">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun aukinna afkasta**.</span><span class="sxs-lookup"><span data-stu-id="2497d-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="2497d-167">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="2497d-168">Á síðunni **Líkanavarpanir**, í aðgerðarúðunni, skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="2497d-169">Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.</span><span class="sxs-lookup"><span data-stu-id="2497d-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="2497d-170">Veljið nýjustu rakninguna sem var mynduð og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="2497d-171">Nýjar upplýsingar eru nú tiltækar fyrir sum atriði gagnagjafa fyrir núverandi líkanavörpun:</span><span class="sxs-lookup"><span data-stu-id="2497d-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="2497d-172">Raunverulegur tími sem fór í að ná í gögn með því að nota gagnagjafann</span><span class="sxs-lookup"><span data-stu-id="2497d-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="2497d-173">Sami tími sýndur sem prósenta af heildartímanum sem fór í að keyra alla líkanavörpunina</span><span class="sxs-lookup"><span data-stu-id="2497d-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Upplýsingar um keyrslutíma á hönnunarsíðu líkanavörpunar](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="2497d-175">Hnitanetið **Tölfræði um afköst** sýnir að gagnagjafinn **Trans** kallar á VendTrans-töfluna einu sinni.</span><span class="sxs-lookup"><span data-stu-id="2497d-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="2497d-176">Gildið **\[265\]\[Q:265\]** af gagnagjafanum **Trans** gefur til kynna að 265 færslur lánardrottins hafi verið sóttar úr forritstöflunni og þeim skilað í gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="2497d-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="2497d-177">Hnitanetið **Tölfræði um afköst** sýnir einnig að núverandi líkanavörpun tvítekur gagnagrunnsbeiðnir á meðan **\#Vend** gagnagjafinn er keyrður.</span><span class="sxs-lookup"><span data-stu-id="2497d-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="2497d-178">Þessi tvítekning gerist af eftirfarandi ástæðum:</span><span class="sxs-lookup"><span data-stu-id="2497d-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="2497d-179">Kallað er á lánardrottnatöfluna tvisvar sinnum fyrir hverja af 265 endurteknu lánardrottnafærslunum, sem gerir samtals 530 köll:</span><span class="sxs-lookup"><span data-stu-id="2497d-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="2497d-180">Eitt kall er gert til að slá inn númer lánardrottnalykilsins.</span><span class="sxs-lookup"><span data-stu-id="2497d-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="2497d-181">Eitt kall er gert til að slá inn lánardrottnaheitið.</span><span class="sxs-lookup"><span data-stu-id="2497d-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="2497d-182">Kallað er á lánardrottnatöfluna fyrir hverja endurtekna lánardrottnafærslu, jafnvel þótt sóttar færslur hafi verið bókaðar fyrir aðeins fimm lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="2497d-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="2497d-183">Af 530 köllum, eru 525 tvítekin.</span><span class="sxs-lookup"><span data-stu-id="2497d-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="2497d-184">Eftirfarandi mynd sýnir skilaboðin sem berast um tvítekin köll (gagnagrunnsbeiðnir).</span><span class="sxs-lookup"><span data-stu-id="2497d-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Skilaboð um tvítekna gagnagrunnsbeiðni á hönnunarsíðu líkanavörpunar](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="2497d-186">Takið eftir að af heildarkeyrslutíma líkanavörpunar (u.þ.b. átta sekúndur) hefur meira en 80% (u.þ.b. sex sekúndum) verið eytt í að sækja gildi úr forritstöflunni VendTable.</span><span class="sxs-lookup"><span data-stu-id="2497d-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="2497d-187">Sú prósenta er of há fyrir tvær eigindir af fimm lánardrottnum, í samanburði við magn upplýsinga úr forritstöflunni VendTrans.</span><span class="sxs-lookup"><span data-stu-id="2497d-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="2497d-188">Til að draga úr fjölda kalla sem gerð eru til að ná í upplýsingar um lánardrottin fyrir hverja færslu, og til að auka afköst líkanavörpunarinnar, er hægt að nota vistun í skyndiminni fyrir gagnagjafann **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="2497d-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="2497d-189">**Trans\\\#Vend** gagnagjafinn verður vistaður í skyndiminni um það sem nemur núverandi færslu af **Trans** gagnagjafanum við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="2497d-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="2497d-190">Með því að sækja **\#Vend** gagnagjafann er dregið úr fjölda tvítekinna kalla úr 525 í 260, en tvítekningum er ekki algjörlega útrýmt.</span><span class="sxs-lookup"><span data-stu-id="2497d-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="2497d-191">Til að útrýma tvítekningum að fullu leyti er hægt að skilgreina nýjan gagnagjafa með færibreytum af gerðinni **Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="2497d-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="2497d-192">Bæta líkanavörpun á grundvelli upplýsinga úr framkvæmdarakningu</span><span class="sxs-lookup"><span data-stu-id="2497d-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="2497d-193">Breyta reiknireglu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="2497d-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="2497d-194">Fylgið þessum skrefum til að nota vistun í skyndiminni og gagnagjafa af gerðinni **Reiknaður reitur** til að hjálpa til við koma í veg fyrir tvítekin köll á gagnagrunn.</span><span class="sxs-lookup"><span data-stu-id="2497d-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="2497d-195">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun aukinna afkasta**.</span><span class="sxs-lookup"><span data-stu-id="2497d-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="2497d-196">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="2497d-197">Á síðunni **Líkanavarpanir**, í aðgerðarúðunni, skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="2497d-198">Á síðunni **Hönnuður líkanavörpunar** skal fylgja þessum skrefum til að bæta við gagnagjafa af gerðinni **Töflufærslur** til að fá aðgang að færslum í forritstöflunni VendTable:</span><span class="sxs-lookup"><span data-stu-id="2497d-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="2497d-199">Í rúðunni **Gerðir gagnagjafa** skal stækka **Dynamics 365 for Operations** og velja **Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="2497d-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="2497d-200">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="2497d-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="2497d-201">Í gluggann, í reitinn **Heiti**, skal slá inn **Vend**.</span><span class="sxs-lookup"><span data-stu-id="2497d-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="2497d-202">Í reitinn **Tafla** skal slá inn **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="2497d-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="2497d-203">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-203">Select **OK**.</span></span>

5. <span data-ttu-id="2497d-204">Hægt er að stilla færibreytur kalla til gagnagjafa af gerðinni **Reiknaður reitur** eingöngu ef þessir gagnagjafar eru í hólfi.</span><span class="sxs-lookup"><span data-stu-id="2497d-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="2497d-205">Þess vegna skal fylgja þessum skrefum til að bæta við gagnagjafa af gerðinni **Tómt hólf** til að geyma nýjum færibreytustilltum gagnagjafa af gerðinni **Reiknaður reitur**:</span><span class="sxs-lookup"><span data-stu-id="2497d-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="2497d-206">Í rúðunni **Gerðir gagnagjafa** skal stækka **Almennt** og velja **Tómt hólf**.</span><span class="sxs-lookup"><span data-stu-id="2497d-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="2497d-207">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="2497d-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="2497d-208">Í gluggann, í reitinn **Heiti**, skal slá inn **Kassi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="2497d-209">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-209">Select **OK**.</span></span>

    ![Gagnagjafi í kassa á hönnunarsíðu líkanavörpunar](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="2497d-211">Fylgið þessum skrefum til að bæta við færibreytustilltum gagnagjafa af gerðinni **Reiknaður reitur**:</span><span class="sxs-lookup"><span data-stu-id="2497d-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="2497d-212">Í rúðunni **Gagnagjafar** skal velja **Kassi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="2497d-213">Í rúðunni **Gerðir gagnagjafa** skal stækka **Virknir** og velja **Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="2497d-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="2497d-214">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="2497d-214">Select **Add**.</span></span>
    4. <span data-ttu-id="2497d-215">Í gluggann, í reitinn **Heiti**, skal slá inn **Vend**.</span><span class="sxs-lookup"><span data-stu-id="2497d-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="2497d-216">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="2497d-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="2497d-217">Á síðunni **Formúluhönnuður** skal velja **Færibreytur** til að tilgreina færibreyturnar sem þarf að útvega þegar kallað er á þennan gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="2497d-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="2497d-218">Í svarglugganum **Færibreytur** skal velja **Ný**.</span><span class="sxs-lookup"><span data-stu-id="2497d-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="2497d-219">Í reitinn **Heiti** skal færa inn **parmVendAccNumber**.</span><span class="sxs-lookup"><span data-stu-id="2497d-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="2497d-220">Í reitnum **Gerð** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="2497d-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="2497d-221">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-221">Select **OK**.</span></span>
    11. <span data-ttu-id="2497d-222">Í reitinn **Formúla** skal færa inn **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="2497d-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="2497d-223">Veljið **Vista** og lokið síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="2497d-224">Veljið **Í lagi** til að bæta við nýja gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="2497d-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="2497d-225">Fylgið þessum skrefum til að merkja viðbættan gagnagjafa sem vistun í skyndiminni við keyrsluna:</span><span class="sxs-lookup"><span data-stu-id="2497d-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="2497d-226">Í rúðunni **Gagnagjafar** skal velja **Kassi\\Vend**.</span><span class="sxs-lookup"><span data-stu-id="2497d-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="2497d-227">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="2497d-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2497d-228">**Kassi\\Vend** gagnagjafinn verður vistaður í skyndiminni um það sem nemur öllum lánardrottnafærslum af **Trans** gagnagjafanum við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="2497d-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="2497d-229">Fylgið eftirfarandi skrefum til að uppfæra faldaðan **Trans\\\#Vend** gagnagjafa svo að hann noti **Kassi\\Vend** gagnagjafann:</span><span class="sxs-lookup"><span data-stu-id="2497d-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="2497d-230">Í rúðunni **Gagnagjafar** skal stækka **Trans**.</span><span class="sxs-lookup"><span data-stu-id="2497d-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="2497d-231">Veljið **Trans\\\#Vend** gagnagjafa og veljið **Breyta** \> **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="2497d-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="2497d-232">Á síðunni **Formúluhönnuður**, í reitinn **Formúla**, skal slá inn **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="2497d-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="2497d-233">Veljið **Vista** og lokið svo síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="2497d-234">Veljið **Í lagi** til að ljúka við breytingar á völdum gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="2497d-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="2497d-235">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="2497d-235">Select **Save**.</span></span>

    ![Vend-gagnagjafi á hönnunarsíðu líkanavörpunar](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="2497d-237">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="2497d-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="2497d-238">Lokið síðunni **Líkanavarpanir**.</span><span class="sxs-lookup"><span data-stu-id="2497d-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="2497d-239">Ljúka við breyttu útgáfuna af líkanavörpun rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="2497d-240">Á síðunni **Skilgreiningar**, í flýtiflipanum **Útgáfur**, skal velja útgáfuna **1.2** af skilgreiningunni **Vörpun aukinna afkasta**.</span><span class="sxs-lookup"><span data-stu-id="2497d-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="2497d-241">Veljið **Breyta stöðu** \> **Ljúka** og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="2497d-242">Keyra breytta lausn rafrænnar skýrslugerðar til að rekja framkvæmd</span><span class="sxs-lookup"><span data-stu-id="2497d-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="2497d-243">Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="2497d-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="2497d-244">Nota afkastarakningu til að greina leiðréttingar á líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="2497d-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="2497d-245">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun aukinna afkasta**.</span><span class="sxs-lookup"><span data-stu-id="2497d-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="2497d-246">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="2497d-247">Á síðunni **Líkanavarpanir**, í aðgerðarúðunni, skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2497d-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="2497d-248">Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.</span><span class="sxs-lookup"><span data-stu-id="2497d-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="2497d-249">Veljið nýjustu rakninguna sem var mynduð og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2497d-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="2497d-250">Takiði eftir að leiðréttingar sem voru gerðar á líkanavörpun hafa eytt tvíteknum fyrirspurnum til gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="2497d-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="2497d-251">Fjöldi kalla í gagnagrunnstöflur og gagnagjafa fyrir þessa líkanavörpun hefur einnig verið fækkað.</span><span class="sxs-lookup"><span data-stu-id="2497d-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Rakningarupplýsingar á hönnunarsíðu líkanavörpunar 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="2497d-253">Heildarkeyrslutími hefur verið minnkaður um 20-falt (úr u.þ.b 8 sekúndum í 400 millisekúndur).</span><span class="sxs-lookup"><span data-stu-id="2497d-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="2497d-254">Afköst á allri lausn rafrænnar skýrslugerðar hefur þar af leiðandi verið endurbætt.</span><span class="sxs-lookup"><span data-stu-id="2497d-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Rakningarupplýsingar á hönnunarsíðu líkanavörpunar 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="2497d-256">Viðauki 1: Sækja þætti fyrir dæmið um rafræna skýrslugerðarlausn Microsoft</span><span class="sxs-lookup"><span data-stu-id="2497d-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="2497d-257">Sækja þarf eftirfarandi skrár og vista þær staðbundið.</span><span class="sxs-lookup"><span data-stu-id="2497d-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="2497d-258">Skrá</span><span class="sxs-lookup"><span data-stu-id="2497d-258">File</span></span>                                        | <span data-ttu-id="2497d-259">Efni</span><span class="sxs-lookup"><span data-stu-id="2497d-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="2497d-260">Aukin afköst model.version.1</span><span class="sxs-lookup"><span data-stu-id="2497d-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="2497d-261">Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="2497d-262">Aukin afköst mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="2497d-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="2497d-263">Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="2497d-264">Aukin afköst format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="2497d-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="2497d-265">Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="2497d-266">Viðauki 2: Skilgreina umgjörð rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="2497d-267">Áður en byrjað er að nota umgjörð rafrænnar skýrslugerðar til að bæta afköstin í dæminu um rafræna skýrslugerðarlausn Microsoft, þarf að skilgreina lágmarkssafn af færibreytum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="2497d-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="2497d-268">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-268">Configure ER parameters</span></span>

1. <span data-ttu-id="2497d-269">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="2497d-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2497d-270">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="2497d-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="2497d-271">Á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Almennt**, skal stilla valkostinn **Kveikja á hönnunarstillingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2497d-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="2497d-272">Í flipanum **Viðhengi** skal stilla eftirfarandi færibreytur:</span><span class="sxs-lookup"><span data-stu-id="2497d-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="2497d-273">Í reitnum **Skilgreiningar** skal velja gerðina **Skrá** fyrir **DEMF** fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="2497d-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="2497d-274">Í reitunum **Verksafn**, **Tímabundið**, **Grunnlína** og **Annað** skal velja gerð fyrir **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="2497d-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="2497d-275">Frekari upplýsingar um færibreytur rafrænnar skýrslugerðar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2497d-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="2497d-276">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="2497d-277">Allar skilgreiningar rafrænnar skýrslugerðar sem bætt er við eru merktar sem eign skilgreingarveitu rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="2497d-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="2497d-278">Skilgreiningarveita rafrænnar skýrslugerðar sem er virkjuð á vinnusvæðinu **Rafræn skýrslugerð** er notuð í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="2497d-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="2497d-279">Þess vegna þarf að virkja skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð** áður en byrjað er að bæta við eða breyta skilgreiningum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="2497d-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="2497d-280">Aðeins eigandi skilgreiningar rafrænnar skýrslugerðar getur breytt skilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="2497d-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="2497d-281">Þess vegna, áður en hægt er að breyta skilgreiningu rafrænnar skýrslugerðar, verður að virkja viðeigandi skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="2497d-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="2497d-282">Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="2497d-283">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="2497d-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2497d-284">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.</span><span class="sxs-lookup"><span data-stu-id="2497d-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="2497d-285">Á síðunni **Tafla yfir skilgreiningarveitur** er hver færsla með einkvæmt heiti og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="2497d-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="2497d-286">Farið yfir efnið á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="2497d-286">Review the contents of this page.</span></span> <span data-ttu-id="2497d-287">Ef færsla fyrir **Litware, Inc.** er þegar til skal sleppa næsta ferli, [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="2497d-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="2497d-288">Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="2497d-289">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="2497d-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2497d-290">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.</span><span class="sxs-lookup"><span data-stu-id="2497d-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="2497d-291">Á síðunni **Skilgreiningarveitur** skal velja **Ný**.</span><span class="sxs-lookup"><span data-stu-id="2497d-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="2497d-292">Í reitinn **Heiti** skal færa inn **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="2497d-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="2497d-293">Í reitinn **Veffang** skal færa inn `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="2497d-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="2497d-294">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="2497d-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="2497d-295">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2497d-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="2497d-296">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="2497d-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2497d-297">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Litware, Inc.** og síðan velja **Stilla sem virkt**.</span><span class="sxs-lookup"><span data-stu-id="2497d-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="2497d-298">Nánari upplýsingar um skilgreiningarveitur rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2497d-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2497d-299">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2497d-299">Additional resources</span></span>

- [<span data-ttu-id="2497d-300">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="2497d-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="2497d-301">Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum</span><span class="sxs-lookup"><span data-stu-id="2497d-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="2497d-302">Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað</span><span class="sxs-lookup"><span data-stu-id="2497d-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]