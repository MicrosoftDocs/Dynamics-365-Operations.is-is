---
title: Hanna nýja lausn rafrænnar skýrslugerðar til að prenta sérsniðna skýrslu
description: Þetta efnisatriði útskýrir hvernig á að hanna lausn rafrænnar skýrslugerðar til að prenta sérsniðna skýrslu.
author: NickSelin
manager: AnnBe
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cd0d8e7aa9595e705416798772f52956ef609da
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680243"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="57849-103">Hanna nýja lausn rafrænnar skýrslugerðar til að prenta sérsniðna skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="57849-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra, hönnuðar rafrænnar skýrslugerðar eða hagnýts ráðgjafa rafrænnar skýrslugerðar getur skilgreint færibreytur fyrir ramma rafrænnar skýrslugerðar, hannað nauðsynlegar skilgreiningar rafrænnar skýrslugerðar fyrir nýja lausn rafrænnar skýrslugerðar til að fá aðgang að gögnum tiltekins viðskiptaléns og útbúið sérsniðna skýrslu á Microsoft Office-sniði.</span><span class="sxs-lookup"><span data-stu-id="57849-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="57849-105">Hægt er að ljúka skrefunum í **USMF** fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="57849-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="57849-106">Skilgreina ramma rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="57849-107">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="57849-108">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="57849-109">Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="57849-110">Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="57849-111">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="57849-112">Hanna gagnalíkan fyrir sérstakt lén</span><span class="sxs-lookup"><span data-stu-id="57849-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="57849-113">Flytja inn nýja skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="57849-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="57849-114">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="57849-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="57849-115">Gefa gagnalíkaninu heiti</span><span class="sxs-lookup"><span data-stu-id="57849-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="57849-116">Bæta við reitum gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="57849-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="57849-117">Ljúka hönnun gagnalíkansins</span><span class="sxs-lookup"><span data-stu-id="57849-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="57849-118">Hanna líkanavörpun fyrir skilgreint gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="57849-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="57849-119">Flytja inn nýja skilgreiningu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="57849-120">Stofna nýja skilgreiningu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="57849-121">Hanna nýjan þátt líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="57849-122">Bæta við gagnagjöfum til að fá aðgang að forritstöflum</span><span class="sxs-lookup"><span data-stu-id="57849-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="57849-123">Bæta við gagnagjöfum til að fá aðgang að upptalningum forrits</span><span class="sxs-lookup"><span data-stu-id="57849-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="57849-124">Bæta við merkjum rafrænnar skýrslugerðar til að búa til skýrslu á tilteknu tungumáli</span><span class="sxs-lookup"><span data-stu-id="57849-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="57849-125">Bæta við gagnagjafa til að umbreyta niðurstöðunum við samanburð upptalningargilda og textagilda</span><span class="sxs-lookup"><span data-stu-id="57849-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="57849-126">Tengja gagnagjafa við reiti gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="57849-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="57849-127">Ljúka hönnun líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="57849-128">Hanna sniðmát fyrir sérsniðna skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="57849-129">Setja upp snið</span><span class="sxs-lookup"><span data-stu-id="57849-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="57849-130">Flytja inn hannaða skilgreiningu sniðs</span><span class="sxs-lookup"><span data-stu-id="57849-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="57849-131">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="57849-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="57849-132">Flytja inn skýrslusniðmát</span><span class="sxs-lookup"><span data-stu-id="57849-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="57849-133">Skilgreina snið</span><span class="sxs-lookup"><span data-stu-id="57849-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="57849-134">Skilgreina gagnatengslin fyrir titil skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="57849-135">Fara yfir gagnagjafa líkans</span><span class="sxs-lookup"><span data-stu-id="57849-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="57849-136">Tengja sniðseiningar við reiti gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="57849-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="57849-137">Keyra hannað snið úr rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="57849-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="57849-138">Stilla hannað snið</span><span class="sxs-lookup"><span data-stu-id="57849-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="57849-139">Laga snið til að breyta heiti á mynduðu skjali</span><span class="sxs-lookup"><span data-stu-id="57849-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="57849-140">Laga snið til að breyta röð spurninga</span><span class="sxs-lookup"><span data-stu-id="57849-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="57849-141">Keyra breytt snið úr rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="57849-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="57849-142">Ljúka hönnun sniðs</span><span class="sxs-lookup"><span data-stu-id="57849-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="57849-143">Þróa forritsgervinga til að kalla á hannaða skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="57849-144">Breyta frumkóða</span><span class="sxs-lookup"><span data-stu-id="57849-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="57849-145">Bæta við gagnasamningsklasa</span><span class="sxs-lookup"><span data-stu-id="57849-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="57849-146">Bæta við smiðsklasa notendaviðmóts</span><span class="sxs-lookup"><span data-stu-id="57849-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="57849-147">Bæta við gagnagjafaklasa</span><span class="sxs-lookup"><span data-stu-id="57849-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="57849-148">Bæta við merkjaskrá</span><span class="sxs-lookup"><span data-stu-id="57849-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="57849-149">Bæta við þjónustuklasa skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="57849-150">Bæta við stýriklasa skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="57849-151">Bæta við valmyndaratriði</span><span class="sxs-lookup"><span data-stu-id="57849-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="57849-152">Bæta valmyndaratriði við valmynd</span><span class="sxs-lookup"><span data-stu-id="57849-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="57849-153">Smíða Visual Studio-verk</span><span class="sxs-lookup"><span data-stu-id="57849-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="57849-154">Keyra snið úr forritinu</span><span class="sxs-lookup"><span data-stu-id="57849-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="57849-155">Stilla hannaða lausn rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="57849-156">Breyta líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="57849-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="57849-157">Bæta við gagnagjöfum til að fá aðgang að gagnasamningshlut</span><span class="sxs-lookup"><span data-stu-id="57849-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="57849-158">Bæta við gagnagjafa til að fá aðgang að sniðsvörpunarfærslum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="57849-159">Bæta við gagnagjafa til að fá aðgang að sniðsvörpunarfærslum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="57849-160">Færið inn heiti á sniði rafrænnar skýrslugerðar sem er í gangi í gagnalíkaninu</span><span class="sxs-lookup"><span data-stu-id="57849-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="57849-161">Ljúka hönnun líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="57849-162">Breyta sniði</span><span class="sxs-lookup"><span data-stu-id="57849-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="57849-163">Bæta við nýrri sniðseiningu</span><span class="sxs-lookup"><span data-stu-id="57849-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="57849-164">Tengja viðbætta sniðseiningu</span><span class="sxs-lookup"><span data-stu-id="57849-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="57849-165">Ljúka sniðshönnun</span><span class="sxs-lookup"><span data-stu-id="57849-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="57849-166">Keyra snið úr forritinu</span><span class="sxs-lookup"><span data-stu-id="57849-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="57849-167">Keyra snið úr rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="57849-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="57849-168">Skilgreina áfangastað sniðs fyrir forskoðun á skjá</span><span class="sxs-lookup"><span data-stu-id="57849-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="57849-169">Keyra snið úr forritinu til að forskoða það sem PDF-skjal</span><span class="sxs-lookup"><span data-stu-id="57849-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="57849-170">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="57849-170">Additional resources</span></span>](#References)

<span data-ttu-id="57849-171">Í þessu dæmi er stofnuð ný lausn rafrænnar skýrslugerðar fyrir eininguna [Spurningalisti](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires).</span><span class="sxs-lookup"><span data-stu-id="57849-171">In this example, you will create a new ER solution for the [Questionnaire](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) module.</span></span> <span data-ttu-id="57849-172">Þessi nýja lausn rafrænnar skýrslugerðar gerir þér kleift að hanna skýrslu með því að nota Microsoft Excel-vinnublað sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="57849-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="57849-173">Síðan er hægt að búa til skýrsluna **Spurningalisti** á Excel- eða PDF-sniði ásamt því að mynda fyrirliggjandi skýrslu SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="57849-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="57849-174">Einnig er hægt að breyta nýju skýrslunni seinna, ef um það er beðið.</span><span class="sxs-lookup"><span data-stu-id="57849-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="57849-175">Ekki er þörf á neinni kóðun.</span><span class="sxs-lookup"><span data-stu-id="57849-175">No coding is required.</span></span>

1. <span data-ttu-id="57849-176">Til að keyra fyrirliggjandi skýrslu skal farið í **Spurningalisti** \> **Hanna** \> **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Að velja valmyndaratriði spurningalistaskýrslunnar í spurningalistaeiningunni til að keyra fyrirliggjandi SSRS-skýrslu](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="57849-178">Í svarglugganum **Spurningalistaskýrsla** skal tilgreina valskilyrði.</span><span class="sxs-lookup"><span data-stu-id="57849-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="57849-179">Notið síu þannig að skýrslan feli aðeins í sér spurningalistann **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="57849-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Tilgreina valskilyrði í svarglugga spurningalistaskýrslu](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="57849-181">Eftirfarandi mynd sýnir útbúna útgáfu SSRS-skýrslunnar fyrir spurningalistann **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="57849-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Mynduð SSRS-skýrsla](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="57849-183">Skilgreina ramma rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-183">Configure the ER framework</span></span>

<span data-ttu-id="57849-184">Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að skilgreina lágmarkssafn af færibreytum rafrænnar skýrslugerðar áður en byrjað er að nota ramma rafrænnar skýrslugerðar til að hanna nýja lausn rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="57849-185">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-185">Configure ER parameters</span></span>

1. <span data-ttu-id="57849-186">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="57849-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="57849-187">Í vinnusvæðinu **Rafræn skýrslugerð** velurðu **Rafrænar skýrslufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="57849-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="57849-188">Á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Almennt**, skal stilla valkostinn **Kveikja á hönnunarstillingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="57849-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="57849-189">Í flipanum **Viðhengi** skal stilla eftirfarandi færibreytur:</span><span class="sxs-lookup"><span data-stu-id="57849-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="57849-190">Stillið reitinn **Skilgreiningar** á **Skrá** fyrir fyrirtækið **USMF**.</span><span class="sxs-lookup"><span data-stu-id="57849-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="57849-191">Stillið **Verksafn**, **Tímabundið**, **Grunnlína** og **Annað** reitina á **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="57849-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="57849-192">Frekari upplýsingar um færibreytur rafrænnar skýrslugerðar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="57849-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="57849-193">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="57849-194">Allar skilgreiningar rafrænnar skýrslugerðar eru merktar í eigu skilgreiningarveitu rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="57849-195">Þess vegna þarf að virkja skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð** áður en byrjað er að bæta við eða breyta einhverjum skilgreiningum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="57849-196">Aðeins eigandi skilgreiningar rafrænnar skýrslugerðar getur breytt henni.</span><span class="sxs-lookup"><span data-stu-id="57849-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="57849-197">Þess vegna, áður en hægt er að breyta skilgreiningu rafrænnar skýrslugerðar, verður að virkja viðeigandi skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="57849-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="57849-198">Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="57849-199">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="57849-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="57849-200">Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Viðeigandi tenglar**, skal velja **Skilgreiningarveitur**.</span><span class="sxs-lookup"><span data-stu-id="57849-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="57849-201">Á síðunni **Skilgreiningarveitur** er hver færsla skilgreiningarveitu með einkvæmt heiti og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="57849-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="57849-202">Farið yfir efnið á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="57849-202">Review the contents of this page.</span></span> <span data-ttu-id="57849-203">Ef færsla fyrir **Litware, Inc.** (`https://www.litware.com`) er þegar til skal sleppa næsta ferli, [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="57849-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="57849-204">Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="57849-205">Á síðunni **Skilgreiningarveitur** skal velja **Ný**.</span><span class="sxs-lookup"><span data-stu-id="57849-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="57849-206">Í reitinn **Heiti** skal færa inn **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="57849-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="57849-207">Í reitinn **Veffang** skal færa inn `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="57849-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="57849-208">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="57849-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="57849-209">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="57849-210">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="57849-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="57849-211">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja skilgreiningarveituna **Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="57849-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="57849-212">Veldu **Stilla sem virkt**.</span><span class="sxs-lookup"><span data-stu-id="57849-212">Select **Set active**.</span></span>

<span data-ttu-id="57849-213">Nánari upplýsingar um skilgreiningarveitur rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="57849-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="57849-214">Hanna gagnalíkan fyrir sérstakt lén</span><span class="sxs-lookup"><span data-stu-id="57849-214">Design a domain-specific data model</span></span>

<span data-ttu-id="57849-215">Stofna þarf nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur [gagnalíkan](general-electronic-reporting.md#data-model-and-model-mapping-components)íhlut fyrir fyrirtækislénið **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="57849-216">Þetta gagnalíkan verður seinna notað sem gagnagjafi þegar hannað er snið rafrænnar skýrslugerðar til að búa til skýrsluna **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="57849-217">Með því að ljúka skrefunum í hlutanum [Flytja inn nýja skilgreiningu gagnalíkans](#ImportDataModel) er hægt að flytja inn nauðsynlegt gagnalíkan úr uppgefinni XML-skrá.</span><span class="sxs-lookup"><span data-stu-id="57849-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="57849-218">Að öðrum kosti er hægt að ljúka skrefunum í hlutanum [Stofna nýjan skilgreiningu gagnalíkans](#DesignDataModel) til að hanna þetta gagnalíkan frá grunni.</span><span class="sxs-lookup"><span data-stu-id="57849-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="57849-219">Flytja inn nýja skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="57849-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="57849-220">Sæktu skrána [Spurningalistar model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) og vistaðu hana á staðbundinni tölvu.</span><span class="sxs-lookup"><span data-stu-id="57849-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="57849-221">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="57849-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="57849-222">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="57849-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="57849-223">Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="57849-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="57849-224">Veljið **Fletta** og finnið síðan og veljið skrána **Spurningalistar model.version.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="57849-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="57849-225">Veljið **Í lagi** til að flytja inn skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="57849-226">Til að halda áfram skal sleppa næsta ferli, [Stofna nýjan skilgreiningu gagnalíkans](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="57849-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="57849-227">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="57849-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="57849-228">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="57849-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="57849-229">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="57849-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="57849-230">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="57849-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="57849-231">Í fellistagluggann, í reitinn **Heiti**, skal færa inn **Líkan spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="57849-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="57849-232">Veljið **Stofna skilgreiningu** til að stofna skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="57849-233">Gefa gagnalíkaninu heiti</span><span class="sxs-lookup"><span data-stu-id="57849-233">Name the data model</span></span>

1. <span data-ttu-id="57849-234">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="57849-235">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="57849-235">Select **Designer**.</span></span>
3. <span data-ttu-id="57849-236">Á síðunni **Hönnuður gagnalíkana**, í flýtiflipanum **Almennt**, í reitinn **Heiti**, skal færa inn <a name="DataModeName"></a>**Spurningalistar**.</span><span class="sxs-lookup"><span data-stu-id="57849-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="57849-237">Bæta við nýjum gagnalíkanareitum</span><span class="sxs-lookup"><span data-stu-id="57849-237">Add new data model fields</span></span>

1. <span data-ttu-id="57849-238">Á síðunni **Hönnuður gagnalíkans** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="57849-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="57849-239">Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="57849-240">Veljið **Rót líkans** sem gerð nýja hnútsins.</span><span class="sxs-lookup"><span data-stu-id="57849-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="57849-241">Í reitinn **Heiti** skal færa inn <a name="RootDefinitionName"></a>**Rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="57849-242">Veljið **Bæta við** til að bæta við nýja hnútnum.</span><span class="sxs-lookup"><span data-stu-id="57849-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="57849-243">Þessi rótarlýsing verður notuð til að útvega gögn fyrir skýrsluna **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="57849-244">Eitt gagnalíkan getur haft margar lýsingar.</span><span class="sxs-lookup"><span data-stu-id="57849-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="57849-245">Hver lýsing getur átt við um eitt snið rafrænnar skýrslugerðar til að finna gögn sem þarf til að mynda skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="57849-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="57849-246">Veljið **Nýtt** aftur og síðan, í fellilistaglugganum til að bæta við gagnalíkanshnút, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="57849-247">Veljið **Undireiningu virks hnúts** sem gerð nýja hnútsins.</span><span class="sxs-lookup"><span data-stu-id="57849-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="57849-248">Í reitinn **Heiti** skal færa inn **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="57849-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="57849-249">Í reitnum **Gerð vöru** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="57849-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="57849-250">Veljið **Bæta við** til að bæta við nýja reitnum.</span><span class="sxs-lookup"><span data-stu-id="57849-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="57849-251">Þessi reitur er nauðsynlegur til að flytja heiti núverandi fyrirtækis yfir í skýrslu rafrænnar skýrslugerðar sem notar þetta gagnalíkan sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="57849-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="57849-252">Veljið **Nýtt** aftur og síðan, í fellilistaglugganum til að bæta við gagnalíkanshnút, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="57849-253">Veljið **Undireiningu virks hnúts** sem gerð nýja hnútsins.</span><span class="sxs-lookup"><span data-stu-id="57849-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="57849-254">Í reitinn **Heiti** skal færa inn **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="57849-255">Í reitnum **Gerð vöru** velurðu **Skráalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="57849-256">Veljið **Bæta við** til að bæta við nýja reitnum.</span><span class="sxs-lookup"><span data-stu-id="57849-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="57849-257">Þessi reitur verður notaður til að flytja lista af spurningalistum í skýrslu rafrænnar skýrslugerðar sem notar þetta gagnalíkan sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="57849-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="57849-258">Veljið hnútinn **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="57849-259">Haldið áfram að bæta nauðsynlegum reitum við breytanlega gagnalíkanið með sama hætti þar til lokið er við eftirfarandi skipulag gagnalíkans.</span><span class="sxs-lookup"><span data-stu-id="57849-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="57849-260">Slóð á reit</span><span class="sxs-lookup"><span data-stu-id="57849-260">Field path</span></span>                                                    | <span data-ttu-id="57849-261">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="57849-261">Data type</span></span>   | <span data-ttu-id="57849-262">Tilnefndur reitur/skilað gildi</span><span class="sxs-lookup"><span data-stu-id="57849-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="57849-263">Rót</span><span class="sxs-lookup"><span data-stu-id="57849-263">Root</span></span>                                                          |             | <span data-ttu-id="57849-264">Tilvísunarpunktur til að biðja um gögn spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="57849-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="57849-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="57849-266">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-266">String</span></span>      | <span data-ttu-id="57849-267">Heiti núverandi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="57849-267">The name of the current company.</span></span> |
    | <span data-ttu-id="57849-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="57849-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="57849-269">Færsla</span><span class="sxs-lookup"><span data-stu-id="57849-269">Record</span></span>      | <span data-ttu-id="57849-270">Upplýsingar um keyrslusnið.</span><span class="sxs-lookup"><span data-stu-id="57849-270">Format execution details.</span></span> |
    | <span data-ttu-id="57849-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="57849-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="57849-272">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-272">String</span></span>      | <span data-ttu-id="57849-273">Heiti sniðs rafrænnar skýrslugerðar sem verið er að keyra.</span><span class="sxs-lookup"><span data-stu-id="57849-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="57849-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="57849-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="57849-275">Færslulisti</span><span class="sxs-lookup"><span data-stu-id="57849-275">Record list</span></span> | <span data-ttu-id="57849-276">Listi yfir spurningalista</span><span class="sxs-lookup"><span data-stu-id="57849-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="57849-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="57849-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="57849-278">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-278">String</span></span>      | <span data-ttu-id="57849-279">Staða núverandi spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="57849-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="57849-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="57849-281">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-281">String</span></span>      | <span data-ttu-id="57849-282">Kóði núverandi spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="57849-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="57849-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="57849-284">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-284">String</span></span>      | <span data-ttu-id="57849-285">Lýsing núverandi spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="57849-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="57849-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="57849-287">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-287">String</span></span>      | <span data-ttu-id="57849-288">Gerð núgildandi spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="57849-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="57849-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="57849-290">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-290">String</span></span>      | <span data-ttu-id="57849-291">Númeraröð núgildandi spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="57849-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="57849-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="57849-293">Færsla</span><span class="sxs-lookup"><span data-stu-id="57849-293">Record</span></span>      | <span data-ttu-id="57849-294">Niðurstöðufæribreytur núverandi spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="57849-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="57849-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="57849-296">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-296">String</span></span>      | <span data-ttu-id="57849-297">Auðkenniskóði núverandi niðurstöðuflokks.</span><span class="sxs-lookup"><span data-stu-id="57849-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="57849-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="57849-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="57849-299">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-299">String</span></span>      | <span data-ttu-id="57849-300">Lýsing á núverandi niðurstöðuflokki.</span><span class="sxs-lookup"><span data-stu-id="57849-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="57849-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="57849-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="57849-302">Rauntala</span><span class="sxs-lookup"><span data-stu-id="57849-302">Real</span></span>        | <span data-ttu-id="57849-303">Hámarksfjöldi punkta sem hægt var að vinna sér inn.</span><span class="sxs-lookup"><span data-stu-id="57849-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="57849-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="57849-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="57849-305">Færslulisti</span><span class="sxs-lookup"><span data-stu-id="57849-305">Record list</span></span> | <span data-ttu-id="57849-306">Listi yfir spurningar fyrir núverandi spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="57849-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="57849-308">Heiltala</span><span class="sxs-lookup"><span data-stu-id="57849-308">Integer</span></span>     | <span data-ttu-id="57849-309">Raðnúmer núverandi samantekt af svörum.</span><span class="sxs-lookup"><span data-stu-id="57849-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="57849-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="57849-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="57849-311">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-311">String</span></span>      | <span data-ttu-id="57849-312">Auðkenniskóði núverandi spurningar.</span><span class="sxs-lookup"><span data-stu-id="57849-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="57849-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="57849-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="57849-314">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-314">String</span></span>      | <span data-ttu-id="57849-315">Flagg sem gefur til kynna hvort svara þurfi núverandi spurningu.</span><span class="sxs-lookup"><span data-stu-id="57849-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="57849-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="57849-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="57849-317">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-317">String</span></span>      | <span data-ttu-id="57849-318">Flagg sem segir til um hvort núverandi spurning er aðalspurning.</span><span class="sxs-lookup"><span data-stu-id="57849-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="57849-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="57849-320">Heiltala</span><span class="sxs-lookup"><span data-stu-id="57849-320">Integer</span></span>     | <span data-ttu-id="57849-321">Raðnúmer núverandi spurningar.</span><span class="sxs-lookup"><span data-stu-id="57849-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="57849-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="57849-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="57849-323">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-323">String</span></span>      | <span data-ttu-id="57849-324">Texti núverandi spurningar.</span><span class="sxs-lookup"><span data-stu-id="57849-324">The text of the current question.</span></span> |
    | <span data-ttu-id="57849-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="57849-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="57849-326">Færslulisti</span><span class="sxs-lookup"><span data-stu-id="57849-326">Record list</span></span> | <span data-ttu-id="57849-327">Svaralisti fyrir núverandi spurningu.</span><span class="sxs-lookup"><span data-stu-id="57849-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="57849-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="57849-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="57849-329">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-329">String</span></span>      | <span data-ttu-id="57849-330">Flagg sem segir til um hvort núverandi svar er rétt.</span><span class="sxs-lookup"><span data-stu-id="57849-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="57849-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="57849-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="57849-332">Rauntala</span><span class="sxs-lookup"><span data-stu-id="57849-332">Real</span></span>        | <span data-ttu-id="57849-333">Punktar sem eru unnir þegar gildandi svar er valið.</span><span class="sxs-lookup"><span data-stu-id="57849-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="57849-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="57849-335">Heiltala</span><span class="sxs-lookup"><span data-stu-id="57849-335">Integer</span></span>     | <span data-ttu-id="57849-336">Raðnúmer núverandi svars.</span><span class="sxs-lookup"><span data-stu-id="57849-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="57849-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="57849-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="57849-338">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-338">String</span></span>      | <span data-ttu-id="57849-339">Texti núverandi svars.</span><span class="sxs-lookup"><span data-stu-id="57849-339">The text of the current answer.</span></span> |

    <span data-ttu-id="57849-340">Eftirfarandi mynd sýnir breytanlegt gagnalíkan sem er lokið á síðunni **Hönnuður gagnalíkans**.</span><span class="sxs-lookup"><span data-stu-id="57849-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Skilgreint gagnalíkan í gagnalíkanahönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="57849-342">Vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="57849-342">Save your changes.</span></span>
8. <span data-ttu-id="57849-343">Lokið síðunni **Hönnuður gagnalíkans**.</span><span class="sxs-lookup"><span data-stu-id="57849-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="57849-344">Ljúka hönnun gagnalíkansins</span><span class="sxs-lookup"><span data-stu-id="57849-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="57849-345">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-346">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="57849-347">Í flýtiflipanum **Útgáfur** skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="57849-348">Veljið **Breyta stöðu** \> **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="57849-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="57849-349">Staða á útgáfu 1 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="57849-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="57849-350">Ekki er lengur hægt að breyta útgáfu 1.</span><span class="sxs-lookup"><span data-stu-id="57849-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="57849-351">Þessi útgáfa inniheldur skilgreinda gagnalíkanið og er hægt að nota sem grunninn fyrir aðrar skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="57849-352">Útgáfa 2 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="57849-353">Hægt er að breyta þessari útgáfu til að leiðrétta gagnalíkanið **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Útgáfur breytanlegra skilgreininga rafrænnar skýrslugerðar á skilgreiningarsíðunni](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="57849-355">Frekari upplýsingar um útgáfustjórnun fyrir skilgreiningar rafrænnar skýrslugerðar er að finna í [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="57849-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="57849-356">Skilgreinda gagnalíkanið er óhlutdræg framsetning þín á fyrirtækisléninu **Spurningalisti** og inniheldur engin tengsl við gervinga sem eru sértækir fyrir Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="57849-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="57849-357">Hanna líkanavörpun fyrir skilgreint gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="57849-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="57849-358">Sem notandi í hönnunarhlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur íhlut [líkanavörpunar](general-electronic-reporting.md#data-model-and-model-mapping-components) fyrir gagnalíkanið **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="57849-359">Vegna þess að þessi íhlutur innleiðir skilgreint gagnalíkan fyrir Finance, á hann sérstaklega við um Finance.</span><span class="sxs-lookup"><span data-stu-id="57849-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="57849-360">Skilgreina verður íhlut líkanavörpunar til að tilgreina hugbúnaðarhluti sem þarf að nota til að fylla út skilgreint gagnalíkan með forritsgögnum við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="57849-361">Til að ljúka þessu verki þarf að gera sér grein fyrir upplýsingum innleiðingar fyrir gagnaskipulagið á fyrirtækisléninu **Spurningalisti** í Finance.</span><span class="sxs-lookup"><span data-stu-id="57849-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="57849-362">Með því að ljúka skrefunum í hlutanum [Flytja inn nýja skilgreiningu gagnalíkans](#ImportModelMapping) sem fylgja, er hægt að flytja inn nauðsynlega skilgreiningu líkanavörpunar úr uppgefinni XML-skrá.</span><span class="sxs-lookup"><span data-stu-id="57849-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="57849-363">Að öðrum kosti er hægt að ljúka skrefunum í hlutanum [Stofna nýja skilgreiningu líkanavörpunar](#CreateModelMapping) til að hanna þessa líkanavörpun frá grunni.</span><span class="sxs-lookup"><span data-stu-id="57849-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="57849-364">Flytja inn nýja skilgreiningu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="57849-365">Sækið skrána [Spurningalistar mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) og vistið hana á staðbundinni tölvu.</span><span class="sxs-lookup"><span data-stu-id="57849-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="57849-366">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="57849-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="57849-367">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="57849-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="57849-368">Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="57849-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="57849-369">Veljið **Fletta** og finnið síðan og veljið skrána **Spurningalistar mapping.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="57849-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="57849-370">Veljið **Í lagi** til að flytja inn skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="57849-371">Til að halda áfram skal sleppa næsta ferli, [Stofna nýja skilgreiningu líkanavörpunar](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="57849-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="57849-372">Stofna nýja skilgreiningu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="57849-373">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-374">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="57849-375">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="57849-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="57849-376">Í fellilistanum skaltu fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="57849-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span><span class="sxs-lookup"><span data-stu-id="57849-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="57849-378">Í reitinn **Heiti** skal færa inn **Vörpun spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="57849-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="57849-379">Í reitnum **Skilgreining gagnalíkans** skal velja **Rótar** skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="57849-380">Veljið **Stofna skilgreiningu** til að stofna skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="57849-381">Hanna nýjan þátt líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="57849-382">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="57849-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="57849-383">Veldu **Hönnuður** til að opna lista yfir varpanir.</span><span class="sxs-lookup"><span data-stu-id="57849-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="57849-384">Veljið vörpunina **Vörpun spurningalista** sem var sjálfkrafa bætt við fyrir **Rótar** skilgreininguna</span><span class="sxs-lookup"><span data-stu-id="57849-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="57849-385">Veljið **Hönnuður** til að hefja skilgreiningu á valdri vörpun.</span><span class="sxs-lookup"><span data-stu-id="57849-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="57849-386">Nýrri vörpun er sjálfkrafa bætt við fyrir **Rótar** skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="57849-387">Þessi vörpun er með stefnuna **Til líkans**.</span><span class="sxs-lookup"><span data-stu-id="57849-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="57849-388">Þess vegna er hægt að nota þessa vörpun til að fylla út gagnalíkan með nauðsynlegum gögnum.</span><span class="sxs-lookup"><span data-stu-id="57849-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="57849-389">Bæta við gagnagjöfum til að fá aðgang að forritstöflum</span><span class="sxs-lookup"><span data-stu-id="57849-389">Add data sources to access application tables</span></span>

<span data-ttu-id="57849-390">Skilgreina þarf gagnagjafa til að fá aðgang að forritstöflum sem innihalda upplýsingar um spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="57849-391">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="57849-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="57849-392">Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að töflunni KMCollection, þar sem sérhver færsla stendur fyrir stakan spurningalista:</span><span class="sxs-lookup"><span data-stu-id="57849-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="57849-393">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="57849-394">Í svarglugganum, í reitinn **Heiti**, skal færa inn **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="57849-395">Í reitinn **Tafla** skal færa inn **KMCollection**.</span><span class="sxs-lookup"><span data-stu-id="57849-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="57849-396">Stillið valkostinn **Biðja um fyrirspurn** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="57849-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="57849-397">Þá er hægt að tilgreina valkosti [síunar](../../fin-ops/get-started/advanced-filtering-query-options.md) fyrir þessa töflu í svarglugga fyrirspurnar í kerfinu við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="57849-398">Veljið **Í lagi** til að bæta við nýja gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="57849-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="57849-399">Í rúðunni **Gerðir gagnagjafa** skal velja **Dynamics 365 for Operations\\Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="57849-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="57849-400">Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að töflunni KMQuestion, þar sem sérhver færsla stendur fyrir staka spurningu í spurningalista:</span><span class="sxs-lookup"><span data-stu-id="57849-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="57849-401">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="57849-402">Í glugganum, í reitinn **Heiti**, skal slá inn **Spurning**.</span><span class="sxs-lookup"><span data-stu-id="57849-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="57849-403">Í reitinn **Tafla** skal færa inn **KMQuestion**.</span><span class="sxs-lookup"><span data-stu-id="57849-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="57849-404">Veljið **Í lagi** til að bæta við nýja gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="57849-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="57849-405">Í rúðunni **Gerðir gagnagjafa** skal velja **Dynamics 365 for Operations\\Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="57849-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="57849-406">Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að töflunni KMAnswer, þar sem sérhver færsla stendur fyrir eitt svar við spurningu í spurningalista:</span><span class="sxs-lookup"><span data-stu-id="57849-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="57849-407">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="57849-408">Í reitinn **Heiti** skal færa inn **Svar**.</span><span class="sxs-lookup"><span data-stu-id="57849-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="57849-409">Í reitinn **Tafla** skal færa inn **KMAnswer**.</span><span class="sxs-lookup"><span data-stu-id="57849-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="57849-410">Veljið **Í lagi** til að bæta við nýja gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="57849-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="57849-411">Í rúðunni **Gerðir gagnagjafa** skal velja **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="57849-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="57849-412">Bætið við nýjum reiknuðum reit sem verður notaður til að opna færslu í töflunni KMQuestionResultGroup úr öllum færslum í yfirtöflunni KMCollection:</span><span class="sxs-lookup"><span data-stu-id="57849-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="57849-413">Í rúðunni **Gagnagjafar** skal velja **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="57849-414">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="57849-414">Select **Add**.</span></span>
    3. <span data-ttu-id="57849-415">Í glugganum, í reitinn **Heiti**, skal slá inn **\$ResultGroup**.</span><span class="sxs-lookup"><span data-stu-id="57849-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="57849-416">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="57849-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="57849-417">Í [Formúluritill rafrænnar skýrslugerðar](general-electronic-reporting-formula-designer.md), í reitinn **Formúla**, skal færa inn **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** til að nota [slóðina](er-formula-language.md#paths) á tengslin „frá einu í margt“ milli taflanna KMCollection og KMQuestionResultGroup.</span><span class="sxs-lookup"><span data-stu-id="57849-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="57849-418">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="57849-419">Veljið **Í lagi** til að bæta við nýja reiknaða reitnum.</span><span class="sxs-lookup"><span data-stu-id="57849-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="57849-420">Í rúðunni **Gerðir gagnagjafa** skal velja **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="57849-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="57849-421">Bætið við nýjum reiknuðum reit sem verður notaður til að opna spurningafærslur í töflunni KMQuestion úr öllum færslum í yfirtöflunni KMCollectionQuestion:</span><span class="sxs-lookup"><span data-stu-id="57849-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="57849-422">Í rúðunni **Gagnagjafar** skal velja **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="57849-423">Útvíkkið hnútinn **\<Tengsl** sem inniheldur tengslin „frá einu í margt“ á töflunni KMCollection.</span><span class="sxs-lookup"><span data-stu-id="57849-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="57849-424">Veljið tengdu **KMCollectionQuestion** töfluna og veljið síðan **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="57849-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="57849-425">Í glugganum, í reitinn **Heiti**, skal slá inn **\$Spurning**.</span><span class="sxs-lookup"><span data-stu-id="57849-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="57849-426">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="57849-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="57849-427">Í formúluritilinn, í reitinn **Formúla**, skal færa inn **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** til að skila viðeigandi spurningafærslum úr töflunni KMQuestion.</span><span class="sxs-lookup"><span data-stu-id="57849-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="57849-428">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="57849-429">Veljið **Í lagi** til að bæta við nýja reiknaða reitnum.</span><span class="sxs-lookup"><span data-stu-id="57849-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="57849-430">Í rúðunni **Gerðir gagnagjafa** skal velja **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="57849-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="57849-431">Bætið við nýjum reiknuðum reit sem verður notaður til að opna svarafærslur í töflunni KMAnswer úr öllum færslum í yfirtöflunni KMQuestion:</span><span class="sxs-lookup"><span data-stu-id="57849-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="57849-432">Í rúðunni **Gagnagjafar** skal velja **Spurningalisti.\<Relations.KMCollectionQuestion.\$Question** og síðan velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="57849-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="57849-433">Í glugganum, í reitinn **Heiti**, skal slá inn **\$Svar**.</span><span class="sxs-lookup"><span data-stu-id="57849-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="57849-434">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="57849-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="57849-435">Í formúluritilinn, í reitinn **Formúla**, skal slá inn **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** til að skila viðeigandi svarfærslum úr töflunni KMAnswer.</span><span class="sxs-lookup"><span data-stu-id="57849-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="57849-436">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="57849-437">Veljið **Í lagi** til að bæta við nýja reiknaða reitnum.</span><span class="sxs-lookup"><span data-stu-id="57849-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="57849-438">Í rúðunni **Gerðir gagnagjafa** skal velja **Dynamics 365 for Operations\\Tafla**.</span><span class="sxs-lookup"><span data-stu-id="57849-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="57849-439">Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að aðferðum töflunnar CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="57849-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="57849-440">Athugið að **find()** aðferðin í þessari töflu skilar færslu sem stendur fyrir fyrirtæki núverandi Finance-tilvik sem þessi vörpun er kölluð í samhengi við.</span><span class="sxs-lookup"><span data-stu-id="57849-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="57849-441">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="57849-442">Í glugganum, í reitinn **Heiti**, skal slá inn **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="57849-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="57849-443">Í reitinn **Tafla** skal slá inn **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="57849-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="57849-444">Veljið **Í lagi** til að bæta við nýja gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="57849-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="57849-445">Bæta við gagnagjöfum til að fá aðgang að upptalningum forrits</span><span class="sxs-lookup"><span data-stu-id="57849-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="57849-446">Skilgreina þarf gagnagjafa til að fá aðgang að upptalningum forrits og bera saman gildin við gildin í reitum af gerðinni **Upptalning** í forritstöflunum.</span><span class="sxs-lookup"><span data-stu-id="57849-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="57849-447">Nota verður niðurstöðu samanburðarins til að fylla út viðeigandi reiti gagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="57849-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="57849-448">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Upptalning**.</span><span class="sxs-lookup"><span data-stu-id="57849-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="57849-449">Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að gildum upptalningarinnar **EnumAppNoYes**:</span><span class="sxs-lookup"><span data-stu-id="57849-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="57849-450">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="57849-451">Í glugganum, í reitnum **Heiti**, skal slá inn **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="57849-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="57849-452">Í reitinn **Upptalning** skal færa inn **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="57849-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="57849-453">Veljið **Í lagi** til að bæta við nýja gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="57849-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="57849-454">Í rúðunni **Gerðir gagnagjafa** skal velja **Dynamics 365 for Operations\\Upptalning**.</span><span class="sxs-lookup"><span data-stu-id="57849-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="57849-455">Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að gildum upptalningarinnar **KMCollectionQuestionMode**:</span><span class="sxs-lookup"><span data-stu-id="57849-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="57849-456">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="57849-457">Í glugganum, í reitnum **Heiti**, skal slá inn **EnumAppQuestionOrder**.</span><span class="sxs-lookup"><span data-stu-id="57849-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="57849-458">Í reitinn **Upptalning** skal færa inn **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="57849-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="57849-459">Veljið **Í lagi** til að bæta við nýja gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="57849-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="57849-460">Bæta við merkjum rafrænnar skýrslugerðar til að búa til skýrslu á tilteknu tungumáli</span><span class="sxs-lookup"><span data-stu-id="57849-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="57849-461">Hægt er að bæta við merkum rafrænnar skýrslugerðar til að skilgreina suma gagnagjafana þannig að þeir skili gildum sem eru háð tungumálinu sem er skilgreint í samhengi við kall líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="57849-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="57849-462">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnagjafar**, skal velja **Svar** og síðan velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="57849-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="57849-463">Virkjið reitinn **Merki**.</span><span class="sxs-lookup"><span data-stu-id="57849-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="57849-464">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="57849-464">Select **Translate**.</span></span>
4. <span data-ttu-id="57849-465">Í svarglugganum **Textaþýðing** skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="57849-466">Í reitinn **Kenni merkis** skal færa inn **PositiveAnswer**.</span><span class="sxs-lookup"><span data-stu-id="57849-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="57849-467">Í reitinn **Texti á sjálfgefnu tungumáli** skal færa inn **Já**.</span><span class="sxs-lookup"><span data-stu-id="57849-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="57849-468">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="57849-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="57849-469">Í reitinn **Kenni merkis** skal færa inn **NegativeAnswer**.</span><span class="sxs-lookup"><span data-stu-id="57849-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="57849-470">Í reitinn **Texti á sjálfgefnu tungumáli** skal færa inn **No**.</span><span class="sxs-lookup"><span data-stu-id="57849-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="57849-471">Veldu **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="57849-471">Select **Translate**.</span></span>

5. <span data-ttu-id="57849-472">Lokið svarglugganum **Textaþýðing**.</span><span class="sxs-lookup"><span data-stu-id="57849-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="57849-473">Veldu **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="57849-473">Select **Cancel**.</span></span>

![Að bæta við merkjum rafrænnar skýrslugerðar fyrir breytanlega líkanavörpun](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="57849-475">Aðeins er búið að færa inn merki fyrir sjálfgefna tungumálið.</span><span class="sxs-lookup"><span data-stu-id="57849-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="57849-476">Frekari upplýsingar um hvernig hægt er að þýða merki rafrænnar skýrslugerðar á önnur tungumál er að finna í [Hanna skýrslur á mörgum tungumálum](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="57849-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="57849-477">Bæta við gagnagjafa til að umbreyta niðurstöðunum við samanburð upptalningargilda og textagilda</span><span class="sxs-lookup"><span data-stu-id="57849-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="57849-478">Fyrst að nauðsynlegt er að umbreyta niðurstöðum samanburðarins milli upptalningargilda og textagilda nokkrum sinnum fyrir mismunandi uppruna, er góð hugmynd að skilgreina þessi rök sem stakan gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="57849-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="57849-479">Til að geta notað þennan gagnagjafa aftur þarf hinsvegar að skilgreina hann sem gagnagjafa með færibreytum.</span><span class="sxs-lookup"><span data-stu-id="57849-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="57849-480">Frekari upplýsingar er að finna í [Styðja færibreytuköll á gagnagjöfum rafrænnar skýrslugerðar af gerðinni reiknaður reitur](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="57849-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="57849-481">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Almennt\\Autt hólf**.</span><span class="sxs-lookup"><span data-stu-id="57849-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="57849-482">Bæta við nýju hólfi gagnagjafa:</span><span class="sxs-lookup"><span data-stu-id="57849-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="57849-483">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="57849-484">Í glugganum, í reitnum **Heiti**, skal slá inn **Hjálp**.</span><span class="sxs-lookup"><span data-stu-id="57849-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="57849-485">Veljið **Í lagi** til að bæta við nýja hólfi gagnagjafans.</span><span class="sxs-lookup"><span data-stu-id="57849-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="57849-486">Í rúðunni **Gerðir gagnagjafa** skal velja **Aðgerðir\\Reiknaður reitur**.</span><span class="sxs-lookup"><span data-stu-id="57849-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="57849-487">Bæta við nýjum gagnagjafa:</span><span class="sxs-lookup"><span data-stu-id="57849-487">Add a new data source:</span></span>

    1. <span data-ttu-id="57849-488">Í rúðunni **Gagnagjafar** skal velja **Hjálp**.</span><span class="sxs-lookup"><span data-stu-id="57849-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="57849-489">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="57849-489">Select **Add**.</span></span>
    3. <span data-ttu-id="57849-490">Í glugganum, í reitinn **Heiti**, skal slá inn **NoYesEnumToString**.</span><span class="sxs-lookup"><span data-stu-id="57849-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="57849-491">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="57849-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="57849-492">Í formúluritlinum skal velja **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="57849-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="57849-493">Fylgið þessum skrefum til að tilgreina færibreytur fyrir skilgreinda segð:</span><span class="sxs-lookup"><span data-stu-id="57849-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="57849-494">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="57849-494">Select **New**.</span></span>
        2. <span data-ttu-id="57849-495">Í glugganum, í reitinn **Heiti**, skal slá inn **Frumbreyta**.</span><span class="sxs-lookup"><span data-stu-id="57849-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="57849-496">Í reitinn **Gerð** skal velja gagnagerðina **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="57849-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="57849-497">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57849-497">Select **OK**.</span></span>

    7. <span data-ttu-id="57849-498">Í reitinn **Formúla** skal slá inn **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** til að skila texta viðeigandi merkis rafrænnar skýrslugerðar, háð tungumálinu í samhengi við keyrsluna og gildi tiltekinnar færibreytu.</span><span class="sxs-lookup"><span data-stu-id="57849-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="57849-499">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="57849-500">Veljið **Í lagi** til að bæta við nýja gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="57849-500">Select **OK** to add the new data source.</span></span>

![Skilgreind líkanavörpun í hönnuði líkanavörpunar rafrænnar skýrslugerðar](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="57849-502">Tengja gagnagjafa við reiti gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="57849-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="57849-503">Nauðsynlegt er að tengja skilgreinda gagnagjafa við reiti gagnalíkansins til að tilgreina hvernig fyllt verðu út í gagnalíkanið með forritsgögnum við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="57849-504">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnalíkan**, skal velja **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="57849-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="57849-505">Í rúðunni **Gagnagjafar** skal útvíkka **CompanyInfo** og síðan fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="57849-506">Útvíkkið hnútinn **CompanyInfo.find()** sem stendur fyrir aðferðina **find()** fyrir töfluna CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="57849-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="57849-507">Veljið **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="57849-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="57849-508">Veljið **Tengja** til að fylla út heiti fyrirtækisins sem er í samhengi við skilgreinda líkanavörpun sem kallað er á við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="57849-509">Í rúðunni **Gagnalíkan** skal velja **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="57849-510">Í rúðunni **Gagnagjafar** skal velja **Spurningalisti** og síðan velja **Tengja** til að fylla út í færslur spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="57849-511">Í rúðunni **Gagnalíkan** skal útvíkka **Spurningalisti** og síðan fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="57849-512">Í rúðunni **Gagnalíkan** skal velja **Virkt**.</span><span class="sxs-lookup"><span data-stu-id="57849-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="57849-513">Í rúðunni **Gagnalíkan** skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="57849-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="57849-514">Í reitinn **Formúla** skal færa inn **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** til að fylla út samanburð á upptalningargildum textaháðrar og tungumálaháðrar niðurstöðu.</span><span class="sxs-lookup"><span data-stu-id="57849-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="57849-515">Haldið áfram að tengja gagnagjafa við reiti gagnalíkans með sama hætti þar til eftirfarandi niðurstöðum er náð.</span><span class="sxs-lookup"><span data-stu-id="57849-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="57849-516">Slóð á reit</span><span class="sxs-lookup"><span data-stu-id="57849-516">Field path</span></span>                                              | <span data-ttu-id="57849-517">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="57849-517">Data type</span></span>   | <span data-ttu-id="57849-518">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-518">Action</span></span> | <span data-ttu-id="57849-519">Segð tengingar</span><span class="sxs-lookup"><span data-stu-id="57849-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="57849-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="57849-520">CompanyName</span></span>                                             | <span data-ttu-id="57849-521">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-521">String</span></span>      | <span data-ttu-id="57849-522">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-522">Bind</span></span>   | <span data-ttu-id="57849-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="57849-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="57849-524">Spurningalisti</span><span class="sxs-lookup"><span data-stu-id="57849-524">Questionnaire</span></span>                                           | <span data-ttu-id="57849-525">Færslulisti</span><span class="sxs-lookup"><span data-stu-id="57849-525">Record list</span></span> | <span data-ttu-id="57849-526">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-526">Bind</span></span>   | <span data-ttu-id="57849-527">Spurningalisti</span><span class="sxs-lookup"><span data-stu-id="57849-527">Questionnaire</span></span> |
    | <span data-ttu-id="57849-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="57849-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="57849-529">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-529">String</span></span>      | <span data-ttu-id="57849-530">Breyta</span><span class="sxs-lookup"><span data-stu-id="57849-530">Edit</span></span>   | <span data-ttu-id="57849-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="57849-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="57849-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="57849-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="57849-533">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-533">String</span></span>      | <span data-ttu-id="57849-534">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-534">Bind</span></span>   | <span data-ttu-id="57849-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="57849-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="57849-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="57849-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="57849-537">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-537">String</span></span>      | <span data-ttu-id="57849-538">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-538">Bind</span></span>   | <span data-ttu-id="57849-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="57849-539">\@.Description</span></span> |
    | <span data-ttu-id="57849-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="57849-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="57849-541">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-541">String</span></span>      | <span data-ttu-id="57849-542">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-542">Bind</span></span>   | <span data-ttu-id="57849-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="57849-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="57849-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="57849-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="57849-545">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-545">String</span></span>      | <span data-ttu-id="57849-546">Breyta</span><span class="sxs-lookup"><span data-stu-id="57849-546">Edit</span></span>   | <span data-ttu-id="57849-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="57849-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="57849-548">EnumAppQuestionOrder.Conditional, „Skilyrðisbundið“,</span><span class="sxs-lookup"><span data-stu-id="57849-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="57849-549">EnumAppQuestionOrder.Random, „Slembi (prósenta í spurningalista)“,</span><span class="sxs-lookup"><span data-stu-id="57849-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="57849-550">EnumAppQuestionOrder.RandomGroup, „Slembi (prósenta í niðurstöðuflokkum)“,</span><span class="sxs-lookup"><span data-stu-id="57849-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="57849-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="57849-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="57849-552">"")</span><span class="sxs-lookup"><span data-stu-id="57849-552">"")</span></span> |
    | <span data-ttu-id="57849-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="57849-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="57849-554">Færsla</span><span class="sxs-lookup"><span data-stu-id="57849-554">Record</span></span>      |        | |
    | <span data-ttu-id="57849-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="57849-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="57849-556">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-556">String</span></span>      | <span data-ttu-id="57849-557">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-557">Bind</span></span>   | <span data-ttu-id="57849-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="57849-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="57849-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="57849-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="57849-560">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-560">String</span></span>      | <span data-ttu-id="57849-561">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-561">Bind</span></span>   | <span data-ttu-id="57849-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="57849-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="57849-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="57849-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="57849-564">Rauntala</span><span class="sxs-lookup"><span data-stu-id="57849-564">Real</span></span>        | <span data-ttu-id="57849-565">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-565">Bind</span></span>   | <span data-ttu-id="57849-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="57849-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="57849-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="57849-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="57849-568">Færslulisti</span><span class="sxs-lookup"><span data-stu-id="57849-568">Record list</span></span> | <span data-ttu-id="57849-569">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-569">Bind</span></span>   | <span data-ttu-id="57849-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="57849-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="57849-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="57849-572">Heiltala</span><span class="sxs-lookup"><span data-stu-id="57849-572">Integer</span></span>     | <span data-ttu-id="57849-573">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-573">Bind</span></span>   | <span data-ttu-id="57849-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="57849-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="57849-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="57849-576">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-576">String</span></span>      | <span data-ttu-id="57849-577">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-577">Bind</span></span>   | <span data-ttu-id="57849-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="57849-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="57849-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="57849-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="57849-580">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-580">String</span></span>      | <span data-ttu-id="57849-581">Breyta</span><span class="sxs-lookup"><span data-stu-id="57849-581">Edit</span></span>   | <span data-ttu-id="57849-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="57849-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="57849-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="57849-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="57849-584">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-584">String</span></span>      | <span data-ttu-id="57849-585">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-585">Bind</span></span>   | <span data-ttu-id="57849-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="57849-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="57849-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="57849-588">Heiltala</span><span class="sxs-lookup"><span data-stu-id="57849-588">Integer</span></span>     | <span data-ttu-id="57849-589">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-589">Bind</span></span>   | <span data-ttu-id="57849-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="57849-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="57849-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="57849-592">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-592">String</span></span>      | <span data-ttu-id="57849-593">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-593">Bind</span></span>   | <span data-ttu-id="57849-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="57849-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="57849-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="57849-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="57849-596">Færslulisti</span><span class="sxs-lookup"><span data-stu-id="57849-596">Record list</span></span> | <span data-ttu-id="57849-597">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-597">Bind</span></span>   | <span data-ttu-id="57849-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="57849-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="57849-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="57849-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="57849-600">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-600">String</span></span>      | <span data-ttu-id="57849-601">Breyta</span><span class="sxs-lookup"><span data-stu-id="57849-601">Edit</span></span>   | <span data-ttu-id="57849-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="57849-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="57849-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="57849-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="57849-604">Rauntala</span><span class="sxs-lookup"><span data-stu-id="57849-604">Real</span></span>        | <span data-ttu-id="57849-605">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-605">Bind</span></span>   | <span data-ttu-id="57849-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="57849-606">\@.point</span></span> |
    | <span data-ttu-id="57849-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="57849-608">Heiltala</span><span class="sxs-lookup"><span data-stu-id="57849-608">Integer</span></span>     | <span data-ttu-id="57849-609">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-609">Bind</span></span>   | <span data-ttu-id="57849-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="57849-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="57849-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="57849-612">Strengur</span><span class="sxs-lookup"><span data-stu-id="57849-612">String</span></span>      | <span data-ttu-id="57849-613">Binda</span><span class="sxs-lookup"><span data-stu-id="57849-613">Bind</span></span>   | <span data-ttu-id="57849-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="57849-614">\@.text</span></span> |

    <span data-ttu-id="57849-615">Eftirfarandi mynd sýnir lokastöðu skilgreindrar líkanavörpunar á síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="57849-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Fullskilgreind líkanavörpun í hönnuði líkanavörpunar rafrænnar skýrslugerðar](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="57849-617">Vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="57849-617">Save your changes.</span></span>
8. <span data-ttu-id="57849-618">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="57849-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="57849-619">Ljúka hönnun líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="57849-620">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-621">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="57849-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="57849-622">Í flýtiflipanum **Útgáfur** skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="57849-623">Veljið **Breyta stöðu** \> **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="57849-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="57849-624">Staða á útgáfu 1.1 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="57849-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="57849-625">Ekki er lengur hægt að breyta útgáfu 1.1.</span><span class="sxs-lookup"><span data-stu-id="57849-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="57849-626">Þessi útgáfa inniheldur skilgreindu líkanavörpunina og er hægt að nota sem grunninn fyrir aðrar skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="57849-627">Útgáfa 1.2 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="57849-628">Hægt er að breyta þessari útgáfu til að leiðrétta skilgreininguna **Vörpun spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="57849-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Útgáfur breytanlegra skilgreininga rafrænnar skýrslugerðar á skilgreiningarsíðunni](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="57849-630">Skilgreinda líkanavörpunin er Finance-innleiðing á óhlutbundna gagnalíkaninu sem stendur fyrir fyrirtækislénið **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="57849-631">Hanna sniðmát fyrir sérsniðna skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-631">Design a template for a custom report</span></span>

<span data-ttu-id="57849-632">Rammi rafrænnar skýrslugerðar notar fyrirframskilgreind sniðmát til að búa til skýrslur á Microsoft Office-sniði (Excel-vinnubækur eða Word-skjöl).</span><span class="sxs-lookup"><span data-stu-id="57849-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="57849-633">Á meðan nauðsynleg skýrsla er búin til, er sniðmát fyllt út með nauðsynlegum gögnum samkvæmt skilgreindu gagnaflæði.</span><span class="sxs-lookup"><span data-stu-id="57849-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="57849-634">Þess vegna þarf fyrst að hanna sniðmát fyrir sérsniðnu skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="57849-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="57849-635">Þetta sniðmát verður að vera hannað sem Excel-vinnubók, skipulag þess sem stendur fyrir útlit sérsniðinnar skýrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="57849-636">Gefa þarf öllum Excel-atriðum heiti sem ætlunin er að fylla út í með nauðsynlegum gögnum.</span><span class="sxs-lookup"><span data-stu-id="57849-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="57849-637">Sækið skrána [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) og vistið hana á staðbundinni tölvu.</span><span class="sxs-lookup"><span data-stu-id="57849-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="57849-638">Opnið skrána í Excel og farið yfir skipulag vinnubókarinnar.</span><span class="sxs-lookup"><span data-stu-id="57849-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="57849-639">Eins og eftirfarandi mynd sýnir hefur sótt sniðmát verið hannað til að prenta tilgreinda spurningalista sem birta spurningar spurningalistans ásamt viðeigandi svörum.</span><span class="sxs-lookup"><span data-stu-id="57849-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Excel-sniðmát til að prenta tilgreinda spurningalista](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="57849-641">Excel-heitum hefur verið bætt við þetta sniðmát til að fylla út í upplýsingar um spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="57849-642">Hægt er að nota stjórnun heitis til að yfirfara Excel-heitin.</span><span class="sxs-lookup"><span data-stu-id="57849-642">You can use Name Manager to review the Excel names.</span></span>

![Nota stjórnun heitis til að yfirfara Excel-heiti í uppgefnu Excel-sniðmáti](./media/er-quick-start1-template-names.png)

<span data-ttu-id="57849-644">Skýrslumerkjum hefur verið bætt við sem föstum texta á ensku.</span><span class="sxs-lookup"><span data-stu-id="57849-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="57849-645">Hægt er að skipta út skýrslumerkjunum með nýjum Excel-heitum sem fylla út í merkin með tungumálaháðum texta með því að nota [merki](#AddMmLabels) fyrir snið rafrænnar skýrslugerðar, eins og gert var fyrir tungumálaháðar segðir í skilgreindu líkanavörpuninni.</span><span class="sxs-lookup"><span data-stu-id="57849-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="57849-646">Í þessu tilviki verður að bæta við merkjum rafrænnar skýrslugerðar í breytanlegu sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="57849-647">Eins og eftirfarandi mynd sýnir, hefur haus sérsniðinnar skýrslu verið tilgreindur til að gera síðuvíxl möguleg í Excel.</span><span class="sxs-lookup"><span data-stu-id="57849-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Haus sérsniðinnar skýrslu í uppgefnu Excel-sniðmáti](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="57849-649">Setja upp snið</span><span class="sxs-lookup"><span data-stu-id="57849-649">Design a format</span></span>

<span data-ttu-id="57849-650">Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur [sniðs](general-electronic-reporting.md#FormatComponentOutbound) hluta.</span><span class="sxs-lookup"><span data-stu-id="57849-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="57849-651">Skilgreina verður sniðshlutann til að tilgreina hvernig fyllt verður út í skýrslusniðmát með nauðsynlegum gögnum við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="57849-652">Með því að ljúka skrefunum í hlutanum [Flytja inn hannaða skilgreiningu sniðs](#FormatImport) er hægt að flytja inn nauðsynlegt snið úr uppgefinni XML-skrá.</span><span class="sxs-lookup"><span data-stu-id="57849-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="57849-653">Að öðrum kosti er hægt að ljúka skrefunum í hlutanum [Stofna nýja skilgreiningu á sniði](#FormatCreate) til að hanna þetta snið frá grunni.</span><span class="sxs-lookup"><span data-stu-id="57849-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="57849-654">Flytja inn hannaða skilgreiningu sniðs</span><span class="sxs-lookup"><span data-stu-id="57849-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="57849-655">Sækið skrána [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) og vistið hana á staðbundinni tölvu.</span><span class="sxs-lookup"><span data-stu-id="57849-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="57849-656">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="57849-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="57849-657">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="57849-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="57849-658">Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="57849-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="57849-659">Veljið **Fletta** og finnið síðan og veljið skrána **Questionnaires format.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="57849-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="57849-660">Veljið **Í lagi** til að flytja inn skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="57849-661">Til að halda áfram skal sleppa næsta ferli, [Stofna nýja skilgreiningu sniðs](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="57849-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="57849-662">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="57849-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="57849-663">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-664">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="57849-665">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="57849-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="57849-666">Í fellilistanum skaltu fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="57849-667">Í reitnum **Nýtt** skal velja **Snið byggir á spurningalistum gagnalíkans**.</span><span class="sxs-lookup"><span data-stu-id="57849-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="57849-668">Í reitinn **Heiti** skal færa inn **Skýrsla spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="57849-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="57849-669">Í reitnum **Útgáfa gagnalíkans** skal velja **1**.</span><span class="sxs-lookup"><span data-stu-id="57849-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="57849-670">Ef valin er sérstök útgáfa af grunngagnalíkaninu verður skipulag samsvarandi útgáfu gagnalíkansins kynnt þér sem skipulag gagnagjafans **Líkan** á sniðinu sem stofnað er.</span><span class="sxs-lookup"><span data-stu-id="57849-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="57849-671">Hægt er að skilja þennan reit eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="57849-671">You can leave this field blank.</span></span> <span data-ttu-id="57849-672">Í því tilfelli verður skipulag útgáfunnar **Drög** fyrir gagnalíkanið kynnt þér sem skipulag gagnagjafans **Líkan** á sniðinu sem stofnað er.</span><span class="sxs-lookup"><span data-stu-id="57849-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="57849-673">Síðan er hægt að leiðrétta líkanið og sjá svo leiðréttingarnar strax í sniðinu.</span><span class="sxs-lookup"><span data-stu-id="57849-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="57849-674">Þessi nálgun gæti bætt skilvirkni á hönnun á lausnum rafrænnar skýrslugerðar þegar gagnalíkanið, líkanavörpunin og sniðið er skilgreint á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="57849-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="57849-675">Ef valin er sérstök útgáfa af grunngagnalíkaninu er hægt að skipta yfir í að nota útgáfuna **Drög** seinna, þegar hafist er handa við að breyta sniðinu.</span><span class="sxs-lookup"><span data-stu-id="57849-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="57849-676">Í reitnum **Skilgreining gagnalíkans** skal velja **Rótar** skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="57849-677">Veljið **Stofna skilgreiningu** til að stofna skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="57849-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="57849-678">Flytja inn skýrslusniðmát</span><span class="sxs-lookup"><span data-stu-id="57849-678">Import a report template</span></span>

1. <span data-ttu-id="57849-679">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Skýrsla spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="57849-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="57849-680">Veljið **Hönnuður** til að hefja skilgreiningu á sérsniðnu sniði.</span><span class="sxs-lookup"><span data-stu-id="57849-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="57849-681">Á síðunni **Sniðshönnuður**, í aðgerðarúðunni, skal velja **Flytja inn** \> **Flytja inn úr Excel**.</span><span class="sxs-lookup"><span data-stu-id="57849-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="57849-682">Í svarglugganum skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="57849-683">Veljið **Bæta við sniðmáti**.</span><span class="sxs-lookup"><span data-stu-id="57849-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="57849-684">Finnið og veljið staðbundið vistuðu skrána **Questionnaires report template.xslx** og veljið síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="57849-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="57849-685">Veljið **Í lagi** til að flytja inn sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="57849-685">Select **OK** to import the template.</span></span>

    ![Flytja inn skýrslusniðmát](./media/er-quick-start1-template-import.png)

<span data-ttu-id="57849-687">Sniðseiningin **Excel\\File** er sjálfkrafa bætt við breytanlega sniðið sem rótareining.</span><span class="sxs-lookup"><span data-stu-id="57849-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="57849-688">Þar að auki er annaðhvort sniðseiningin **Excel\\Range** eða sniðseiningin **Excel\\Cell** sjálfkrafa bætt við fyrir hvert viðurkennt Excel-heiti á innfluttu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="57849-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="57849-689">Sniðið **Excel\\Header** sem er með földuðu eininguna **Strengur** er sjálfkrafa bætt við til að endurspegla hausstillingar á innfluttu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="57849-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Sniðsskipulag sem inniheldur sjálfkrafa viðbættum einingum í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="57849-691">Skilgreina snið</span><span class="sxs-lookup"><span data-stu-id="57849-691">Configure a format</span></span>

1. <span data-ttu-id="57849-692">Á síðunni **Sniðshönnuður**, í sniðstrénu, skal velja rótareininguna **Excel**.</span><span class="sxs-lookup"><span data-stu-id="57849-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="57849-693">Í flipanum **Snið** hægra megin á síðunni, í reitnum **Heiti**, skal færa inn <a name="AddFormatRootElement"></a>**Skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="57849-694">Í reitnum **Tungumálastillingar** skal velja **Kjörstilling notanda** til að keyra skýrsluna á kjörtungumáli notanda.</span><span class="sxs-lookup"><span data-stu-id="57849-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="57849-695">Í reitnum **Kjörstillingar menningar** skal velja **Kjörstilling notanda** til að keyra skýrsluna samkvæmt kjörmenningu notanda.</span><span class="sxs-lookup"><span data-stu-id="57849-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="57849-696">Frekari upplýsingar um hvernig á að tilgreina samhengi tungumáls og menningar fyrir ferli rafrænnar skýrslugerðar er að finna í [Hanna skýrslur á mörgum tungumálum](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="57849-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Stillingar tungumáls og menningar fyrir hannaða skýrslu í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="57849-698">Í sniðstrénu skal útvíkka rótarhnútinn og velja ´siðan **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="57849-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="57849-699">Í flipanum **Snið**, í reitnum **Stefna eftirlíkingar**, skal velja **Engin eftirlíking** því að þú býst ekki við því að fá marga niðurstöðuflokka fyrir einn spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Skilgreining á stefnu eftirlíkingar fyrir sniðseininguna Svið í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="57849-701">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="57849-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="57849-702">Skilgreina gagnatengslin fyrir titil skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-702">Define the data binding for a report title</span></span>

<span data-ttu-id="57849-703">Tilgreina verður gagnatengsl fyrir sniðseiningu sem er notuð til að fylla út titil á myndaðri skýrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="57849-704">Á síðunni **Sniðshönnuður**, í flipanum **Vörpun** hægra megin, skal velja eininguna **Report\\ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="57849-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="57849-705">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="57849-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="57849-706">Í formúluritlinum skal velja **Þýða**.</span><span class="sxs-lookup"><span data-stu-id="57849-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="57849-707">Í svarglugganum **Textaþýðing** skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="57849-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="57849-708">Í reitinn **Kenni merkis** skal færa inn **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="57849-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="57849-709">Í reitinn **Texti á sjálfgefnu tungumáli** skal færa inn **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="57849-710">Veljið **Þýða** og veljið síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="57849-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="57849-711">Veljið **Þýða** til að loka svarglugganum **Textaþýðing**.</span><span class="sxs-lookup"><span data-stu-id="57849-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="57849-712">Lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-712">Close the formula editor.</span></span>

    ![Skilgreining tengingar til að fylla út í titilinn á myndaðri skýrslu](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="57849-714">Hægt er að nota þessa tækni til að gera öll önnur merki núverandi sniðmáts tungumálaháð.</span><span class="sxs-lookup"><span data-stu-id="57849-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="57849-715">Frekar upplýsingar um hvernig hægt er að þýða viðbætt merki á einni skilgreiningu rafrænnar skýrslugerðar yfir á öll studd tungumál er að finna í [Hanna skýrslur á mörgum tungumálum](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="57849-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="57849-716">Fara yfir gagnagjafa líkans</span><span class="sxs-lookup"><span data-stu-id="57849-716">Review model data source</span></span>

1. <span data-ttu-id="57849-717">Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, skal velja gagnagjafann <a name="ModelDSName"></a>**líkan** sem stendur fyrir grunngagnalíkan þessa sniðs rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="57849-718">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="57849-718">Select **Edit**.</span></span>
3. <span data-ttu-id="57849-719">Yfirfara upplýsingarnar í svarglugganum **Eiginleikar gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="57849-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="57849-720">Þessi gagnagjafi stendur fyrir útgáfu 1 af gagnalíkanshlutanum **Spurningalistar** sem er að finna í **Líkan spurningalista** fyrir skilgreiningu rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Eiginleikar gagnagjafa líkansins í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="57849-722">Tengja sniðseiningar við reiti gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="57849-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="57849-723">Til að tilgreina hvernig sniðmát er fyllt út við keyrslu verður að tengja hverja sniðseiningu sem tengist viðeigandi Excel-heiti við stakan reit í gagnagjafa þessa sniðs.</span><span class="sxs-lookup"><span data-stu-id="57849-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="57849-724">Á síðunni **Sniðshönnuður**, í sniðstrénu, skal velja sniðseininguna **Report\\CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="57849-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="57849-725">Í flipanum **Vörpun** skal velja gagnagjafareitinn **model.CompanyName** af gerðinni **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="57849-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="57849-726">Veljið **Tengja** til að færa inn fyrirtækisheiti í sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="57849-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="57849-727">Í sniðstrénu er valinn einingin **Report\\Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="57849-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="57849-728">Í flipanum **Vörpun** skal velja gagnagjafareitinn **model.Questionnaire** af gerðinni **Færslulisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="57849-729">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="57849-729">Select **Bind**.</span></span>
7. <span data-ttu-id="57849-730">Veljið **Sýna upplýsingar** til að fá nánari upplýsingar um sniðseiningar.</span><span class="sxs-lookup"><span data-stu-id="57849-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="57849-731">Sviðssniðseiningin **Spurningalisti** er skilgreind sem endurtekin lóðrétt.</span><span class="sxs-lookup"><span data-stu-id="57849-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="57849-732">Þegar hún er tengd við gagnagjafa af gerðinni **Færslulisti** er viðeigandi sviðið **Spurningalisti** af Excel-sniðmátinu endurtekið fyrir allar skrár tengda gagnagjafans.</span><span class="sxs-lookup"><span data-stu-id="57849-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Að tengja sviðssniðseiningu spurningalistans við viðeigandi gagnagjafa færslulista í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="57849-734">Þar sem sviðið **Spurningalisti** í Excel-sniðmátinu er skilgreint milli línu 5 og 14, eru þessar líknur endurteknar fyrir hvern uppgefinn spurningalista.</span><span class="sxs-lookup"><span data-stu-id="57849-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Línur í Excel-sniðmátinu sem verða endurteknar í myndaðri skýrslu fyrir hverja færslu í gagnagjafa færslulistans](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="57849-736">Skilgreinið svipaðar tengingar fyrir eftirstandandi sniðseiningar, eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="57849-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57849-737">Í þessari töflu er í upplýsingunum í dálknum „Slóð gagnagjafa“ gert ráð fyrir að kveikt sé á [tengdri slóð](relative-path-data-bindings-er-models-format.md) eiginleika rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="57849-738">Slóð sniðseiningar</span><span class="sxs-lookup"><span data-stu-id="57849-738">Format element path</span></span>                                      | <span data-ttu-id="57849-739">Slóð gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="57849-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="57849-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="57849-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="57849-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="57849-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="57849-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="57849-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="57849-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="57849-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="57849-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="57849-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="57849-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="57849-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="57849-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="57849-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="57849-747">**\@.Active**, þar sem **\@** er **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="57849-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="57849-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="57849-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="57849-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="57849-749">**\@.Code**</span></span> |
    | <span data-ttu-id="57849-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="57849-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="57849-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="57849-751">**\@.Description**</span></span> |
    | <span data-ttu-id="57849-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="57849-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="57849-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="57849-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="57849-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="57849-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="57849-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="57849-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="57849-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="57849-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="57849-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="57849-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="57849-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="57849-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="57849-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="57849-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="57849-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="57849-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="57849-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="57849-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="57849-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="57849-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="57849-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="57849-763">**\@.Question**</span></span> |
    | <span data-ttu-id="57849-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="57849-765">**\@.CollectionSequenceNumber**, þar sem **\@** er **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="57849-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="57849-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="57849-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="57849-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="57849-767">**\@.Id**</span></span> |
    | <span data-ttu-id="57849-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="57849-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="57849-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="57849-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="57849-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="57849-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="57849-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="57849-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="57849-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="57849-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="57849-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="57849-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="57849-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="57849-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="57849-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="57849-775">**\@.Text**</span></span> |
    | <span data-ttu-id="57849-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="57849-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="57849-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="57849-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="57849-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="57849-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="57849-779">**\@.CorrectAnswer**, þar sem **\@** er **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="57849-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="57849-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="57849-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="57849-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="57849-781">**\@.Points**</span></span> |
    | <span data-ttu-id="57849-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="57849-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="57849-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="57849-783">**\@.Text**</span></span> |

9. <span data-ttu-id="57849-784">Þegar þessu er lokið skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="57849-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="57849-785">Eftirfarandi mynd sýnir lokastöðu skilgreindra gagnatengsla á síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="57849-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Skilgreind gagnatengsl í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="57849-787">Allt safn tilgreindra gagnagjafa og tengsla stendur fyrir sniðsvörpunaríhlut fyrir skilgreinda sniðið.</span><span class="sxs-lookup"><span data-stu-id="57849-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="57849-788">Kallað er á þessa sniðsvörpun þegar skilgreint snið fyrir skýrslumyndun er keyrt.</span><span class="sxs-lookup"><span data-stu-id="57849-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="57849-789">Keyra hannað snið úr rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="57849-789">Run a designed format from ER</span></span>

<span data-ttu-id="57849-790">Nú er hægt að keyra hannað snið í prófunartilgangi af síðunni **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="57849-791">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-792">Á síðunni **Skilgreining**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="57849-793">Veljið **Hönnuður** fyrir sniðsútgáfuna sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="57849-794">Á síðunni **Sniðshönnuður** skal velja **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="57849-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="57849-795">Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.</span><span class="sxs-lookup"><span data-stu-id="57849-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="57849-796">Veljið **Í lagi** til að staðfesta síunarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="57849-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="57849-797">Veljið **Í lagi** til að keyra skýrsla.</span><span class="sxs-lookup"><span data-stu-id="57849-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="57849-798">Farið yfir myndaða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-798">Review the generated report.</span></span>

<span data-ttu-id="57849-799">Mynduð skýrsla er [sjálfgefið](electronic-reporting-destinations.md#default-behavior) afhent sem Excel-skrá sem hægt er að sækja.</span><span class="sxs-lookup"><span data-stu-id="57849-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="57849-800">Eftirfarandi myndir sýna tvær síður af myndaðri skýrslu á Excel-sniði.</span><span class="sxs-lookup"><span data-stu-id="57849-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Dæmi um myndaða skýrslu á Excel-sniði, síða 1](./media/er-quick-start1-report1a.png)

![Dæmi um myndaða skýrslu á Excel-sniði, síða 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="57849-803">Stilla hannað snið</span><span class="sxs-lookup"><span data-stu-id="57849-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="57849-804">Laga snið til að breyta heiti á mynduðu skjali</span><span class="sxs-lookup"><span data-stu-id="57849-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="57849-805">Sjálfgefið er að myndað skjal sé nefnt með því að nota samnefni núverandi notanda.</span><span class="sxs-lookup"><span data-stu-id="57849-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="57849-806">Með því að breyta sniðinu er hægt að breyta þessari hegðun þannig að mynduðu skjali sé gefið heiti sem byggir á sérstilltum rökum.</span><span class="sxs-lookup"><span data-stu-id="57849-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="57849-807">Til dæmis er hægt að byggja heiti myndaðs skjals á núverandi dagsetningu og tíma lotunnar og á titli skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="57849-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="57849-808">Á síðunni **Sniðshönnuður** skal velja rótaratriðið **Skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="57849-809">Í flipanum **Vörpun** skal velja **Breyta skráarheiti**.</span><span class="sxs-lookup"><span data-stu-id="57849-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="57849-810">Í reitinn **Formúla** skal færa inn **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="57849-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="57849-811">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="57849-812">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="57849-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="57849-813">Laga snið til að breyta röð spurninga</span><span class="sxs-lookup"><span data-stu-id="57849-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="57849-814">Spurningunum er ekki rétt raðað í myndaðri skýrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="57849-815">Hægt er að breyta röðinni með því að breyta sniðinu.</span><span class="sxs-lookup"><span data-stu-id="57849-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="57849-816">Á síðunni **Sniðshönnuður** skal velja rótaratriðið **Skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="57849-817">Í flipanum **Vörpun**, í sniðstrénu, skal útvíkka **Report\\Questionnaire\\Question**.</span><span class="sxs-lookup"><span data-stu-id="57849-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Sniðseining spurningar af sviðsgerðinni í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="57849-819">Í flipanum **Vörpun** skal velja **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="57849-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="57849-820">Veljið **Bæta við** \> **Functions\\Calculated field** og því næst, í reitinn **Heiti**, skal færa inn **OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="57849-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="57849-821">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="57849-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="57849-822">Í formúluritilinn, í reitinn **Formúla**, skal færa inn **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** til að raða lista yfir spurningar í núgildandi spurningalista eftir númeraröðinni.</span><span class="sxs-lookup"><span data-stu-id="57849-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="57849-823">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="57849-824">Veljið **Í lagi** til að ljúka færslu á nýjum reiknuðum reit.</span><span class="sxs-lookup"><span data-stu-id="57849-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="57849-825">Í flipanum **Vörpun** skal velja **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="57849-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="57849-826">Í sniðstrénu skal velja **Excel\\Questionnaire\\Question**.</span><span class="sxs-lookup"><span data-stu-id="57849-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="57849-827">Veljið **Tengja** og staðfestið síðan að núverandi slóðinni **model.Questionnaire.Questions** sé skipt út fyrir nýju slóðina **model.Questionnaire.OrderedQuestions** í öllum tengslum faldaðra eininga.</span><span class="sxs-lookup"><span data-stu-id="57849-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="57849-828">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="57849-828">Select **Save**.</span></span>

![Tengja sniðseiningu spurningar við skilgreinda gagnagjafann OrderedQuestions í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="57849-830">Keyra breytt snið úr rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="57849-830">Run a modified format from ER</span></span>

<span data-ttu-id="57849-831">Nú er hægt að keyra breytt snið í prófunartilgangi í ramma rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="57849-832">Á síðunni **Sniðshönnuður** skal velja **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="57849-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="57849-833">Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.</span><span class="sxs-lookup"><span data-stu-id="57849-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="57849-834">Veljið **Í lagi** til að staðfesta síunarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="57849-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="57849-835">Veljið **Í lagi** til að keyra skýrsla.</span><span class="sxs-lookup"><span data-stu-id="57849-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="57849-836">Farið yfir myndaða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-836">Review the generated report.</span></span>

<span data-ttu-id="57849-837">Eftirfarandi mynd sýnir myndaða skýrslu á Excel-sniði þar sem spurningunum er rétt raðað.</span><span class="sxs-lookup"><span data-stu-id="57849-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Mynduð skýrsla á Excel-sniði sem er með rétt röðuðum spurningum](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="57849-839">Ljúka sniðshönnun</span><span class="sxs-lookup"><span data-stu-id="57849-839">Complete the format design</span></span>

1. <span data-ttu-id="57849-840">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-841">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="57849-842">Í flýtiflipanum **Útgáfur** skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="57849-843">Veljið **Breyta stöðu** \> **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="57849-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="57849-844">Staða á útgáfu 1.1 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="57849-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="57849-845">Ekki er lengur hægt að breyta útgáfu 1.1.</span><span class="sxs-lookup"><span data-stu-id="57849-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="57849-846">Þessi útgáfa inniheldur skilgreinda sniðið og er hægt að nota til að prenta sérsniðnu skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="57849-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="57849-847">Útgáfa 1.2 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="57849-848">Hægt er að breyta þessari útgáfu til að leiðrétta snið skýrslunnar **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Útgáfur breytanlegra skilgreininga rafrænnar skýrslugerðar á skilgreiningarsíðunni](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="57849-850">Skilgreinda sniðið er hönnunin þín á skýrslunni **Spurningalisti** og hefur engin tengsl við sérstaka Finance-gervinga.</span><span class="sxs-lookup"><span data-stu-id="57849-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="57849-851">Þróa forritsgervinga til að kalla á hannaða skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="57849-852">Sem notandi í hlutverki kerfisstjóra þarf að þróa ný rök þannig að hægt sé að kalla á skilgreint snið rafrænnar skýrslugerðar úr notendaviðmóti forritsins til að mynda sérsniðnu skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="57849-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="57849-853">Sem stendur býður rafræn skýrslugerð er ekki upp á neina möguleika á því að skilgreina þessa gerð af rökum.</span><span class="sxs-lookup"><span data-stu-id="57849-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="57849-854">Þess vegna er einhver hönnunarvinna nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="57849-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="57849-855">Til að þróa nýju rökin þarf að setja upp grannfræði sem styður samfellda smíði.</span><span class="sxs-lookup"><span data-stu-id="57849-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="57849-856">Nánari upplýsingar er að finna [Setja upp grannfræði sem styður samfellda smíði og sjálfvirkni prófunar](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="57849-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="57849-857">Þú verður einnig að hafa aðgang að þróunarumhverfi fyrir þessa grannfræði.</span><span class="sxs-lookup"><span data-stu-id="57849-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="57849-858">Frekari upplýsingar um tiltækt API rafrænnar skýrslugerðar er að finna í [API fyrir ramma rafrænnar skýrslugerðar](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="57849-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="57849-859">Breyta frumkóða</span><span class="sxs-lookup"><span data-stu-id="57849-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="57849-860">Bæta við gagnasamningsklasa</span><span class="sxs-lookup"><span data-stu-id="57849-860">Add a data contract class</span></span>

<span data-ttu-id="57849-861">Bætið nýja klasanum **QuestionnairesErReportContract** við Microsoft Visual Studio-verkið og skrifið kóða sem tilgreinir gagnasamninginn sem á að nota til að keyra skilgreint snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="57849-862">Bæta við smiðsklasa notendaviðmóts</span><span class="sxs-lookup"><span data-stu-id="57849-862">Add a UI builder class</span></span>

<span data-ttu-id="57849-863">Bætið nýja klasanum **QuestionnairesErReportUIBuilder** við Visual Studio-verkið og skrifið kóða til að mynda svarglugga við keyrslutíma sem verður notaður til að fletta upp á auðkenni sniðsvörpunar fyrir snið rafrænnar skýrslugerðar sem þarf að keyra.</span><span class="sxs-lookup"><span data-stu-id="57849-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="57849-864">Uppgefinn kóði flettir aðeins upp á sniðum rafrænnar skýrslugerðar sem innihalda gagnagjafa af gerðinni **Gagnalíkan** sem vísar til gagnalíkansins **[Spurningalistar](#DataModeName)** með því að nota skilgreininguna **[Rót](#RootDefinitionName)**.</span><span class="sxs-lookup"><span data-stu-id="57849-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="57849-865">Einnig er hægt að nota samþættingarstaði rafrænnar skýrslugerðar til að sía snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="57849-866">Frekari upplýsingar er að finna í [API til að sýna uppflettingu sniðsvörpunar](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="57849-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="57849-867">Bæta við gagnaveituklasa</span><span class="sxs-lookup"><span data-stu-id="57849-867">Add a data provider class</span></span>

<span data-ttu-id="57849-868">Bætið nýja klasanum **QuestionnairesErReportDP** við Visual Studio-verkið og skrifið kóða sem tilgreinir gagnaveituna sem á að nota til að keyra skilgreint snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="57849-869">Uppgefinn kóði inniheldur aðeins gagnasamninginn fyrir þessa gagnaveitu.</span><span class="sxs-lookup"><span data-stu-id="57849-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="57849-870">Bæta við merkjaskrá</span><span class="sxs-lookup"><span data-stu-id="57849-870">Add a labels file</span></span>

<span data-ttu-id="57849-871">Bætið nýju **QuestionnairesErReportLabels\_en-US** merkjaskránum við Visual Studio-verkið og tilgreinið eftirfarandi töflur fyrir ný tilföng notendaviðmóts:</span><span class="sxs-lookup"><span data-stu-id="57849-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="57849-872">Merkið **\@QuestionnairesReport** fyrir nýtt valmyndaratriði sem inniheldur eftirfarandi texta á bandarískri ensku (en-US): **Skýrsla spurningalista (knúin af rafrænni skýrslugerð)**</span><span class="sxs-lookup"><span data-stu-id="57849-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="57849-873">Merkið **\@QuestionnairesReportBatchJobDescription** fyrir titil runuvinnslu ef valið snið rafrænnar skýrslugerðar er áætlað fyrir keyrslu sem runuvinnsla</span><span class="sxs-lookup"><span data-stu-id="57849-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="57849-874">Bæta við þjónustuklasa skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-874">Add a report service class</span></span>

<span data-ttu-id="57849-875">Bætið nýja klasanum **QuestionnairesErReportService** við Visual Studio-verkið og skrifið kóða sem kallar á snið rafrænnar skýrslugerðar, finnur það eftir auðkenni sniðsvörpunar og gefur upp gagnasamning sem færibreytu.</span><span class="sxs-lookup"><span data-stu-id="57849-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="57849-876">Þegar þarf að nota snið rafrænnar skýrslugerðar sem keyrir forritsgögn þarf að skilgreina gagnagjafa af gerðinni **Gagnalíkan** í sniðsvörpuninni.</span><span class="sxs-lookup"><span data-stu-id="57849-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="57849-877">Þessi gagnagjafi vísar til ákveðins hluta tiltekins gagnalíkans með því að nota eina rótarskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="57849-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="57849-878">Þegar snið rafrænnar skýrslugerðar er keyrt, kallar það á þennan gagnagjafa til að opna viðeigandi líkanavörpun rafrænnar skýrslugerðar sem er skilgreind fyrir uppgefið líkan og rótarskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="57849-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="57849-879">Allar upplýsingar sem kunna að vera undirbúnar í frumkóðanum og verslun sem hluti af gagnasamningnum er hægt að flytja yfir í snið rafrænnar skýrslugerðar sem er í gangi með því að nota líkanavörpun rafrænnar skýrslugerðar af þessari gerð.</span><span class="sxs-lookup"><span data-stu-id="57849-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="57849-880">Í líkanavörpun rafrænnar skýrslugerðar þarf að skilgreina gagnagjafa af gerðinni **Hlutur** sem vísar til klasans **[QuestionnairesErReportContract](#DataContractClass)**.</span><span class="sxs-lookup"><span data-stu-id="57849-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="57849-881">Til að auðkenna líkanavörpun þarf að tilgreina gagnagjafa sem kallar á þessa líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="57849-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="57849-882">Í uppgefnum kóða er þessi gagnagjafi tilgreindur af fastanum **ERModelDataSourceName** sem er með gildið fyrir **[líkan](#ModelDSName)**.</span><span class="sxs-lookup"><span data-stu-id="57849-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="57849-883">Til að gera grein fyrir því hvaða gagnagjafi er notaður til að birta gagnasamninginn í líkanavörpuninni þarf að tilgreina heiti gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="57849-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="57849-884">Í uppgefnum kóða er þetta heiti tilgreint af fastanum **ParametersDataSourceName** sem er með gildið <a name="DataContractDSName"></a>**RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="57849-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="57849-885">Í nýju umhverfi gæti þurft að uppfæra lýsigögn rafrænnar skýrslugerðar þannig að þessi gerð af klasa sé tiltæk í hönnuði líkanavörpunar í rafrænni skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="57849-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="57849-886">Frekari upplýsingar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="57849-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="57849-887">Bæta við stýriklasa skýrslu</span><span class="sxs-lookup"><span data-stu-id="57849-887">Add a report controller class</span></span>

<span data-ttu-id="57849-888">Bætið nýja klasanum **QuestionnairesErReportController** við Visual Studio-verkið og skrifið kóða sem keyrir snið rafrænnar skýrslugerðar í annaðhvort samstilltri stillingu eða runustillingu, eftir þörfum, í svarglugganum sem er smíðaður samkvæmt rökunum fyrir uppgefinn klasa **QuestionnairesErReportUIBuilder**.</span><span class="sxs-lookup"><span data-stu-id="57849-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="57849-889">Bæta við valmyndaratriði</span><span class="sxs-lookup"><span data-stu-id="57849-889">Add a menu item</span></span>

<span data-ttu-id="57849-890">Bætið nýja valmyndaratriðinu **QuestionnairesErReport** við Visual Studio-verkið.</span><span class="sxs-lookup"><span data-stu-id="57849-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="57849-891">Í eiginleikanum **Hlutur**, vísar þetta valmyndaratriði til klasans **QuestionnairesErReportController** og hann er notaður til að tilgreina heimild notanda til að velja og keyra snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="57849-892">Í eiginleikanum **Merki**, vísar þetta valmyndaratriði til merkisins **\@QuestionnairesReport** sem var búið til hér á undan, þannig að réttur texti er sýndur í notendaviðmóti forritsins.</span><span class="sxs-lookup"><span data-stu-id="57849-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="57849-893">Bæta valmyndaratriði við valmynd</span><span class="sxs-lookup"><span data-stu-id="57849-893">Add a menu item to a menu</span></span>

<span data-ttu-id="57849-894">Bæta núverandi valmyndinni **Þekkingarstjórnun** við Visual Studio-verkið.</span><span class="sxs-lookup"><span data-stu-id="57849-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="57849-895">Bæta þarf nýju **QuestionnairesErReport** atriði af gerðinni **Úttak** við þessa valmynd.</span><span class="sxs-lookup"><span data-stu-id="57849-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="57849-896">Þetta atriði verður að vísa til valmyndaratriðisins **QuestionnairesErReport** sem er lýst í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="57849-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="57849-897">Smíða Visual Studio-verk</span><span class="sxs-lookup"><span data-stu-id="57849-897">Build a Visual Studio project</span></span>

<span data-ttu-id="57849-898">Smíðið verkið til að búa til nýtt valmyndaratriði sem verður í boði fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="57849-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="57849-899">Keyra snið úr forritinu</span><span class="sxs-lookup"><span data-stu-id="57849-899">Run a format from the application</span></span>

1. <span data-ttu-id="57849-900">Farið í **Spurningalisti** \> **Hönnun** \> **Skýrsla spurningalista (knúin af rafrænni skýrslugerð)**.</span><span class="sxs-lookup"><span data-stu-id="57849-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Að velja valmyndaratriði spurningalistaskýrslunnar (knúin af rafrænni skýrslugerð) í spurningalistaeiningunni til að keyra skilgreint snið rafrænnar skýrslugerðar](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="57849-902">Í svarglugganum, í reitnum **Sniðsvörpun**, skal velja **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="57849-903">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57849-903">Select **OK**.</span></span>
4. <span data-ttu-id="57849-904">Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.</span><span class="sxs-lookup"><span data-stu-id="57849-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="57849-905">Veljið **Í lagi** til að staðfesta síunarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="57849-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="57849-906">Veljið **Í lagi** til að keyra skýrsla.</span><span class="sxs-lookup"><span data-stu-id="57849-906">Select **OK** to run the report.</span></span>

    ![Að tilgreina valskilyrðin í svarglugga rafrænnar skýrslugerðar](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="57849-908">Farið yfir myndaða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="57849-909">Stilla hannaða lausn rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-909">Tune a designed ER solution</span></span>

<span data-ttu-id="57849-910">Hægt er að breyta skilgreindri lausn rafrænnar skýrslugerðar þannig að hún noti klasa gagnaveitunnar sem var þróuð til að fá aðgang að upplýsingum um snið rafrænnar skýrslugerðar sem er í gangi, og þannig að hún færi inn heiti á þessu snið rafrænnar skýrslugerðar í myndaðri skýrslu.</span><span class="sxs-lookup"><span data-stu-id="57849-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="57849-911">Breyta líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="57849-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="57849-912">Bæta við gagnagjöfum til að fá aðgang að gagnasamningshlut</span><span class="sxs-lookup"><span data-stu-id="57849-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="57849-913">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-914">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Vörpun spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="57849-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="57849-915">Veljið **Hönnuður** til að opna síðuna **Líkanavörpun á gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="57849-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="57849-916">Veljið **Hönnuður** til að opna valda vörpun í hönnuði líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="57849-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="57849-917">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Hlutur**.</span><span class="sxs-lookup"><span data-stu-id="57849-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="57849-918">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="57849-919">Í svarglugganum, í reitinn **Heiti**, skal færa inn **[RunTimeParameters](#DataContractDSName)**, eins og það er skilgreint í frumkóða klasans **QuestionnairesErReportService**.</span><span class="sxs-lookup"><span data-stu-id="57849-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="57849-920">Í reitinn **Klasi** skal færa inn **[QuestionnairesErReportContract](#DataContractClass)**, sem var kóðaður hér áður.</span><span class="sxs-lookup"><span data-stu-id="57849-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="57849-921">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57849-921">Select **OK**.</span></span>
10. <span data-ttu-id="57849-922">Útvíkkið **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="57849-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="57849-923">Viðbættur gagnagjafi veitir upplýsingar um færslukenni á sniðsvörpun rafrænnar skýrslugerðar sem er í gangi.</span><span class="sxs-lookup"><span data-stu-id="57849-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Viðbættur gagnagjafi í hönnuði sniðsvörpunar rafrænnar skýrslugerðar](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="57849-925">Bæta við gagnagjafa til að fá aðgang að sniðsvörpunarfærslum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="57849-926">Haldið áfram að breyta valdri líkanavörpun með því að bæta við gagnagjafa til að fá aðgang að vörpunarfærslum á sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="57849-927">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="57849-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="57849-928">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="57849-929">Í glugganum, í reitinn **Heiti**, skal slá inn **ER1**.</span><span class="sxs-lookup"><span data-stu-id="57849-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="57849-930">Í reitinn **Tafla** skal slá inn **ERFormatMappingTable**.</span><span class="sxs-lookup"><span data-stu-id="57849-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="57849-931">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57849-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="57849-932">Bæta við gagnagjafa til að fá aðgang að sniðsvörpunarfærslum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="57849-933">Haldið áfram að breyta valdri líkanavörpun með því að bæta við gagnagjafa til að fá aðgang að vörpunarfærslum á sniði rafrænnar skýrslugerðar sem er í gangi.</span><span class="sxs-lookup"><span data-stu-id="57849-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="57849-934">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Functions\\Calculated field**.</span><span class="sxs-lookup"><span data-stu-id="57849-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="57849-935">Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="57849-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="57849-936">Í glugganum, í reitinn **Heiti**, skal slá inn **ER2**.</span><span class="sxs-lookup"><span data-stu-id="57849-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="57849-937">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="57849-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="57849-938">Í formúluritilinn, í reitinn **Formúla**, skal færa inn **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="57849-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="57849-939">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="57849-940">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57849-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="57849-941">Færið inn heiti á sniði rafrænnar skýrslugerðar sem er í gangi í gagnalíkaninu</span><span class="sxs-lookup"><span data-stu-id="57849-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="57849-942">Haldið áfram að breyta valdri líkanavörpun þannig að heiti á snið rafrænnar skýrslugerðar sem er í gangi sé fært inn í gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="57849-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="57849-943">Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnalíkan**, skal útvíkka **ExecutionContext** og síðan velja **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="57849-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="57849-944">Í rúðunni **Gagnalíkan** skal velja **Breyta** til að skilgreina gagnatengsl fyrir valinn reit gagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="57849-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="57849-945">Í formúluritilinn, í reitinn **Formúla**, skal færa inn **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="57849-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="57849-946">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="57849-947">Þar sem reiturinn **FormatName** var notaður, sýnir skilgreind líkanavörpun nú heitið á snið rafrænnar skýrslugerðar sem kallar á þessa líkanavörpun í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="57849-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Að tengja reit gagnalíkansins við aðferð viðbætta gagnagjafans í hönnuði sniðsvörpunar rafrænnar skýrslugerðar](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="57849-949">Ljúka hönnun líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="57849-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="57849-950">Á síðunni **Hönnuður líkanavörpunar** skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="57849-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="57849-951">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="57849-951">Close the page.</span></span>
3. <span data-ttu-id="57849-952">Lokið síðunni Líkanavarpanir.</span><span class="sxs-lookup"><span data-stu-id="57849-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="57849-953">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal ganga úr skugga um skilgreiningin **Vörpun spurningalista** sé enn valin.</span><span class="sxs-lookup"><span data-stu-id="57849-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="57849-954">Því næst, í flýtiflipanum **Útgáfur**, skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="57849-955">Veljið **Breyta stöðu** \> **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="57849-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="57849-956">Staða á útgáfu 1.2 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="57849-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="57849-957">Ekki er lengur hægt að breyta útgáfu 1.2.</span><span class="sxs-lookup"><span data-stu-id="57849-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="57849-958">Þessi útgáfa inniheldur skilgreindu líkanavörpunina og er hægt að nota sem grunninn fyrir aðrar skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="57849-959">Útgáfa 1.3 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="57849-960">Hægt er að breyta þessari útgáfu til að leiðrétta líkanavörpunina **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="57849-961">Breyta sniði</span><span class="sxs-lookup"><span data-stu-id="57849-961">Modify a format</span></span>

<span data-ttu-id="57849-962">Hægt er að breyta skilgreindu sniði rafrænnar skýrslugerðar þannig að heiti þess sé sýnt í síðufæti skýrslu sem er mynduð þegar snið rafrænnar skýrslugerðar er keyrt.</span><span class="sxs-lookup"><span data-stu-id="57849-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="57849-963">Bæta við nýrri sniðseiningu</span><span class="sxs-lookup"><span data-stu-id="57849-963">Add a new format element</span></span>

1. <span data-ttu-id="57849-964">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-965">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="57849-966">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="57849-966">Select **Designer**.</span></span>
4. <span data-ttu-id="57849-967">Á síðunni **Sniðshönnuður** skal velja rótaratriðið **Skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="57849-968">Veljið **Bæta við** til að bæta nýrri faldaðri sniðseiningu fyrir valið rótaratriðið **Skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="57849-969">Veljið **Excel\\Footer**.</span><span class="sxs-lookup"><span data-stu-id="57849-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="57849-970">Í reitinn **Heiti** skal færa inn **Síðufótur**.</span><span class="sxs-lookup"><span data-stu-id="57849-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="57849-971">Veljið **Skýrsla/Síðufótur** og því næst veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="57849-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="57849-972">Veljið **Text\\String**.</span><span class="sxs-lookup"><span data-stu-id="57849-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="57849-973">Tengja viðbætta sniðseiningu</span><span class="sxs-lookup"><span data-stu-id="57849-973">Bind the added format element</span></span>

1. <span data-ttu-id="57849-974">Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, í sniðstrénu, fyrir virku eininguna **Footer\\String**, skal velja **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="57849-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="57849-975">Í formúluritilinn, í reitinn **Formúla**, skal færa inn **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="57849-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="57849-976">Veljið **Vista** og lokið formúluritlinum.</span><span class="sxs-lookup"><span data-stu-id="57849-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="57849-977">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="57849-977">Select **Save**.</span></span>

<span data-ttu-id="57849-978">Skilgreinda sniðinu hefur nú verið breytt þannig að heiti þess verður fært inn í síðufótinn á myndaðri skýrslu með því að nota eininguna **Footer\\String**.</span><span class="sxs-lookup"><span data-stu-id="57849-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Að bæta sniðseiningu síðufóts við skilgreint snið í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="57849-980">Ljúka sniðshönnun</span><span class="sxs-lookup"><span data-stu-id="57849-980">Complete the format design</span></span>

1. <span data-ttu-id="57849-981">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="57849-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="57849-982">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal ganga úr skugga um skilgreiningin **Skýrsla spurningalista** sé enn valin.</span><span class="sxs-lookup"><span data-stu-id="57849-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="57849-983">Því næst, í flýtiflipanum **Útgáfur**, skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="57849-984">Veljið **Breyta stöðu** \> **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="57849-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="57849-985">Staða á útgáfu 1.2 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="57849-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="57849-986">Ekki er lengur hægt að breyta útgáfu 1.2.</span><span class="sxs-lookup"><span data-stu-id="57849-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="57849-987">Þessi útgáfa inniheldur skilgreinda sniðið og er hægt að nota sem grunninn fyrir aðrar skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="57849-988">Útgáfa 1.3 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="57849-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="57849-989">Hægt er að breyta þessari útgáfu til að leiðrétta skýrsluna **Spurningalisti**.</span><span class="sxs-lookup"><span data-stu-id="57849-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="57849-990">Keyra snið úr forritinu</span><span class="sxs-lookup"><span data-stu-id="57849-990">Run a format from the application</span></span>

1. <span data-ttu-id="57849-991">Farið í **Spurningalisti** \> **Hönnun** \> **Skýrsla spurningalista (knúin af rafrænni skýrslugerð)**.</span><span class="sxs-lookup"><span data-stu-id="57849-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="57849-992">Í svarglugganum, í reitnum **Sniðsvörpun**, skal velja **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="57849-993">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57849-993">Select **OK**.</span></span>
4. <span data-ttu-id="57849-994">Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.</span><span class="sxs-lookup"><span data-stu-id="57849-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="57849-995">Veljið **Í lagi** til að staðfesta síunarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="57849-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="57849-996">Veljið **Í lagi** til að keyra skýrsla.</span><span class="sxs-lookup"><span data-stu-id="57849-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="57849-997">Farið yfir myndaða skýrslu á Excel-sniði.</span><span class="sxs-lookup"><span data-stu-id="57849-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="57849-998">Takið eftir að síðufótur myndaðrar skýrslu inniheldur heiti á sniði rafrænnar skýrslugerðar sem var notað til að mynda hana.</span><span class="sxs-lookup"><span data-stu-id="57849-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Mynduð skýrsla á Excel-sniði](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="57849-1000">Keyra snið úr rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="57849-1000">Run a format from ER</span></span>

1. <span data-ttu-id="57849-1001">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="57849-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="57849-1002">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="57849-1003">Í aðgerðarúðunni skal velja **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="57849-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="57849-1004">Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.</span><span class="sxs-lookup"><span data-stu-id="57849-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="57849-1005">Veljið **Í lagi** til að staðfesta síunarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="57849-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="57849-1006">Veljið **Í lagi** til að keyra skýrsla.</span><span class="sxs-lookup"><span data-stu-id="57849-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="57849-1007">Farið yfir myndaða skýrslu á Excel-sniði.</span><span class="sxs-lookup"><span data-stu-id="57849-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="57849-1008">Takið eftir því að síðufótur myndaðrar skýrslu inniheldur ekki heitið á sniði rafrænnar skýrslugerðar sem var notað til að mynda hana, því að gagnasamningshluturinn var ekki færður yfir í líkanavörpunina sem er í gangi þegar snið rafrænnar skýrslugerðar sem var keyrt úr rafrænni skýrslugerð kallaði á hana.</span><span class="sxs-lookup"><span data-stu-id="57849-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="57849-1009">Skilgreina áfangastað sniðs fyrir forskoðun á skjá</span><span class="sxs-lookup"><span data-stu-id="57849-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="57849-1010">Fara á **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="57849-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="57849-1011">Á síðunni **Viðtökustaður rafrænnar skýrslugerðar** skal bæta við færslu viðtökustaðar fyrir skilgreint snið **Skýrsla spurningalista** fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="57849-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="57849-1012">Í flýtiflipanum **Viðtökustaður skráar** skal setja upp **Skjá** [Viðtökustaðar](er-destination-type-screen.md) fyrir sniðsíhlutinn **Skýrsla** sem hefur verið [bætt við](#AddFormatRootElement) sem rótareiningu skilgreindrar **Skýrslu spurningalista** fyrir snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="57849-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="57849-1013">Í flýtiflipanum **Umbreytingarstillingar PDF-skjals** skal skilgreina viðtökustaðinn til að umbreyta skýrslu í [PDF-snið](electronic-reporting-destinations.md#OutputConversionToPDF) sem notar síðuuppsetninguna **Langsnið**.</span><span class="sxs-lookup"><span data-stu-id="57849-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Að skilgreina sérsniðinn viðtökustað skjás fyrir snið rafrænnar skýrslugerðar á viðtökusíðu rafrænnar skýrslugerðar](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="57849-1015">Keyra snið úr forritinu til að forskoða það sem PDF-skjal</span><span class="sxs-lookup"><span data-stu-id="57849-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="57849-1016">Farið í **Spurningalisti** \> **Hönnun** \> **Skýrsla spurningalista (knúin af rafrænni skýrslugerð)**.</span><span class="sxs-lookup"><span data-stu-id="57849-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="57849-1017">Í svarglugganum, í reitnum **Sniðsvörpun**, skal velja **Spurningalistaskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="57849-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="57849-1018">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57849-1018">Select **OK**.</span></span>
4. <span data-ttu-id="57849-1019">Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.</span><span class="sxs-lookup"><span data-stu-id="57849-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="57849-1020">Veljið **Í lagi** til að staðfesta síunarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="57849-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="57849-1021">Takið eftir að í flýtiflipanum **Viðtökustaðir** er reiturinn **Úttak** stilltur á **Skjár**.</span><span class="sxs-lookup"><span data-stu-id="57849-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="57849-1022">Ef ætlunin er að breyta skilgreindum viðtökustað skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="57849-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![Svargluggi keyrslu fyrir skýrslu rafrænnar skýrslugerðar þar sem hægt er að breyta skilgreindum viðtökustað](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="57849-1024">Veljið **Í lagi** til að keyra skýrsla.</span><span class="sxs-lookup"><span data-stu-id="57849-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="57849-1025">Farið yfir myndaða skýrslu á PDF-sniði.</span><span class="sxs-lookup"><span data-stu-id="57849-1025">Review the generated report in PDF format.</span></span>

    ![Forskoðun myndaðrar skýrslu á PDF-sniði](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="57849-1027">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="57849-1027">Additional resources</span></span>

- [<span data-ttu-id="57849-1028">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="57849-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="57849-1029">Formúlutungumál í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="57849-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="57849-1030">Hanna skýrslur á mörgum tungumálum</span><span class="sxs-lookup"><span data-stu-id="57849-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="57849-1031">API fyrir ramma rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="57849-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="57849-1032">CASE-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="57849-1033">CONCATENAT-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="57849-1034">DATETIMEFORMAT-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="57849-1035">FILTER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="57849-1036">FIRSTORNULL-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="57849-1037">FORMAT-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="57849-1038">IF-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="57849-1039">ORDERBY-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="57849-1040">SESSIONNOW-aðgerð</span><span class="sxs-lookup"><span data-stu-id="57849-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)
