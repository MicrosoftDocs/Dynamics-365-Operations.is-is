---
title: Breyta sniði rafrænnar skýrslugerðar til að mynda sérsniðið rafrænt skjal
description: Í þessu efnisatriði er útskýrt hvernig á að breyta rafrænu skýrslugerðarsniði frá Microsoft svo það búi til sérsniðið rafrænt skjal.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7355fbb3321a6b5707ab561e88aed2d22cc967cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743654"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="cbf27-103">Breyta sniði rafrænnar skýrslugerðar til að mynda sérsniðið rafrænt skjal</span><span class="sxs-lookup"><span data-stu-id="cbf27-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cbf27-104">Aðferðirnar í þessu efnisatriði útskýra hvernig notandi í hlutverki kerfisstjóra eða í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar getur framkvæmt þessi verk:</span><span class="sxs-lookup"><span data-stu-id="cbf27-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="cbf27-105">Skilgreinið færibreytur fyrir [Ramma rafrænnar skýrslugerðar](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="cbf27-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="cbf27-106">Flytjið inn skilgreiningar rafrænnar skýrslugerðar sem Microsoft veitir og eru notaðar til að búa til greiðsluskrár á meðan [greiðsla lánardrottins](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) er í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="cbf27-107">Búið til sérsniðna útgáfu af staðlaðri skilgreiningu rafræns skýrslugerðarsniðs sem Microsoft býður upp á.</span><span class="sxs-lookup"><span data-stu-id="cbf27-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="cbf27-108">Breytið sérsniðinni skilgreiningu rafrænnar skýrslugerðar þannig að hún búi til greiðsluskrár sem uppfylla kröfur tiltekins banka.</span><span class="sxs-lookup"><span data-stu-id="cbf27-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="cbf27-109">Innleiðið breytingar sem gerðar eru á staðlaðri skilgreiningu rafræns skýrslugerðarsniðs í sérsniðinni skilgreiningu rafræns skýrslugerðarsniðs.</span><span class="sxs-lookup"><span data-stu-id="cbf27-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="cbf27-110">Öll eftirfarandi ferli er hægt að vinna í **GBSI** fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="cbf27-111">Ekki er þörf á neinni kóðun.</span><span class="sxs-lookup"><span data-stu-id="cbf27-111">No coding is required.</span></span>

- [<span data-ttu-id="cbf27-112">Skilgreina ramma rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="cbf27-113">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="cbf27-114">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="cbf27-115">Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="cbf27-116">Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="cbf27-117">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="cbf27-118">Flytja inn staðlaðar skilgreiningar rafræns skýrslugerðarsniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="cbf27-119">Flytja inn staðlaðar skilgreiningar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="cbf27-120">Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="cbf27-121">Undirbúa greiðslu lánardrottins fyrir úrvinnslu</span><span class="sxs-lookup"><span data-stu-id="cbf27-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="cbf27-122">Bæta við bankaupplýsingum fyrir lánardrottnalykil</span><span class="sxs-lookup"><span data-stu-id="cbf27-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="cbf27-123">Færa inn greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="cbf27-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="cbf27-124">Vinna úr lánardrottnagreiðslu með því að nota staðlað snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="cbf27-125">Setja upp rafrænan greiðslumáta</span><span class="sxs-lookup"><span data-stu-id="cbf27-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="cbf27-126">Vinna úr lánardrottnagreiðslu</span><span class="sxs-lookup"><span data-stu-id="cbf27-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="cbf27-127">Sérsníða staðlað snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="cbf27-128">Búa til sérsniðið snið</span><span class="sxs-lookup"><span data-stu-id="cbf27-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="cbf27-129">Breyta sérsniðnu sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="cbf27-130">Merkja sérsniðið snið sem keyrsluhæft</span><span class="sxs-lookup"><span data-stu-id="cbf27-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="cbf27-131">Vinna úr greiðslu lánardrottins með því að nota sérsniðið snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="cbf27-132">Setja upp rafrænan greiðslumáta</span><span class="sxs-lookup"><span data-stu-id="cbf27-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="cbf27-133">Vinna úr lánardrottnagreiðslu</span><span class="sxs-lookup"><span data-stu-id="cbf27-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="cbf27-134">Flytja inn nýjar útgáfur af stöðluðum skilgreiningum rafræns skýrslugerðarsniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="cbf27-135">Flytja inn nýjar útgáfur af stöðluðum skilgreiningum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="cbf27-136">Fara yfir innfluttar skilgreiningar rafræns skýrslugerðarsniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="cbf27-137">Innleiða breytingarnar í nýju útgáfu innflutts sniðs í sérsniðnu sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="cbf27-138">Ljúkið við núgildandi drög að útgáfu sérsniðins sniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="cbf27-139">Endurstilla grunn sérsniðins sniðs á nýja grunnútgáfu</span><span class="sxs-lookup"><span data-stu-id="cbf27-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="cbf27-140">Vinna úr greiðslu lánardrottins með því að nota endurstilltan grunn rafræns skýrslugerðarsniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="cbf27-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cbf27-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="cbf27-142">Skilgreina ramma rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-142">Configure the ER framework</span></span>

<span data-ttu-id="cbf27-143">Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að skilgreina lágmarksstillingu á færibreytum rafrænnar skýrslugerðar áður en byrjað er að nota ramma rafrænnar skýrslugerðar til að hanna sérsniðna útgáfu á stöðluðu snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="cbf27-144">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-144">Configure ER parameters</span></span>

1. <span data-ttu-id="cbf27-145">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-146">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="cbf27-147">Á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Almennt**, skal stilla valkostinn **Kveikja á hönnunarstillingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="cbf27-148">Í flipanum **Viðhengi** skal stilla eftirfarandi færibreytur:</span><span class="sxs-lookup"><span data-stu-id="cbf27-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="cbf27-149">Í reitnum **Skilgreiningar** skal velja gerðina **Skrá** fyrir **USMF** fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="cbf27-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="cbf27-150">Í reitunum **Verksafn**, **Tímabundið**, **Grunnlína** og **Annað** skal velja gerð fyrir **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="cbf27-151">Frekari upplýsingar um færibreytur rafrænnar skýrslugerðar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cbf27-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="cbf27-152">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="cbf27-153">Allar skilgreiningar rafrænnar skýrslugerðar sem bætt er við eru merktar sem eign skilgreingarveitu rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="cbf27-154">Skilgreiningarveita rafrænnar skýrslugerðar sem er virkjuð á vinnusvæðinu **Rafræn skýrslugerð** er notuð í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="cbf27-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="cbf27-155">Þess vegna þarf að virkja skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð** áður en byrjað er að bæta við eða breyta skilgreiningum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="cbf27-156">Aðeins eigandi skilgreiningar rafrænnar skýrslugerðar getur breytt henni.</span><span class="sxs-lookup"><span data-stu-id="cbf27-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="cbf27-157">Þess vegna, áður en hægt er að breyta skilgreiningu rafrænnar skýrslugerðar, verður að virkja viðeigandi skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="cbf27-158">Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="cbf27-159">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-160">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="cbf27-161">Á síðunni **Tafla yfir skilgreiningarveitur** er hver færsla með einkvæmt heiti og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="cbf27-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="cbf27-162">Farið yfir efnið á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-162">Review the contents of this page.</span></span> <span data-ttu-id="cbf27-163">Ef færsla fyrir **Litware, Inc.** (`https://www.litware.com`) er þegar til skal sleppa næsta ferli, [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="cbf27-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="cbf27-164">Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="cbf27-165">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-166">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="cbf27-167">Á síðunni **Skilgreiningarveitur** skal velja **Ný**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="cbf27-168">Í reitinn **Heiti** skal færa inn **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="cbf27-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="cbf27-169">Í reitinn **Veffang** skal færa inn `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="cbf27-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="cbf27-170">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="cbf27-171">Virkja skilgreiningarveitu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="cbf27-172">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-173">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Litware, Inc.** og síðan velja **Stilla sem virkt**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="cbf27-174">Nánari upplýsingar um skilgreiningarveitur rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="cbf27-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="cbf27-175">Flytja inn staðlaðar skilgreiningar rafræns skýrslugerðarsniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="cbf27-176">Flytja inn staðlaðar skilgreiningar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-176">Import the standard ER configurations</span></span>

<span data-ttu-id="cbf27-177">Til að bæta stöðluðum skilgreiningum rafrænnar skýrslugerðar við núverandi tilvik af Microsoft Dynamics 365 Finance, þarf að flytja þær inn úr [gagnageymslu](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar sem var skilgreind fyrir það tilvik.</span><span class="sxs-lookup"><span data-stu-id="cbf27-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="cbf27-178">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-179">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Microsoft** og síðan velja **Gagnageymslur** til að skoða lista yfir gagnageymslur fyrir Microsoft-veituna.</span><span class="sxs-lookup"><span data-stu-id="cbf27-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="cbf27-180">Á síðunni **Skilgreiningageymslur** skal velja gagnageymslu af gerðinni **Altæk** og síðan velja **Opna**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="cbf27-181">Ef beðið er um heimild til að tengjast við Regulatory Configuration Service, skal fylgja leiðbeiningum um heimild.</span><span class="sxs-lookup"><span data-stu-id="cbf27-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="cbf27-182">Á síðunni **Skilgreiningageymsla**, í skilgreiningatrénu vinstra megin á svæðinu, skal velja skilgreiningarsniðið **BACS (Bretland)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="cbf27-183">Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1** af valdri skilgreiningu rafræns skýrslugerðarsniðs.</span><span class="sxs-lookup"><span data-stu-id="cbf27-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="cbf27-184">Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu í núverandi fjármálatilvik.</span><span class="sxs-lookup"><span data-stu-id="cbf27-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Síðan Skilgreiningagagnasafn](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="cbf27-186">Ef það reynist erfitt að opna [Altæka geymsla](er-download-configurations-global-repo.md) er hægt að [sækja skilgreiningar](download-electronic-reporting-configuration-lcs.md) hjá Microsoft Dynamics Lifecycle Services (LCS) í staðinn.</span><span class="sxs-lookup"><span data-stu-id="cbf27-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="cbf27-187">Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="cbf27-188">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-189">Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="cbf27-190">Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="cbf27-191">Takið eftir að til viðbótar við valið **BACS (Bretland)** snið rafrænnar skýrslugerðar, voru aðrar áskildar skilgreiningar rafrænnar skýrslugerðar fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="cbf27-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="cbf27-192">Gangið úr skugga um að eftirfarandi skilgreiningar rafrænnar skýrslugerðar séu í boði í skilgreiningartrénu:</span><span class="sxs-lookup"><span data-stu-id="cbf27-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="cbf27-193">**Greiðslulíkan** – Þessi skilgreining inniheldur hlutann [gagnalíkan](general-electronic-reporting.md#data-model-and-model-mapping-components) í rafrænni skýrslugerð sem táknar gagnaskipulag fyrir viðskiptalén greiðslna.</span><span class="sxs-lookup"><span data-stu-id="cbf27-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="cbf27-194">**Vörpun greiðslulíkans 1611** – Þessi skilgreining inniheldur hlutann [líkanavörpun](general-electronic-reporting.md#data-model-and-model-mapping-components) fyrir rafræna skýrslugerð sem lýsir því hvernig gagnalíkanið er fyllt út með forritsgögnum við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="cbf27-195">**BACS (Bretland)** – Þessi skilgreining inniheldur hlutann [snið](general-electronic-reporting.md#FormatComponentOutbound) og sniðsvörpun í rafrænni skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="cbf27-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="cbf27-196">Sniðshlutinn tilgreinir útlit skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-196">The format component specifies the report layout.</span></span> <span data-ttu-id="cbf27-197">Sniðsvörpunarhlutinn inniheldur gagnagjafa líkansins og tilgreinir hvernig fyllt er út í skýrsluútlitið með því að nota þennan gagnagjafa við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Skilgreiningasíða](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="cbf27-199">Undirbúa greiðslu lánardrottins fyrir úrvinnslu</span><span class="sxs-lookup"><span data-stu-id="cbf27-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="cbf27-200">Bæta við bankaupplýsingum fyrir lánardrottnalykil</span><span class="sxs-lookup"><span data-stu-id="cbf27-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="cbf27-201">Bæta þarf við bankaupplýsingum fyrir lánardrottnalykil sem vísað verður til síðar í skráðri greiðslu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="cbf27-202">Farið í **Viðskiptaskuldir** \> **Lánardrottnar** \> **Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="cbf27-203">Á síðunni **Allir lánardrottnar** skal velja lánardrottnalykilinn **GB_SI_000001** og síðan, á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Uppsetning**, skal velja **Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="cbf27-204">Á síðunni **Bankareikningar lánardrottins** skal smella á **Nýr** og færa síðan inn eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="cbf27-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="cbf27-205">Í reitinn **Bankareikningur** skal færa inn **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="cbf27-206">Í reitnum **Bankaflokkar** skal velja **BankGBP**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="cbf27-207">Í reitinn **Bankareikningsnúmer** skal færa inn **202015**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="cbf27-208">Í reitinn **SWIFT-kóði** skal færa inn <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="cbf27-209">Í reitinn **IBAN** skal færa inn **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="cbf27-210">Í reitnum **Leiðarnúmer** skal halda sjálfgefna gildinu <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Síðan fyrir bankareikninga lánardrottna](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="cbf27-212">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-212">Select **Save**.</span></span>
5. <span data-ttu-id="cbf27-213">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cbf27-213">Close the page.</span></span>
6. <span data-ttu-id="cbf27-214">Á síðunni **Allir lánardrottnar** skal opna lánardrottnalykilinn **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="cbf27-215">Á upplýsingasíðu lánardrottins skal velja **Breyta** til að gera síðuna breytanleg ef á þarf að halda.</span><span class="sxs-lookup"><span data-stu-id="cbf27-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="cbf27-216">Í flýtiflipanum **Greiðsla**, í reitnum **Bankareikningur**, skal velja **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Upplýsingasíða lánardrottins](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="cbf27-218">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-218">Select **Save**.</span></span>
10. <span data-ttu-id="cbf27-219">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cbf27-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="cbf27-220">Færa inn greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="cbf27-220">Enter a vendor payment</span></span>

<span data-ttu-id="cbf27-221">Færa verður inn nýja lánardrottnagreiðslu með því að nota [greiðslutillaga](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span><span class="sxs-lookup"><span data-stu-id="cbf27-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="cbf27-222">Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="cbf27-223">Á síðunni **Greiðslubók lánardrottins** skal velja **Ný**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="cbf27-224">Í reitinn **Heiti** skal velja **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="cbf27-225">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-225">Select **Lines**.</span></span>
5. <span data-ttu-id="cbf27-226">Veljið **Greiðslutillaga** \> **Stofna greiðslutillögu**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="cbf27-227">Í svarglugganum **Greiðslutillaga lánardrottins** skal stilla skilyrði til að afmarka færslur niður í eingöngu lánardrottnalykilinn **GB_SI_000001** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="cbf27-228">Veljið línuna fyrir reikninginn **00000007_Inv** og veljið síðan **Stofna greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Svargluggi greiðslutillögu lánardrottins](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="cbf27-230">Gangið úr skugga um að greiðslan sem slegin er inn sé skilgreind til að nota **Rafrænan** greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="cbf27-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Síðan Greiðslur lánardrottna](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="cbf27-232">Vinna úr lánardrottnagreiðslu með því að nota staðlað snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="cbf27-233">Setja upp rafrænan greiðslumáta</span><span class="sxs-lookup"><span data-stu-id="cbf27-233">Set up the electronic payment method</span></span>

<span data-ttu-id="cbf27-234">Skilgreina þarf rafrænan greiðslumáta þannig að hann noti innflutta skilgreiningu fyrir snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="cbf27-235">Farið í **Viðskiptaskuldir** \> **Greiðsluuppsetning** \> **Greiðsluháttur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="cbf27-236">Á síðunni **Greiðslumátar - lánardrottnar** skal velja greiðslumátann **Rafrænt** vinstra megin á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="cbf27-237">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-237">Select **Edit**.</span></span>
4. <span data-ttu-id="cbf27-238">Í flýtiflipanum **Skráarsnið** skal stilla valkostinn **Almennt rafrænt útflutningssnið** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="cbf27-239">Í reitnum **Skilgreining útflutningssniðs** skal velja skilgreiningarsniðið **BACS (Bretland)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Greiðslumátar - síða lánardrottins](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="cbf27-241">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="cbf27-242">Vinna úr lánardrottnagreiðslu</span><span class="sxs-lookup"><span data-stu-id="cbf27-242">Process a vendor payment</span></span>

1. <span data-ttu-id="cbf27-243">Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="cbf27-244">Á síðunni **Greiðslubók lánardrottins** skal velja þá greiðslubók sem var áður bætt við og síðan velja **Línur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="cbf27-245">Á síðunni **Greiðslur lánardrottna** skal velja **Búa til greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="cbf27-246">Í svarglugganum **Búa til greiðslur** skal færa inn eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="cbf27-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="cbf27-247">Í reitnum **Greiðslumáti** skal velja **Rafrænn**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="cbf27-248">Í reitnum **Bankareikningur** skal velja **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="cbf27-249">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-249">Select **OK**.</span></span>
6. <span data-ttu-id="cbf27-250">Í svarglugganum **Rafrænar skýrslufæribreytur** skal stilla valkostinn **Prenta eftirlitsskýrslu** á **Já** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Síða rafrænna skýrslufæribreyta](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="cbf27-252">Auk greiðsluskrárinnar er nú hægt að búa til eftirlitsskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="cbf27-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="cbf27-253">Sækið zip-skrána og dragið síðan eftirfarandi skrár út úr henni:</span><span class="sxs-lookup"><span data-stu-id="cbf27-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="cbf27-254">Eftirlitsskýrslan á Excel-sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-254">The control report in Excel format</span></span>
    - <span data-ttu-id="cbf27-255">Greiðsluskráin á TXT-sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-255">The payment file in TXT format</span></span>

        <span data-ttu-id="cbf27-256">Takið eftir því, að í samræmi við [skipulag](#PositionRoutingNumber) á uppgefnu sniði rafrænnar skýrslugerðar, hefst greiðslulínan í útbúinni skrá á leiðarnúmerinu sem var [skilgreint](#DefineRoutingNumber) fyrir skilgreindan bankareikning.</span><span class="sxs-lookup"><span data-stu-id="cbf27-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Greiðsluskrá á TXT-sniði](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="cbf27-258">Sérsníða staðlað snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-258">Customize the standard ER format</span></span>

<span data-ttu-id="cbf27-259">Fyrir dæmið sem sýnt er í þessum hluta er best að nota skilgreiningar rafrænnar skýrslugerðar sem Microsoft býður upp á til að búa til greiðsluskrár lánardrottna á BACS-sniði, en bæta verður við sérstillingu til að styðja kröfur tiltekins banka.</span><span class="sxs-lookup"><span data-stu-id="cbf27-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="cbf27-260">Einnig á að vera hægt að uppfæra sérstillta sniðið þegar koma nýjar útgáfur á skilgreiningum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="cbf27-261">Aftur á móti vill maður geta uppfært með sem minnstum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="cbf27-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="cbf27-262">Í þessu tilfelli, sem fulltrúi Litware, Inc., þarf að búa til (afleiða) nýja skilgreiningu rafrænnar skýrslugerðar með því að nota **BACS (Bretland)** skilgreiningu sem Microsoft býður upp á sem grunn.</span><span class="sxs-lookup"><span data-stu-id="cbf27-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="cbf27-263">Búa til sérsniðið snið</span><span class="sxs-lookup"><span data-stu-id="cbf27-263">Create a custom format</span></span>

1. <span data-ttu-id="cbf27-264">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="cbf27-265">Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja síðan **BACS (Bretland)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="cbf27-266">Litware, Inc. notar útgáfu 1.1 af þessari skilgreiningu rafrænnar skýrslugerðar sem grunn fyrir sérsniðnu útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="cbf27-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="cbf27-267">Veljið **Stofna skilgreiningu** til að opna fellilistagluggann.</span><span class="sxs-lookup"><span data-stu-id="cbf27-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="cbf27-268">Hægt er að nota þennan glugga til að stofna nýja skilgreiningu fyrir sérstillt greiðslusnið.</span><span class="sxs-lookup"><span data-stu-id="cbf27-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="cbf27-269">Í reitahópnum **Ný** skal velja valkostinn **Leiða af heiti: BACS (Bretland), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="cbf27-270">Í reitinn **Heiti** skal færa inn **BACS (Bresk tollayfirvöld)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Stofna fellivalmynd stillinga](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="cbf27-272">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-272">Select **Create configuration**.</span></span>

<span data-ttu-id="cbf27-273">Útgáfa 1.1.1 af **BACS (Bresk tollayfirvöld)** skilgreiningarsniði rafrænnar skýrslugerðar er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="cbf27-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="cbf27-274">Þessi útgáfa er með [stöðuna](general-electronic-reporting.md#component-versioning) **Drög** og er hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="cbf27-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="cbf27-275">Núverandi efni af sérstilltu sniði rafrænnar skýrslugerðar samsvarar efni sniðsins sem Microsoft býður upp á.</span><span class="sxs-lookup"><span data-stu-id="cbf27-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Skilgreiningasíða](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="cbf27-277">Breyta sérsniðnu sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-277">Edit a custom format</span></span>

<span data-ttu-id="cbf27-278">Skilgreina þarf sérstillta sniðið þannig að það standist tilteknar kröfur bankans.</span><span class="sxs-lookup"><span data-stu-id="cbf27-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="cbf27-279">Bank gæti til dæmis gert kröfu um að greiðsluskrár sem búnar eru til feli í sér SWIFT-kóða þess banka sem úthlutað er hlutverki umboðsaðila í meðhöndlaðri greiðslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="cbf27-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="cbf27-280">SWIFT-kóðar eru alþjóðlegir bankakóðar sem auðkenna tiltekna banka um allan heim.</span><span class="sxs-lookup"><span data-stu-id="cbf27-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="cbf27-281">Þeir eru einnig þekktar sem auðkenniskóðar banka (BICs).</span><span class="sxs-lookup"><span data-stu-id="cbf27-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="cbf27-282">SWIFT-kóðinn verður að vera 11 stafir að lengd og það verður að færa hann inn við upphaf allra greiðslulína í greiðsluskrá sem búin er til.</span><span class="sxs-lookup"><span data-stu-id="cbf27-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="cbf27-283">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="cbf27-284">Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja síðan **BACS (Bresk tollayfirvöld)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="cbf27-285">Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1.1** af valdri skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="cbf27-286">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-286">Select **Designer**.</span></span>
5. <span data-ttu-id="cbf27-287">Á síðunni **Sniðshönnuður** skal velja **Sýna upplýsingar** til að skoða frekari upplýsingar um sniðseiningarnar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="cbf27-288">Stækkið og yfirfarið eftirfarandi einingar:</span><span class="sxs-lookup"><span data-stu-id="cbf27-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="cbf27-289">**BACSReportsFolder** eining af gerðinni **Mappa**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="cbf27-290">Þessi eining er notuð til að búa til úttak á ZIP-sniði.</span><span class="sxs-lookup"><span data-stu-id="cbf27-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="cbf27-291">Einingin **skrá** af gerðinni **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="cbf27-292">Þessi eining er notuð til að búa til greiðsluskrá á TXT-sniði.</span><span class="sxs-lookup"><span data-stu-id="cbf27-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="cbf27-293">Einingin **færslur** af gerðinni **Röð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="cbf27-294">Þessi eining er notuð til að búa til eina greiðslulínu í greiðsluskrá.</span><span class="sxs-lookup"><span data-stu-id="cbf27-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="cbf27-295">Einingin **færsla** af gerðinni **Röð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="cbf27-296">Þessi eining er notuð til að búa til staka reiti fyrir eina greiðslulínu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="cbf27-297">Veljið eininguna **færsla**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-297">Select the **transaction** element.</span></span>

    ![Færslueining í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="cbf27-299">Uppgefin skýrsla er stillt þannig að <a id="PositionRoutingNumber"></a>hver greiðslulína hefjist á leiðarnúmeri bankans.</span><span class="sxs-lookup"><span data-stu-id="cbf27-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="cbf27-300">Sniðseiningin **vendBankRouteNum** er notuð í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="cbf27-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="cbf27-301">Veljið **Bæta við** og síðan gerðina **Texti\\Strengur** fyrir sniðseininguna sem verið er að bæta við:</span><span class="sxs-lookup"><span data-stu-id="cbf27-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="cbf27-302">Í reitinn **Heiti** skal færa inn **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="cbf27-303">Í reitinn **Lágmarkslengd** skal slá inn **11**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="cbf27-304">Í reitinn **Hámarkslengd** skal slá inn **11**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="cbf27-305">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cbf27-306">Einingin **vendBankSWIFT** verður notuð til að færa inn SWIFT-kóða fyrir banka lánardrottins í útbúnum skrám.</span><span class="sxs-lookup"><span data-stu-id="cbf27-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="cbf27-307">Í trjáskipan sniðs skal velja **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="cbf27-308">Veljið **Færa upp** til að færa valda sniðseiningu upp um eitt stig.</span><span class="sxs-lookup"><span data-stu-id="cbf27-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="cbf27-309">Endurtakið þetta skref þar til einingin **vendBankSWIFT** er <a id="PositionSWIFTCode"></a>fyrsta einingin undir yfireiningunni **færsla**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT sem fyrsta einingin undir færslu í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="cbf27-311">Á meðan **vendBankSWIFT** er enn valið í trjáskipan sniðs skal velja flipann **Vörpun** og síðan stækka gagnagjafann **líkan**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="cbf27-312">Stækkið **model.Payment** \> **model.Payment.CreditorAgent** og veljið gagnagjafareitinn **model.Payment.CreditorAgent.BICFI**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="cbf27-313">Þessi gagnagjafareitur sýnir SWIFT-kóðann fyrir banka lánardrottins sem úthlutað er hlutverki umboðsaðila í meðhöndlaðri greiðslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="cbf27-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="cbf27-314">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-314">Select **Bind**.</span></span> <span data-ttu-id="cbf27-315">Sniðseiningin **vendBankSWIFT** er nú bundin við gagnagjafareitinn **model.Payment.CreditorAgent.BICFI** þannig að SWIFT-kóðar verða færðir inn í greiðsluskrár sem búnar eru til.</span><span class="sxs-lookup"><span data-stu-id="cbf27-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![vendBankSWIFT sniðseiningin bundin við gagnagjafareitinn model.Payment.CreditorAgent.BICFI í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="cbf27-317">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-317">Select **Save**.</span></span>
15. <span data-ttu-id="cbf27-318">Lokið hönnunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="cbf27-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="cbf27-319">Merkja sérsniðið snið sem keyrsluhæft</span><span class="sxs-lookup"><span data-stu-id="cbf27-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="cbf27-320">Nú þegar fyrsta útgáfa af sérstilltu sniði hefur verið stofnuð og er með stöðuna **Drög**, er hægt að prufukeyra hana.</span><span class="sxs-lookup"><span data-stu-id="cbf27-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="cbf27-321">Til að keyra skýrsluna þarf að vinna úr greiðslu lánardrottins með því að nota greiðslumátann sem vísar til sérstillts sniðs rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="cbf27-322">Sjálfgefið er að þegar kallað er á snið rafrænnar skýrslugerðar úr forritinu, eru aðeins útgáfur sem eru með stöðuna **Lokið** eða **Samnýtt** [teknar til greina](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="cbf27-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="cbf27-323">Þessi leið hjálpar til við að koma í veg fyrir að snið rafrænnar skýrslugerðar með ókláraðri hönnun verði notuð.</span><span class="sxs-lookup"><span data-stu-id="cbf27-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="cbf27-324">Fyrir prufukeyrslur er hinsvegar hægt að þvinga forritið til að nota sniðsútgáfu rafrænnar skýrslugerðar sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="cbf27-325">Á þennan hátt er hægt að leiðrétta núverandi sniðsútgáfu ef gera þarf einhverjar breytingar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="cbf27-326">Frekari upplýsingar er að finna í [Nothæfni](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="cbf27-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="cbf27-327">Til að nota útgáfudrög af sniði rafrænnar skýrslugerðar þarf sérstaklega að merkja rafræna skýrslugerðarsniðið.</span><span class="sxs-lookup"><span data-stu-id="cbf27-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="cbf27-328">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="cbf27-329">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="cbf27-330">Í glugganum **Færibreytur notanda** skal stilla valkostinn **Keyra stillingar** á **Já** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="cbf27-331">Veljið **Breyta** til að gera núverandi síðu breytanlega ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="cbf27-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="cbf27-332">Í skilgreiningatrénu vinstra megin á svæðinu skal velja **BACS (Bresk tollayfirvöld)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="cbf27-333">Stillið valkostinn **Keyra drög** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Keyra valkostinn fyrir drög á skilgreiningarsíðunni](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="cbf27-335">Vinna úr greiðslu lánardrottins með því að nota sérsniðið snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="cbf27-336">Setja upp rafrænan greiðslumáta</span><span class="sxs-lookup"><span data-stu-id="cbf27-336">Set up the electronic payment method</span></span>

<span data-ttu-id="cbf27-337">Skilgreina þarf rafrænan greiðslumáta þannig að sérstillt snið rafrænnar skýrslugerðar sé notað til að vinna úr lánardrottnagreiðslum.</span><span class="sxs-lookup"><span data-stu-id="cbf27-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="cbf27-338">Farið í **Viðskiptaskuldir** \> **Greiðsluuppsetning** \> **Greiðsluháttur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="cbf27-339">Á síðunni **Greiðslumátar - lánardrottnar** skal velja greiðslumátann **Rafrænt** vinstra megin á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="cbf27-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="cbf27-340">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-340">Select **Edit**.</span></span>
4. <span data-ttu-id="cbf27-341">Í flýtiflipanum **Skráarsnið** skal stilla valkostinn **Almennt rafrænt útflutningssnið** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="cbf27-342">Í reitnum **Skilgreining útflutningssniðs** skal velja skilgreiningarsniðið **BACS (Bresk tollayfirvöld)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Greiðslumátar - síða lánardrottins](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="cbf27-344">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="cbf27-345">Vinna úr lánardrottnagreiðslu</span><span class="sxs-lookup"><span data-stu-id="cbf27-345">Process a vendor payment</span></span>

1. <span data-ttu-id="cbf27-346">Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="cbf27-347">Á síðunni **Greiðslubók lánardrottins** skal velja þá greiðslubók sem var áður búin til.</span><span class="sxs-lookup"><span data-stu-id="cbf27-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="cbf27-348">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-348">Select **Lines**.</span></span>
4. <span data-ttu-id="cbf27-349">Á síðunni **Greiðslur lánardrottna**, fyrir ofan hnitanetið, skal velja **Greiðslustaða** \> **Engin**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="cbf27-350">Smellið á **Búa til greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="cbf27-351">Í svarglugganum **Búa til greiðslur** skal færa inn eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="cbf27-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="cbf27-352">Í reitnum **Greiðslumáti** skal velja **Rafrænn**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="cbf27-353">Í reitnum **Bankareikningur** skal velja **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="cbf27-354">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-354">Select **OK**.</span></span>
8. <span data-ttu-id="cbf27-355">Í svarglugganum **Rafrænar skýrslufæribreytur** skal stilla valkostinn **Prenta eftirlitsskýrslu** á **Já** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cbf27-356">Auk greiðsluskráarinnar er eingöngu hægt að búa til eftirlitsskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="cbf27-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="cbf27-357">Sækið zip-skrána og dragið síðan eftirfarandi skrár út úr henni:</span><span class="sxs-lookup"><span data-stu-id="cbf27-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="cbf27-358">Eftirlitsskýrslan á Excel-sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-358">The control report in Excel format</span></span>
    - <span data-ttu-id="cbf27-359">Greiðsluskráin á TXT-sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-359">The payment file in TXT format</span></span>

        <span data-ttu-id="cbf27-360">Takið eftir því, í samræmi við skipulag á sérstilltu sniði rafrænnar skýrslugerðar, að greiðslulínan [hefst](#PositionSWIFTCode) nú á SWIFT-kóðanum sem var [sleginn inn](#DefineSWIFTCode) fyrir bankareikning lánardrottins sem er með greiðslu sem unnið hefur verið úr.</span><span class="sxs-lookup"><span data-stu-id="cbf27-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Greiðsluskrá á TXT-sniði](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="cbf27-362">Flytja inn nýjar útgáfur af stöðluðum skilgreiningum rafræns skýrslugerðarsniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="cbf27-363">Fyrir dæmið sem sýnt er í þessum hluta kemur tilkynning um þekkingargrunnsgreinina [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="cbf27-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="cbf27-364">Þessi tilkynning veitir upplýsingar um nýju sniðsútgáfuna **BACS (Bretland)** fyrir rafræna skýrslugerð sem Microsoft hefur gefið út.</span><span class="sxs-lookup"><span data-stu-id="cbf27-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="cbf27-365">Ásamt eftirlitsskýrslunni gerir þessi nýja útgáfa notendum kleift að búa til skýrslu greiðslutilkynningr og skýrsla um þátttökuathugasemd á meðan unnið er úr greiðslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="cbf27-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="cbf27-366">Mælt er með því að hefja notkun á þessari virkni.</span><span class="sxs-lookup"><span data-stu-id="cbf27-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="cbf27-367">Flytja inn nýjar útgáfur af stöðluðum skilgreiningum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cbf27-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="cbf27-368">Til að bæta nýjum útgáfum af skilgreiningum rafrænnar skýrslugerðar við núverandi Finance-tilvik þarf að flytja þær inn úr [gagnageymslu](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar sem voru skilgreindar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="cbf27-369">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-370">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Microsoft** og síðan velja **Gagnageymslur** til að skoða lista yfir gagnageymslur fyrir Microsoft-veituna.</span><span class="sxs-lookup"><span data-stu-id="cbf27-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="cbf27-371">Á síðunni **Skilgreiningageymslur** skal velja gagnageymslu af gerðinni **Altæk** og síðan velja **Opna**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="cbf27-372">Ef beðið er um heimild til að tengjast við Regulatory Configuration Service, skal fylgja leiðbeiningum um heimild.</span><span class="sxs-lookup"><span data-stu-id="cbf27-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="cbf27-373">Á síðunni **Skilgreiningageymsla**, í skilgreiningatrénu vinstra megin á svæðinu, skal velja skilgreiningarsniðið **BACS (Bretland)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="cbf27-374">Í flýtiflipanum **Útgáfur** skal velja útgáfuna **3.3** af valdri skilgreiningu rafræns skýrslugerðarsniðs.</span><span class="sxs-lookup"><span data-stu-id="cbf27-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="cbf27-375">Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu í núverandi fjármálatilvik.</span><span class="sxs-lookup"><span data-stu-id="cbf27-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Síðan Skilgreiningagagnasafn](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="cbf27-377">Ef það reynist erfitt að opna [Altæka geymsla](er-download-configurations-global-repo.md) er hægt að [sækja skilgreiningar](download-electronic-reporting-configuration-lcs.md) hjá LCS í staðinn.</span><span class="sxs-lookup"><span data-stu-id="cbf27-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="cbf27-378">Fara yfir innfluttar skilgreiningar rafræns skýrslugerðarsniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="cbf27-379">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-380">Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="cbf27-381">Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja síðan **BACS (Bretland)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="cbf27-382">Í flýtiflipanum **Útgáfur** skal velja útgáfuna **3.3**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="cbf27-383">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-383">Select **Designer**.</span></span>
6. <span data-ttu-id="cbf27-384">Á síðunni **Sniðshönnuður** skal stækka sniðseininguna **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="cbf27-385">Takið eftir að útgáfa 3.3 inniheldur sniðseininguna **PaymentAdviceReport** sem notuð er til að búa til skýrslu greiðslutilkynninga þegar unnið er úr greiðslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="cbf27-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![Sniðseiningin PaymentAdviceReport í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="cbf27-387">Lokið hönnunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="cbf27-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="cbf27-388">Innleiða breytingarnar í nýju útgáfu innflutts sniðs í sérsniðnu sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="cbf27-389">Ljúkið við núgildandi drög að útgáfu sérsniðins sniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="cbf27-390">Ef ætlunin er að halda núverandi ástandi á sérstilltu sniði, skal ljúka útgáfudrögum 1.1.1 með því að breyta stöðu hennar úr **Drög** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="cbf27-391">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cbf27-392">Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="cbf27-393">Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan**, stækka **BACS (Bretland)** og velja síðan **BACS (Bresk tollayfirvöld)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="cbf27-394">Í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="cbf27-395">Staða útgáfu 1.1.1 er breytt úr **Drög** í **Lokið** og útgáfa verður skrifvarin.</span><span class="sxs-lookup"><span data-stu-id="cbf27-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="cbf27-396">Nýrri og breytanlegri útgáfa 1.1.2 hefur verið bætt við og er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="cbf27-397">Hægt er að nota þessa útgáfu til að gera frekari breytingar á sérstilltu sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="cbf27-398">Endurstilla grunn sérsniðins sniðs á nýja grunnútgáfu</span><span class="sxs-lookup"><span data-stu-id="cbf27-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="cbf27-399">Til að byrja að nota nýja virkni fyrir útgáfu 3.3 af sniðinu **BACS (Bretland)** í sérstillingunum, þarf að breyta grunnskilgreiningu útgáfunnar fyrir sérstilltu skilgreininguna, **BACS (Bresk tollayfirvöld)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="cbf27-400">Þetta ferli kallast [endurreikningur](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="cbf27-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="cbf27-401">Í stað útgáfu 1.1 af **BACS (Bretland)** skal nota útgáfu 3.3.</span><span class="sxs-lookup"><span data-stu-id="cbf27-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="cbf27-402">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="cbf27-403">Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja síðan **BACS (Bresk tollayfirvöld)**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="cbf27-404">Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1.2** og síðan velja **Endurstilla grunn**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="cbf27-405">Í svarglugganum **Endurstilla grunn**, í reitnum **Markútgáfa**, skal velja útgáfu **3.3** grunnskilgreiningarinnar til að nota hana sem nýja grunninn og til að uppfæra skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="cbf27-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Gluggi fyrir endurreikning grunns](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="cbf27-407">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-407">Select **OK**.</span></span>
6. <span data-ttu-id="cbf27-408">Takið eftir að númer útgáfudraga hefur breyst úr **1.1.2** í **3.3.2** til að endurspegla breytinguna í grunnútgáfunni.</span><span class="sxs-lookup"><span data-stu-id="cbf27-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="cbf27-409">Þegar sérstillta útgáfan og nýja grunnútgáfan eru sameinaðar gætu einhverjir árekstrar uppgötvast vegna sniðsbreytinga sem ekki er hægt að sameina sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="cbf27-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Endurstilltur grunnur skilgreiningar með árekstrum á skilgreiningarsíðunni](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="cbf27-411">Ef árekstrar uppgötvast verða að leysa úr þeim handvirkt í sniðshönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="cbf27-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="cbf27-412">Í flýtiflipanum **Útgáfur** skal velja útgáfuna **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="cbf27-413">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-413">Select **Designer**.</span></span>
9. <span data-ttu-id="cbf27-414">Á síðunni **Sniðshönnuður**, í flýtiflipanum **Upplýsingar**, skal velja færslu fyrir árekstur endurstillts grunns og síðan velja **Nota grunngildi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Færsla fyrir árekstur endurstillts grunns í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="cbf27-416">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-416">Select **Save**.</span></span>

    <span data-ttu-id="cbf27-417">Færsla fyrir árekstur endurstillts grunns ætti ekki lengur að birtast í flýtiflipanum **Upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Leyst úr árekstri í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="cbf27-419">Leyst var úr árekstrinum með því að staðfesta að nota verður útgáfu 3 fyrir grunnlíkanið í þessu sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="cbf27-420">Stækkið **BACSReportsFolder** \> **skrá** \> **færslur** \> **færsla**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="cbf27-421">Takið eftir í flipanum **Vörpun** að útgáfa 3.3.2 af sérstilltu sniði rafrænnar skýrslugerðar inniheldur bæði sérstillinguna (sniðseiningin **vendBankSWIFT** og bindingu hennar) og nýja virkni útgáfu 3.3 af grunnsniði rafrænnar skýrslugerðar sem kom frá Microsoft (sniðseiningin **PaymentAdviceReport** ásamt földuðum einingum og skilgreindum bindingum).</span><span class="sxs-lookup"><span data-stu-id="cbf27-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="cbf27-422">Í aðeins örfáum músarsmellum voru breytingarnar gerðar á nýju grunnútgáfunni með því að sameina þær við sérstillinguna.</span><span class="sxs-lookup"><span data-stu-id="cbf27-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Sameinað snið í aðgerðarhönnuði rafrænnar skýrslugerðar](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="cbf27-424">Lokið hönnunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="cbf27-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="cbf27-425">Endurstillingaraðgerð grunns er afturkræf.</span><span class="sxs-lookup"><span data-stu-id="cbf27-425">The rebase action is reversible.</span></span> <span data-ttu-id="cbf27-426">Til að hætta við þessa endurstillingu grunns skal velja **1.1.1** fyrir sniðið **BACS (Bresk tollayfirvöld)** í flýtiflipanum **Útgáfur** og velja síðan **Ná í þessa útgáfu**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="cbf27-427">Útgáfa 3.3.2 verður síðan gefið númerið 1.1.2 og efni útgáfudraga 1.1.2 munu samsvara efni í útgáfu 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="cbf27-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="cbf27-428">Vinna úr greiðslu lánardrottins með því að nota endurstilltan grunn rafræns skýrslugerðarsniðs</span><span class="sxs-lookup"><span data-stu-id="cbf27-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="cbf27-429">Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="cbf27-430">Á síðunni **Greiðslubók lánardrottins** skal velja þá greiðslubók sem var áður búin til.</span><span class="sxs-lookup"><span data-stu-id="cbf27-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="cbf27-431">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-431">Select **Lines**.</span></span>
4. <span data-ttu-id="cbf27-432">Á síðunni **Greiðslur lánardrottna**, fyrir ofan hnitanetið, skal velja **Greiðslustaða** \> **Engin**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="cbf27-433">Smellið á **Búa til greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="cbf27-434">Í svarglugganum **Búa til greiðslur** skal færa inn eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="cbf27-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="cbf27-435">Í reitnum **Greiðslumáti** skal velja **Rafrænn**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="cbf27-436">Í reitnum **Bankareikningur** skal velja **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="cbf27-437">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-437">Select **OK**.</span></span>
8. <span data-ttu-id="cbf27-438">Í svarglugganum **Rafrænar skýrslufæribreytur** skal færa inn eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="cbf27-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="cbf27-439">Stilltu valkostinn **Prenta eftirlitsskýrslu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="cbf27-440">Stillið valkostinn **Prenta greiðslutilkynningu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Svargluggi rafrænna skýrslufæribreyta](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="cbf27-442">Auk greiðsluskráarinnar er nú hægt að búa til eftirlitsskýrsluna og skýrslu greiðslutilkynningar.</span><span class="sxs-lookup"><span data-stu-id="cbf27-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="cbf27-443">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cbf27-443">Select **OK**.</span></span>
10. <span data-ttu-id="cbf27-444">Sækið zip-skrána og dragið síðan eftirfarandi skrár út úr henni:</span><span class="sxs-lookup"><span data-stu-id="cbf27-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="cbf27-445">Eftirlitsskýrslan á Excel-sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-445">The control report in Excel format</span></span>
    - <span data-ttu-id="cbf27-446">Skýrsla greiðslutilkynningar á Excel-sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-446">The payment advice report in Excel format</span></span>

        ![Skýrsla greiðslutilkynningar á Excel-sniði](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="cbf27-448">Greiðsluskráin á TXT-sniði</span><span class="sxs-lookup"><span data-stu-id="cbf27-448">The payment file in TXT format</span></span>

        <span data-ttu-id="cbf27-449">Takið eftir því að greiðslulínan í myndaðri skrá hefst á SWIFT-kóðanum sem var sleginn inn fyrir bankareikning lánardrottins sem er með greiðslu sem unnið hefur verið úr.</span><span class="sxs-lookup"><span data-stu-id="cbf27-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Greiðsluskrá á TXT-sniði](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="cbf27-451">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cbf27-451">Additional resources</span></span>

- [<span data-ttu-id="cbf27-452">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="cbf27-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cbf27-453">Sækja skilgreiningar rafrænnar skýrslugerðar úr Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="cbf27-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="cbf27-454">Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu</span><span class="sxs-lookup"><span data-stu-id="cbf27-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]