---
title: Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum
description: Þetta efnisatriði veitir upplýsingar um hvernig á að nota eiginleika fyrir rakningu afkasta í rafrænni skýrslugerð til að úrræðaleita vandamál er varða afköst.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295574"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="e63d9-103">Rekja framkvæmd á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum</span><span class="sxs-lookup"><span data-stu-id="e63d9-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e63d9-104">Sem hluti af hönnunarferlinu fyrir skilgreiningar rafrænnar skýrslugerðar til að búa til rafræn skjöl, skilgreinir þú aðferðina sem er notuð til að ná í göng úr forritinu og færa þau inn í úttak sem er myndað.</span><span class="sxs-lookup"><span data-stu-id="e63d9-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="e63d9-105">Eiginleikinn fyrir rakningu á afköstum rafrænnar skýrslugerðar auðveldar að draga umtalsvert úr tíma og kostnaði sem eru hluti af því að safna saman upplýsingum um framkvæmd rafrænnar skýrslugerðar og nota þau til að úrræðaleita vandamál er varða afköst.</span><span class="sxs-lookup"><span data-stu-id="e63d9-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="e63d9-106">Þessi leiðsögn veitir leiðbeiningar um hvernig á að gera rakningar á afköstum fyrir snið rafrænnar skýrslugerðar sem eru keyrð og hvernig á að nota upplýsingarnar úr þessum rakningum til að hjálpa til við að bæta afköst.</span><span class="sxs-lookup"><span data-stu-id="e63d9-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e63d9-107">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="e63d9-107">Prerequisites</span></span>

<span data-ttu-id="e63d9-108">Til að ljúka dæmunum í þessari leiðsögn þarftu að hafa eftirfarandi aðgang:</span><span class="sxs-lookup"><span data-stu-id="e63d9-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="e63d9-109">Aðgangur að einu af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="e63d9-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="e63d9-110">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="e63d9-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="e63d9-111">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e63d9-112">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="e63d9-112">System administrator</span></span>

- <span data-ttu-id="e63d9-113">Aðgang að tilviki Skilgreiningarþjónustu reglugerðar (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir forritið, fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="e63d9-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="e63d9-114">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="e63d9-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="e63d9-115">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e63d9-116">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="e63d9-116">System administrator</span></span>

<span data-ttu-id="e63d9-117">Einnig verður að sækja og geyma staðbundið eftirfarandi skrár.</span><span class="sxs-lookup"><span data-stu-id="e63d9-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="e63d9-118">Skrá</span><span class="sxs-lookup"><span data-stu-id="e63d9-118">File</span></span>                                  | <span data-ttu-id="e63d9-119">Efni</span><span class="sxs-lookup"><span data-stu-id="e63d9-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="e63d9-120">Afkastarakning model.version.1</span><span class="sxs-lookup"><span data-stu-id="e63d9-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="e63d9-121">Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="e63d9-122">Afkastarakning metadata.version.1</span><span class="sxs-lookup"><span data-stu-id="e63d9-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="e63d9-123">Sýnishorn af skilgreiningu lýsigagna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="e63d9-124">Afkastarakning mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="e63d9-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="e63d9-125">Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="e63d9-126">Afkastarakning format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="e63d9-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="e63d9-127">Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="e63d9-128">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-128">Configure ER parameters</span></span>

<span data-ttu-id="e63d9-129">Hver afkastarakning rafrænnar skýrslugerðar sem er búin til í forritinu er geymd sem viðhengi skráar fyrir aðgerðarskráningu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="e63d9-130">Rammi skjalastjórnunar (DM) er notaður til að stjórna þessum viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="e63d9-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="e63d9-131">Skilgreina verður færibreytur rafrænnar skýrslugerðar fyrirfram til að tilgreina skjalagerð skjalastjórnunar sem á að nota til að hengja afkastarakningar við.</span><span class="sxs-lookup"><span data-stu-id="e63d9-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="e63d9-132">Í vinnusvæðinu **Rafræn skýrslugerð** velurðu **Rafrænar skýrslufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="e63d9-133">Síðan, á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Viðhengi**, í reitnum **Annað**, skal velja skjalagerð skjalastjórnunar til að nota fyrir afkastarakningar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Síða rafrænna skýrslufæribreyta](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="e63d9-135">Til að vera tiltækt í uppflettingarreitnum **Annað** verður skjalagerð skjalastjórnunar að vera skilgreind á eftirfarandi hátt á síðunni **Skjalagerðir** (**Fyrirtækisstjórnun \> Skjalastjórnun \> Skjalagerðir**):</span><span class="sxs-lookup"><span data-stu-id="e63d9-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="e63d9-136">**Klasi:** Hengja skrá við</span><span class="sxs-lookup"><span data-stu-id="e63d9-136">**Class:** Attach file</span></span>
- <span data-ttu-id="e63d9-137">**Flokkur:** Skrá</span><span class="sxs-lookup"><span data-stu-id="e63d9-137">**Group:** File</span></span>

![Síðan Gerðir skjala](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="e63d9-139">Valin skjalagerð verður að vera tiltæk í öllum fyrirtækjum í núverandi tilviki vegna þess að viðhengi skjalastjórnunar miðast við fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="e63d9-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="e63d9-140">Skilgreina færibreytur RCS</span><span class="sxs-lookup"><span data-stu-id="e63d9-140">Configure RCS parameters</span></span>

<span data-ttu-id="e63d9-141">Afkastarakningar rafrænnar skýrslugerðar sem eru myndaðar verða fluttar inn í RCS til greiningar með því að nota sniðshönnuð rafrænnar skýrslugerðar og hönnuð fyrir vörpun rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="e63d9-142">Vegna þess að afkastarakningar rafrænnar skýrslugerðar eru geymdar sem viðhengi fyrir skrá aðgerðarskráningar sem tengist sniði rafrænnar skýrslugerðar er nauðsynlegt að skilgreina færibreytur RCS fyrirfram til að tilgreina skjalagerð skjalastjórnunar sem á að nota til að hengja afkastarakningar við.</span><span class="sxs-lookup"><span data-stu-id="e63d9-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="e63d9-143">Í tilfelli RCS sem hefur verið úthlutað fyrir fyrirtækið þitt, á vinnusvæðinu **Rafræn skýrslugerð**, skal velja **Rafrænar skýrslugerðarfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="e63d9-144">Síðan, á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Viðhengi**, í reitnum **Annað**, skal velja skjalagerð skjalastjórnunar til að nota fyrir afkastarakningar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Síða rafrænna skýrslugerðarfæribreyta í RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="e63d9-146">Til að vera tiltækt í uppflettingarreitnum **Annað** verður skjalagerð skjalastjórnunar að vera skilgreind á eftirfarandi hátt á síðunni **Skjalagerðir** (**Fyrirtækisstjórnun \> Skjalastjórnun \> Skjalagerðir**):</span><span class="sxs-lookup"><span data-stu-id="e63d9-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="e63d9-147">**Klasi:** Hengja skrá við</span><span class="sxs-lookup"><span data-stu-id="e63d9-147">**Class:** Attach file</span></span>
- <span data-ttu-id="e63d9-148">**Flokkur:** Skrá</span><span class="sxs-lookup"><span data-stu-id="e63d9-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="e63d9-149">Hanna lausn rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-149">Design an ER solution</span></span>

<span data-ttu-id="e63d9-150">Gerum ráð fyrir að þú hafir byrjað að hanna nýja lausn rafrænnar skýrslugerðar til að búa til nýja skýrslu sem sýnir lánardrottnafærslur.</span><span class="sxs-lookup"><span data-stu-id="e63d9-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="e63d9-151">Eins og er geturðu fundið færslurnar fyrir valinn lánardrottin á síðunni **Lánardrottnafærslur** (opnaðu **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar**, veldu lánardrottin og síðan, í aðgerðarúðunni, í flipanum **Lánardrottinn**, í flokknum **Færslur**, skal velja **Færslur**).</span><span class="sxs-lookup"><span data-stu-id="e63d9-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="e63d9-152">Hins vegar viltu hafa allar lánardrottnafærslur á sama tíma í einu rafrænu skjali á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="e63d9-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="e63d9-153">Þessi lausn mun samanstanda af nokkrum skilgreiningum rafrænnar skýrslugerðar sem innihalda nauðsynlegt gagnalíkan, lýsigögn, líkanavörpun og sniðseiningar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="e63d9-154">Skráðu þig inn á tilvik RCS sem hefur verið úthlutað fyrir fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="e63d9-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="e63d9-155">Í þessari leiðsögn býrðu til og breytir skilgreiningum fyrir sýnifyrirtækið **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="e63d9-156">Gakktu því úr skugga um að þessari skilgreiningarveitu hafi verið bætt við RCS og verið valin sem virk.</span><span class="sxs-lookup"><span data-stu-id="e63d9-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="e63d9-157">Fyrir leiðbeiningar skal sjá ferlið [Stofna skilgreiningarveitendur og merkja þá sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e63d9-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="e63d9-158">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="e63d9-159">Á síðunni **Skilgreiningar**, skal flytja inn skilgreiningar rafrænnar skýrslugerðar sem voru sóttar sem forkröfur í RCS, í eftirfarandi röð: gagnalíkan, lýsigögn, líkanavörpun, snið.</span><span class="sxs-lookup"><span data-stu-id="e63d9-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="e63d9-160">Fyrir hverja skilgreiningu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="e63d9-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="e63d9-161">Í aðgerðarúðunni skal velja **Skipta út \> Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="e63d9-162">Veljið **Vafra** til að velja viðeigandi skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="e63d9-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="e63d9-163">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-163">Select **OK**.</span></span>

    ![Skilgreiningarsíða í RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="e63d9-165">Keyra lausn rafrænnar skýrslugerðar til að rekja framkvæmd</span><span class="sxs-lookup"><span data-stu-id="e63d9-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="e63d9-166">Gerum ráð fyrir að þú hafir lokið við að hanna fyrstu útgáfu af lausn rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="e63d9-167">Núna viltu prófa hana í tilviki og greina afköst keyrslu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="e63d9-168">Flytja inn skilgreiningu rafrænnar skýrslugerðar úr RCS í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e63d9-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="e63d9-169">Skráðu þig inn á forritstilvikið.</span><span class="sxs-lookup"><span data-stu-id="e63d9-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="e63d9-170">Fyrir þessa leiðsögn flytur þú inn skilgreiningar úr RCS-tilvikinu þínu (þar sem þú hannar þætti rafrænnar skýrslugerðar) í tilvik (þar sem þú prófar og að lokum notar þær).</span><span class="sxs-lookup"><span data-stu-id="e63d9-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="e63d9-171">Þess vegna verður þú að ganga úr skugga um að allir nauðsynlegir gervingar hafi verið undirbúnir.</span><span class="sxs-lookup"><span data-stu-id="e63d9-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="e63d9-172">Til að fá leiðbeiningar skal sjá ferlið [Flytja inn skilgreiningar rafrænnar skýrslugerðar úr Skilgreiningarþjónustu reglugerðar (RCS)](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e63d9-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="e63d9-173">Fylgið þessum skrefum til að flytja inn skilgreiningar úr RCS í forritið:</span><span class="sxs-lookup"><span data-stu-id="e63d9-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="e63d9-174">Á vinnusvæðinu **Rafræn skýrslugerð**, í reitnum fyrir skilgreiningarveituna **Litware, Inc.**, skal velja **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="e63d9-175">Á síðunni **Skilgreiningageymsla** skal velja geymslu af gerðinni **RCS** og síðan velja **Opna**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="e63d9-176">Í flýtiflipanum **Skilgreiningar** skal velja skilgreininguna **Snið afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="e63d9-177">Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1** af valdri skilgreiningu og síðan velja **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Síðan Skilgreiningagagnasafn](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="e63d9-179">Samsvarandi útgáfur af skilgreiningum gagnalíkans og líkanavörpunar eru fluttar inn sjálfvirkt sem forkröfur fyrir innflutta skilgreiningu á sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="e63d9-180">Kveikja á afkastarakningu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="e63d9-181">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="e63d9-182">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="e63d9-183">Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="e63d9-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="e63d9-184">Í reitnum **Snið framkvæmdarakningar** skal tilgreina snið fyrir myndaða afkastarakningu sem upplýsingar um framkvæmd eru geymdar í fyrir snið rafrænnar skýrslugerðar og einingar vörpunar:</span><span class="sxs-lookup"><span data-stu-id="e63d9-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="e63d9-185">**Snið kembirakningar** – Veljið þetta gildi ef ætlunin er að keyra á gagnvirkan hátt snið rafrænnar skýrslugerðar sem er með stuttan keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="e63d9-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="e63d9-186">Söfnun á upplýsingum um framkvæmd á sniði rafrænnar skýrslugerðar fer þá í gang.</span><span class="sxs-lookup"><span data-stu-id="e63d9-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="e63d9-187">Þegar þetta gildi er valið safnar afkastarakningin upplýsingum um tímann sem eftirfarandi aðgerðir taka:</span><span class="sxs-lookup"><span data-stu-id="e63d9-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="e63d9-188">Að keyra hvern gagnagjafa í líkanavörpuninni sem er kallað á til að ná í gögn</span><span class="sxs-lookup"><span data-stu-id="e63d9-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="e63d9-189">Úrvinnsla á öllum sniðsatriðum til að færa gögn inn í frálagið sem myndast</span><span class="sxs-lookup"><span data-stu-id="e63d9-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="e63d9-190">Ef valið er gildið **Snið kembirakningar** er hægt að greina innihald rakningar í aðgerðarhönnuði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="e63d9-191">Þar er hægt að skoða snið rafrænnar skýrslugerðar eða vörpunareiningar sem minnst er á í rakningunni.</span><span class="sxs-lookup"><span data-stu-id="e63d9-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="e63d9-192">**Snið uppsafnaðrar rakningar** – Veljið þetta gildi ef ætlunin er að keyra snið rafrænnar skýrslugerðar sem er með langan keyrslutíma í runustillingu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="e63d9-193">Söfnun á uppsöfnuðum upplýsingum um framkvæmd á sniði rafrænnar skýrslugerðar fer þá í gang.</span><span class="sxs-lookup"><span data-stu-id="e63d9-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="e63d9-194">Þegar þetta gildi er valið safnar afkastarakningin upplýsingum um tímann sem eftirfarandi aðgerðir taka:</span><span class="sxs-lookup"><span data-stu-id="e63d9-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="e63d9-195">Að keyra hvern gagnagjafa í líkanavörpuninni sem er kallað á til að ná í gögn</span><span class="sxs-lookup"><span data-stu-id="e63d9-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="e63d9-196">Að keyra hvern gagnagjafa í sniðsvörpuninni sem er kallað á til að ná í gögn</span><span class="sxs-lookup"><span data-stu-id="e63d9-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="e63d9-197">Úrvinnsla á öllum sniðsatriðum til að færa gögn inn í frálagið sem myndast</span><span class="sxs-lookup"><span data-stu-id="e63d9-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="e63d9-198">Gildið **Snið uppsafnaðrar rakningar** er í boði í Microsoft Dynamics 365 Finance útgáfu 10.0.20 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="e63d9-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="e63d9-199">Í hönnuði rafræns skýrslugerðarsniðs og hönnuði líkanavörpunar rafrænnar skýrslugerðar er hægt að skoða heildartíma keyrslunnar fyrir stakan hlut.</span><span class="sxs-lookup"><span data-stu-id="e63d9-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="e63d9-200">Auk þess inniheldur rakningin upplýsingar um framkvæmdina, t.d. keyrslufjölda og lágmarks- og hámarkstíma einnar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="e63d9-201">Þessari rakningu er safnað samkvæmt slóð rakinna hluta.</span><span class="sxs-lookup"><span data-stu-id="e63d9-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="e63d9-202">Því gæti verið að tölfræðin sé röng þegar stök yfireining hlutar inniheldur nokkrar undireiningar hluta, eða þegar nokkrar undireiningar hluta eru með sama heiti.</span><span class="sxs-lookup"><span data-stu-id="e63d9-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="e63d9-203">Stillið eftirfarandi valkosti á **Já** til að safna saman ákveðnum upplýsingum um framkvæmdina á líkanavörpun rafrænnar skýrslugerðar og sniðseiningum rafrænnar skýrslugerðar:</span><span class="sxs-lookup"><span data-stu-id="e63d9-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="e63d9-204">**Safna saman tölfræði um fyrirspurnir** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman eftirfarandi upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="e63d9-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="e63d9-205">Fjölda gagnagrunnsköllum sem voru gerð eftir gagnaveitum</span><span class="sxs-lookup"><span data-stu-id="e63d9-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="e63d9-206">Fjölda afrita af köllum á gagnagrunninn</span><span class="sxs-lookup"><span data-stu-id="e63d9-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="e63d9-207">Upplýsingar um SQL-yrðingar sem voru notaðar til að gera gagnagrunnsköll</span><span class="sxs-lookup"><span data-stu-id="e63d9-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="e63d9-208">**Rekja aðgang að skyndiminni** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um notkun á skyndiminni líkanavörpunar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="e63d9-209">**Rekja gagnaaðgang** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um fjölda kalla á gagnagrunninn fyrir framkvæmdar gagnaveitur af færslulistagerðinni.</span><span class="sxs-lookup"><span data-stu-id="e63d9-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="e63d9-210">**Rekja tölusetningarlista** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um fjölda færslna sem gagnaveitur af færslulistagerðinni óska eftir.</span><span class="sxs-lookup"><span data-stu-id="e63d9-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e63d9-211">Færibreyturnar í svarglugganum **Færibreytur notanda** eru sérstaklega fyrir notandann og núverandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="e63d9-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Svarglugginn Notandafæribreytur](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="e63d9-213">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-213">Run the ER format</span></span>

1. <span data-ttu-id="e63d9-214">Veldu fyrirtækið **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="e63d9-215">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="e63d9-216">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja atriðið **Snið afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="e63d9-217">Í aðgerðarúðunni skal velja **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="e63d9-218">Takið eftir að skráin sem er búin til veitir upplýsingar um 265 færslur fyrir sex lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e63d9-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="e63d9-219">Yfirfara framkvæmdarakningu</span><span class="sxs-lookup"><span data-stu-id="e63d9-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="e63d9-220">Flytja myndaða rakningu úr forritinu</span><span class="sxs-lookup"><span data-stu-id="e63d9-220">Export the generated trace from the application</span></span>

<span data-ttu-id="e63d9-221">Afkastarakningar eru aftengdar frá upprunasniði rafrænnar skýrslugerðar og er hægt að númera við utanaðkomandi zip-skrá.</span><span class="sxs-lookup"><span data-stu-id="e63d9-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="e63d9-222">Farðu í **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Kembingarkladdar skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="e63d9-223">Á síðunni **Keyrslukladdar rafrænnar skýrslugjafar**, í vinstri rúðunni, í reitnum **Heiti skilgreiningar**, skal velja **Snið afkastarakningar** til að finna kladdafærslur sem framkvæmdin hefur búið til í skilgreiningunni **Snið afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="e63d9-224">Veljið hnappinn **Viðhengi** (bréfaklemmutáknið) efst í hægra horni síðunnar eða ýtið á **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Hnappur viðhengis í keyrslukladdasíðu rafrænnar skýrslugerðar](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="e63d9-226">Á síðunni **Viðhengi fyrir keyrslukladda rafrænnar skýrslugerðar**, í aðgerðarúðunni, skal velja **Opna** til að ná í afkastarakninguna sem zip-skrá og geyma hana staðbundið.</span><span class="sxs-lookup"><span data-stu-id="e63d9-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Viðhengi fyrir keyrslukladda rafrænnar skýrslugerðar](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="e63d9-228">Rakningin sem er búin til er með tilvísun í upprunaskýrslu rafrænnar skýrslugerðar í gegnum einkvæmt kennimerki skýrslu aðeins á sniðinu **GUID**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="e63d9-229">Númeraúthlutun fyrir útgáfu sniðsins er ekki tekin með í reikninginn.</span><span class="sxs-lookup"><span data-stu-id="e63d9-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="e63d9-230">Takið eftir að tengingin milli afkastarakningar sem hefur verið búin til fyrir framkvæmt snið rafrænnar skýrslugerðar og líkanavörpun rafrænnar skýrslugerðar byggist á rótarlýsingu sem var notuð og algenga gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="e63d9-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="e63d9-231">Númeraúthlutun fyrir útgáfu sniðsins og líkanavörpunar eru ekki teknar með í reikninginn.</span><span class="sxs-lookup"><span data-stu-id="e63d9-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="e63d9-232">Stillingin á flagginu **Sjálfgefið fyrir líkanavörpun** fyrir líkanavörpunina er einnig ekki tekin með í reikninginn.</span><span class="sxs-lookup"><span data-stu-id="e63d9-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="e63d9-233">Flytja inn mynda rakningu í RCS</span><span class="sxs-lookup"><span data-stu-id="e63d9-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="e63d9-234">Í RCS, á vinnusvæðinu **Rafræn skýrslugerð**, skal velja reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="e63d9-235">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal stækka atriðið **Líkan afkastarakningar** og velja atriðið **Snið afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="e63d9-236">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="e63d9-237">Á síðunni **Sniðshönnuður**, í aðgerðarúðunni, skal velja **Afkastarakning**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="e63d9-238">Í svarglugganum **Stillingar fyrir niðurstöðu afkastarakningar** skal velja **Flytja inn afkastarakningu**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="e63d9-239">Veldu **Fletta** til að velja þjöppuðu skrána sem þú fluttir áður út.</span><span class="sxs-lookup"><span data-stu-id="e63d9-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="e63d9-240">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-240">Select **OK**.</span></span>

    ![Svargluggi stillinga fyrir niðurstöðu afkastarakningar í RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="e63d9-242">Nota afkastarakningu fyrir greiningu í RCS - framkvæmd sniðs</span><span class="sxs-lookup"><span data-stu-id="e63d9-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="e63d9-243">Í RCS, á síðunni **Sniðshönnuður**, skal velja **Stækka/fella saman** til að stækka efni allra sniðsatriða.</span><span class="sxs-lookup"><span data-stu-id="e63d9-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="e63d9-244">Takið eftir að frekari upplýsingar eru sýndar fyrir sum atriði núverandi sniðs:</span><span class="sxs-lookup"><span data-stu-id="e63d9-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="e63d9-245">Raunverulegur tími sem fór í að færa gögn inn í myndað frálag með því að nota sniðsatriðið</span><span class="sxs-lookup"><span data-stu-id="e63d9-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="e63d9-246">Sami tími sýndur sem prósenta af heildartímanum sem fór í að búa til allt frálagið</span><span class="sxs-lookup"><span data-stu-id="e63d9-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Síða sniðshönnuðar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="e63d9-248">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="e63d9-249">Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="e63d9-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="e63d9-250">Í RCS, á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja atriðið **Vörpun afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="e63d9-251">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e63d9-252">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-252">Select **Designer**.</span></span>
4. <span data-ttu-id="e63d9-253">Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="e63d9-254">Veljið rakninguna sem var flutt inn áður.</span><span class="sxs-lookup"><span data-stu-id="e63d9-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="e63d9-255">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-255">Select **OK**.</span></span>

<span data-ttu-id="e63d9-256">Takið eftir að nýjar upplýsingar verða tiltækar fyrir sum atriði gagnaveitu fyrir núverandi líkanavörpun:</span><span class="sxs-lookup"><span data-stu-id="e63d9-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="e63d9-257">Raunverulegur tími sem fór í að ná í gögn með því að nota gagnagjafann</span><span class="sxs-lookup"><span data-stu-id="e63d9-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="e63d9-258">Sami tími sýndur sem prósenta af heildartímanum sem fór í að keyra alla líkanavörpunina</span><span class="sxs-lookup"><span data-stu-id="e63d9-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="e63d9-259">Takið eftir því að rafræn skýrslugerð segir þér að núverandi líkanavörpun afritar beiðnir gagnagrunns á meðan VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafi er keyrður.</span><span class="sxs-lookup"><span data-stu-id="e63d9-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="e63d9-260">Þessi tvítekning á sér stað vegna þess að kallað er á listann yfir lánardrottnafærslur tvisvar sinnum fyrir hverja endurtekna lánardrottnafærslu:</span><span class="sxs-lookup"><span data-stu-id="e63d9-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="e63d9-261">Eitt kall er framkvæmt til að færa upplýsingar um hverja færslu inn í gagnalíkanið, sem byggist á skilgreindum bindingum.</span><span class="sxs-lookup"><span data-stu-id="e63d9-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="e63d9-262">Eitt kall er framkvæmt til að færa reiknaðan fjölda færslna á hvern lánardrottin inn í gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="e63d9-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Skilaboð um tvítekna gagnagrunnsbeiðni á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="e63d9-264">Gildið **\[Q:530\]** gefur til kynna að kallað var á VendTrans-töfluna 530 sinnum til að skila færslu úr þeirri töflu yfir í VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann.</span><span class="sxs-lookup"><span data-stu-id="e63d9-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="e63d9-265">Gildið **\[530\]** gefur til kynna að kallað var á VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann 530 sinnum til að skila færslu úr þeim gagnagjafa og færa inn upplýsingarnar úr henni inn í gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="e63d9-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="e63d9-266">Við mælum með að þú notir vistun í skyndiminni fyrir VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann til að fækka fjölda kalla sem eru gerð til að ná í upplýsingar fyrir 265 færslur og hjálpa til við að bæta afköst líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="e63d9-267">Hún getur einnig verið gagnleg til að fækka fjölda kalla til LedgerTransTypeList gagnagjafann.</span><span class="sxs-lookup"><span data-stu-id="e63d9-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="e63d9-268">Þessi gagnagjafi er notaður til að tengja hvert gildi tölusetningarinnar **LedgerTransType** við merkið sitt.</span><span class="sxs-lookup"><span data-stu-id="e63d9-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="e63d9-269">Með því að nota þennan gagnagjafa geturðu fundið viðeigandi merki og fært það inn í gagnalíkanið fyrir hverja lánardrottnafærsla.</span><span class="sxs-lookup"><span data-stu-id="e63d9-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="e63d9-270">Núverandi fjöldi kalla á þennan gagnagjafa (9027) er frekar hár fyrir 265 færslur.</span><span class="sxs-lookup"><span data-stu-id="e63d9-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Hönnunarsíða líkanavörpunar í RCS sýnir 9027 köll á gagnagjafa](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="e63d9-272">Bæta líkanavörpun á grundvelli upplýsinga úr framkvæmdarakningu</span><span class="sxs-lookup"><span data-stu-id="e63d9-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="e63d9-273">Breyta reiknireglu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="e63d9-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="e63d9-274">Fylgið þessum skrefum til að nota vistun í skyndiminni, til að hjálpa til við koma í veg fyrir tvítekin köll á gagnagrunn:</span><span class="sxs-lookup"><span data-stu-id="e63d9-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="e63d9-275">Í RCS, á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnagjafar**, skal velja atriðið **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="e63d9-276">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="e63d9-277">Stækkið atriðið **VendTable**, stækkið listann yfir einn í mörg tengsl fyrir VendTable gagnagjafann (atriðið **\<Tengsl**) og veljið atriðið **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="e63d9-278">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-278">Select **Cache**.</span></span>

    ![Uppsetning á vistun í skyndiminni til að hjálpa til við að koma í veg fyrir tvítekin köll](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="e63d9-280">Fylgið þessum skrefum til að færa LedgerTransTypeList gagnagjafann inn í umfang VendTable gagnagjafans:</span><span class="sxs-lookup"><span data-stu-id="e63d9-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="e63d9-281">Í rúðunni **Gerðir gagnagjafa** skal stækka atriðið **Virknir** og velja atriðið **Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="e63d9-282">Í rúðunni **Gagnagjafar** skal velja atriðið **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="e63d9-283">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-283">Select **Add**.</span></span>
    4. <span data-ttu-id="e63d9-284">Í reitinn **Heiti** skal færa inn **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="e63d9-285">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="e63d9-286">Í reitinn **Formúla** skal færa inn **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="e63d9-287">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-287">Select **Save**.</span></span>
    8. <span data-ttu-id="e63d9-288">Lokið síðunni **Formúluritill**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="e63d9-289">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-289">Click **OK**.</span></span>

3. <span data-ttu-id="e63d9-290">Fylgið þessum skrefum til að vista í skyndiminni á reitnum **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="e63d9-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="e63d9-291">Veljið atriðið **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="e63d9-292">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="e63d9-293">Veljið atriðið **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="e63d9-294">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-294">Select **Cache**.</span></span>

    ![Uppsetning á vistun í skyndiminni fyrir reitinn $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="e63d9-296">Fylgið þessum skrefum til að breyta reitnum **\$TransTypeRecord** svo hann byrji að nota skyndiminni reitsins **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="e63d9-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="e63d9-297">Í rúðunni **Gagnagjafar** skal stækka atriðið **VendTable**, stækka atriðið **\<Tengsl**, stækka atriðið **VendTrans.VendTable\_AccountNum** og velja atriðið **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="e63d9-298">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="e63d9-299">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="e63d9-300">Í reitnum **Formúla** skal finna eftirfarandi segð:</span><span class="sxs-lookup"><span data-stu-id="e63d9-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="e63d9-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="e63d9-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="e63d9-302">Í reitnum **Formúla** skal færa inn eftirfarandi segð:</span><span class="sxs-lookup"><span data-stu-id="e63d9-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="e63d9-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="e63d9-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="e63d9-304">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-304">Select **Save**.</span></span>
    7. <span data-ttu-id="e63d9-305">Lokið síðunni **Formúluritill**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="e63d9-306">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-306">Select **OK**.</span></span>

5. <span data-ttu-id="e63d9-307">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-307">Select **Save**.</span></span>
6. <span data-ttu-id="e63d9-308">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="e63d9-309">Lokið síðunni **Líkanavarpanir**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="e63d9-310">Ljúka við breyttu útgáfuna af líkanavörpun rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="e63d9-311">Í RCS, á síðunni **Skilgreiningar**, í flýtiflipanum **Útgáfur**, skal velja útgáfuna **1.2** af skilgreiningunni **Vörpun afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="e63d9-312">Veljið **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-312">Select **Change status**.</span></span>
3. <span data-ttu-id="e63d9-313">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="e63d9-314">Flytja inn breytta skilgreiningu á líkanavörpun rafrænnar skýrslugerðar úr RCS í forritið</span><span class="sxs-lookup"><span data-stu-id="e63d9-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="e63d9-315">Endurtakið skrefin í hlutanum [Flytja inn skilgreiningu rafrænnar skýrslugerðar úr RCS í Finance and Operations](#import-configuration) hlutann fyrr í þessu efnisatriði til að flytja inn útgáfu 1.2 af skilgreiningunni **Vörpun afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="e63d9-316">Keyra breytta lausn rafrænnar skýrslugerðar til að rekja framkvæmd</span><span class="sxs-lookup"><span data-stu-id="e63d9-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="e63d9-317">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-317">Run the ER format</span></span>

<span data-ttu-id="e63d9-318">Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="e63d9-319">Vinna með framkvæmdarakningu</span><span class="sxs-lookup"><span data-stu-id="e63d9-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="e63d9-320">Flytja myndaða rakningu úr forritinu</span><span class="sxs-lookup"><span data-stu-id="e63d9-320">Export the generated trace from the application</span></span>

<span data-ttu-id="e63d9-321">Endurtakið skrefin í hlutanum [Flytja út myndaða rakningu úr forritinu](#export-trace) fyrr í þessu efnisatriði til að vista nýja afkastarakningu staðbundið.</span><span class="sxs-lookup"><span data-stu-id="e63d9-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="e63d9-322">Flytja inn myndaða rakningu í RCS</span><span class="sxs-lookup"><span data-stu-id="e63d9-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="e63d9-323">Endurtakið skrefin í hlutanum [Flytja inn myndaða rakningu í RCS](#import-trace) fyrr í þessu efnisatriði til að flytja inn nýja afkastarakningu í RCS.</span><span class="sxs-lookup"><span data-stu-id="e63d9-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="e63d9-324">Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="e63d9-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="e63d9-325">Endurtakið skrefin í hlutanum [Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun](#use-trace) fyrr í þessu efnisatriði til að greina síðustu afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="e63d9-326">Takiði eftir að leiðréttingar sem voru gerðar á líkanavörpun hafa eytt tvíteknum fyrirspurnum til gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="e63d9-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="e63d9-327">Fjöldi kalla í gagnagrunnstöflur og gagnagjafa fyrir þessa líkanavörpun hefur einnig verið fækkað.</span><span class="sxs-lookup"><span data-stu-id="e63d9-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="e63d9-328">Afköst á allri lausn rafrænnar skýrslugerðar hefur þar af leiðandi verið endurbætt.</span><span class="sxs-lookup"><span data-stu-id="e63d9-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![Rakningarupplýsingar fyrir VendTable gagnagjafann á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="e63d9-330">Í rakningarupplýsingunum gefur gildið **\[12\]** fyrir VendTable gagnagjafa til kynna að kallað hafi verið á þennan gagnagjafa 12 sinnum.</span><span class="sxs-lookup"><span data-stu-id="e63d9-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="e63d9-331">Gildið **\[Q:6\]** gefur til kynna að sex köll hafi verið þýdd yfir á gagnagrunnsköll til VendTable-töflunnar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="e63d9-332">Gildið **\[C:6\]** gefur til kynna að færslurnar sem voru sóttar úr gagnagrunninum hafi verið skyndiminni og unnið hafi verið úr sex öðrum köllum með því að nota skyndiminnið.</span><span class="sxs-lookup"><span data-stu-id="e63d9-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="e63d9-333">Athugið að fjöldi kalla á LedgerTransTypeList gagnagjafann hefur fækkað úr 9027 í 240.</span><span class="sxs-lookup"><span data-stu-id="e63d9-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Rakningarupplýsingar fyrir LedgerTransTypeList gagnagjafann á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="e63d9-335">Farðu yfir framkvæmdarrakningu í forritinu</span><span class="sxs-lookup"><span data-stu-id="e63d9-335">Review the execution trace in the application</span></span>

<span data-ttu-id="e63d9-336">Auk RCS kunna sumar útgáfur að bjóða upp á möguleika fyrir hönnunarupplifun á ramma rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="e63d9-337">Þessar útgáfur eru með valkostinn **Virkja hönnunarsnið** sem hægt er að kveikja á.</span><span class="sxs-lookup"><span data-stu-id="e63d9-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="e63d9-338">Hægt er að finna þennan valkost í flipanum **Almennt** á síðunni **Rafrænar skýrslugerðarfæribreytur** sem hægt er að opna úr vinnusvæðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Kveiktu á hönnunarstillingarvalkosti á síðunni Færibreytur rafrænnar skýrslugerðar](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="e63d9-340">Ef þú notar eina af þessum útgáfum geturðu greint upplýsingar á mynduðum afkastarakningum beint í forritinu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="e63d9-341">Ekki þarf að flytja þær út úr forritinu og flytja inn í RCS.</span><span class="sxs-lookup"><span data-stu-id="e63d9-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="e63d9-342">Yfirfara framkvæmdarakningu með utanaðkomandi verkfærum</span><span class="sxs-lookup"><span data-stu-id="e63d9-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="e63d9-343">Skilgreina færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="e63d9-343">Configure user parameters</span></span>

1. <span data-ttu-id="e63d9-344">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="e63d9-345">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="e63d9-346">Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, í reitnum **Snið framkvæmdarakningar**, skal velja **Perfview XML**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="e63d9-347">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-347">Run the ER format</span></span>

<span data-ttu-id="e63d9-348">Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="e63d9-349">Athugið að netvafrinn býður upp á zip-skrá fyrir niðurhal.</span><span class="sxs-lookup"><span data-stu-id="e63d9-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="e63d9-350">Þessi skrá inniheldur afkastarakningu á PerfView-sniði.</span><span class="sxs-lookup"><span data-stu-id="e63d9-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="e63d9-351">Síðan er hægt að nota greiningarverkfæri fyrir verkfæri PerfView-afkastagreiningar til að greina upplýsingarnar fyrir framkvæmd á sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Upplýsingar um frammistöðurakningu í PerfView](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="e63d9-353">Notaðu ytri verkfæri til að endurskoða framkvæmdarspor sem inniheldur gagnagrunnsfyrirspurnir</span><span class="sxs-lookup"><span data-stu-id="e63d9-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="e63d9-354">Vegna úrbóta sem hafa verið gerðar á ER-ramma býður afkastarakningin sem myndast á PerfView-sniði fleiri upplýsingar um framkvæmd ER-sniðs.</span><span class="sxs-lookup"><span data-stu-id="e63d9-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="e63d9-355">Í Microsoft Dynamics 365 for Finance and Operations útgáfu 10.0.4 (júlí 2019) getur þessi rakning einnig innihaldið upplýsingar um framkvæmdar SQL-fyrirspurnir í forritsgagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="e63d9-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="e63d9-356">Skilgreina færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="e63d9-356">Configure user parameters</span></span>

1. <span data-ttu-id="e63d9-357">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e63d9-358">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="e63d9-359">Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, skal stilla þessar færibreytur:</span><span class="sxs-lookup"><span data-stu-id="e63d9-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="e63d9-360">Í reitnum **Snið framkvæmdarakningar** velurðu **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="e63d9-361">Stilltu valkostinn **Safna saman tölfræði um fyrirspurnir** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="e63d9-362">Stillið valkostinn **Rekja fyrirspurn** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e63d9-362">Set the **Trace query** option to **Yes**.</span></span>

    ![Svæði keyrslurakningar, svargluggi fyrir færibreytur notanda](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="e63d9-364">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e63d9-364">Run the ER format</span></span>

<span data-ttu-id="e63d9-365">Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="e63d9-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="e63d9-366">Athugið að netvafrinn býður upp á zip-skrá fyrir niðurhal.</span><span class="sxs-lookup"><span data-stu-id="e63d9-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="e63d9-367">Þessi skrá inniheldur afkastarakningu á PerfView-sniði.</span><span class="sxs-lookup"><span data-stu-id="e63d9-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="e63d9-368">Síðan er hægt að nota greiningarverkfæri fyrir verkfæri PerfView-afkastagreiningar til að greina upplýsingarnar fyrir framkvæmd á sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e63d9-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="e63d9-369">Þessi rakning inniheldur núna upplýsingar um SQL-gagnagrunnsaðgang við framkvæmd ER-sniðsins.</span><span class="sxs-lookup"><span data-stu-id="e63d9-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Rekja upplýsingar fyrir framkvæmt ER-snið í PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="e63d9-371">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e63d9-371">Additional resources</span></span>

- [<span data-ttu-id="e63d9-372">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="e63d9-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e63d9-373">Bættu frammistöðu rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum með REIKNAÐA REITI með færibreytum</span><span class="sxs-lookup"><span data-stu-id="e63d9-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
