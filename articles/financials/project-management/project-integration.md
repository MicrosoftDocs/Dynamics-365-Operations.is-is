---
title: Microsoft Project biðlarasamþætting
description: Skipuleggja og vinna með verkáætlun getur verið flókið, þannig að verkefnastjórar þurfa að nota verkfæri sem hjálpa þeim að stjórna þessu verki. Samþætting við Microsoft Project Client veitir stuðning til að opna og stjórna sundurliðun verkþátta í verki.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 48feb0182c623714b2acffafc42016c0471ba6c1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "317477"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="9a7c0-104">Microsoft Project biðlarasamþætting</span><span class="sxs-lookup"><span data-stu-id="9a7c0-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a7c0-105">Skipuleggja og vinna með verkáætlun getur verið flókið, þannig að verkefnastjórar þurfa að nota verkfæri sem hjálpa þeim að stjórna þessu verki.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="9a7c0-106">Samþætting við Microsoft Project Client veitir stuðning til að opna og stjórna sundurliðun verkþátta í verki.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="9a7c0-107">Verkefnastjórinn getur birt allar breytingar aftur í Finance and Operations sundurliðun verkþátta í verki.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="9a7c0-108">Ef þú notar Microsoft Dynamics 365 for Finance and Operations, uppfærslu frá júlí, verður þú að setja upp KB 4054797 og 4055884.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="9a7c0-109">Stilltu viðbótina fyrir Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9a7c0-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="9a7c0-110">Til að virkja samþættingu við Microsoft Project Client er nauðsynlegt að Microsoft Dynamics 365 viðbót sé sett upp á Microsoft Project forriti biðlara notandans.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="9a7c0-111">Þetta er gert með því að opna **Vinnusvæði verkefnastjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="9a7c0-112">• Smelltu á **Stilla verkefnisviðbót biðlara** frá **Tenglar** > **Uppsetningar** hluta vinnusvæðisins.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="9a7c0-113">• Smelltu á **Opna**, smelltu síðan á **Keyra** þegar beðið er um það.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="9a7c0-114">Opnaðu og breyttu núverandi drögum að sundurliðun verkþátta í Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9a7c0-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="9a7c0-115">Ef verk í Finance and Operations hefur nú þegar stofnað sundurliðun verkþátta, þá er hægt að opna sundurliðun verkþátta í Microsoft Project Client forritinu ef sundurliðun verkþátta er enn í drögum.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="9a7c0-116">Til að opna frá **Verk** síðunni smellirðu á **Opna í Microsoft Project** tengil í **Áætlunar** flipanum. Þessi síða er einnig hægt að opna innan Microsoft Project Client forritinu með því að smella á **Opna** í **Microsoft Dynamics 365** flipanum. Veldu **Lögaðilar** og **Verk** úr listanum.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="9a7c0-117">Ef þú notar Internet Explorer sem vafra þarftu að smella á **Vista** til að opna handvirkt frá staðsetningu sem skráin er sótt til.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="9a7c0-118">Eða smelltu á **Vista og opna** til að opna skrána í Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="9a7c0-119">Ekki endurnefna skráarheiti þegar þú vistar.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="9a7c0-120">Áður en þú gerir breytingar á skránni með Microsoft Project Client þarftu að athuga hana. Smelltu á **Skoða í** í **Microsoft Dynamics 365** flipanum. Þetta kemur í veg fyrir að aðrir notendur geti breytt sundurliðun verkþátta innan Finance and Operations á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="9a7c0-121">Til að birta sundurliðun verkþátta eftir að breytingar hafa verið gerðar skaltu smella á **Skoða í** á **Microsoft Dynamics 365** flipanum.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="9a7c0-122">Ef verkhópi hefur þegar verið bætt við verkið í Finance and Operations mun tilfangalistinn innihalda hópmeðlimi.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="9a7c0-123">Ef verkhópur hefur ekki enn verið bætt við verkið geturðu valið tilföng og búið til hópinn í Microsoft Project Client með því að smella á hnappinn **Tilföng** á **Microsoft Dynamics 365** flipanum.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="9a7c0-124">Eftirfarandi gögn verða samstillt aftur til Finance and Operations sem hluti af innskráningarferlinu:</span><span class="sxs-lookup"><span data-stu-id="9a7c0-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="9a7c0-125">• Verkheiti</span><span class="sxs-lookup"><span data-stu-id="9a7c0-125">•   Task name</span></span>

<span data-ttu-id="9a7c0-126">• Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="9a7c0-126">•   Start date</span></span>

<span data-ttu-id="9a7c0-127">• Lokadagsetning</span><span class="sxs-lookup"><span data-stu-id="9a7c0-127">•   Finish date</span></span>

<span data-ttu-id="9a7c0-128">• Forverar</span><span class="sxs-lookup"><span data-stu-id="9a7c0-128">•   Predecessors</span></span>

<span data-ttu-id="9a7c0-129">• Heiti tilfanga</span><span class="sxs-lookup"><span data-stu-id="9a7c0-129">•   Resource names</span></span>

<span data-ttu-id="9a7c0-130">• Flokkur</span><span class="sxs-lookup"><span data-stu-id="9a7c0-130">•   Category</span></span>

<span data-ttu-id="9a7c0-131">• Tilfangaflokkur</span><span class="sxs-lookup"><span data-stu-id="9a7c0-131">•   Resource category</span></span>

<span data-ttu-id="9a7c0-132">• Vinnutími</span><span class="sxs-lookup"><span data-stu-id="9a7c0-132">•   Work hours</span></span>

<span data-ttu-id="9a7c0-133">• Athugasemdir</span><span class="sxs-lookup"><span data-stu-id="9a7c0-133">•   Notes</span></span>

<span data-ttu-id="9a7c0-134">• Forgangur</span><span class="sxs-lookup"><span data-stu-id="9a7c0-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="9a7c0-135">Ef þú bætir við öðrum dálkum við Microsoft Project Client skrána þína, þá verða þær ekki vistaðar í skránni og birtast ekki þegar skráin er opnuð aftur.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="9a7c0-136">Stofnaðu sundurliðun verkþátta fyrir núverandi verk með Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9a7c0-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="9a7c0-137">Til að stofna nýja sundurliðun verkþátta með Microsoft Project Client skaltu fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="9a7c0-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="9a7c0-138">Opnaðu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9a7c0-139">Á **Microsoft Dynamics 365** flipanum skaltu smella á **Opna**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="9a7c0-140">Veldu **lögaðila** fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="9a7c0-141">Veldu **Verk**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="9a7c0-142">Smelltu á **Útritun** á **Microsoft Dynamics 365** flipanum.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="9a7c0-143">Þegar þú ert tilbúin til að birta á Finance and Operations, smelltu á **Innritun** á **Microsoft Dynamics 365** flipanum.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="9a7c0-144">Skiptu um núverandi sundurliðun verkþátta fyrir núverandi verk með Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9a7c0-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="9a7c0-145">Til að stofna nýja sundurliðun verkþátta með Microsoft Project Client og skipta um núverandi sundurliðun verkþátta fyrir núverandi verk skaltu fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="9a7c0-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="9a7c0-146">Opnaðu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9a7c0-147">Stofnaðu áætlunina í Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="9a7c0-148">Á **Microsoft Dynamics 365** flipanum, smelltu á **Vista breytingar** > **Skipta út núverandi verki**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="9a7c0-149">Veldu **lögaðila** fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="9a7c0-150">Veldu **Verk**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="9a7c0-151">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="9a7c0-152">Stofnaðu nýtt verk innan Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9a7c0-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="9a7c0-153">Opnaðu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9a7c0-154">Stofnaðu áætlunina í Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="9a7c0-155">Á **Microsoft Dynamics 365** flipanum skaltu smella á **Vista breytingar** > **Vista sem nýtt verk**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="9a7c0-156">Veldu **lögaðila** fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="9a7c0-157">Sláðu inn **kenni verks** ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="9a7c0-158">Sláðu inn **Verkheiti**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="9a7c0-159">Veldu **Gerð verks**, **Verkhóp** og **Kenni verksamnings**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="9a7c0-160">Einnig getur þú búið til nýjan verksamning með því að smella á **Nýr**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="9a7c0-161">Veldu **Dagatalið** fyrir tilföng.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="9a7c0-162">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-162">Click **OK**.</span></span>
