---
title: Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Ítalíu
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Ítalíu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ea0408f4ef72bf77a0659799075338e4e6b2aa30
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835973"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="f61cc-103">Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Ítalíu</span><span class="sxs-lookup"><span data-stu-id="f61cc-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="f61cc-104">Viðbót rafrænnar reikningsfærslu fyrir Ítalíu styður eins og er hugsanlega ekki allar aðgerðir sem eru í boði fyrir rafræna reikningsfærslu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f61cc-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="f61cc-105">Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Ítalíu.</span><span class="sxs-lookup"><span data-stu-id="f61cc-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="f61cc-106">Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi fyrir sig í Regulatory Configuration Services (RCS) og Finance.</span><span class="sxs-lookup"><span data-stu-id="f61cc-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="f61cc-107">Það leiðir notandann einnig í gegnum ferlið til að senda inn rafræna reikninga sem eru myndaðir á ítalska sniðinu **FatturaPA** í gegnum þjónustuna og það útskýrir hvernig á að yfirfara niðurstöður vinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="f61cc-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f61cc-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="f61cc-108">Prerequisites</span></span>

<span data-ttu-id="f61cc-109">Áður en farið er í gegnum skrefin í þessu efnisatriði þarf að ljúka skrefunum í [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="f61cc-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="f61cc-110">RCS-uppsetning</span><span class="sxs-lookup"><span data-stu-id="f61cc-110">RCS setup</span></span>

<span data-ttu-id="f61cc-111">Við RCS-uppsetningu verður farið í gegnum þessi skref:</span><span class="sxs-lookup"><span data-stu-id="f61cc-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="f61cc-112">Flytjið inn eiginleika rafrænnar reikningsfærslu fyrir útflutning á rafrænum reikningum viðskiptavinar á sniði **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="f61cc-113">Farið yfir skilgreiningar sniðsins sem þarf til að búa til, senda inn og taka við svörum um rafræna reikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="f61cc-114">Skilgreinið tilvikin sem styðja við innsendingar rafrænna reikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="f61cc-115">Birtið eiginleika rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="f61cc-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="f61cc-116">„Eiginleiki rafrænnar reikningsfærslu“ er almennt heiti fyrir tilfangið sem er skilgreint og gefið út til að nota þjón rafrænnar reikningsfærsluviðbótar.</span><span class="sxs-lookup"><span data-stu-id="f61cc-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="f61cc-117">Í þessu tilfelli er útflutningur á rafrænum reikningum viðskiptavinar eiginleiki rafrænnar reikningsfærslu sem á að setja upp.</span><span class="sxs-lookup"><span data-stu-id="f61cc-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="f61cc-118">Flytja inn eiginleika rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="f61cc-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="f61cc-119">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="f61cc-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="f61cc-120">Á vinnusvæðinu **Altækir eiginleikar**, undir hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="f61cc-121">Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Flytja inn** til að flytja inn eiginleika rafrænnar reikningsfærslu úr altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="f61cc-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f61cc-122">Ef listinn yfir tiltæka eiginleika sést ekki skal velja **Samstilla**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="f61cc-123">Veljið eiginleikann **Útflutningur rafrænna reikninga (IT)** og síðan **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![Eiginleiki fyrir útflutning rafrænna reikninga (IT) fluttur inn](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="f61cc-125">Þegar eiginleikinn **Útflutningur rafrænna reikninga (IT)** úr altæku geymslunni, eru allar stillingarnar sem lýst er í næsta hluta einnig fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="f61cc-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="f61cc-126">Búa til nýja útgáfu af eiginleika fyrir útflutning rafrænna reikninga (IT)</span><span class="sxs-lookup"><span data-stu-id="f61cc-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="f61cc-127">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja **Ný**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Nýrri útgáfu rafrænnar reikningsfærslu bætt við](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="f61cc-129">Næst verða skilgreind snið rafrænnar skýrslugerðar sem tengjast eiginleika rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="f61cc-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="f61cc-130">Í flipanum **Skilgreiningar** skal velja **Bæta við** til að stjórna útgáfum skilgreininga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![Umsjón með skilgreiningarútgáfum fyrir eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="f61cc-132">Í þessu skrefi er bætt við og skilgreind snið rafrænnar skýrslugerðar fyrir mismunandi skrár sem notaðar eru til að flytja út ítalska rafræna reikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="f61cc-133">Fyrir ítalska FatturaPA rafræna reikninga skal nota annaðhvort hefðbundnar skilgreiningar eða sérstilltu skilgreiningarnar sem notaðar eru fyrir rafræna reikningsfærslu:</span><span class="sxs-lookup"><span data-stu-id="f61cc-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="f61cc-134">Sölureikningur (IT)</span><span class="sxs-lookup"><span data-stu-id="f61cc-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="f61cc-135">Verkreikningur (IT)</span><span class="sxs-lookup"><span data-stu-id="f61cc-135">Project invoice (IT)</span></span>

    <span data-ttu-id="f61cc-136">Þegar búinn er til eiginleiki rafrænnar reikningsfærslu út frá öðrum eiginleika rafrænnar reikningsfærslu, eru öll snið rafrænnar skýrslugerðar erfð frá upprunalega eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="f61cc-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="f61cc-137">Veljið ákveðna skráarskilgreiningu fyrir snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f61cc-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="f61cc-138">Veljið **Breyta** eða **Skoða** til að opna síðuna **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Síða sniðshönnuðar opnuð](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="f61cc-140">Notið síðuna **Sniðshönnuður** til að breyta og skoða skilgreiningar á skrá rafræns skýrslugerðarsniðs.</span><span class="sxs-lookup"><span data-stu-id="f61cc-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Síða sniðshönnuðar](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="f61cc-142">Stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="f61cc-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="f61cc-143">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, skal velja **Bæta við**, **Eyða** eða **Breyta** til að stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="f61cc-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Umsjón með uppsetningum á eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="f61cc-145">Í þessu skrefi eru skilgreind tilvik sem eiga við um rafræna reikninga, þar á meðal myndun XML-úttaksskráa á **FatturaPA** sniði og stafræna undirskrift (ef þess er krafist).</span><span class="sxs-lookup"><span data-stu-id="f61cc-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="f61cc-146">Skilgreina uppsetningu á eiginleika sölureiknings</span><span class="sxs-lookup"><span data-stu-id="f61cc-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="f61cc-147">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, í dálknum **Uppsetning eiginleika**, skal velja **Sölureikningur**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="f61cc-148">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-148">Select **Edit**.</span></span>
3. <span data-ttu-id="f61cc-149">Á síðunni **Uppsetning á útgáfu eiginleika** skal velja flipann **Aðgerðir** til að stjórna lista yfir aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="f61cc-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="f61cc-150">Aðgerðir skilgreina lista yfir aðgerðir sem þarf að keyra í réttri röð til að ná fullri keyrslu á tilvikinu.</span><span class="sxs-lookup"><span data-stu-id="f61cc-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Flipinn Aðgerðir.](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="f61cc-152">Aðgerðarkenni</span><span class="sxs-lookup"><span data-stu-id="f61cc-152">Action ID</span></span> | <span data-ttu-id="f61cc-153">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="f61cc-153">Action name</span></span>        | <span data-ttu-id="f61cc-154">Aðgerðarlýsing</span><span class="sxs-lookup"><span data-stu-id="f61cc-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="f61cc-155">1</span><span class="sxs-lookup"><span data-stu-id="f61cc-155">1</span></span>         | <span data-ttu-id="f61cc-156">Breyta skjali</span><span class="sxs-lookup"><span data-stu-id="f61cc-156">Transform document</span></span> | <span data-ttu-id="f61cc-157">Stofnið XML-skrá fyrir rafrænan reikning á **FatturaPA** sniði.</span><span class="sxs-lookup"><span data-stu-id="f61cc-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="f61cc-158">2</span><span class="sxs-lookup"><span data-stu-id="f61cc-158">2</span></span>         | <span data-ttu-id="f61cc-159">Skrifa undir skjal</span><span class="sxs-lookup"><span data-stu-id="f61cc-159">Sign document</span></span>      | <span data-ttu-id="f61cc-160">Notið stafræna undirskrift á XML-skrána.</span><span class="sxs-lookup"><span data-stu-id="f61cc-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="f61cc-161">Veljið flipann **Gildissviðsreglur** til að skoða og vinna með gildissviðsreglur.</span><span class="sxs-lookup"><span data-stu-id="f61cc-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="f61cc-162">Gildissviðsreglur skilgreina samhengið þar sem aðgerðin verður framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="f61cc-162">Applicability rules define the context where the action will be run.</span></span>

    ![Flipi fyrir gildissviðsreglur](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="f61cc-164">Veljið flipann **Breytur** til að skoða og vinna með breyturnar.</span><span class="sxs-lookup"><span data-stu-id="f61cc-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Breytuflipi](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="f61cc-166">Skilgreinið almennu breyturnar sem eru nauðsynlegar til að framkvæma aðgerðirnar.</span><span class="sxs-lookup"><span data-stu-id="f61cc-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="f61cc-167">Skilgreina uppsetningu á eiginleika verkreiknings</span><span class="sxs-lookup"><span data-stu-id="f61cc-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="f61cc-168">Skrefin og stillingarnar sem eru nauðsynleg til að skilgreina uppsetningu á eiginleika **Verkreiknings** eru mjög svipuð skrefum og stillingum fyrir uppsetningu á eiginleika **Sölureiknings**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="f61cc-169">Þegar unnið er með verkreikninga skal líta á ferla fyrir sölureikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="f61cc-170">Úthluta eiginleika rafrænnar reikningsfærslur á umhverfið</span><span class="sxs-lookup"><span data-stu-id="f61cc-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="f61cc-171">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Umhverfi**, skal velja **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="f61cc-172">Í reitnum **Umhverfi** skal velja umhverfið.</span><span class="sxs-lookup"><span data-stu-id="f61cc-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="f61cc-173">Í reitnum **Gildir frá** skal velja dagsetninguna þegar nýja umhverfið tekur gildi.</span><span class="sxs-lookup"><span data-stu-id="f61cc-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="f61cc-174">Veljið **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-174">Select **Enable**.</span></span> 

![Umhverfi rafrænnar reikningsfærslu virkjað](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="f61cc-176">Birta eiginleika rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="f61cc-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="f61cc-177">Hægt er að birta eiginleika rafrænnar reikningsfærslu með því að breyta stöðu útgáfunnar í **Lokið** eða **Birtur**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="f61cc-178">Breyta stöðu útgáfu í Lokið</span><span class="sxs-lookup"><span data-stu-id="f61cc-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="f61cc-179">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="f61cc-180">Velduð **Breyta stöðu \> Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="f61cc-181">Breyta stöðu útgáfu í Birt</span><span class="sxs-lookup"><span data-stu-id="f61cc-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="f61cc-182">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="f61cc-183">Veljið **Breyta stöðu \> Birta**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-183">Select **Change status \> Publish**.</span></span>

![Stöðu eiginleika rafrænnar reikningsfærslu breytt](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="f61cc-185">Setja upp samþættingu á viðbót rafrænnar reikningsfærslu í Finance</span><span class="sxs-lookup"><span data-stu-id="f61cc-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="f61cc-186">Við uppsetningu á Finance verður þessum verkum lokið:</span><span class="sxs-lookup"><span data-stu-id="f61cc-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="f61cc-187">Flytjið inn gagnalíkan rafrænnar skýrslugerðar, gagnalíkanavörpun rafrænnar skýrslugerðar og skilgreiningar samhengis fyrir rafræna FatturaPA-reikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="f61cc-188">Skilgreinið vottorðið sem er krafist til að skrifa undir ítalska rafræna reikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="f61cc-189">Flytja inn gagnalíkan rafrænnar skýrslugerðar, vörpun gagnalíkans og snið</span><span class="sxs-lookup"><span data-stu-id="f61cc-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="f61cc-190">Á vinnusvæðinu **Rafræn skýrslugerð** skal staðfesta að skilgreiningarveitan **Þjónusta viðskiptaskjala** sé stillt á **Virk**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="f61cc-191">Veldu **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="f61cc-192">Veljið **Altæk tilföng \> Opna**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="f61cc-193">Flytjið inn **Reikningslíkan**, **Vörpun reikningslíkans** og **Samhengislíkan viðskiptavinareiknings**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="f61cc-194">Kveikja á eiginleikanum fyrir útflutning á rafrænum reikningum viðskiptavinar fyrir Ítalíu</span><span class="sxs-lookup"><span data-stu-id="f61cc-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="f61cc-195">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="f61cc-196">Í flipanum **Eiginleikar** skal velja gátreitinn **Virkjað** í línunni fyrir tilvísun eiginleika **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![Kveikt á eiginleika FatturaPA](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="f61cc-198">Skilgreina rafræn skjöl</span><span class="sxs-lookup"><span data-stu-id="f61cc-198">Configure electronic documents</span></span>

1. <span data-ttu-id="f61cc-199">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="f61cc-200">Í flipanum **Rafrænt skjal** skal velja **Bæta við** og færa inn töflurnar sem þarf til að mynda ítalska rafræna reikninga:</span><span class="sxs-lookup"><span data-stu-id="f61cc-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="f61cc-201">**Töfluheiti:** Reikningabók viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f61cc-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="f61cc-202">**Töfluheiti:** Verkreikningur</span><span class="sxs-lookup"><span data-stu-id="f61cc-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="f61cc-203">Fyrir hverja töflu skal skilgreina tengt skjalasamhengi:</span><span class="sxs-lookup"><span data-stu-id="f61cc-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="f61cc-204">Fyrir **Reikningabók viðskiptavinar** skal velja **Samhengi viðskiptavinareiknings**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="f61cc-205">Fyrir **Verkreikningur** skal velja **Samhengi verkreiknings**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Svargerðir settar upp](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="f61cc-207">Rafræn reikningsfærsla í vinnslu</span><span class="sxs-lookup"><span data-stu-id="f61cc-207">Electronic invoice processing</span></span>

<span data-ttu-id="f61cc-208">Við úrvinnslu í Finance verður lokið við þessi verk:</span><span class="sxs-lookup"><span data-stu-id="f61cc-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="f61cc-209">Mynda ítalska rafræna reikninga í gegnum viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="f61cc-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="f61cc-210">Skoða keyrslukladda og yfirfara niðurstöður vinnslu</span><span class="sxs-lookup"><span data-stu-id="f61cc-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="f61cc-211">Búa til rafræna reikninga</span><span class="sxs-lookup"><span data-stu-id="f61cc-211">Generate electronic invoices</span></span>

<span data-ttu-id="f61cc-212">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu** og eiginleikinn **IT00036** hefur verið virkjaður, verður ekki lengur hægt að nota gamla Finance-ferlið til að mynda ítalska rafræna reikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="f61cc-213">Því er skipt út fyrir nýtt ferli sem kallast **Senda inn rafræn skjöl**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="f61cc-214">Hægt er að senda skjölin inn handvirkt, út frá eftirspurn eftir skjölum rafrænna reikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="f61cc-215">Áður en haldið er áfram skal ganga úr skugga um að uppsetningunni sem krafist er fyrir ítalska rafræna reikninga sé lokið.</span><span class="sxs-lookup"><span data-stu-id="f61cc-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="f61cc-216">Frekari upplýsingar er að finna í [Rafrænir reikningar viðskiptavinar](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="f61cc-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="f61cc-217">Hafa skal í huga að einhver uppsetningarskref sem lýst er í því efnisatriði kunna að vera ekki í boði vegna virkjunar á viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="f61cc-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="f61cc-218">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Senda inn rafræn skjöl**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="f61cc-219">Fyrir fyrstu innsendingu á skjali skal stilla valkostinn **Senda skjöl inn aftur** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="f61cc-220">Ef senda þarf skjal inn aftur í gegnum þjónustuna skal stilla þennan valkost á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="f61cc-221">Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann **Fyrirspurn** þar sem hægt er að búa til fyrirspurn til að velja skjöl til innsendingar.</span><span class="sxs-lookup"><span data-stu-id="f61cc-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Svarglugginn fyrir innsendingu rafrænna skjala](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="f61cc-223">Síufyrirspurn</span><span class="sxs-lookup"><span data-stu-id="f61cc-223">Filter query</span></span>

1. <span data-ttu-id="f61cc-224">Í svarglugganum **Fyrirspurn** skal skilgreina síuskilyrðin fyrir bæði sölureikninga og verkreikninga eða skilja skilyrðin eftir auð til að hafa með alla ósenda reikninga.</span><span class="sxs-lookup"><span data-stu-id="f61cc-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Síuskilyrði innsendingar stillt](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="f61cc-226">Veljið **Í lagi** til að loka svarglugganum **Fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="f61cc-227">Veljið **Í lagi** til að senda inn valin skjöl.</span><span class="sxs-lookup"><span data-stu-id="f61cc-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="f61cc-228">![ATHUGIÐ] Í fyrstu tilraun til að senda inn skjal í gegnum þjónustuna verður beðið um að staðfesta tenginguna við viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="f61cc-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="f61cc-229">Veljið **Smelltu hér til að tengjast sendingarþjónustu rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="f61cc-230">Skoða innsendingarkladda</span><span class="sxs-lookup"><span data-stu-id="f61cc-230">View submission logs</span></span>

<span data-ttu-id="f61cc-231">Hægt er að skoða innsendingarkladda fyrir öll send skjöl.</span><span class="sxs-lookup"><span data-stu-id="f61cc-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="f61cc-232">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="f61cc-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="f61cc-233">Í reitnum **Gerð skjals** skal velja **Reikningabók viðskiptavinar** eða **Verkreikningur** til að síða fyrir nauðsynleg rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="f61cc-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Gerð skjals valin til að skoða innsendingarkladda](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="f61cc-235">Gildið sem er sýnt í dálknum **Staða innsendingar** táknar stöðu innsendingarferlisins.</span><span class="sxs-lookup"><span data-stu-id="f61cc-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="f61cc-236">Það gefur til kynna hvort ferlið hafið gengið samkvæmt skilgreiningu og hvort frekari aðgerða sé þörf.</span><span class="sxs-lookup"><span data-stu-id="f61cc-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="f61cc-237">Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.</span><span class="sxs-lookup"><span data-stu-id="f61cc-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Skoða upplýsingar um innsendingarkladda](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="f61cc-239">Í flýtiflipanum **Vinnsluaðgerðir** er hægt að skoða keyrslukladdann fyrir aðgerðirnar sem eru skilgreindar í útgáfu eiginleikans sem var sett upp í RCS.</span><span class="sxs-lookup"><span data-stu-id="f61cc-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="f61cc-240">Dálkurinn **Staða** sýnir hvort tekist hafi að keyra aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="f61cc-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="f61cc-241">Í flýtiflipanum **Aðgerðaskrár** er hægt að skoða milliskrár sem voru myndaðar við keyrslu aðgerðanna.</span><span class="sxs-lookup"><span data-stu-id="f61cc-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="f61cc-242">Hægt er að velja **Skoða** til að hlaða niður XML-úttaksskránni á **FatturaPA** sniði og skoða innihald hennar.</span><span class="sxs-lookup"><span data-stu-id="f61cc-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f61cc-243">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="f61cc-243">Related topics</span></span>

- [<span data-ttu-id="f61cc-244">Yfirlit innbótar rafrænna reikninga</span><span class="sxs-lookup"><span data-stu-id="f61cc-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="f61cc-245">Hafist handa með innbót rafrænna reikninga</span><span class="sxs-lookup"><span data-stu-id="f61cc-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="f61cc-246">Setja upp viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="f61cc-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
