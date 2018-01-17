---
title: "Setja upp vöruhús með því að nota skilgreiningarsniðmát vöruhúss"
description: "Þetta efnisatriði útskýrir hvernig skal setja upp vöruhús með því að nota skilgreiningarsniðmát vöruhúss."
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 87ade03ec2ba78c4d7f5832bfa6dc1b7eabd8d94
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="7cc60-103">Setja upp vöruhús með því að nota skilgreiningarsniðmát vöruhúss</span><span class="sxs-lookup"><span data-stu-id="7cc60-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7cc60-104">Þetta efnisatriði útskýrir hvernig skal setja upp vöruhús með því að nota skilgreiningarsniðmát vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="7cc60-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="7cc60-105">Til eru nokkrar forskilgreind skilgreiningarsniðmát sem hægt er að nota.</span><span class="sxs-lookup"><span data-stu-id="7cc60-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="7cc60-106">Fyrir upplýsingar um hvernig á að nota þessi sniðmát, sjá [Sniðmát fyrir skilgreiningargögn](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="7cc60-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="7cc60-107">Atburðarás þar sem skilgreiningarsniðmát geta reynst hjálpleg</span><span class="sxs-lookup"><span data-stu-id="7cc60-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="7cc60-108">Skilgreiningarsniðmát geta reynst hjálpleg í margskonar atburðarás.</span><span class="sxs-lookup"><span data-stu-id="7cc60-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="7cc60-109">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="7cc60-109">Here are some examples:</span></span>

- <span data-ttu-id="7cc60-110">Þú hefur lokið og prófað skilgreiningaruppsetningu í prófunarumhverfi og þú vilt nú afrita uppsetninguna yfir í framleiðslu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="7cc60-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="7cc60-111">Þú vilt velta vöruhúsauppsetningu út til nokkurra lögaðila eða búa til nýtt vöruhús í sama lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7cc60-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="7cc60-112">Þú vilt undirbúa þig skjótt fyrir kynningu á vöruhúsvirkninni.</span><span class="sxs-lookup"><span data-stu-id="7cc60-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="7cc60-113">Þú vilt að núverandi vörur og vöruhús noti virknina í Vöruhúsastýringu í staðinn fyrir virknina í Birgðastýringu.</span><span class="sxs-lookup"><span data-stu-id="7cc60-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="7cc60-114">Í þessu efnisatriði er lögð áherslu á fyrstu atburðarásina.</span><span class="sxs-lookup"><span data-stu-id="7cc60-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="7cc60-115">Það sýnir hvernig þú getur notað skilgreiningarsniðmát til að afrita skilgreiningu á uppsetningu frá próf umhverfi yfir í framleiðslu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="7cc60-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="7cc60-116">Afrita skilgreiningu á uppsetningu frá próf umhverfi yfir í framleiðslu umhverfi</span><span class="sxs-lookup"><span data-stu-id="7cc60-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="7cc60-117">Fyrir þessa atburðarás eru skilgreining á uppsetningu fyrir vöruhús og sum færsluferli nú þegar til í próf umhverfi.</span><span class="sxs-lookup"><span data-stu-id="7cc60-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="7cc60-118">Þú vilt nú afrita skilgreininguna á uppsetningu fyrir vöruhús frá prófunarumhverfi yfir í framleiðslu umhverfis.</span><span class="sxs-lookup"><span data-stu-id="7cc60-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="7cc60-119">Það er mikilvægt að þú takir með önnur tengd uppsetningargögn þegar þú afritar skilgreiningu á uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="7cc60-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="7cc60-120">Til dæmis viltu setja upp vörur með því að afrita uppsetninguna úr prófunarumhverfi.</span><span class="sxs-lookup"><span data-stu-id="7cc60-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="7cc60-121">Hins vegar getur þú ekki sett upp fasta tiltektarstaðsetningu fyrir vöru áður en sú vara er búin til.</span><span class="sxs-lookup"><span data-stu-id="7cc60-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="7cc60-122">Þó að einstakar skilgreiningarsniðmát styðji ekki þessa tegund af ákvæðum, þá eru til sjálfgefin gagnasniðmát sem styðja hana.</span><span class="sxs-lookup"><span data-stu-id="7cc60-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="7cc60-123">Þú getur auðveldlega haft þessar sjálfgefna gagnasniðmát með í skilgreiningarferli.</span><span class="sxs-lookup"><span data-stu-id="7cc60-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="7cc60-124">Flytja út sjálfgefið vöruhúsasniðmát</span><span class="sxs-lookup"><span data-stu-id="7cc60-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="7cc60-125">Opnaðu vinnusvæðið **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7cc60-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cc60-126">Ef þú er að notar þetta vinnusvæði í fyrsta skipti verður þú að hlaða öllum gagnaeiningar áður en þú heldur áfram.</span><span class="sxs-lookup"><span data-stu-id="7cc60-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="7cc60-127">Velja **Sniðmátið** reitinn og síðan **Hlaða sjálfgefin sniðmát** til að hlaða sjálfgefnu sniðmátin.</span><span class="sxs-lookup"><span data-stu-id="7cc60-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cc60-128">**Hlaða sjálfgefna sniðmát** er aðeins í boði í **Aukið** yfirlit.</span><span class="sxs-lookup"><span data-stu-id="7cc60-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="7cc60-129">Smellið á **Rammafæribreytur** og síðan í reitnum **Skoða sjálfgildi** skal velja **Aukið yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="7cc60-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="7cc60-130">Eftir að sjálfgefin sniðmát eru hlaðin geturðu breytt þeim svo að þær uppfylli kröfur fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="7cc60-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cc60-131">Til að hlaða sjálfgefnum sniðmátum og flytja inn sniðmát þarftu að hafa aðgang kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="7cc60-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="7cc60-132">Þessi krafa hjálpar til við að tryggja að allir einingar séu rétt hlaðnir inn í sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="7cc60-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="7cc60-133">Vertu viss um að vera inni í lögaðilanum sem þú vilt flytja gögn tengd fyrirtækinu frá.</span><span class="sxs-lookup"><span data-stu-id="7cc60-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="7cc60-134">Í vinnusvæði, veldu **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="7cc60-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="7cc60-135">Stofna nýtt útflutningsverk.</span><span class="sxs-lookup"><span data-stu-id="7cc60-135">Create a new export project.</span></span>
7. <span data-ttu-id="7cc60-136">Veldu **+ Bæta við sniðmáti**, og finndu **400 - WMS** sjálfgefið vöruhúsasniðmát.</span><span class="sxs-lookup"><span data-stu-id="7cc60-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="7cc60-137">Þetta sniðmát bætir við gagnaeiningum fyrir vöruhúsaskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="7cc60-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cc60-138">Ef gögnin sem þú ert að flytja út þarf að sía (til dæmis, þú vilt aðeins flytja út gögnin sem tengjast tilteknu vöruhúsi), þú verður að meta hverja gagnaeiningu og bæta við síun í gegnum fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="7cc60-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="7cc60-139">Einnig er hægt að flytja út öll gögn og eyða þeim færslum sem ekki er krafist í áfangastaðaskránum.</span><span class="sxs-lookup"><span data-stu-id="7cc60-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="7cc60-140">Velja **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="7cc60-140">Select **Export**.</span></span> <span data-ttu-id="7cc60-141">Gögn sem tengjast öllum gagnaeiningum í verkinu er flutt út.</span><span class="sxs-lookup"><span data-stu-id="7cc60-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="7cc60-142">Þú getur sótt zip-skrá fyrir gagnapakkann.</span><span class="sxs-lookup"><span data-stu-id="7cc60-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="7cc60-143">Þessi skrá inniheldur öll gögnin á völdu sniðinu (til dæmis Excel snið).</span><span class="sxs-lookup"><span data-stu-id="7cc60-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="7cc60-144">Eins og áður hefur komið fram gæti verið að sumar færslur í gagnapakkaskránum þyrftu uppfærslu áður en hægt er að flytja þær inn í framleiðslu umhverfið.</span><span class="sxs-lookup"><span data-stu-id="7cc60-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="7cc60-145">Ef þú uppfærir færslu skaltu ganga úr skugga um að þú breytir ekki skráarnafninu.</span><span class="sxs-lookup"><span data-stu-id="7cc60-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="7cc60-146">Flytja inn skilgreiningu á uppsetningu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="7cc60-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="7cc60-147">Í áfangastaður umhverfi skaltu vera viss um að þú sért í fyrirtækið sem flytja á vöruhúsagögnin inn í.</span><span class="sxs-lookup"><span data-stu-id="7cc60-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cc60-148">Áður en þú framkvæmir innflutninginn ættir þú að bera kennsl á öll ákvæði milli gagna.</span><span class="sxs-lookup"><span data-stu-id="7cc60-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="7cc60-149">Til dæmis inniheldur sniðmátið **Vöruhúsastýring** gagnaeiningu sem heitir **Ráðstöfunarkóðar vöruhúss**.</span><span class="sxs-lookup"><span data-stu-id="7cc60-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="7cc60-150">Þessi eining inniheldur gögn sem tengjast uppsetningarsíðu **Ráðstöfunarkóðar** (**Vöruhúsastýring** > **Uppsetning** > **Fartæki** > **Ráðstöfunarkóðar**).</span><span class="sxs-lookup"><span data-stu-id="7cc60-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="7cc60-151">Ef núverandi uppsetning meðhöndlar nú þegar skilaferlið fyrir sölupantanir, inniheldur reiturinn **Skilaráðstöfunarkóði** gildi.</span><span class="sxs-lookup"><span data-stu-id="7cc60-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="7cc60-152">Ráðstöfunarkóðinn í þessum reit er tengdur við gagnaeiningu **Ráðstöfunarkóði**, sem er hluti af **Sölu- og markaðs** sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="7cc60-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="7cc60-153">Ef gögnin úr gagnaeiningu **Ráðstöfunarkóði** eru ekki flutt inn á undan gögnin úr reitnum **Ráðstöfunarkóðar vöruhúss** mun innflutningurinn mistakast.</span><span class="sxs-lookup"><span data-stu-id="7cc60-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="7cc60-154">Á vinnusvæðið **Gagnastjórnun** skal velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="7cc60-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="7cc60-155">Stofna nýtt innflutningsverk.</span><span class="sxs-lookup"><span data-stu-id="7cc60-155">Create a new import project.</span></span>
4. <span data-ttu-id="7cc60-156">Veldu **+ Bæta við skrá** og hlaða upp zip-skránni fyrir gagnapakkann.</span><span class="sxs-lookup"><span data-stu-id="7cc60-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="7cc60-157">Velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="7cc60-157">Select **Import**.</span></span> <span data-ttu-id="7cc60-158">Í **Aukið** yfirlit geturðu notað **Sía** valkost til að fá snögglega yfirlit yfir vandamál sem kunna að eiga sér stað við innflutning.</span><span class="sxs-lookup"><span data-stu-id="7cc60-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="7cc60-159">**Yfirlit aðgerða** skráin veitir nákvæmar upplýsingar um hverja gagnaeiningu sem er flutt inn.</span><span class="sxs-lookup"><span data-stu-id="7cc60-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="7cc60-160">Þú getur notað sviðsetningargögn yfirlitið til að komast á skömmum tíma að markgögnunum.</span><span class="sxs-lookup"><span data-stu-id="7cc60-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="7cc60-161">Þannig geturðu séð hvernig innfluttu gögnin líta út á tengdum síðum í forritinu.</span><span class="sxs-lookup"><span data-stu-id="7cc60-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="7cc60-162">Þegar þú notar sjálfgefin gagnasniðmát, virkar innflutningsröðin fyrir hverja gagnaeiningu á fyrirfram ákveðinni hátt, til að tryggja að öll háð gögn séu flutt inn fyrst.</span><span class="sxs-lookup"><span data-stu-id="7cc60-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="7cc60-163">Ef sérsniðin gagnaeiningar eru hluti af verkinu, verður þú að ganga úr skugga um að rétta röðin sé skilgreind.</span><span class="sxs-lookup"><span data-stu-id="7cc60-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="7cc60-164">Nánari upplýsingar, sjá [Gagnasniðmát skilgreiningar](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="7cc60-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="related-topic"></a><span data-ttu-id="7cc60-165">Tengt efni</span><span class="sxs-lookup"><span data-stu-id="7cc60-165">Related topic</span></span>

[<span data-ttu-id="7cc60-166">Gagnsniðmát stillingar</span><span class="sxs-lookup"><span data-stu-id="7cc60-166">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)

