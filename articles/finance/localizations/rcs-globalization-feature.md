---
title: Regulatory Configuration Service (RCS) – altækir eiginleikar
description: Þetta efnisatriði útskýrir hvernig á að nota Microsoft Regulatory Configuration Services (RCS) og altæku geymsluna til að stofna og nota altæka eiginleika.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444289"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="6764e-103">Regulatory Configuration Service (RCS) – altækir eiginleikar</span><span class="sxs-lookup"><span data-stu-id="6764e-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6764e-104">Hægt er að nota Microsoft Regulatory Configuration Services (RCS) til að stofna altækan eiginleika sem hægt er að nota í altækri þjónustu, svo sem rafrænnar reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="6764e-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="6764e-105">RCS gerir þér kleift að framkvæma þessi verk:</span><span class="sxs-lookup"><span data-stu-id="6764e-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="6764e-106">Skilgreina tengda íhluti eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6764e-106">Define related components of a feature.</span></span>
- <span data-ttu-id="6764e-107">Stjórna líftíma eiginleikans í gegnum stöðu eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6764e-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="6764e-108">Gera eiginleika tiltækan fyrir skilgreind umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6764e-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="6764e-109">Deila eiginleika með öðrum fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="6764e-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="6764e-110">Eftirfarandi ferli útskýra hvernig notandi í RCS getur bætt við altækum eiginleika og tengdum íhlutum, uppfært stöðu eiginleika og gert eiginleikann tiltækan þannig að hægt sé að nota hann í altækri þjónustu.</span><span class="sxs-lookup"><span data-stu-id="6764e-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="6764e-111">Áður en ferlunum er lokið þarf að ljúka við skrefin sem tengjast eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="6764e-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="6764e-112">RCS-tilvik opnað.</span><span class="sxs-lookup"><span data-stu-id="6764e-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="6764e-113">Stofnun og virkjun skilgreiningarveitu.</span><span class="sxs-lookup"><span data-stu-id="6764e-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="6764e-114">Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6764e-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="6764e-115">Í tilviki Finance and Operations-forrita skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6764e-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="6764e-116">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="6764e-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6764e-117">Ef engu RCS-umhverfi er úthlutað fyrir fyrirtækið skaltu velja **Regulatory Services – Skilgreining** og fylgja leiðbeiningunum til að úthluta einu slíku.</span><span class="sxs-lookup"><span data-stu-id="6764e-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="6764e-118">Ef RCS-umhverfi hefur þegar verið útvegað fyrir þitt fyrirtæki, notaðu slóðina á síðunni til að fá aðgang að umhverfinu með því að velja innskráningarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="6764e-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="6764e-119">Kveikja á altækum eiginleikum</span><span class="sxs-lookup"><span data-stu-id="6764e-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="6764e-120">Í RCS-tilvikinu skal velja reitinn **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="6764e-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="6764e-121">Á vinnusvæðinu **Eiginleikastjórnun** skal velja **Altækir eiginleikar** í listanum og síðan velja **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="6764e-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Altækir eiginleikar í eiginleikastjórnun](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="6764e-123">Altækir eiginleikar</span><span class="sxs-lookup"><span data-stu-id="6764e-123">Globalization features</span></span>

<span data-ttu-id="6764e-124">Til að nota altækan eiginleika verður fyrst að flytja hann inn úr altæku geymslunni og búa til eigin útgáfu af honum.</span><span class="sxs-lookup"><span data-stu-id="6764e-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="6764e-125">Hægt er að bæta við altækum eiginleikum með tvennum hætti:</span><span class="sxs-lookup"><span data-stu-id="6764e-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="6764e-126">Bæta við afleiddum eiginleika sem byggir á fyrirliggjandi eiginleika sem hefur verið birtur eða honum deilt.</span><span class="sxs-lookup"><span data-stu-id="6764e-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="6764e-127">Bæta við nýjum eiginleika sem hefur verið búinn til frá grunni.</span><span class="sxs-lookup"><span data-stu-id="6764e-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="6764e-128">Aðgangur að altækum eiginleikum</span><span class="sxs-lookup"><span data-stu-id="6764e-128">Access Globalization features</span></span>

1. <span data-ttu-id="6764e-129">Gangið úr skugga um að kveikt sé á eiginleikanum **Altækir eiginleikar** í eiginleikastjórnun eins og lýst er hér á undan í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="6764e-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="6764e-130">Opnið nýja vinnusvæðið **Altækir eiginleikar** og síðan, undir **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="6764e-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Vinnusvæði altækra eiginleika](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="6764e-132">Síðan **Eiginleikar rafrænnar reikningsfærslu** opnast.</span><span class="sxs-lookup"><span data-stu-id="6764e-132">The **e-Invoicing Features** page is opened.</span></span>

    ![Eiginleikasíða rafrænnar reikningsfærslu](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="6764e-134">Bæta við afleiddum altækum eiginleika</span><span class="sxs-lookup"><span data-stu-id="6764e-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="6764e-135">Hægt er að bæta við nýjum altækum eiginleika með því að notast við fyrirliggjandi eiginleika sem hefur verið birtur eða honum deilt.</span><span class="sxs-lookup"><span data-stu-id="6764e-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="6764e-136">Veljið **Flytja inn** til að opna síðuna **Flytja inn eiginleika úr altækri geymslu**.</span><span class="sxs-lookup"><span data-stu-id="6764e-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Flytja inn eiginleika af síðu altækrar geymslu](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="6764e-138">Veljið **Samstilla** til að fá nýjustu eiginleikana.</span><span class="sxs-lookup"><span data-stu-id="6764e-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="6764e-139">Samstillti listinn inniheldur eiginleika sem eru tiltækir annaðhvort vegna þess að þeir voru gefnir út af Microsoft eða vegna þess að þeim var deilt með öðrum skilgreiningarveitum.</span><span class="sxs-lookup"><span data-stu-id="6764e-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Samstilltur listi yfir eiginleika](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="6764e-141">Í listanum skal velja eiginleikana sem á að flytja inn og síðan velja **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="6764e-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="6764e-142">Þú færð skilaboð þegar valdir eiginleikar hafa verið fluttir inn.</span><span class="sxs-lookup"><span data-stu-id="6764e-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Skilaboð um lokinn innflutning](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="6764e-144">Veljið **Bæta við** og síðan í fellilista svarglugga skal velja valkostinn **Byggt á fyrirliggjandi útgáfu**.</span><span class="sxs-lookup"><span data-stu-id="6764e-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="6764e-145">Færið inn heiti og lýsingu á eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="6764e-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="6764e-146">Í lista yfir tiltæka eiginleika skal velja grunnútgáfu eiginleikans og síðan velja **Stofna eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="6764e-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Afleiddum eiginleika bætt við](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="6764e-148">Eiginleikinn sem bætt var við er stofnaður og er með stöðuna **Drög**.</span><span class="sxs-lookup"><span data-stu-id="6764e-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Afleiddur eiginleiki sem er með stöðuna drög](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="6764e-150">Yfirfara skal íhluti eiginleika til að ákvarða hvort uppfærslur eru nauðsynlegar:</span><span class="sxs-lookup"><span data-stu-id="6764e-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="6764e-151">Fara skal yfir skilgreiningarnar ef skyldi reynast nauðsynlegt að sérstilla snið rafrænnar skýrslugerðar og bindingu þeirra við sniðsvarpanir fyrir eiginleikaútgáfuna.</span><span class="sxs-lookup"><span data-stu-id="6764e-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="6764e-152">Fara skal yfir uppsetninguna ef skyldi reynast nauðsynlegt að sérstilla flipann **Aðgerðir**, flipann **Gildissviðsreglur** eða flipann **Breytur** fyrir eiginleikaútgáfuna.</span><span class="sxs-lookup"><span data-stu-id="6764e-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="6764e-153">Í flipanum **Útgáfur** skal velja dagsetningu fyrir **Gildir frá** og færa inn lýsingu ef reiturinn **Lýsing** er auður.</span><span class="sxs-lookup"><span data-stu-id="6764e-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="6764e-154">Veljið **Breyta stöðu** til að ljúka við eiginleikann.</span><span class="sxs-lookup"><span data-stu-id="6764e-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="6764e-155">Hægt er að bjóða upp á fullkláraða eiginleika fyrir tiltekið umhverfi til að hægt sé að nota þá í altækri þjónustu, eða hægt er að birta þá í altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="6764e-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="6764e-156">Eiginleikar sem eru með gildi fyrir **Staða útgáfu eiginleika** sem **Útgefið** er hægt að deila með ytri fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="6764e-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="6764e-157">Bæta við nýjum altækum eiginleika</span><span class="sxs-lookup"><span data-stu-id="6764e-157">Add a new Globalization feature</span></span>

<span data-ttu-id="6764e-158">Hægt er að bæta við nýjum altækum eiginleika með því að búa hann til frá grunni.</span><span class="sxs-lookup"><span data-stu-id="6764e-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="6764e-159">Á síðunni **Flytja inn eiginleika úr altækri geymslu** skal velja **Bæta við** og síðan, í fellilista svargluggans, skal velja valkostinn **Nýr eiginleiki**.</span><span class="sxs-lookup"><span data-stu-id="6764e-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="6764e-160">Færið inn heiti og lýsingu á eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="6764e-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="6764e-161">Veljið **Stofna eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="6764e-161">Select **Create feature**.</span></span>

    ![Nýjum eiginleika bætt við](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="6764e-163">Í flipanum **Útgáfur** skal velja dagsetningu fyrir **Gildir frá** og síðan velja **Breyta stöðu** til að ljúka við eiginleikann.</span><span class="sxs-lookup"><span data-stu-id="6764e-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="6764e-164">Hægt er að bjóða upp á fullkláraða eiginleika fyrir tiltekið umhverfi til að hægt sé að nota þá í altækri þjónustu, eða hægt er að birta þá í altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="6764e-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="6764e-165">Eiginleikar sem eru með gildi fyrir **Staða útgáfu eiginleika** sem **Útgefið** er hægt að deila með ytri fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="6764e-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="6764e-166">Eiginleikastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="6764e-166">Feature component overview</span></span>

<span data-ttu-id="6764e-167">Altækir eiginleikar eru með nokkra íhluti:</span><span class="sxs-lookup"><span data-stu-id="6764e-167">Globalization features have several components:</span></span>

- <span data-ttu-id="6764e-168">**Útgáfa** – Þessi íhlutur styður eiginleika líftímastjórnunar og gerir notendum kleift að stjórna stöðu fyrir mismunandi útgáfur af eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="6764e-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="6764e-169">**Skilgreiningar** - Þessi íhlutur gerir notendum kleift að stjórna, skoða og breyta tengdum sniðum rafrænnar skýrslugerðar og sniðsvörpunum.</span><span class="sxs-lookup"><span data-stu-id="6764e-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="6764e-170">**Uppsetningar** – Þessi íhlutur leyfir notendum altækrar þjónustu, t.d. rafrænnar reikningsfærsluþjónustu, að stjórna uppsetningu á tengdri eiginleikaútgáfu.</span><span class="sxs-lookup"><span data-stu-id="6764e-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="6764e-171">Hann styður þar af leiðandi sveigjanlega smíði á samskipta- og svörunarreglum.</span><span class="sxs-lookup"><span data-stu-id="6764e-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="6764e-172">**Umhverfi** – Þessi íhlutur leyfir notendum altækrar þjónustu, t.d. rafrænnar reikningsfærsluþjónustu, að stjórna umhverfi þar sem uppsetning eiginleikaútgáfu er notuð og veitir notendum sem hafa aðgang að henni heimild.</span><span class="sxs-lookup"><span data-stu-id="6764e-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="6764e-173">**Fyrirtæki** – Þessi íhlutur gerir notendum kleift að deila eiginleika með ytri fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="6764e-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="6764e-174">Eiginleikaíhlutir skilgreindir</span><span class="sxs-lookup"><span data-stu-id="6764e-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="6764e-175">Útgáfa og staða</span><span class="sxs-lookup"><span data-stu-id="6764e-175">Version and status</span></span>

<span data-ttu-id="6764e-176">Útgáfan er notuð til að stjórna stuðningstíma altæks eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6764e-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="6764e-177">Hægt er að breyta stöðunni í reitnum **Staða** í flipanum **Útgáfa**. Eftirfarandi stöður eru í boði:</span><span class="sxs-lookup"><span data-stu-id="6764e-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="6764e-178">**Drög** – Aðeins er hægt að breyta eiginleikanum þegar hann er í þessari stöðu.</span><span class="sxs-lookup"><span data-stu-id="6764e-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="6764e-179">**Lokið** – Eiginleikinn og allir tengdir íhlutir hafa verið fullkláraðir (lokið) og ekki er hægt að breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="6764e-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="6764e-180">**Útgefið** – Eiginleikinn og allir tengdir íhlutir hafa verið gefnir út í altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="6764e-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="6764e-181">**Deilt** – Eiginleikanum og öllum tengdum íhlutum hefur verið deilt með ytri fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="6764e-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="6764e-182">**Virkjað** – Eiginleikinn og allir tengdir íhlutir hafa verið virkjaðir til að nota í altækri þjónustu, t.d. rafrænni reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="6764e-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="6764e-183">Eiginleikar verða að fara í réttri röð í gegnum þessar stöður.</span><span class="sxs-lookup"><span data-stu-id="6764e-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="6764e-184">Þess vegna er ekki endilega hægt að nálgast allar stöður á hverju stigi líftíma.</span><span class="sxs-lookup"><span data-stu-id="6764e-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="6764e-185">Afbrigði</span><span class="sxs-lookup"><span data-stu-id="6764e-185">Configurations</span></span>

<span data-ttu-id="6764e-186">Eftirtaldar aðgerðir er hægt að stilla:</span><span class="sxs-lookup"><span data-stu-id="6764e-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="6764e-187">**Skoða** – Skoða undirliggjandi skilgreiningar eiginleika sem krefjast ekki neinnar uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="6764e-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="6764e-188">**Breyta** – Stofna útgáfudrög af valinni skilgreiningu til að hægt sé að breyta sniði eða sniðsvörpun í sniðshönnuði.</span><span class="sxs-lookup"><span data-stu-id="6764e-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="6764e-189">**Eyða** – Eyða valinni skilgreiningu úr eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="6764e-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="6764e-190">**Endurreikna grunn** – Endurreikna grunn eiginleikans.</span><span class="sxs-lookup"><span data-stu-id="6764e-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="6764e-191">Nánari upplýsingar er að finna í hlutanum [Endurreikna grunn afleiddra altækra eiginleika](#rebase) síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="6764e-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="6764e-192">Uppsetningar</span><span class="sxs-lookup"><span data-stu-id="6764e-192">Setups</span></span>

<span data-ttu-id="6764e-193">Eftirtaldar aðgerðir eru í boði fyrir uppsetningar eiginleika:</span><span class="sxs-lookup"><span data-stu-id="6764e-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="6764e-194">**Bæta við** – Stofna nýja uppsetningu eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6764e-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="6764e-195">Hægt er að taka þessa eiginleikauppsetningu úr fyrirliggjandi eiginleikauppsetningu eða búa hana til frá grunni.</span><span class="sxs-lookup"><span data-stu-id="6764e-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="6764e-196">**Eyða** – Eyða valinni uppsetningu eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6764e-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="6764e-197">**Skoða** – Skoða undirliggjandi uppsetningu eiginleika sem þarfnast ekki breytinga.</span><span class="sxs-lookup"><span data-stu-id="6764e-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="6764e-198">**Breyta** – Stofna, eyða eða breyta eigindum þriggja helstu íhluta eiginleikauppsetningar:</span><span class="sxs-lookup"><span data-stu-id="6764e-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="6764e-199">Aðgerðir og færibreytur þeirra</span><span class="sxs-lookup"><span data-stu-id="6764e-199">Actions and their parameters</span></span>
    - <span data-ttu-id="6764e-200">Gildissviðsreglur</span><span class="sxs-lookup"><span data-stu-id="6764e-200">Applicability rules</span></span>
    - <span data-ttu-id="6764e-201">Breytur</span><span class="sxs-lookup"><span data-stu-id="6764e-201">Variables</span></span>

![Uppsetningarsíða eiginleikaútgáfu](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="6764e-203">Umhverfi</span><span class="sxs-lookup"><span data-stu-id="6764e-203">Environments</span></span>

<span data-ttu-id="6764e-204">Eftirtaldar aðgerðir eru í boði fyrir umhverfi:</span><span class="sxs-lookup"><span data-stu-id="6764e-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="6764e-205">**Virkja** – Fyrir valda eiginleikaútgáfu skal velja útgefið umhverfi og velja dagsetningu fyrir **Gildir frá** þegar hún á að vera í boði.</span><span class="sxs-lookup"><span data-stu-id="6764e-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="6764e-206">Nánari upplýsingar er að finna í hlutanum [Skilgreina umhverfi fyrir virkjun](#configureenvironment) síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="6764e-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="6764e-207">**Hætta við** – Fjarlægja umhverfi fyrir eiginleikauppsetningu.</span><span class="sxs-lookup"><span data-stu-id="6764e-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="6764e-208">Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="6764e-208">Organizations</span></span>

<span data-ttu-id="6764e-209">Fylgið eftirfarandi skrefum til að samnýta altæka eiginleika með ytra fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="6764e-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="6764e-210">Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleikann og eiginleikaútgáfuna sem á að samnýta.</span><span class="sxs-lookup"><span data-stu-id="6764e-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="6764e-211">Í flipanum **Fyrirtæki** skal velja **Samnýta með** og síðan, í fellilistaglugganum, skal færa inn lénsheiti fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6764e-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="6764e-212">Veldu **Deila**.</span><span class="sxs-lookup"><span data-stu-id="6764e-212">Select **Share**.</span></span>

    ![Samnýta eiginleika með fyrirtæki](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="6764e-214">Eiginleikanum er deilt með ytra fyrirtækinu og er aðgengilegur fyrir það fyrirtæki í altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="6764e-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="6764e-215">Þaðan er hægt að flytja hann inn í tilvik fyrirtækisins í RCS eða Dynamics 365 Finance svo hægt sé að nota hann.</span><span class="sxs-lookup"><span data-stu-id="6764e-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="6764e-216">Endurreikna grunn afleiddra altækra eiginleika</span><span class="sxs-lookup"><span data-stu-id="6764e-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="6764e-217">Hægt er að endurreikna grunn afleidds altæks eiginleika yfir í nýja eða uppfærða útgáfu grunneiginleikans.</span><span class="sxs-lookup"><span data-stu-id="6764e-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="6764e-218">Á þennan hátt er hægt að uppfæra breytingar sem hafa átt sér stað í grunnútgáfunni sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="6764e-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="6764e-219">Uppfærð útgáfa grunneiginleika er stofnuð af upprunalegri skilgreiningarveitu og hún er síðan gefin út eða samnýtt.</span><span class="sxs-lookup"><span data-stu-id="6764e-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Uppfærð útgáfa grunneiginleika](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="6764e-221">Til dæmis, ef ætlunin er að endurgera afleidda útgáfu eiginleika sem var stofnuð þarf fyrst að sækja nýjustu útgáfuna aðgerðarinnar með því að flytja hana inn úr altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="6764e-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="6764e-222">Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="6764e-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="6764e-223">Veljið **Samstilla** til að fá nýjustu eiginleikana.</span><span class="sxs-lookup"><span data-stu-id="6764e-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="6764e-224">Í listanum yfir eiginleika skal velja eiginleikana sem á að flytja inn og síðan velja **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="6764e-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Nýjasta útgáfa eiginleika flutt inn](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="6764e-226">Í listanum yfir eiginleika skal velja eiginleikann sem á að endurreikna grunn fyrir.</span><span class="sxs-lookup"><span data-stu-id="6764e-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="6764e-227">Í flipanum **Útgáfa** skal velja **Ný** til að búa til drög að útgáfu.</span><span class="sxs-lookup"><span data-stu-id="6764e-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Ný drög að útgáfu búin til](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="6764e-229">Veldu **Endurreikna grunn**.</span><span class="sxs-lookup"><span data-stu-id="6764e-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="6764e-230">Í svarglugganum **Endurreikna grunn** skal velja nýjustu útgáfu eiginleikans til að endurreikna til.</span><span class="sxs-lookup"><span data-stu-id="6764e-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Gluggi fyrir endurreikning grunns](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="6764e-232">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6764e-232">Select **OK**.</span></span>
9. <span data-ttu-id="6764e-233">Farið yfir íhluti eiginleikans og gerið allar nauðsynlegar breytingar.</span><span class="sxs-lookup"><span data-stu-id="6764e-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="6764e-234">Veljið **Breyta stöðu** til að ljúka við eiginleika með endurreiknaðan grunn.</span><span class="sxs-lookup"><span data-stu-id="6764e-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="6764e-235">Þegar endurreikning grunns er lokið er hægt að framkvæma fleiri aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="6764e-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="6764e-236">Til dæmis er hægt að gefa út eiginleikann og gera hann tiltækan til að nota í altækri þjónustu.</span><span class="sxs-lookup"><span data-stu-id="6764e-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Eiginleikastaða uppfærð í Lokið](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="6764e-238">Stilla umhverfi fyrir altæka eiginleika</span><span class="sxs-lookup"><span data-stu-id="6764e-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="6764e-239">Notendur altækrar þjónustu geta stjórnað umhverfinu til að setja upp altækan eiginleika og veitt heimild til annarra notenda sem hafa aðgang að honum.</span><span class="sxs-lookup"><span data-stu-id="6764e-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="6764e-240">Á vinnusvæðinu **Altækir eiginleikar**, undir **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="6764e-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Vinnusvæði altækra eiginleika](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="6764e-242">Veljið **Færibreytur lyklageymslu** og veljið síðan **Nýr** til að búa til leynilykil Azure-lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="6764e-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="6764e-243">Sláið inn heiti og lýsingu fyrir lyklageymsluna og síðan, í reitnum **Lyklageymsla**, skal slá inn vefslóðina sem auðkennir tilfang lyklageymslunnar í Azure.</span><span class="sxs-lookup"><span data-stu-id="6764e-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="6764e-244">Í flýtiflipanum **Vottorð** skal velja **Bæta við** til að bæta vottorðinu við og færa inn heiti og lýsingu fyrir hvert vottorð.</span><span class="sxs-lookup"><span data-stu-id="6764e-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Vottorði bætt við](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="6764e-246">Velja skal **Nýtt** til að stofna nýtt umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6764e-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="6764e-247">Færa skal inn heiti, lýsingu og samnýtt leynitákn undirskriftar fyrir aðgang sem þarf fyrir geymsluna.</span><span class="sxs-lookup"><span data-stu-id="6764e-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="6764e-248">Á flýtiflipanum **Notendur** skal velja **Nýr** til að bæta við nýjum notanda sem fær aðgang að þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6764e-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="6764e-249">Sláið inn notandakenni og tölvupóstfang notanda.</span><span class="sxs-lookup"><span data-stu-id="6764e-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="6764e-250">Endurtakið skref 7 og 8 til að bæta við fleiri notendum.</span><span class="sxs-lookup"><span data-stu-id="6764e-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="6764e-251">Veljið **Gefa út** til að gefa út umhverfið.</span><span class="sxs-lookup"><span data-stu-id="6764e-251">Select **Publish** to publish the environment.</span></span>

    ![Útgefið umhverfi](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
