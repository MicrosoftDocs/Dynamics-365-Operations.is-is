---
title: Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Brasilíu
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Brasilíu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
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
ms.openlocfilehash: 6472672f5d618cc6d100298dd35939afa4c0066d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835978"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="a04d1-103">Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Brasilíu</span><span class="sxs-lookup"><span data-stu-id="a04d1-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="a04d1-104">Viðbót rafrænnar reikningsfærslu fyrir Brasilíu styður ekki sem stendur allar aðgerðir sem eru í boði í samþættingu fjárhagsskjals sem er innbyggt í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a04d1-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a04d1-105">Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Brasilíu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="a04d1-106">Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi fyrir sig í Regulatory Configuration Services (RCS) og í Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a04d1-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="a04d1-107">Það leiðir notandann einnig í gegnum ferlið við að senda inn NF-e-fjárhagsskjal (rafrænt fjárhagsskjalslíkan 55) í gegnum þjónustuna og útskýrir hvernig farið er yfir niðurstöður úrvinnslunnar og stöðu fjárhagsskjalanna.</span><span class="sxs-lookup"><span data-stu-id="a04d1-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a04d1-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="a04d1-108">Prerequisites</span></span>

<span data-ttu-id="a04d1-109">Áður en farið er í gegnum skrefin í þessu efnisatriði þarf að ljúka skrefunum í [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="a04d1-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="a04d1-110">RCS-uppsetning</span><span class="sxs-lookup"><span data-stu-id="a04d1-110">RCS setup</span></span>

<span data-ttu-id="a04d1-111">Við RCS-uppsetningu verður farið í gegnum þessi skref:</span><span class="sxs-lookup"><span data-stu-id="a04d1-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="a04d1-112">Flytja inn eiginleika rafrænnar reikningsfærslu fyrir NF-e fjárhagsskjöl.</span><span class="sxs-lookup"><span data-stu-id="a04d1-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="a04d1-113">Fara yfir skráarsniðin sem þarf til að senda inn NF-e fjárhagsskjöl til að fá heimild.</span><span class="sxs-lookup"><span data-stu-id="a04d1-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="a04d1-114">Fara yfir skráarsniðin sem þarf til að biðja um afturköllun á samþykktu NF-e.</span><span class="sxs-lookup"><span data-stu-id="a04d1-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="a04d1-115">Skilgreina tilvikið sem þarf til að senda inn NF-e fjárhagsskjöl til að fá heimild.</span><span class="sxs-lookup"><span data-stu-id="a04d1-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="a04d1-116">Skilgreina tilvikið sem þarf til að biðja um afturköllun á samþykktu NF-e.</span><span class="sxs-lookup"><span data-stu-id="a04d1-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="a04d1-117">Úthluta eiginleika rafrænnar reikningsfærslu á umhverfi rafrænnar reikningsfærsluviðbótar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="a04d1-118">Birtið eiginleika rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="a04d1-119">„Eiginleiki rafrænnar reikningsfærslu“ er almennt heiti fyrir tilfangið sem er skilgreint og gefið út til að nota þjón rafrænnar reikningsfærsluviðbótar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="a04d1-120">Uppsetning á eiginleika rafrænnar reikningsfærslu sameinar meðal annars notkun á sniðum rafrænna skýrslugerðarskilgreininga til að búa til stillanlegar útflutnings- og innflutningsskrá, og notkun á aðgerðum og aðgerðarflæði til að virkja stofnun á stillanlegum reglum til að senda beiðnir, flytja inn svör og þátta innihald svara.</span><span class="sxs-lookup"><span data-stu-id="a04d1-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="a04d1-121">Flytja inn eiginleika rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="a04d1-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="a04d1-122">Skráðu þig inn á RCS-reikninginn þinn</span><span class="sxs-lookup"><span data-stu-id="a04d1-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="a04d1-123">Á vinnusvæðinu **Altækir eiginleikar**, undir hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="a04d1-124">Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Flytja inn** til að flytja inn eiginleika rafrænnar reikningsfærslu fyrir NF-e fjárhagsskjal úr altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="a04d1-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![Flytja inn hnappur](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="a04d1-126">Veljið eiginleika NF-e-fjárhagsskjals og veljið svo **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![Eiginleiki NF-e fluttur inn](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="a04d1-128">Búa til nýja útgáfu af eiginleika NF-e fjárhagsskjals</span><span class="sxs-lookup"><span data-stu-id="a04d1-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="a04d1-129">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja **Ný**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Nýrri útgáfu rafrænnar reikningsfærslu bætt við](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="a04d1-131">Uppfæra útgáfu skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="a04d1-131">Update the configuration version</span></span>

1. <span data-ttu-id="a04d1-132">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Skilgreiningar**, skal velja **Bæta við** eða **Eyða** til að stjórna útgáfum skilgreininga (skilgreiningar á skráarsniði rafrænnar skýrslugerðar).</span><span class="sxs-lookup"><span data-stu-id="a04d1-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Stjórnun skilgreininga á eiginleikum rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="a04d1-134">Þegar ný útgáfa af eiginleika NF-e fjárhagsskjals er búin til er öll skilgreiningarútgáfan (skráarsnið rafrænnar skýrslugerðar) erfð frá nýjustu útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="a04d1-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="a04d1-135">Til að senda inn NF-e fjárhagsskjal vegna heimildar, eru eftirfarandi útgáfur skilgreiningar nauðsynlegar:</span><span class="sxs-lookup"><span data-stu-id="a04d1-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="a04d1-136">Útflutningssnið á innsendu NF-e</span><span class="sxs-lookup"><span data-stu-id="a04d1-136">NFe submit export format</span></span>
        - <span data-ttu-id="a04d1-137">Innflutningur á svarskilaboði NF-e</span><span class="sxs-lookup"><span data-stu-id="a04d1-137">NFe response message import</span></span>
        - <span data-ttu-id="a04d1-138">Innflutningur á villukladda NF-e</span><span class="sxs-lookup"><span data-stu-id="a04d1-138">NFe error log import</span></span>

    - <span data-ttu-id="a04d1-139">Til að senda inn afturköllun á NF-e er eftirfarandi útgáfa skilgreiningar nauðsynleg:</span><span class="sxs-lookup"><span data-stu-id="a04d1-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="a04d1-140">Hætta við útflutningssnið NFe</span><span class="sxs-lookup"><span data-stu-id="a04d1-140">NFe cancel export format</span></span>

2. <span data-ttu-id="a04d1-141">Í listanum skal velja skilgreiningarútgáfu og síðan velja **Breyta** eða **Skoða** til að opna síðuna **Sniðshönnuður** þar sem hægt er að breyta eða skoða skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="a04d1-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Síða sniðshönnuðar opnuð](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="a04d1-143">Notið síðuna **Sniðshönnuður** til að breyta eða skoða skilgreiningar á skrá rafræns skýrslugerðarsniðs.</span><span class="sxs-lookup"><span data-stu-id="a04d1-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="a04d1-144">Frekari upplýsingar er að finna í [Stofna skilgreiningar rafræns skjals](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span><span class="sxs-lookup"><span data-stu-id="a04d1-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![Síða sniðshönnuðar](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="a04d1-146">Stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="a04d1-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="a04d1-147">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, skal velja **Bæta við** eða **Eyða** til að stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu (þ.e. tilvikum NF-e).</span><span class="sxs-lookup"><span data-stu-id="a04d1-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![Umsjón með uppsetningum á eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="a04d1-149">Þegar ný útgáfa af eiginleika NF-e fjárhagsskjals sem fengin er frá öðrum eiginleika rafrænnar reikningsfærslu, eru allar uppsetningar eiginleikans (tilvik NF-e) erfðar frá nýjustu útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="a04d1-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="a04d1-150">Til að senda inn NF-e fjárhagsskjöl vegna heimildar, er uppsetning eiginleikans **Senda inn** nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="a04d1-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="a04d1-151">Til að senda inn afturköllun á NF-e, er uppsetning eiginleikans **Afturköllun** nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="a04d1-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="a04d1-152">Skilgreina uppsetningu á eiginleika innsendingar</span><span class="sxs-lookup"><span data-stu-id="a04d1-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="a04d1-153">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, í dálknum **Uppsetning eiginleika**, skal velja **Senda inn**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="a04d1-154">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-154">Select **Edit**.</span></span>

    ![Breyta uppsetningu á eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="a04d1-156">Á síðunni **Uppsetning á útgáfu eiginleika** skal velja flipann **Aðgerðir** til að stjórna lista yfir aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="a04d1-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![Flipinn Aðgerðir.](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="a04d1-158">Farið yfir þær aðgerðir sem þarf til að senda inn NF-e vegna heimildar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="a04d1-159">Aðgerðarkenni</span><span class="sxs-lookup"><span data-stu-id="a04d1-159">Action ID</span></span> | <span data-ttu-id="a04d1-160">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="a04d1-160">Action name</span></span>                  | <span data-ttu-id="a04d1-161">Aðgerðarlýsing</span><span class="sxs-lookup"><span data-stu-id="a04d1-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="a04d1-162">1</span><span class="sxs-lookup"><span data-stu-id="a04d1-162">1</span></span>         | <span data-ttu-id="a04d1-163">Breyta skjali</span><span class="sxs-lookup"><span data-stu-id="a04d1-163">Transform document</span></span>           | <span data-ttu-id="a04d1-164">Stofnið NF-e XML-skrá til að senda inn.</span><span class="sxs-lookup"><span data-stu-id="a04d1-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="a04d1-165">2</span><span class="sxs-lookup"><span data-stu-id="a04d1-165">2</span></span>         | <span data-ttu-id="a04d1-166">Skrifa undir skjal</span><span class="sxs-lookup"><span data-stu-id="a04d1-166">Sign document</span></span>                | <span data-ttu-id="a04d1-167">Notið stafrænt vottorð í XML-skránni.</span><span class="sxs-lookup"><span data-stu-id="a04d1-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="a04d1-168">3</span><span class="sxs-lookup"><span data-stu-id="a04d1-168">3</span></span>         | <span data-ttu-id="a04d1-169">Hringja í SEFAZ-þjónustu í Brasilíu</span><span class="sxs-lookup"><span data-stu-id="a04d1-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="a04d1-170">Sendið inn undirritaða XML-skrá til vefþjónustunnar til að fá heimild.</span><span class="sxs-lookup"><span data-stu-id="a04d1-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="a04d1-171">4</span><span class="sxs-lookup"><span data-stu-id="a04d1-171">4</span></span>         | <span data-ttu-id="a04d1-172">Vinna úr svari</span><span class="sxs-lookup"><span data-stu-id="a04d1-172">Process response</span></span>             | <span data-ttu-id="a04d1-173">Fá svar vefþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="a04d1-174">5</span><span class="sxs-lookup"><span data-stu-id="a04d1-174">5</span></span>         | <span data-ttu-id="a04d1-175">Breyta skjali</span><span class="sxs-lookup"><span data-stu-id="a04d1-175">Transform document</span></span>           | <span data-ttu-id="a04d1-176">Þáttið innihald skráarinnar sem er móttekið svar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="a04d1-177">6</span><span class="sxs-lookup"><span data-stu-id="a04d1-177">6</span></span>         | <span data-ttu-id="a04d1-178">Breyta skjali</span><span class="sxs-lookup"><span data-stu-id="a04d1-178">Transform document</span></span>           | <span data-ttu-id="a04d1-179">Stofnið XML-skrána til að spyrjast fyrir um stöðu innsendingar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="a04d1-180">7</span><span class="sxs-lookup"><span data-stu-id="a04d1-180">7</span></span>         | <span data-ttu-id="a04d1-181">Hringja í SEFAZ-þjónustu í Brasilíu</span><span class="sxs-lookup"><span data-stu-id="a04d1-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="a04d1-182">Sendið inn XML-skrána sem biður um stöðu innsendingar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="a04d1-183">8</span><span class="sxs-lookup"><span data-stu-id="a04d1-183">8</span></span>         | <span data-ttu-id="a04d1-184">Vinna úr svari</span><span class="sxs-lookup"><span data-stu-id="a04d1-184">Process response</span></span>             | <span data-ttu-id="a04d1-185">Fá svar vefþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="a04d1-186">Setja upp vefslóð fyrir SEFAZ-vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="a04d1-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="a04d1-187">Á síðunni **Uppsetning á útgáfu eiginleika**, í flipanum **Aðgerðir**, í flýtiflipanum **Aðgerðir**, skal velja **Hringja í SEFAZ-þjónustu í Brasilíu** (aðgerðarkenni **3**).</span><span class="sxs-lookup"><span data-stu-id="a04d1-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="a04d1-188">Í flýtiflipann **Færibreytur**, í reitinn **Færibreyta veffangs**, skal slá inn vefslóð SEFAZ-vefþjónustunnar fyrir innsendingu NF-e.</span><span class="sxs-lookup"><span data-stu-id="a04d1-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="a04d1-189">Í flýtiflipanum **Aðgerðir** skal velja **Hringja í SEFAZ-þjónustu í Brasilíu** (aðgerðarkenni **7**).</span><span class="sxs-lookup"><span data-stu-id="a04d1-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7**).</span></span>
4. <span data-ttu-id="a04d1-190">Í flýtiflipann **Færibreytur**, í reitinn **Færibreyta veffangs**, skal slá inn vefslóð SEFAZ-vefþjónustunnar fyrir innsendingu NF-e.</span><span class="sxs-lookup"><span data-stu-id="a04d1-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="a04d1-191">Skilgreina uppsetningu á eiginleika afturköllunar</span><span class="sxs-lookup"><span data-stu-id="a04d1-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="a04d1-192">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, í dálknum **Uppsetning eiginleika**, skal velja **Afturköllun**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="a04d1-193">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-193">Select **Edit**.</span></span>
3. <span data-ttu-id="a04d1-194">Á síðunni **Uppsetning á útgáfu eiginleika** skal velja flipann **Aðgerðir** til að stjórna lista yfir aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="a04d1-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="a04d1-195">Fara yfir aðgerðirnar sem þarf til að biðja um afturköllun á samþykktu NF-e.</span><span class="sxs-lookup"><span data-stu-id="a04d1-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="a04d1-196">Aðgerðarkenni</span><span class="sxs-lookup"><span data-stu-id="a04d1-196">Action ID</span></span> | <span data-ttu-id="a04d1-197">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="a04d1-197">Action name</span></span>                  | <span data-ttu-id="a04d1-198">Aðgerðarlýsing</span><span class="sxs-lookup"><span data-stu-id="a04d1-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="a04d1-199">1</span><span class="sxs-lookup"><span data-stu-id="a04d1-199">1</span></span>         | <span data-ttu-id="a04d1-200">Breyta skjali</span><span class="sxs-lookup"><span data-stu-id="a04d1-200">Transform document</span></span>           | <span data-ttu-id="a04d1-201">Stofnið NF-e XML-skrá afturköllunar til að senda inn.</span><span class="sxs-lookup"><span data-stu-id="a04d1-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="a04d1-202">2</span><span class="sxs-lookup"><span data-stu-id="a04d1-202">2</span></span>         | <span data-ttu-id="a04d1-203">Skrifa undir skjal</span><span class="sxs-lookup"><span data-stu-id="a04d1-203">Sign document</span></span>                | <span data-ttu-id="a04d1-204">Notið stafrænt vottorð í XML-skránni.</span><span class="sxs-lookup"><span data-stu-id="a04d1-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="a04d1-205">3</span><span class="sxs-lookup"><span data-stu-id="a04d1-205">3</span></span>         | <span data-ttu-id="a04d1-206">Hringja í SEFAZ-þjónustu í Brasilíu</span><span class="sxs-lookup"><span data-stu-id="a04d1-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="a04d1-207">Sendið inn undirritaða XML-skrá til vefþjónustunnar vegna afturköllunar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="a04d1-208">4</span><span class="sxs-lookup"><span data-stu-id="a04d1-208">4</span></span>         | <span data-ttu-id="a04d1-209">Vinna úr svari</span><span class="sxs-lookup"><span data-stu-id="a04d1-209">Process response</span></span>             | <span data-ttu-id="a04d1-210">Fá svar vefþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="a04d1-211">Setja upp vefslóð fyrir SEFAZ-vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="a04d1-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="a04d1-212">Á síðunni **Uppsetning á útgáfu eiginleika**, í flipanum **Aðgerðir**, í flýtiflipanum **Aðgerðir**, skal velja **Hringja í SEFAZ-þjónustu í Brasilíu** (aðgerðarkenni **3**).</span><span class="sxs-lookup"><span data-stu-id="a04d1-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="a04d1-213">Í flýtiflipann **Færibreytur**, í reitinn **Færibreyta veffangs**, skal slá inn vefslóð SEFAZ-vefþjónustunnar fyrir afturköllun á samþykktu NF-e.</span><span class="sxs-lookup"><span data-stu-id="a04d1-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="a04d1-214">Gera umhverfi rafrænnar reikningsfærslu tiltækt og úthluta útgáfudrög</span><span class="sxs-lookup"><span data-stu-id="a04d1-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="a04d1-215">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Umhverfi**, skal velja **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="a04d1-216">Í reitnum **Umhverfi** skal velja umhverfið.</span><span class="sxs-lookup"><span data-stu-id="a04d1-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="a04d1-217">Í reitnum **Gildir frá** skal velja dagsetninguna þegar nýja umhverfið tekur gildi.</span><span class="sxs-lookup"><span data-stu-id="a04d1-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="a04d1-218">Veljið **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-218">Select **Enable**.</span></span>

![Umhverfi rafrænnar reikningsfærslu virkjað](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="a04d1-220">Breyta stöðu í lokið</span><span class="sxs-lookup"><span data-stu-id="a04d1-220">Change the status to Completed</span></span>

1. <span data-ttu-id="a04d1-221">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="a04d1-222">Velduð **Breyta stöðu \> Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="a04d1-223">Breyta stöðu í birta</span><span class="sxs-lookup"><span data-stu-id="a04d1-223">Change the status to Publish</span></span>

1. <span data-ttu-id="a04d1-224">Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="a04d1-225">Veljið **Breyta stöðu \> Birta**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-225">Select **Change status \> Publish**.</span></span>

![Eiginleiki rafrænnar reikningsfærslu birtur](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="a04d1-227">Setja upp samþættingu rafrænnar reikningsfærsluviðbótar í Finance eða Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a04d1-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="a04d1-228">Við uppsetningu verður farið í gegnum þessi skref:</span><span class="sxs-lookup"><span data-stu-id="a04d1-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="a04d1-229">Kveikið á eiginleika NF-e Federal fyrir Brasilíu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="a04d1-230">Flytjið inn tilgreint gagnalíkan rafrænnar skýrslugerðar, gagnalíkansvörpun og snið sem eru nauðsynleg fyrir NF-e-fjárhagsskjöl.</span><span class="sxs-lookup"><span data-stu-id="a04d1-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="a04d1-231">Flytjið inn skilgreiningu rafrænnar skýrslugerðar og setjið upp svargerðir sem eru nauðsynlegar til að uppfæra stöðu fjárhagsskjalsins þegar innsendingarferlinu er skilað.</span><span class="sxs-lookup"><span data-stu-id="a04d1-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="a04d1-232">Kveikja á eiginleika NF-e Federal fyrir Brasilíu</span><span class="sxs-lookup"><span data-stu-id="a04d1-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="a04d1-233">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="a04d1-234">Í flipanum **Eiginleikar** skal velja gátreitinn **Virkja** í línunni fyrir tilvísun eiginleika **BR00053**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="a04d1-235">Flytja inn gagnalíkanavörpun rafrænnar skýrslugerðar sem þarf fyrir NF-e fjárhagsskjöl</span><span class="sxs-lookup"><span data-stu-id="a04d1-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="a04d1-236">Skráðu þig inn í Finance.</span><span class="sxs-lookup"><span data-stu-id="a04d1-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="a04d1-237">Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="a04d1-238">Gangið úr skugga um að þessi skilgreiningarveita sé stillt á **Virk**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="a04d1-239">Frekari upplýsingar um hvernig á að stilla veitu á **Virk** er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="a04d1-239">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="a04d1-240">Veldu **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="a04d1-241">Veljið **Altæk tilföng \> Opna**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="a04d1-242">Flytja inn skilgreiningar **Fjárhagsskjalavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="a04d1-243">Flytja inn skilgreiningar rafrænnar skýrslugerðar og setja upp svargerðir fyrir fjárhagsskjöl</span><span class="sxs-lookup"><span data-stu-id="a04d1-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="a04d1-244">Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="a04d1-245">Veldu **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="a04d1-246">Veljið **Altæk tilföng \> Opna**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="a04d1-247">Flytjið inn **Innflutningur villukladda NF-e**, **Gagnainnflutningssnið NF-e svars** og **Innflutning svarskilaboða NF-e**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-247">Import **NF-e error log import (BR)**, **NF-e response data import format (BR)**, and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="a04d1-248">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="a04d1-249">Í flipanum **Rafrænt skjal** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="a04d1-250">Í reitinn **Töfluheiti** skal færa inn **Haus fjárhagsskjals**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="a04d1-251">Í reitnum **Samhengi skjals** skal velja **Samhengislíkan viðskiptavinareiknings - Samhengi fjárhagsskjals**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="a04d1-252">Veljið **Svargerðir**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-252">Select **Response types**.</span></span>
9. <span data-ttu-id="a04d1-253">Veljið **Nýtt** og svo, í reitnum **Svargerð**, skal velja **Svar**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-253">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="a04d1-254">Í reitnum **Staða sendingar** skal velja **Í bið**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="a04d1-255">Í reitnum **Líkanavörpun** skal velja **Innflutningssnið svarskilaboða - Líkanavörpun úr svarskilaboðum**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="a04d1-256">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-256">Select **Save**.</span></span>
13. <span data-ttu-id="a04d1-257">Veljið **Nýtt** og svo, í reitinn **Svargerð**, skal velja **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-257">Select **New**, and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="a04d1-258">Í reitnum **Staða sendingar** skal velja **Í bið**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="a04d1-259">Í reitinn **Líkanavörpun** skal velja **Gagnainnflutningssnið NF-e svars - Gagnainnflutningur svars**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="a04d1-260">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="a04d1-261">Rafræn reikningsfærsla í vinnslu</span><span class="sxs-lookup"><span data-stu-id="a04d1-261">Electronic invoice processing</span></span>

<span data-ttu-id="a04d1-262">Við úrvinnslu í Finance verður lokið við þessi verk:</span><span class="sxs-lookup"><span data-stu-id="a04d1-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="a04d1-263">Sendið inn fjárhagsskjal í gegnum viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="a04d1-264">Skoðið keyrslukladda fyrir innsendingar og yfirfarið niðurstöður vinnslu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="a04d1-265">Sendið inn afturköllun á fjárhagsskjali í gegnum viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="a04d1-266">Sendið inn NF-e-fjárhagsskjöl fyrir SEFAZ-heimild</span><span class="sxs-lookup"><span data-stu-id="a04d1-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="a04d1-267">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, ekki er elengur hægt að nota gamla ferlið til að senda inn NF-e fjárhagsskjöl fyrir heimild (**Útflutningur/innflutningur á NF-e-ferli**).</span><span class="sxs-lookup"><span data-stu-id="a04d1-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization (**Export/Import NF-e process**) can no longer be used.</span></span> <span data-ttu-id="a04d1-268">Því er skipt út fyrir nýtt ferli sem kallast **Senda inn rafræn skjöl**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="a04d1-269">Áður en haldið er áfram skal ganga úr skugga um að til staðar sé eitt eða fleiri fjárhagsskjalalíkan viðskiptavinar 55 sem voru gefin út af fjárhagsstofnun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="a04d1-270">Stefna þessara fjárhagsskjala verður að vera stillt á **Á útleið** og staðan verður að vera **Stofnað**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-270">The direction for these fiscal documents must be set to **Outgoing**, and the status must be **Created**.</span></span> <span data-ttu-id="a04d1-271">Frekari upplýsingar er að finna í [Gefa út fjárhagsskjal viðskiptavinar (Brasilía)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span><span class="sxs-lookup"><span data-stu-id="a04d1-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="a04d1-272">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Senda inn rafræn skjöl**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="a04d1-273">Fyrir fyrstu innsendingu á skjali skal alltaf stilla valkostinn **Senda skjöl inn aftur** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="a04d1-274">Ef senda þarf skjal inn aftur í gegnum þjónustuna skal stilla þennan valkost á **Já**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="a04d1-275">Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann **Fyrirspurn** þar sem hægt er að búa til fyrirspurn til að velja skjöl til innsendingar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="a04d1-276">Í flipanum **Svið** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="a04d1-277">Í reitnum **Tafla** skal velja **Haus fjárhagsskjals**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="a04d1-278">Í reitnum **Afleidd tafla** skal velja **Haus fjárhagsskjals**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="a04d1-279">Í reitnum **Svæði** skal velja **Númer**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="a04d1-280">Í reitinn **Skilyrði** skal færa inn númer fjárhagsskjalsins sem á að senda inn.</span><span class="sxs-lookup"><span data-stu-id="a04d1-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="a04d1-281">Veljið **Í lagi** til að loka svarglugganum **Fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="a04d1-282">Veljið **Í lagi** til að senda inn valin skjöl.</span><span class="sxs-lookup"><span data-stu-id="a04d1-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="a04d1-283">Í fyrstu tilraun til að senda inn skjal í gegnum þjónustuna verður beðið um að staðfesta tenginguna við viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="a04d1-284">Veljið **Smelltu hér til að tengjast sendingarþjónustu rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="a04d1-285">Skoða alla innsendingarkladda</span><span class="sxs-lookup"><span data-stu-id="a04d1-285">View all submission logs</span></span>

<span data-ttu-id="a04d1-286">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu** er ný síða í boði sem gerir kleift að fylgja eftir innsendingarferli skjalsins.</span><span class="sxs-lookup"><span data-stu-id="a04d1-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="a04d1-287">Hægt er að nota þessa síðu til að skoða innsendingarkladda fyrir öll send skjöl.</span><span class="sxs-lookup"><span data-stu-id="a04d1-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="a04d1-288">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="a04d1-289">Í reitnum **Gerð skjals** skal velja **Haus fjárhagsskjals** til að sía eingöngu fyrir fjárhagsskjölum.</span><span class="sxs-lookup"><span data-stu-id="a04d1-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="a04d1-290">Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![Skoða upplýsingar um innsendingarkladda](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="a04d1-292">Fyrir NF-e-fjárhagsskjöl, sýnir dálkurinn **Villukóði** skilakóðann sem SEFAZ-vefþjónustan skilaði.</span><span class="sxs-lookup"><span data-stu-id="a04d1-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="a04d1-293">Skoða innsendingarkladda í gegnum síðu fjárhagsskjala</span><span class="sxs-lookup"><span data-stu-id="a04d1-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="a04d1-294">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, er einnig hægt að skoða innsendingarkladdana í gegnum síðu fjárhagsskjala.</span><span class="sxs-lookup"><span data-stu-id="a04d1-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="a04d1-295">Farið í **Fjárhagur \> Fyrirspurnir og skýrslur \> Fjárhagsskjöl \> Öll fjárhagsskjöl**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="a04d1-296">Veljið fjárhagsskjal sem var áður sent inn í gegnum viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="a04d1-297">Á aðgerðasvæðinu, í flipanum **NF-e Federal** skal velja **Kladdi rafræns skjals**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![Innsendingarkladdar skoðaðir á síðu fjárhagsskjala](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="a04d1-299">Senda inn samþykkt NF-e-fjárhagsskjöl fyrir SEFAZ-afturköllun</span><span class="sxs-lookup"><span data-stu-id="a04d1-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="a04d1-300">Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, verður ekki lengur hægt að nota gamla ferlið til að afturkalla NF-e fjárhagsskjöl.</span><span class="sxs-lookup"><span data-stu-id="a04d1-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="a04d1-301">Því er skipt út fyrir nýja afturköllunarferlið sem er fellt inn í síðuna **Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="a04d1-302">Gangið úr skugga um að afturköllun á fjárhagsskjali viðskiptavinar hafi verið keyrð fyrir samþykkt NF-e fjárhagsskjal.</span><span class="sxs-lookup"><span data-stu-id="a04d1-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="a04d1-303">Frekari upplýsingar er að finna í [Hætta við fjárhagsskjal viðskiptavinar (Brasilía)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span><span class="sxs-lookup"><span data-stu-id="a04d1-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="a04d1-304">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="a04d1-305">Veljið fjárhagsskjalið og veljið síðan **Aðgerðir \> Senda tengdar innsendingar**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="a04d1-306">Færið inn lýsingu fyrir tengdu innsendinguna og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="a04d1-307">Skoða innsendingarkladda afturköllunar</span><span class="sxs-lookup"><span data-stu-id="a04d1-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="a04d1-308">Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="a04d1-309">Í reitnum **Gerð skjals** skal velja **Haus fjárhagsskjals** til að sía eingöngu fyrir fjárhagsskjölum.</span><span class="sxs-lookup"><span data-stu-id="a04d1-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="a04d1-310">Veljið fjárhagsskjalið og síðan, á aðgerðasvæðinu, skal velja **Fyrirspurnir \> Tengdar innsendingar**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="a04d1-311">Tengdar innsendingar eru innsendingar sem tengjast aðalinnsendingunni sem var gerð fyrst.</span><span class="sxs-lookup"><span data-stu-id="a04d1-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="a04d1-312">Til dæmis er innsendingin sem heimilar tiltekið NF-e aðalinnsendingin.</span><span class="sxs-lookup"><span data-stu-id="a04d1-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="a04d1-313">Innsendingin sem biður um afturköllun á sama NF-e í SEFAZ er tengd innsending.</span><span class="sxs-lookup"><span data-stu-id="a04d1-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="a04d1-314">Hún er aðeins til vegna þess að hún biður um afturköllun vinnslunnar sem var gerð í gegnum aðra innsendingu.</span><span class="sxs-lookup"><span data-stu-id="a04d1-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="a04d1-315">Síðan **Tengdar innsendingar** sýnir allar tengdar innsendingar og stöðu þeirra fyrir tilgreint fjárhagsskjal.</span><span class="sxs-lookup"><span data-stu-id="a04d1-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="a04d1-316">Á eftirfarandi mynd merkir fyrsta línan innsendinguna sem bað um samþykki á fjárhagsskjali.</span><span class="sxs-lookup"><span data-stu-id="a04d1-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="a04d1-317">Önnur línan táknar innsendingu sem afturkallaði fjárhagsskjalið.</span><span class="sxs-lookup"><span data-stu-id="a04d1-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![Innsendingarkladdar afturköllunar skoðaðir](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="a04d1-319">Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.</span><span class="sxs-lookup"><span data-stu-id="a04d1-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Upplýsingar um innsendingarkladda afturköllunar skoðaðar](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="a04d1-321">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="a04d1-321">Privacy notice</span></span>
<span data-ttu-id="a04d1-322">Til að virkja eiginleikann BR-00053 (NF-e Federal) þarf hugsanlega að senda takmörkuð gögn, sem fela í sér skattskráningarkenni fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="a04d1-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="a04d1-323">Þetta verður sent til stofnanir þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda.</span><span class="sxs-lookup"><span data-stu-id="a04d1-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="a04d1-324">Stjórnandi getur kveikt og slökkt á eiginleika BR-00053 (NF-e Federal) með því að fara í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="a04d1-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="a04d1-325">Veljið flipann **Eiginleikar**, veljið línuna sem inniheldur BR-00053 eiginleikann og veljið viðeigandi atriði.</span><span class="sxs-lookup"><span data-stu-id="a04d1-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="a04d1-326">Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="a04d1-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="a04d1-327">Frekari upplýsingar er að finna í köflunum um persónuverndaryfirlýsingu í fylgiskjölum um eiginleika eftir löndum.</span><span class="sxs-lookup"><span data-stu-id="a04d1-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a04d1-328">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a04d1-328">Additional resources</span></span>

- [<span data-ttu-id="a04d1-329">Yfirlit innbótar rafrænna reikninga</span><span class="sxs-lookup"><span data-stu-id="a04d1-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="a04d1-330">Hafist handa með innbót rafrænna reikninga</span><span class="sxs-lookup"><span data-stu-id="a04d1-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="a04d1-331">Setja upp viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="a04d1-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
