---
title: Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum
description: Þetta efnisatriði veitir upplýsingar um hvernig á að nota eiginleika fyrir rakningu afkasta í rafrænni skýrslugerð til að úrræðaleita vandamál er varða afköst.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6585e44701160bf31c107c07226f992b12cf035e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550649"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="0d5d3-103">Rekja framkvæmd á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum</span><span class="sxs-lookup"><span data-stu-id="0d5d3-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0d5d3-104">Sem hluti af hönnunarferlinu fyrir skilgreiningar rafrænnar skýrslugerðar til að búa til rafræn skjöl, skilgreinir þú aðferðina sem er notuð til að ná í göng úr forritinu og færa þau inn í úttak sem er myndað.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="0d5d3-105">Eiginleikinn fyrir rakningu á afköstum rafrænnar skýrslugerðar auðveldar að draga umtalsvert úr tíma og kostnaði sem eru hluti af því að safna saman upplýsingum um framkvæmd rafrænnar skýrslugerðar og nota þau til að úrræðaleita vandamál er varða afköst.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="0d5d3-106">Þessi leiðsögn veitir leiðbeiningar um hvernig á að gera rakningar á afköstum fyrir snið rafrænnar skýrslugerðar sem eru keyrð og hvernig á að nota upplýsingarnar úr þessum rakningum til að hjálpa til við að bæta afköst.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d5d3-107">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="0d5d3-107">Prerequisites</span></span>

<span data-ttu-id="0d5d3-108">Til að ljúka dæmunum í þessari leiðsögn þarftu að hafa eftirfarandi aðgang:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="0d5d3-109">Aðgangur að einu af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="0d5d3-110">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="0d5d3-111">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0d5d3-112">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="0d5d3-112">System administrator</span></span>

- <span data-ttu-id="0d5d3-113">Aðgang að tilviki Skilgreiningarþjónustu reglugerðar (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir forritið, fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="0d5d3-114">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="0d5d3-115">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0d5d3-116">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="0d5d3-116">System administrator</span></span>

<span data-ttu-id="0d5d3-117">Einnig verður að sækja og geyma staðbundið eftirfarandi skrár.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="0d5d3-118">Skrá</span><span class="sxs-lookup"><span data-stu-id="0d5d3-118">File</span></span>                                  | <span data-ttu-id="0d5d3-119">Efni</span><span class="sxs-lookup"><span data-stu-id="0d5d3-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="0d5d3-120">Afkastarakning model.version.1</span><span class="sxs-lookup"><span data-stu-id="0d5d3-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="0d5d3-121">Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="0d5d3-122">Afkastarakning metadata.version.1</span><span class="sxs-lookup"><span data-stu-id="0d5d3-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="0d5d3-123">Sýnishorn af skilgreiningu lýsigagna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="0d5d3-124">Afkastarakning mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="0d5d3-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="0d5d3-125">Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="0d5d3-126">Afkastarakning format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="0d5d3-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="0d5d3-127">Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="0d5d3-128">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-128">Configure ER parameters</span></span>

<span data-ttu-id="0d5d3-129">Hver afkastarakning rafrænnar skýrslugerðar sem er búin til í forritinu er geymd sem viðhengi skráar fyrir aðgerðarskráningu.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="0d5d3-130">Rammi skjalastjórnunar (DM) er notaður til að stjórna þessum viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="0d5d3-131">Skilgreina verður færibreytur rafrænnar skýrslugerðar fyrirfram til að tilgreina skjalagerð skjalastjórnunar sem á að nota til að hengja afkastarakningar við.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="0d5d3-132">Í vinnusvæðinu **Rafræn skýrslugerð** velurðu **Rafrænar skýrslufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="0d5d3-133">Síðan, á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Viðhengi**, í reitnum **Annað**, skal velja skjalagerð skjalastjórnunar til að nota fyrir afkastarakningar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Síða rafrænna skýrslufæribreyta](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="0d5d3-135">Til að vera tiltækt í uppflettingarreitnum **Annað** verður skjalagerð skjalastjórnunar að vera skilgreind á eftirfarandi hátt á síðunni **Skjalagerðir** (**Fyrirtækisstjórnun \> Skjalastjórnun \> Skjalagerðir**):</span><span class="sxs-lookup"><span data-stu-id="0d5d3-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="0d5d3-136">**Klasi:** Hengja skrá við</span><span class="sxs-lookup"><span data-stu-id="0d5d3-136">**Class:** Attach file</span></span>
- <span data-ttu-id="0d5d3-137">**Flokkur:** Skrá</span><span class="sxs-lookup"><span data-stu-id="0d5d3-137">**Group:** File</span></span>

![Síðan Gerðir skjala](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="0d5d3-139">Valin skjalagerð verður að vera tiltæk í öllum fyrirtækjum í núverandi tilviki vegna þess að viðhengi skjalastjórnunar miðast við fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="0d5d3-140">Skilgreina færibreytur RCS</span><span class="sxs-lookup"><span data-stu-id="0d5d3-140">Configure RCS parameters</span></span>

<span data-ttu-id="0d5d3-141">Afkastarakningar rafrænnar skýrslugerðar sem eru myndaðar verða fluttar inn í RCS til greiningar með því að nota sniðshönnuð rafrænnar skýrslugerðar og hönnuð fyrir vörpun rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="0d5d3-142">Vegna þess að afkastarakningar rafrænnar skýrslugerðar eru geymdar sem viðhengi fyrir skrá aðgerðarskráningar sem tengist sniði rafrænnar skýrslugerðar er nauðsynlegt að skilgreina færibreytur RCS fyrirfram til að tilgreina skjalagerð skjalastjórnunar sem á að nota til að hengja afkastarakningar við.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="0d5d3-143">Í tilfelli RCS sem hefur verið úthlutað fyrir fyrirtækið þitt, á vinnusvæðinu **Rafræn skýrslugerð**, skal velja **Rafrænar skýrslugerðarfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="0d5d3-144">Síðan, á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Viðhengi**, í reitnum **Annað**, skal velja skjalagerð skjalastjórnunar til að nota fyrir afkastarakningar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Síða rafrænna skýrslugerðarfæribreyta í RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="0d5d3-146">Til að vera tiltækt í uppflettingarreitnum **Annað** verður skjalagerð skjalastjórnunar að vera skilgreind á eftirfarandi hátt á síðunni **Skjalagerðir** (**Fyrirtækisstjórnun \> Skjalastjórnun \> Skjalagerðir**):</span><span class="sxs-lookup"><span data-stu-id="0d5d3-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="0d5d3-147">**Klasi:** Hengja skrá við</span><span class="sxs-lookup"><span data-stu-id="0d5d3-147">**Class:** Attach file</span></span>
- <span data-ttu-id="0d5d3-148">**Flokkur:** Skrá</span><span class="sxs-lookup"><span data-stu-id="0d5d3-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="0d5d3-149">Hanna lausn rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-149">Design an ER solution</span></span>

<span data-ttu-id="0d5d3-150">Gerum ráð fyrir að þú hafir byrjað að hanna nýja lausn rafrænnar skýrslugerðar til að búa til nýja skýrslu sem sýnir lánardrottnafærslur.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="0d5d3-151">Eins og er geturðu fundið færslurnar fyrir valinn lánardrottin á síðunni **Lánardrottnafærslur** (opnaðu **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar**, veldu lánardrottin og síðan, í aðgerðarúðunni, í flipanum **Lánardrottinn**, í flokknum **Færslur**, skal velja **Færslur**).</span><span class="sxs-lookup"><span data-stu-id="0d5d3-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="0d5d3-152">Hins vegar viltu hafa allar lánardrottnafærslur á sama tíma í einu rafrænu skjali á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="0d5d3-153">Þessi lausn mun samanstanda af nokkrum skilgreiningum rafrænnar skýrslugerðar sem innihalda nauðsynlegt gagnalíkan, lýsigögn, líkanavörpun og sniðseiningar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="0d5d3-154">Skráðu þig inn á tilvik RCS sem hefur verið úthlutað fyrir fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="0d5d3-155">Í þessari leiðsögn býrðu til og breytir skilgreiningum fyrir sýnifyrirtækið **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="0d5d3-156">Gakktu því úr skugga um að þessari skilgreiningarveitu hafi verið bætt við RCS og verið valin sem virk.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="0d5d3-157">Fyrir leiðbeiningar skal sjá ferlið [Stofna skilgreiningarveitendur og merkja þá sem virka](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="0d5d3-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="0d5d3-158">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="0d5d3-159">Á síðunni **Skilgreiningar**, skal flytja inn skilgreiningar rafrænnar skýrslugerðar sem voru sóttar sem forkröfur í RCS, í eftirfarandi röð: gagnalíkan, lýsigögn, líkanavörpun, snið.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="0d5d3-160">Fyrir hverja skilgreiningu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="0d5d3-161">Í aðgerðarúðunni skal velja **Skipta út \> Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="0d5d3-162">Veljið **Vafra** til að velja viðeigandi skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="0d5d3-163">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-163">Select **OK**.</span></span>

    ![Skilgreiningarsíða í RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="0d5d3-165">Keyra lausn rafrænnar skýrslugerðar til að rekja framkvæmd</span><span class="sxs-lookup"><span data-stu-id="0d5d3-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="0d5d3-166">Gerum ráð fyrir að þú hafir lokið við að hanna fyrstu útgáfu af lausn rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="0d5d3-167">Núna viltu prófa hana í tilviki og greina afköst keyrslu.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="0d5d3-168">Flytja inn skilgreiningu rafrænnar skýrslugerðar úr RCS í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0d5d3-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="0d5d3-169">Skráðu þig inn á forritstilvikið.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="0d5d3-170">Fyrir þessa leiðsögn flytur þú inn skilgreiningar úr RCS-tilvikinu þínu (þar sem þú hannar þætti rafrænnar skýrslugerðar) í tilvik (þar sem þú prófar og að lokum notar þær).</span><span class="sxs-lookup"><span data-stu-id="0d5d3-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="0d5d3-171">Þess vegna verður þú að ganga úr skugga um að allir nauðsynlegir gervingar hafi verið undirbúnir.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="0d5d3-172">Til að fá leiðbeiningar skal sjá ferlið [Flytja inn skilgreiningar rafrænnar skýrslugerðar úr Skilgreiningarþjónustu reglugerðar (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="0d5d3-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="0d5d3-173">Fylgið þessum skrefum til að flytja inn skilgreiningar úr RCS í forritið:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="0d5d3-174">Á vinnusvæðinu **Rafræn skýrslugerð**, í reitnum fyrir skilgreiningarveituna **Litware, Inc.**, skal velja **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="0d5d3-175">Á síðunni **Skilgreiningageymsla** skal velja geymslu af gerðinni **RCS** og síðan velja **Opna**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="0d5d3-176">Í flýtiflipanum **Skilgreiningar** skal velja skilgreininguna **Snið afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="0d5d3-177">Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1** af valdri skilgreiningu og síðan velja **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Síðan Skilgreiningagagnasafn](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="0d5d3-179">Samsvarandi útgáfur af skilgreiningum gagnalíkans og líkanavörpunar eru fluttar inn sjálfvirkt sem forkröfur fyrir innflutta skilgreiningu á sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="0d5d3-180">Kveikja á afkastarakningu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="0d5d3-181">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="0d5d3-182">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="0d5d3-183">Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="0d5d3-184">Í reitnum **Snið framkvæmdarakningar** skal velja **Kemba rakningasnið** til að byrja að safna saman upplýsingum um framkvæmd á sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="0d5d3-185">Þegar þetta gildi er valið safnar afkastarakningin upplýsingum um tímann sem eftirfarandi aðgerðir taka:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="0d5d3-186">Að keyra hvern gagnagjafa í líkanavörpuninni sem er kallað á til að ná í gögn</span><span class="sxs-lookup"><span data-stu-id="0d5d3-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="0d5d3-187">Úrvinnsla á öllum sniðsatriðum til að færa gögn inn í frálagið sem myndast</span><span class="sxs-lookup"><span data-stu-id="0d5d3-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="0d5d3-188">Notaður er reiturinn **Snið framkvæmdarakningar** til að tilgreina snið fyrir myndaða afkastarakningu sem upplýsingar um framkvæmd eru geymdar í fyrir snið rafrænnar skýrslugerðar og einingar vörpunar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="0d5d3-189">Með því að velja **Kemba sniðsrakningu** sem gildið geturðu greint innihald rakningarinnar í aðgerðarhönnuði rafrænnar skýrslugerðar og séð snið rafrænnar skýrslugerðar eða einingar vörpunar sem minnst er á í rakningunni.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="0d5d3-190">Stillið eftirfarandi valkosti á **Já** til að safna saman ákveðnum upplýsingum um framkvæmdina á líkanavörpun rafrænnar skýrslugerðar og sniðseiningum rafrænnar skýrslugerðar:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="0d5d3-191">**Safna saman tölfræði um fyrirspurnir** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman eftirfarandi upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="0d5d3-192">Fjölda gagnagrunnsköllum sem voru gerð eftir gagnaveitum</span><span class="sxs-lookup"><span data-stu-id="0d5d3-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="0d5d3-193">Fjölda afrita af köllum á gagnagrunninn</span><span class="sxs-lookup"><span data-stu-id="0d5d3-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="0d5d3-194">Upplýsingar um SQL-yrðingar sem voru notaðar til að gera gagnagrunnsköll</span><span class="sxs-lookup"><span data-stu-id="0d5d3-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="0d5d3-195">**Rekja aðgang að skyndiminni** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um notkun á skyndiminni líkanavörpunar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="0d5d3-196">**Rekja gagnaaðgang** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um fjölda kalla á gagnagrunninn fyrir framkvæmdar gagnaveitur af færslulistagerðinni.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="0d5d3-197">**Rekja tölusetningarlista** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um fjölda færslna sem gagnaveitur af færslulistagerðinni óska eftir.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d5d3-198">Færibreyturnar í svarglugganum **Færibreytur notanda** eru sérstaklega fyrir notandann og núverandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Svarglugginn Notandafæribreytur](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="0d5d3-200">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-200">Run the ER format</span></span>

1. <span data-ttu-id="0d5d3-201">Veldu fyrirtækið **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-201">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="0d5d3-202">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="0d5d3-203">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja atriðið **Snið afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="0d5d3-204">Í aðgerðarúðunni skal velja **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="0d5d3-205">Takið eftir að skráin sem er búin til veitir upplýsingar um 265 færslur fyrir sex lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="0d5d3-206">Yfirfara framkvæmdarakningu</span><span class="sxs-lookup"><span data-stu-id="0d5d3-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="0d5d3-207">Flytja myndaða rakningu úr forritinu</span><span class="sxs-lookup"><span data-stu-id="0d5d3-207">Export the generated trace from the application</span></span>

<span data-ttu-id="0d5d3-208">Afkastarakningar eru aftengdar frá upprunasniði rafrænnar skýrslugerðar og er hægt að númera við utanaðkomandi zip-skrá.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="0d5d3-209">Farðu í **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Kembingarkladdar skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-209">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="0d5d3-210">Á síðunni **Keyrslukladdar rafrænnar skýrslugjafar**, í vinstri rúðunni, í reitnum **Heiti skilgreiningar**, skal velja **Snið afkastarakningar** til að finna kladdafærslur sem framkvæmdin hefur búið til í skilgreiningunni **Snið afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="0d5d3-211">Veljið hnappinn **Viðhengi** (bréfaklemmutáknið) efst í hægra horni síðunnar eða ýtið á **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Hnappur viðhengis í keyrslukladdasíðu rafrænnar skýrslugerðar](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="0d5d3-213">Á síðunni **Viðhengi fyrir keyrslukladda rafrænnar skýrslugerðar**, í aðgerðarúðunni, skal velja **Opna** til að ná í afkastarakninguna sem zip-skrá og geyma hana staðbundið.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Viðhengi fyrir keyrslukladda rafrænnar skýrslugerðar](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="0d5d3-215">Rakningin sem er búin til er með tilvísun í upprunaskýrslu rafrænnar skýrslugerðar í gegnum einkvæmt kennimerki skýrslu aðeins á sniðinu **GUID**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="0d5d3-216">Númeraúthlutun fyrir útgáfu sniðsins er ekki tekin með í reikninginn.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="0d5d3-217">Takið eftir að tengingin milli afkastarakningar sem hefur verið búin til fyrir framkvæmt snið rafrænnar skýrslugerðar og líkanavörpun rafrænnar skýrslugerðar byggist á rótarlýsingu sem var notuð og algenga gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="0d5d3-218">Númeraúthlutun fyrir útgáfu sniðsins og líkanavörpunar eru ekki teknar með í reikninginn.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="0d5d3-219">Stillingin á flagginu **Sjálfgefið fyrir líkanavörpun** fyrir líkanavörpunina er einnig ekki tekin með í reikninginn.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="0d5d3-220">Flytja inn mynda rakningu í RCS</span><span class="sxs-lookup"><span data-stu-id="0d5d3-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="0d5d3-221">Í RCS, á vinnusvæðinu **Rafræn skýrslugerð**, skal velja reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="0d5d3-222">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal stækka atriðið **Líkan afkastarakningar** og velja atriðið **Snið afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="0d5d3-223">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="0d5d3-224">Á síðunni **Sniðshönnuður**, í aðgerðarúðunni, skal velja **Afkastarakning**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="0d5d3-225">Í svarglugganum **Stillingar fyrir niðurstöðu afkastarakningar** skal velja **Flytja inn afkastarakningu**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="0d5d3-226">Veldu **Fletta** til að velja þjöppuðu skrána sem þú fluttir áður út.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-226">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="0d5d3-227">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-227">Select **OK**.</span></span>

    ![Svargluggi stillinga fyrir niðurstöðu afkastarakningar í RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="0d5d3-229">Nota afkastarakningu fyrir greiningu í RCS - framkvæmd sniðs</span><span class="sxs-lookup"><span data-stu-id="0d5d3-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="0d5d3-230">Í RCS, á síðunni **Sniðshönnuður**, skal velja **Stækka/fella saman** til að stækka efni allra sniðsatriða.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="0d5d3-231">Takið eftir að frekari upplýsingar eru sýndar fyrir sum atriði núverandi sniðs:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="0d5d3-232">Raunverulegur tími sem fór í að færa gögn inn í myndað frálag með því að nota sniðsatriðið</span><span class="sxs-lookup"><span data-stu-id="0d5d3-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="0d5d3-233">Sami tími sýndur sem prósenta af heildartímanum sem fór í að búa til allt frálagið</span><span class="sxs-lookup"><span data-stu-id="0d5d3-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Síða sniðshönnuðar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="0d5d3-235">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="0d5d3-236">Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="0d5d3-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="0d5d3-237">Í RCS, á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja atriðið **Vörpun afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="0d5d3-238">Í aðgerðarúðunni skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="0d5d3-239">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-239">Select **Designer**.</span></span>
4. <span data-ttu-id="0d5d3-240">Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="0d5d3-241">Veljið rakninguna sem var flutt inn áður.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="0d5d3-242">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-242">Select **OK**.</span></span>

<span data-ttu-id="0d5d3-243">Takið eftir að nýjar upplýsingar verða tiltækar fyrir sum atriði gagnaveitu fyrir núverandi líkanavörpun:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="0d5d3-244">Raunverulegur tími sem fór í að ná í gögn með því að nota gagnagjafann</span><span class="sxs-lookup"><span data-stu-id="0d5d3-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="0d5d3-245">Sami tími sýndur sem prósenta af heildartímanum sem fór í að keyra alla líkanavörpunina</span><span class="sxs-lookup"><span data-stu-id="0d5d3-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="0d5d3-246">Takið eftir því að rafræn skýrslugerð segir þér að núverandi líkanavörpun afritar beiðnir gagnagrunns á meðan VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafi er keyrður.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="0d5d3-247">Þessi tvítekning á sér stað vegna þess að kallað er á listann yfir lánardrottnafærslur tvisvar sinnum fyrir hverja endurtekna lánardrottnafærslu:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="0d5d3-248">Eitt kall er framkvæmt til að færa upplýsingar um hverja færslu inn í gagnalíkanið, sem byggist á skilgreindum bindingum.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="0d5d3-249">Eitt kall er framkvæmt til að færa reiknaðan fjölda færslna á hvern lánardrottin inn í gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Skilaboð um tvítekna gagnagrunnsbeiðni á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="0d5d3-251">Gildið **\[Q:530\]** gefur til kynna að kallað var á VendTrans-töfluna 530 sinnum til að skila færslu úr þeirri töflu yfir í VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="0d5d3-252">Gildið **\[530\]** gefur til kynna að kallað var á VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann 530 sinnum til að skila færslu úr þeim gagnagjafa og færa inn upplýsingarnar úr henni inn í gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="0d5d3-253">Við mælum með að þú notir vistun í skyndiminni fyrir VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann til að fækka fjölda kalla sem eru gerð til að ná í upplýsingar fyrir 265 færslur og hjálpa til við að bæta afköst líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="0d5d3-254">Hún getur einnig verið gagnleg til að fækka fjölda kalla til LedgerTransTypeList gagnagjafann.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="0d5d3-255">Þessi gagnagjafi er notaður til að tengja hvert gildi tölusetningarinnar **LedgerTransType** við merkið sitt.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="0d5d3-256">Með því að nota þennan gagnagjafa geturðu fundið viðeigandi merki og fært það inn í gagnalíkanið fyrir hverja lánardrottnafærsla.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="0d5d3-257">Núverandi fjöldi kalla á þennan gagnagjafa (9027) er frekar hár fyrir 265 færslur.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Hönnunarsíða líkanavörpunar í RCS sýnir 9027 köll á gagnagjafa](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="0d5d3-259">Bæta líkanavörpun á grundvelli upplýsinga úr framkvæmdarakningu</span><span class="sxs-lookup"><span data-stu-id="0d5d3-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="0d5d3-260">Breyta reiknireglu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="0d5d3-261">Fylgið þessum skrefum til að nota vistun í skyndiminni, til að hjálpa til við koma í veg fyrir tvítekin köll á gagnagrunn:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="0d5d3-262">Í RCS, á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnagjafar**, skal velja atriðið **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="0d5d3-263">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="0d5d3-264">Stækkið atriðið **VendTable**, stækkið listann yfir einn í mörg tengsl fyrir VendTable gagnagjafann (atriðið **\<Tengsl**) og veljið atriðið **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="0d5d3-265">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-265">Select **Cache**.</span></span>

    ![Uppsetning á vistun í skyndiminni til að hjálpa til við að koma í veg fyrir tvítekin köll](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="0d5d3-267">Fylgið þessum skrefum til að færa LedgerTransTypeList gagnagjafann inn í umfang VendTable gagnagjafans:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="0d5d3-268">Í rúðunni **Gerðir gagnagjafa** skal stækka atriðið **Virknir** og velja atriðið **Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="0d5d3-269">Í rúðunni **Gagnagjafar** skal velja atriðið **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="0d5d3-270">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-270">Select **Add**.</span></span>
    4. <span data-ttu-id="0d5d3-271">Í reitinn **Heiti** skal færa inn **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="0d5d3-272">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="0d5d3-273">Í reitinn **Formúla** skal færa inn **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="0d5d3-274">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-274">Select **Save**.</span></span>
    8. <span data-ttu-id="0d5d3-275">Lokið síðunni **Formúluritill**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="0d5d3-276">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-276">Click **OK**.</span></span>

3. <span data-ttu-id="0d5d3-277">Fylgið þessum skrefum til að vista í skyndiminni á reitnum **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="0d5d3-278">Veljið atriðið **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="0d5d3-279">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="0d5d3-280">Veljið atriðið **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="0d5d3-281">Veljið **Skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-281">Select **Cache**.</span></span>

    ![Uppsetning á vistun í skyndiminni fyrir reitinn $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="0d5d3-283">Fylgið þessum skrefum til að breyta reitnum **\$TransTypeRecord** svo hann byrji að nota skyndiminni reitsins **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="0d5d3-284">Í rúðunni **Gagnagjafar** skal stækka atriðið **VendTable**, stækka atriðið **\<Tengsl**, stækka atriðið **VendTrans.VendTable\_AccountNum** og velja atriðið **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="0d5d3-285">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="0d5d3-286">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="0d5d3-287">Í reitnum **Formúla** skal finna eftirfarandi segð:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="0d5d3-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="0d5d3-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="0d5d3-289">Í reitnum **Formúla** skal færa inn eftirfarandi segð:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="0d5d3-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="0d5d3-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="0d5d3-291">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-291">Select **Save**.</span></span>
    7. <span data-ttu-id="0d5d3-292">Lokið síðunni **Formúluritill**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="0d5d3-293">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-293">Select **OK**.</span></span>

5. <span data-ttu-id="0d5d3-294">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-294">Select **Save**.</span></span>
6. <span data-ttu-id="0d5d3-295">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="0d5d3-296">Lokið síðunni **Líkanavarpanir**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="0d5d3-297">Ljúka við breyttu útgáfuna af líkanavörpun rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="0d5d3-298">Í RCS, á síðunni **Skilgreiningar**, í flýtiflipanum **Útgáfur**, skal velja útgáfuna **1.2** af skilgreiningunni **Vörpun afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="0d5d3-299">Veljið **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-299">Select **Change status**.</span></span>
3. <span data-ttu-id="0d5d3-300">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="0d5d3-301">Flytja inn breytta skilgreiningu á líkanavörpun rafrænnar skýrslugerðar úr RCS í forritið</span><span class="sxs-lookup"><span data-stu-id="0d5d3-301">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="0d5d3-302">Endurtakið skrefin í hlutanum [Flytja inn skilgreiningu rafrænnar skýrslugerðar úr RCS í Finance and Operations](#import-configuration) fyrr í þessu efnisatriði til að flytja inn útgáfu 1.2 af skilgreiningunni **Vörpun afkastarakningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="0d5d3-303">Keyra breytta lausn rafrænnar skýrslugerðar til að rekja framkvæmd</span><span class="sxs-lookup"><span data-stu-id="0d5d3-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="0d5d3-304">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-304">Run the ER format</span></span>

<span data-ttu-id="0d5d3-305">Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="0d5d3-306">Yfirfara framkvæmdarakningu</span><span class="sxs-lookup"><span data-stu-id="0d5d3-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="0d5d3-307">Flytja myndaða rakningu úr forritinu</span><span class="sxs-lookup"><span data-stu-id="0d5d3-307">Export the generated trace from the application</span></span>

<span data-ttu-id="0d5d3-308">Endurtakið skrefin í hlutanum [Flytja út myndaða rakningu úr forritinu](#export-trace) fyrr í þessu efnisatriði til að vista nýja afkastarakningu staðbundið.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-308">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="0d5d3-309">Flytja inn myndaða rakningu í RCS</span><span class="sxs-lookup"><span data-stu-id="0d5d3-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="0d5d3-310">Endurtakið skrefin í hlutanum [Flytja inn myndaða rakningu í RCS](#import-trace) fyrr í þessu efnisatriði til að flytja inn nýja afkastarakningu í RCS.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="0d5d3-311">Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="0d5d3-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="0d5d3-312">Endurtakið skrefin í hlutanum [Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun](#use-trace) fyrr í þessu efnisatriði til að greina síðustu afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="0d5d3-313">Takiði eftir að leiðréttingar sem voru gerðar á líkanavörpun hafa eytt tvíteknum fyrirspurnum til gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="0d5d3-314">Fjöldi kalla í gagnagrunnstöflur og gagnagjafa fyrir þessa líkanavörpun hefur einnig verið fækkað.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="0d5d3-315">Afköst á allri lausn rafrænnar skýrslugerðar hefur þar af leiðandi verið endurbætt.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Rakningarupplýsingar fyrir VendTable gagnagjafann á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="0d5d3-317">Í rakningarupplýsingunum gefur gildið **\[12\]** fyrir VendTable gagnagjafa til kynna að kallað hafi verið á þennan gagnagjafa 12 sinnum.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="0d5d3-318">Gildið **\[Q:6\]** gefur til kynna að sex köll hafi verið þýdd yfir á gagnagrunnsköll til VendTable-töflunnar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="0d5d3-319">Gildið **\[C:6\]** gefur til kynna að færslurnar sem voru sóttar úr gagnagrunninum hafi verið skyndiminni og unnið hafi verið úr sex öðrum köllum með því að nota skyndiminnið.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="0d5d3-320">Athugið að fjöldi kalla á LedgerTransTypeList gagnagjafann hefur fækkað úr 9027 í 240.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Rakningarupplýsingar fyrir LedgerTransTypeList gagnagjafann á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="0d5d3-322">Farðu yfir framkvæmdarrakningu í forritinu</span><span class="sxs-lookup"><span data-stu-id="0d5d3-322">Review the execution trace in the application</span></span>

<span data-ttu-id="0d5d3-323">Auk RCS kunna sumar útgáfur að bjóða upp á möguleika fyrir hönnunarupplifun á ramma rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-323">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="0d5d3-324">Þessar útgáfur eru með valkostinn **Virkja hönnunarsnið** sem hægt er að kveikja á.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-324">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="0d5d3-325">Hægt er að finna þennan valkost í flipanum **Almennt** á síðunni **Rafrænar skýrslugerðarfæribreytur** sem hægt er að opna úr vinnusvæðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Kveiktu á hönnunarstillingarvalkosti á síðunni Færibreytur rafrænnar skýrslugerðar](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="0d5d3-327">Ef þú notar eina af þessum útgáfum geturðu greint upplýsingar á mynduðum afkastarakningum beint í forritinu.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-327">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="0d5d3-328">Ekki þarf að flytja þær út úr forritinu og flytja inn í RCS.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-328">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="0d5d3-329">Yfirfara framkvæmdarakningu með utanaðkomandi verkfærum</span><span class="sxs-lookup"><span data-stu-id="0d5d3-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="0d5d3-330">Skilgreina færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="0d5d3-330">Configure user parameters</span></span>

1. <span data-ttu-id="0d5d3-331">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-331">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="0d5d3-332">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="0d5d3-333">Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, í reitnum **Snið framkvæmdarakningar**, skal velja **Perfview XML**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="0d5d3-334">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-334">Run the ER format</span></span>

<span data-ttu-id="0d5d3-335">Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="0d5d3-336">Athugið að netvafrinn býður upp á zip-skrá fyrir niðurhal.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="0d5d3-337">Þessi skrá inniheldur afkastarakningu á PerfView-sniði.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="0d5d3-338">Síðan er hægt að nota greiningarverkfæri fyrir verkfæri PerfView-afkastagreiningar til að greina upplýsingarnar fyrir framkvæmd á sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Rekja upplýsingar fyrir framkvæmt ER-snið í PerfView](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="0d5d3-340">Notaðu ytri verkfæri til að endurskoða framkvæmdarspor sem inniheldur gagnagrunnsfyrirspurnir</span><span class="sxs-lookup"><span data-stu-id="0d5d3-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="0d5d3-341">Vegna úrbóta sem hafa verið gerðar á ER-ramma býður afkastarakningin sem myndast á PerfView-sniði fleiri upplýsingar um framkvæmd ER-sniðs.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="0d5d3-342">Í Microsoft Dynamics 365 for Finance and Operations útgáfu 10.0.4 (júlí 2019) getur þessi rakning einnig innihaldið upplýsingar um framkvæmdar SQL-fyrirspurnir í forritsgagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="0d5d3-343">Skilgreina færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="0d5d3-343">Configure user parameters</span></span>

1. <span data-ttu-id="0d5d3-344">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-344">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0d5d3-345">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="0d5d3-346">Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, skal stilla þessar færibreytur:</span><span class="sxs-lookup"><span data-stu-id="0d5d3-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="0d5d3-347">Í reitnum **Snið framkvæmdarakningar** velurðu **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="0d5d3-348">Stilltu valkostinn **Safna saman tölfræði um fyrirspurnir** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="0d5d3-349">Stillið valkostinn **Rekja fyrirspurn** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-349">Set the **Trace query** option to **Yes**.</span></span>

    ![Svarglugginn Notandafæribreytur](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="0d5d3-351">Keyra snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="0d5d3-351">Run the ER format</span></span>

<span data-ttu-id="0d5d3-352">Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="0d5d3-353">Athugið að netvafrinn býður upp á zip-skrá fyrir niðurhal.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="0d5d3-354">Þessi skrá inniheldur afkastarakningu á PerfView-sniði.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="0d5d3-355">Síðan er hægt að nota greiningarverkfæri fyrir verkfæri PerfView-afkastagreiningar til að greina upplýsingarnar fyrir framkvæmd á sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="0d5d3-356">Þessi rakning inniheldur núna upplýsingar um SQL-gagnagrunnsaðgang við framkvæmd ER-sniðsins.</span><span class="sxs-lookup"><span data-stu-id="0d5d3-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Rekja upplýsingar fyrir framkvæmt ER-snið í PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)