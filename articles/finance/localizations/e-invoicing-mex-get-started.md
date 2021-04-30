---
title: Hafist handa með rafrænar reikningsfærslur fyrir Mexíkó
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Mexíkó.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c1112ba8394afb3aa9c9b4f68249524498bd8b32
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894884"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a><span data-ttu-id="18ecf-103">Hafist handa með rafrænar reikningsfærslur fyrir Mexíkó</span><span class="sxs-lookup"><span data-stu-id="18ecf-103">Get started with Electronic invoicing for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="18ecf-104">Rafræn reikningsfærsla fyrir Mexíkó styður hugsanlega ekki sem stendur allar aðgerðir sem eru í boði í skjalinu Comprobante Fiscal Digital por Internet (CFDI) og í tengdri samþættingu sem er byggð inn í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18ecf-104">Electronic invoicing for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="18ecf-105">Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="18ecf-105">This topic provides information that will help you get started with Electronic invoicing for Mexico.</span></span> <span data-ttu-id="18ecf-106">Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi fyrir sig í Regulatory Configuration Services (RCS) og Finance.</span><span class="sxs-lookup"><span data-stu-id="18ecf-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="18ecf-107">Það fer einnig í gegnum skrefin sem þarf að fylgja í Finance til að senda inn CFDI-reikninga í gegnum þjónustuna og það útskýrir hvernig á að fara yfir niðurstöður vinnslunnar og stöður CFDI-reikninga.</span><span class="sxs-lookup"><span data-stu-id="18ecf-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="18ecf-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="18ecf-108">Prerequisites</span></span>

<span data-ttu-id="18ecf-109">Áður en farið er í gegnum skrefin í þessu efnisatriði þarf að ljúka skrefunum í [Hafist handa með rafrænni reikningsfærslu](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="18ecf-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="18ecf-110">RCS-uppsetning</span><span class="sxs-lookup"><span data-stu-id="18ecf-110">RCS setup</span></span>

<span data-ttu-id="18ecf-111">Við RCS-uppsetningu verður farið í gegnum þessi skref:</span><span class="sxs-lookup"><span data-stu-id="18ecf-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="18ecf-112">Flytja inn eiginleika rafrænnar reikningsfærslu fyrir úrvinnslu á CFDI-reikningum.</span><span class="sxs-lookup"><span data-stu-id="18ecf-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="18ecf-113">Farið yfir skilgreiningar sniðsins sem þarf til að búa til, senda inn og taka við svörum um CFDI-reikninga og til að senda inn og taka á móti svörum um afturköllun.</span><span class="sxs-lookup"><span data-stu-id="18ecf-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="18ecf-114">Skilgreinið tilvikin sem styðja við innsendingar CFDI-reikninga.</span><span class="sxs-lookup"><span data-stu-id="18ecf-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="18ecf-115">Birta eiginleika rafrænnar reikningsfærslu fyrir CFDI-reikninga.</span><span class="sxs-lookup"><span data-stu-id="18ecf-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="18ecf-116">„Eiginleiki rafrænnar reikningsfærslu“ er almennt heiti fyrir tilfangið sem er skilgreint og gefið út til að nota þjón rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="18ecf-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="18ecf-117">Í þessu tilfelli eru CFDI-reikningar (MX) eiginleikinn fyrir rafræna reikningsfærslu sem verður settur upp.</span><span class="sxs-lookup"><span data-stu-id="18ecf-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="18ecf-118">Flytja inn eiginleika rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="18ecf-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="18ecf-119">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="18ecf-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="18ecf-120">Á vinnusvæðinu **Altækir eiginleikar**, undir hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="18ecf-121">Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Flytja inn** til að flytja inn eiginleikann **CFDI-reikningar (MX)** úr altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="18ecf-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="18ecf-122">Ef ekki er hægt að sjá eiginleikann í listanum skal velja **Samstilla** og síðan endurtaka skref 3.</span><span class="sxs-lookup"><span data-stu-id="18ecf-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![Eiginleiki CFDI-reikninga (MX) fluttur inn](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="18ecf-124">Þegar eiginleikinn **CFDI-reikningar (MX)** er fluttur inn úr altæku geymslunni, eru allar stillingar eiginleikans, þ.m.t. skilgreiningar og aðgerðir, einnig fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="18ecf-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="18ecf-125">Búa til nýja útgáfu af eiginleika CFDI-reikninga (MX)</span><span class="sxs-lookup"><span data-stu-id="18ecf-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="18ecf-126">Hægt er að búa til nýja útgáfu ef til dæmis þarf að uppfæra vefslóðir.</span><span class="sxs-lookup"><span data-stu-id="18ecf-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="18ecf-127">Frekari upplýsingar er að finna í [Rafræn reikningsfærsla CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="18ecf-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="18ecf-128">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja **Ný**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Nýrri útgáfu rafrænnar reikningsfærslu bætt við](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="18ecf-130">Uppfæra útgáfu skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="18ecf-130">Update the configuration version</span></span>

1. <span data-ttu-id="18ecf-131">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Skilgreiningar**, skal velja **Bæta við** eða **Eyða** til að stjórna útgáfum skilgreininga (skilgreiningar á skráarsniði rafrænnar skýrslugerðar).</span><span class="sxs-lookup"><span data-stu-id="18ecf-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Stjórnun skilgreininga á eiginleikum rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="18ecf-133">Þegar ný útgáfa er stofnuð eru allar skilgreiningar erfðar frá síðustu birtu útgáfu.</span><span class="sxs-lookup"><span data-stu-id="18ecf-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="18ecf-134">Til að vinna úr CFDI-reikningum eru eftirfarandi skilgreiningar nauðsynlegar:</span><span class="sxs-lookup"><span data-stu-id="18ecf-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="18ecf-135">CFDI-reikningur (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="18ecf-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="18ecf-136">Innflutningur á svarskilaboði CFDI</span><span class="sxs-lookup"><span data-stu-id="18ecf-136">CFDI response message import</span></span>
    - <span data-ttu-id="18ecf-137">Innflutningur á villukladda CFDI</span><span class="sxs-lookup"><span data-stu-id="18ecf-137">CFDI error log import</span></span>
    - <span data-ttu-id="18ecf-138">CFDI-afturköllunarbeiðni (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="18ecf-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="18ecf-139">CFDI-reikningur (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="18ecf-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="18ecf-140">Í listanum skal velja skilgreiningarútgáfu og síðan velja **Breyta** eða **Skoða** til að opna síðuna **Sniðshönnuður** þar sem hægt er að breyta eða skoða skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="18ecf-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Síða sniðshönnuðar opnuð](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="18ecf-142">Notið síðuna **Sniðshönnuður** til að breyta og skoða skilgreiningar á skrá rafræns skýrslugerðarsniðs.</span><span class="sxs-lookup"><span data-stu-id="18ecf-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="18ecf-143">Frekari upplýsingar er að finna í [Stofna skilgreiningar rafræns skjals](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="18ecf-143">For more information, see [Create electronic document configurations](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Síða sniðshönnuðar](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="18ecf-145">Stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="18ecf-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="18ecf-146">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, skal velja **Bæta við**, **Eyða** eða **Breyta** til að stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="18ecf-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Umsjón með uppsetningum á eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="18ecf-148">Til að senda CFDI-reikninga fyrir heimild (búa til XML-skrána, senda XML-skrána inn og vinna úr svari), þarf að setja upp eiginleikann **Sölureikningur**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="18ecf-149">Til að senda inn afturköllun á CFDI-reikningi þarf að setja upp eiginleikana **Afturköllun** og **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="18ecf-150">Skilgreina uppsetningu á eiginleika sölureiknings</span><span class="sxs-lookup"><span data-stu-id="18ecf-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="18ecf-151">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, í dálknum **Uppsetning eiginleika**, skal velja **Sölureikningur**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="18ecf-152">Veljið **Breyta** til að skilgreina aðgerðir, gildissviðsreglur og breytur.</span><span class="sxs-lookup"><span data-stu-id="18ecf-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![Uppsetning á eiginleika rafrænnar reikningsfærslu breytt](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="18ecf-154">Á síðunni **Uppsetning á útgáfu eiginleika** skal velja flipann **Aðgerðir** til að stjórna lista yfir aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="18ecf-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="18ecf-155">Aðgerðir skilgreina lista yfir aðgerðir sem þarf að keyra í réttri röð til að ná fullri keyrslu á tilvikinu.</span><span class="sxs-lookup"><span data-stu-id="18ecf-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Flipinn Aðgerðir.](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="18ecf-157">Aðgerðarkenni</span><span class="sxs-lookup"><span data-stu-id="18ecf-157">Action ID</span></span> | <span data-ttu-id="18ecf-158">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="18ecf-158">Action</span></span>                   | <span data-ttu-id="18ecf-159">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="18ecf-159">Action name</span></span>                                  | <span data-ttu-id="18ecf-160">Aðgerðarlýsing</span><span class="sxs-lookup"><span data-stu-id="18ecf-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="18ecf-161">1</span><span class="sxs-lookup"><span data-stu-id="18ecf-161">1</span></span>         | <span data-ttu-id="18ecf-162">Breyta skjali</span><span class="sxs-lookup"><span data-stu-id="18ecf-162">Transform document</span></span>       | <span data-ttu-id="18ecf-163">Mynda rafrænan CFDI-reikning án stafrænnar undirskriftar</span><span class="sxs-lookup"><span data-stu-id="18ecf-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="18ecf-164">Mynda rafrænan CFDI-reikning.</span><span class="sxs-lookup"><span data-stu-id="18ecf-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="18ecf-165">2</span><span class="sxs-lookup"><span data-stu-id="18ecf-165">2</span></span>         | <span data-ttu-id="18ecf-166">Skrifa undir skjal</span><span class="sxs-lookup"><span data-stu-id="18ecf-166">Sign document</span></span>            | <span data-ttu-id="18ecf-167">Stafræn undirskrift</span><span class="sxs-lookup"><span data-stu-id="18ecf-167">Digital sign</span></span>                                 | <span data-ttu-id="18ecf-168">Skrifið stafrænt undir rafrænan reikning fyrir innsendingu.</span><span class="sxs-lookup"><span data-stu-id="18ecf-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="18ecf-169">3</span><span class="sxs-lookup"><span data-stu-id="18ecf-169">3</span></span>         | <span data-ttu-id="18ecf-170">Hringja í PAC-þjónustu í Mexíkó</span><span class="sxs-lookup"><span data-stu-id="18ecf-170">Call Mexican PAC service</span></span> | <span data-ttu-id="18ecf-171">Senda inn rafrænan CFDI-reikning</span><span class="sxs-lookup"><span data-stu-id="18ecf-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="18ecf-172">Biðlarinn Windows Communication Foundation (WCF) sendir inn rafrænan CFDI-reikning.</span><span class="sxs-lookup"><span data-stu-id="18ecf-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="18ecf-173">4</span><span class="sxs-lookup"><span data-stu-id="18ecf-173">4</span></span>         | <span data-ttu-id="18ecf-174">Vinna úr svari</span><span class="sxs-lookup"><span data-stu-id="18ecf-174">Process response</span></span>         | <span data-ttu-id="18ecf-175">Greina svar vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="18ecf-175">Analyze web service response</span></span>                 | <span data-ttu-id="18ecf-176">Greina svar vefþjónustunnar og skila villukladdanum.</span><span class="sxs-lookup"><span data-stu-id="18ecf-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="18ecf-177">Setja upp vefslóð fyrir mexíkóska PAC-vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="18ecf-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="18ecf-178">Á síðunni **Uppsetning á útgáfu eiginleika**, í flipanum **Aðgerðir**, í flýtiflipanum **Aðgerðir**, skal velja **Hringja í mexíkóska PAC-þjónustu**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="18ecf-179">Í flýtiflipann **Færibreytur**, í reitinn **Veffang**, skal slá inn vefslóð vefþjónustunnar fyrir innsendingu á CFDI-reikningi.</span><span class="sxs-lookup"><span data-stu-id="18ecf-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="18ecf-180">Notið sömu skrefin til að uppfæra vefslóðina fyrir aðgerðina **Hringja í mexíkóska PAC-þjónustu** fyrir uppsetninga á eiginleikunum **Hætta við** og **Afturköllunarbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="18ecf-181">Úthluta útgáfudrögum á umhverfi rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="18ecf-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="18ecf-182">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Umhverfi**, skal velja **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="18ecf-183">Í reitnum **Umhverfi** skal velja umhverfið.</span><span class="sxs-lookup"><span data-stu-id="18ecf-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="18ecf-184">Í reitnum **Gildir frá** skal velja dagsetninguna þegar nýja umhverfið tekur gildi.</span><span class="sxs-lookup"><span data-stu-id="18ecf-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="18ecf-185">Veljið **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-185">Select **Enable**.</span></span>

![Umhverfi rafrænnar reikningsfærslu virkjað](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="18ecf-187">Breyta stöðu útgáfu í Lokið</span><span class="sxs-lookup"><span data-stu-id="18ecf-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="18ecf-188">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="18ecf-189">Velduð **Breyta stöðu \> Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="18ecf-190">Breyta stöðu útgáfu í Birt</span><span class="sxs-lookup"><span data-stu-id="18ecf-190">Change the version status to Published</span></span>

- <span data-ttu-id="18ecf-191">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja **Breyta stöðu \> Birta**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="18ecf-192">Birta eiginleika rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="18ecf-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="18ecf-193">Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja flipann **Útgáfur** til að stjórna stöðunni á eiginleikanum **CFDI-reikningar (MX)**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="18ecf-194">Veljið **Breyta stöðu** til að breyta stöðu eiginleikans.</span><span class="sxs-lookup"><span data-stu-id="18ecf-194">Select **Change status** to change the status of the feature.</span></span>

![Stöðu eiginleika rafrænnar reikningsfærslu breytt](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a><span data-ttu-id="18ecf-196">Setja upp samþættingu rafrænnar reikningsfærslu í Finance</span><span class="sxs-lookup"><span data-stu-id="18ecf-196">Set up Electronic invoicing  integration in Finance</span></span>

<span data-ttu-id="18ecf-197">Til að setja upp rafræna reikningsfærslu í Finance þarf að ljúka þessum verkum:</span><span class="sxs-lookup"><span data-stu-id="18ecf-197">To set up Electronic invoicing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="18ecf-198">Flytjið inn gagnalíkan rafrænnar skýrslugerðar, gagnalíkansvörpun rafrænnar skýrslugerðar og snið sem eru nauðsynleg fyrir CFDI-reikninga.</span><span class="sxs-lookup"><span data-stu-id="18ecf-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="18ecf-199">Skilgreinið svargerðir fyrir uppfærslu á CFDI-reikningum.</span><span class="sxs-lookup"><span data-stu-id="18ecf-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="18ecf-200">Þessar svargerðir eru notaðar fyrir svar frá þjóni samþykktrar vottorðaveitu (PAC).</span><span class="sxs-lookup"><span data-stu-id="18ecf-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="18ecf-201">Flytja inn gagnalíkan rafrænnar skýrslugerðar, gagnalíkanavörpun rafrænnar skýrslugerðar og skilgreiningar samhengis fyrir CFDI-reikninga</span><span class="sxs-lookup"><span data-stu-id="18ecf-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="18ecf-202">Skráðu þig inn í Finance.</span><span class="sxs-lookup"><span data-stu-id="18ecf-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="18ecf-203">Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="18ecf-204">Gangið úr skugga um að þessi skilgreiningarveita sé stillt á **Virk**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="18ecf-205">Frekari upplýsingar um hvernig á að stilla veitu á **Virk** er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="18ecf-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="18ecf-206">Veldu **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="18ecf-207">Veljið **Altæk tilföng \> Opna**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="18ecf-208">Flytjið inn **Reikningslíkan**, **Vörpun reikningslíkans**, **CFDI-reikningssnið (MX)**, **Snið afturköllunarbeiðni CFDI-reiknings (MX)** og **Afturköllunarsnið CFDI-reiknings (MX)**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="18ecf-209">Kveikja á eiginleikanum fyrir úrvinnslu CFDI-reikninga</span><span class="sxs-lookup"><span data-stu-id="18ecf-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="18ecf-210">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="18ecf-211">Í flipanum **Eiginleikar** skal velja gátreitinn **Virkja** í línunum fyrir tilvísanir eiginleika **MX-00010** og **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![Kveikt á eiginleikunum fyrir úrvinnslu CFDI-reikninga](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="18ecf-213">Flytja inn skilgreiningar rafrænnar skýrslugerðar og setja upp svargerðir fyrir uppfærslu á CFDI-reikningum</span><span class="sxs-lookup"><span data-stu-id="18ecf-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="18ecf-214">Flytja inn rafræn skýrslugerð grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="18ecf-214">Import ER configurations</span></span>

1. <span data-ttu-id="18ecf-215">Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="18ecf-216">Veldu **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="18ecf-217">Veljið **Altæk tilföng \> Opna**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="18ecf-218">Flytjið inn **Líkan svarskilaboða**, **Innflutningur á villukladda CFDI (MX)** og **Innflutningur á svarskilaboði CFDI (MX)**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="18ecf-219">Setja upp svargerðirnar</span><span class="sxs-lookup"><span data-stu-id="18ecf-219">Set up the response types</span></span>

1. <span data-ttu-id="18ecf-220">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="18ecf-221">Í flipanum **Rafrænt skjal** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="18ecf-222">Færið inn reikningabók viðskiptavinar og síðan í reitnum **Töfluheiti** skal velja verkreikninginn.</span><span class="sxs-lookup"><span data-stu-id="18ecf-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="18ecf-223">Fyrir hverja töflu skal skilgreina tengt skjalasamhengi:</span><span class="sxs-lookup"><span data-stu-id="18ecf-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="18ecf-224">Fyrir **Reikningabók viðskiptavinar** skal færa inn **Samhengi viðskiptavinareiknings**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="18ecf-225">Fyrir **Verkreikningur** skal færa inn **Samhengi verkreiknings**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="18ecf-226">Veljið **Svargerðir** til að skilgreina svargerðirnar sem hægt er að skila úr rafrænni reikningsfærslu og hafa með í reikningabók viðskiptavinar eða verkreikningi.</span><span class="sxs-lookup"><span data-stu-id="18ecf-226">Select **Response types** to configure the response types that can be returned from Electronic invoicing and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="18ecf-227">Veljið **Nýtt** og svo, í reitnum **Svargerð**, skal velja **Svar**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="18ecf-228">Í reitnum **Staða sendingar** skal velja **Í bið**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="18ecf-229">Í reitnum **Líkanavörpun** skal velja **Innflutningssnið svarskilaboða - Líkanavörpun úr svarskilaboðum**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="18ecf-230">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-230">Select **Save**.</span></span>
9. <span data-ttu-id="18ecf-231">Veljið **Nýtt** og svo, í reitnum **Svargerð**, skal velja **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="18ecf-232">Í reitnum **Staða sendingar** skal velja **Í bið**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="18ecf-233">Í reitinn **Líkanavörpun** skal velja **Gagnainnflutningssnið CFDI-svars (upplýsingar) - Gagnainnflutningur svars**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="18ecf-234">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="18ecf-235">Vinna úr rafrænum reikningum í Finance</span><span class="sxs-lookup"><span data-stu-id="18ecf-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="18ecf-236">Við vinnslu CFDI-reikninga í Finance í gegnum rafræna reikningsfærslu er hægt að framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="18ecf-236">During the processing of CFDI invoices in Finance through Electronic invoicing, you can perform the following tasks:</span></span>

- <span data-ttu-id="18ecf-237">Senda inn rafræna CFDI-reikninga.</span><span class="sxs-lookup"><span data-stu-id="18ecf-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="18ecf-238">Skoða keyrslukladda fyrir sendingar.</span><span class="sxs-lookup"><span data-stu-id="18ecf-238">View the submission execution logs.</span></span>
- <span data-ttu-id="18ecf-239">Senda inn afturköllun á CFDI-reikningi.</span><span class="sxs-lookup"><span data-stu-id="18ecf-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="18ecf-240">Senda inn rafræna CFDI-reikninga</span><span class="sxs-lookup"><span data-stu-id="18ecf-240">Submit CFDI invoices</span></span>

<span data-ttu-id="18ecf-241">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri rafrænni reikningsfærslu**, verður ekki lengur hægt að nota ferlið **Útflutningur/innflutningur á rafrænum reikningi** (**Viðskiptakröfur \> Reikningar \> Rafrænir reikningar**) til að senda inn CFDI-reikninga.</span><span class="sxs-lookup"><span data-stu-id="18ecf-241">After you turn on the **Configurable Electronic invoicing integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="18ecf-242">Því er skipt út fyrir nýtt ferli sem kallast **Senda inn rafræn skjöl**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="18ecf-243">Áður en nýja ferlið **Senda inn rafræn skjöl** er notað skal ganga úr skugga um að uppsetningunni sem þarf fyrir rafræna mexíkóska reikninga sé lokið.</span><span class="sxs-lookup"><span data-stu-id="18ecf-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="18ecf-244">Frekari upplýsingar er að finna í [CFDI-útlitsútgáfu 3.3](./latam-mex-cfdi-3-3.md).</span><span class="sxs-lookup"><span data-stu-id="18ecf-244">For more information, see [CFDI layout version 3.3](./latam-mex-cfdi-3-3.md).</span></span>

1. <span data-ttu-id="18ecf-245">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Senda inn rafræn skjöl**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="18ecf-246">Fyrir fyrstu innsendingu á skjali skal alltaf stilla valkostinn **Senda skjöl inn aftur** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="18ecf-247">Ef senda þarf skjal inn aftur í gegnum þjónustuna skal stilla þennan valkost á **Já**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="18ecf-248">Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann **Fyrirspurn** þar sem hægt er að búa til fyrirspurn til að velja skjöl til innsendingar.</span><span class="sxs-lookup"><span data-stu-id="18ecf-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![CFDI-skjal sent inn](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="18ecf-250">Í fyrstu tilraun til að senda inn skjal í gegnum þjónustuna verður beðið um að staðfesta tenginguna við rafræna reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="18ecf-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="18ecf-251">Veljið **Smelltu hér til að tengjast sendingarþjónustu rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="18ecf-252">Skoða innsendingarkladda</span><span class="sxs-lookup"><span data-stu-id="18ecf-252">View submission logs</span></span>

<span data-ttu-id="18ecf-253">Hægt er að skoða innsendingarkladda fyrir öll send skjöl eða fyrir aðeins eitt innsent skjal.</span><span class="sxs-lookup"><span data-stu-id="18ecf-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="18ecf-254">Skoða alla innsendingarkladda</span><span class="sxs-lookup"><span data-stu-id="18ecf-254">View all submission logs</span></span>

<span data-ttu-id="18ecf-255">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri rafrænnni reikningsfærslu** er ný síða í boði sem gerir kleift að fylgja eftir innsendingarferli skjalsins.</span><span class="sxs-lookup"><span data-stu-id="18ecf-255">After you turn on the **Configurable Electronic invoicing integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="18ecf-256">Hægt er að nota þessa síðu til að skoða innsendingarkladda fyrir öll send skjöl.</span><span class="sxs-lookup"><span data-stu-id="18ecf-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="18ecf-257">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="18ecf-258">Í reitnum **Gerð skjals** skal velja **Reikningabók viðskiptavinar** til að sía fyrir nauðsynlegum rafrænum skjölum.</span><span class="sxs-lookup"><span data-stu-id="18ecf-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Gerð skjals valin til að skoða innsendingarkladda](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="18ecf-260">Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.</span><span class="sxs-lookup"><span data-stu-id="18ecf-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Skoða upplýsingar um innsendingarkladda](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="18ecf-262">Upplýsingunum í innsendingarkladdanum er skipt niður á þrjá flýtiflipa:</span><span class="sxs-lookup"><span data-stu-id="18ecf-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="18ecf-263">**Vinnsluaðgerðir** - Þessi flýtiflipi sýnir keyrslukladdann fyrir aðgerðirnar sem eru skilgreindar í útgáfu eiginleikans sem var sett upp í RCS.</span><span class="sxs-lookup"><span data-stu-id="18ecf-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="18ecf-264">Dálkurinn **Staða** sýnir hvort tekist hafi að keyra aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="18ecf-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="18ecf-265">**Aðgerðaskrár** – Þessi flýtiflipi sýnir milliskrárnar sem voru myndaðar við keyrslu aðgerðanna.</span><span class="sxs-lookup"><span data-stu-id="18ecf-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="18ecf-266">Hægt er að velja **Skoða** til að hlaða niður og skoða skrána.</span><span class="sxs-lookup"><span data-stu-id="18ecf-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="18ecf-267">**Aðgerðarkladdi vinnslu** - Þessi flýtiflipi sýnir niðurstöður samskiptanna milli rafrænnar reikningsfærslu og tilheyrandi vefþjónustu.</span><span class="sxs-lookup"><span data-stu-id="18ecf-267">**Processing action log** – This FastTab shows the results of the communication between Electronic invoicing and the target web service.</span></span> <span data-ttu-id="18ecf-268">Hann sýnir hverju úrvinnsla vefþjónustunnar skilaði.</span><span class="sxs-lookup"><span data-stu-id="18ecf-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="18ecf-269">Dálkurinn **Villukóði** sýnir skilakóðann sem vefþjónusta heimildar skilaði.</span><span class="sxs-lookup"><span data-stu-id="18ecf-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="18ecf-270">Þegar innsendur CFDI-reikningur er heimilaður verður staða hans uppfærð í **Samþykktur**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="18ecf-271">Skoða innsendingarkladda úr CFDI-reikningum</span><span class="sxs-lookup"><span data-stu-id="18ecf-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="18ecf-272">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri rafrænni reikningsfærslu** er einnig hægt að skoða innsendingarkladdana úr CFDI-reikningum.</span><span class="sxs-lookup"><span data-stu-id="18ecf-272">After you turn on the **ConfigurableElectronic invoicing integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="18ecf-273">Farið í **Viðskiptakröfur \> Fyrirspurnir og skýrslur \> CFDI (rafrænir reikningar)**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="18ecf-274">Veljið CFDI-reikning sem var sendur inn eftir að kveikt var á eiginleikanum **Samþætting á stillanlegri rafrænni reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>
3. <span data-ttu-id="18ecf-275">Á aðgerðasvæðinu, í flipanum **Ferill**, skal velja **Kladdi rafræns skjals**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Innsendingarkladdar skoðaðir í CFDI-reikningum](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="18ecf-277">Fyrir CFDI-reikninga sem voru sendir inn áður en kveikt var á eiginleikanum **Samþætting á stillanlegri rafrænni reikningsfærslu**, er hnappurinn **Ferill** í boði.</span><span class="sxs-lookup"><span data-stu-id="18ecf-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="18ecf-278">Hnappurinn **Ferill** er ekki tiltækur fyrir CFDI-reikninga sem voru sendir inn eftir að kveikt var á eiginleikanum **Samþætting á stillanlegri rafrænni reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="18ecf-279">Senda inn afturköllun CFDI-reikninga</span><span class="sxs-lookup"><span data-stu-id="18ecf-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="18ecf-280">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri rafrænni reikningsfærslu**, verður ekki lengur hægt að nota gamla ferlið til að hætta við CFDI-reikninga.</span><span class="sxs-lookup"><span data-stu-id="18ecf-280">After you turn on the **Configurable Electronic invoicing integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="18ecf-281">Því er skipt út fyrir nýja afturköllunarferlið sem er fellt inn í síðuna **Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="18ecf-282">Farið í **Viðskiptakröfur \> Fyrirspurnir og skýrslur \> CFDI (rafrænir reikningar)**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="18ecf-283">Ef CFDI-reikningurinn er með stöðuna **Samþykktur** skal velja **Aðgerðir \> Hætta við CFDI**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="18ecf-284">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="18ecf-285">Veljið CFDI reikninginn og veljið síðan **Aðgerðir \> Senda tengdar innsendingar**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="18ecf-286">Færið inn lýsingu fyrir tengdu innsendinguna og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="18ecf-287">Skoða innsendingarkladda afturköllunar</span><span class="sxs-lookup"><span data-stu-id="18ecf-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="18ecf-288">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="18ecf-289">Í reitnum **Gerð skjals** skal velja **Reikningabók viðskiptavinar** til að sía eingöngu fyrir skjölum reikningabókar viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="18ecf-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="18ecf-290">Veljið CFDI reikninginn og síðan, á aðgerðasvæðinu, skal velja **Fyrirspurnir \> Tengdar innsendingar**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="18ecf-291">Síðan **Tengdar innsendingar** sýnir allar tengdar innsendingar og stöðu þeirra fyrir tilgreindan CFDI-reikning.</span><span class="sxs-lookup"><span data-stu-id="18ecf-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="18ecf-292">Á eftirfarandi mynd merkir fyrsta línan innsendinguna sem bað um samþykki á CFDI-reikningnum.</span><span class="sxs-lookup"><span data-stu-id="18ecf-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="18ecf-293">Önnur línan táknar innsendingu sem hætti við þennan CFDI-reikning.</span><span class="sxs-lookup"><span data-stu-id="18ecf-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Innsendingarkladdar afturköllunar skoðaðir](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="18ecf-295">Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.</span><span class="sxs-lookup"><span data-stu-id="18ecf-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Upplýsingar um innsendingarkladda afturköllunar skoðaðar](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="18ecf-297">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="18ecf-297">Privacy notice</span></span>
<span data-ttu-id="18ecf-298">Til að virkja eiginleikann **CFDI - Mexíkóskur rafrænn reikningur (MX)** þarf hugsanlega að senda takmörkuð gögn, sem fela í sér skattskráningarkenni fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="18ecf-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="18ecf-299">Þetta verður sent til stofnanir þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda.</span><span class="sxs-lookup"><span data-stu-id="18ecf-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="18ecf-300">Stjórnandi getur kveikt og slökkt á eiginleikanum **CFDI - Mexíkóskur rafrænn reikningur (MX)** með því að fara í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="18ecf-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="18ecf-301">Veljið flipann **Eiginleikar**, veljið línurnar sem innihalda eiginleikann **CFDI - Mexíkóskur rafrænn reikningur (MX)** og veljið viðeigandi atriði.</span><span class="sxs-lookup"><span data-stu-id="18ecf-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="18ecf-302">Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="18ecf-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="18ecf-303">Frekari upplýsingar er að finna í köflunum um persónuverndaryfirlýsingu í fylgiskjölum um eiginleika eftir löndum.</span><span class="sxs-lookup"><span data-stu-id="18ecf-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18ecf-304">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="18ecf-304">Additional resources</span></span>

- [<span data-ttu-id="18ecf-305">Yfirlit rafrænna reikninga</span><span class="sxs-lookup"><span data-stu-id="18ecf-305">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="18ecf-306">Hafist handa með rafrænar reikningsfærslur</span><span class="sxs-lookup"><span data-stu-id="18ecf-306">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="18ecf-307">Setja upp rafrænar reikningsfærslur</span><span class="sxs-lookup"><span data-stu-id="18ecf-307">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]