---
title: Byrjaðu með hagræðingu skipulags
description: Þetta efnisatriði útskýrir hvernig skuli hefja notkun á virkninni Fínstilling skipulagningar.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773979"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="98a5b-103">Byrjaðu með hagræðingu skipulags</span><span class="sxs-lookup"><span data-stu-id="98a5b-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="98a5b-104">Virkni fínstillingar áætlunar styður ekki eins og er alla þá eiginleika sem eru fáanlegir í áætlunarvélinni sem er innbyggð í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98a5b-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="98a5b-105">Þess vegna er mikilvægt að þú metir hvort eiginleikasettið sem nú er fáanlegt í fínstillingu skipulagsins uppfylli kröfur þínar.</span><span class="sxs-lookup"><span data-stu-id="98a5b-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="98a5b-106">Sjálfgefið er að ekki er kveikt á virkni fínstillingar skipulagningar í Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="98a5b-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="98a5b-107">Þess vegna hefurðu tækifæri til að gera úttektina áður en kveikt er á henni.</span><span class="sxs-lookup"><span data-stu-id="98a5b-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="98a5b-108">Að lokum mun fínstilling skipulagningar koma í stað núverandi innbyggðrar áætlunarvélar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98a5b-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="98a5b-109">Áður en þú kveikir á fínstillingu skipulags mælum við eindregið með því að þú metir niðurstöður greiningar á fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="98a5b-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="98a5b-110">Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="98a5b-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="98a5b-111">Leyfisveiting</span><span class="sxs-lookup"><span data-stu-id="98a5b-111">Licensing</span></span>

<span data-ttu-id="98a5b-112">Ef þú getur keyrt aðalskipulagningu með því að nota núverandi leyfi þitt þarftu ekki að kaupa viðbótarleyfi til að byrja að nota fínstillingu skipulagsins.</span><span class="sxs-lookup"><span data-stu-id="98a5b-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="98a5b-113">Setja upp innbótina</span><span class="sxs-lookup"><span data-stu-id="98a5b-113">Install the add-in</span></span>

<span data-ttu-id="98a5b-114">Til að nota fínstillingu skipulagningar skaltu setja upp innbótina fínstilling skipulagningar fyrir Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98a5b-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="98a5b-115">Þú getur fengið aðgang að viðbótinni frá LCS verkinu og kveikt á virkni fínstillingar skipulagningar úr notendaviðmóti (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98a5b-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="98a5b-116">Skráðu þig inn á LCS og opnaðu viðkomandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="98a5b-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="98a5b-117">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="98a5b-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="98a5b-118">Veldu **Viðhalda** eða skrunaðu niður að flýtiflipanum **Umhverfisinnbætur**.</span><span class="sxs-lookup"><span data-stu-id="98a5b-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="98a5b-119">Veldu **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="98a5b-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="98a5b-120">Veldu **Fínstillingu skipulagningar**.</span><span class="sxs-lookup"><span data-stu-id="98a5b-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="98a5b-121">Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="98a5b-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="98a5b-122">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="98a5b-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="98a5b-123">Samþætting fínstillingar skipulagningar</span><span class="sxs-lookup"><span data-stu-id="98a5b-123">Planning Optimization integration</span></span>

<span data-ttu-id="98a5b-124">Til að stilla hvort nota eigi innbótina fínstilling skipulagningara fyrir aðaláætlanagerð, farðu í **Aðaláætlanargerð** \> **Uppsetning** \> **Samþætting fínstillingar skipulagningar** \> **Samþættingarfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="98a5b-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="98a5b-125">Staða tengingar</span><span class="sxs-lookup"><span data-stu-id="98a5b-125">Connection status</span></span>

<span data-ttu-id="98a5b-126">Staða tengingarinnar gefur til kynna núverandi stöðu tengingarinnar milli Supply Chain Management og þjónustunnar Fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="98a5b-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="98a5b-127">Eftirfarandi tafla sýnir hugsanleg gildi.</span><span class="sxs-lookup"><span data-stu-id="98a5b-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="98a5b-128">Staða tengingar</span><span class="sxs-lookup"><span data-stu-id="98a5b-128">Connection status</span></span> | <span data-ttu-id="98a5b-129">Lýsing</span><span class="sxs-lookup"><span data-stu-id="98a5b-129">Description</span></span> | <span data-ttu-id="98a5b-130">Er hægt að nota fínstillingu skipulagningar?</span><span class="sxs-lookup"><span data-stu-id="98a5b-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="98a5b-131">Tengt</span><span class="sxs-lookup"><span data-stu-id="98a5b-131">Connected</span></span> | <span data-ttu-id="98a5b-132">Tengingu hafa verið komið á milli þjónustunnar fínstilling skipulagningar og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98a5b-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="98a5b-133">Já</span><span class="sxs-lookup"><span data-stu-id="98a5b-133">Yes</span></span> |
| <span data-ttu-id="98a5b-134">Tengir</span><span class="sxs-lookup"><span data-stu-id="98a5b-134">Enabling connection</span></span> | <span data-ttu-id="98a5b-135">Nú stendur yfir beiðni um að kveikja á tengingunni við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="98a5b-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="98a5b-136">Nr</span><span class="sxs-lookup"><span data-stu-id="98a5b-136">No</span></span> |
| <span data-ttu-id="98a5b-137">Aftengt</span><span class="sxs-lookup"><span data-stu-id="98a5b-137">Disconnected</span></span> | <span data-ttu-id="98a5b-138">Engin tenging er við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="98a5b-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="98a5b-139">Hægt er að kveikja á tengingunni úr LCS, eins og lýst er fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="98a5b-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="98a5b-140">Nr</span><span class="sxs-lookup"><span data-stu-id="98a5b-140">No</span></span> |
| <span data-ttu-id="98a5b-141">Aftengir</span><span class="sxs-lookup"><span data-stu-id="98a5b-141">Disabling connection</span></span> | <span data-ttu-id="98a5b-142">Nú stendur yfir beiðni um að slökkva á tengingunni við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="98a5b-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="98a5b-143">Nr</span><span class="sxs-lookup"><span data-stu-id="98a5b-143">No</span></span> |
| <span data-ttu-id="98a5b-144">Sækir stöðu</span><span class="sxs-lookup"><span data-stu-id="98a5b-144">Getting status</span></span> | <span data-ttu-id="98a5b-145">Kerfið bíður eftir stöðuupplýsingum úr þjónustunni fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="98a5b-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="98a5b-146">Nr</span><span class="sxs-lookup"><span data-stu-id="98a5b-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="98a5b-147">Valkosturinn Nota fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="98a5b-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="98a5b-148">Stilling á valkostinum **Nota fínstillingu skipulags** ákvarðar hvaða áætlunarvél er notuð við aðaláætlanagerð:</span><span class="sxs-lookup"><span data-stu-id="98a5b-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="98a5b-149">**Já** - Fínstilling skipulags er notuð við aðaláætlungargerð.</span><span class="sxs-lookup"><span data-stu-id="98a5b-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="98a5b-150">**Nei** - Innbyggða áætlunarvélin Supply Chain Management er notuð til aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="98a5b-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="98a5b-151">Ef fyrirliggjandi runuvinnslur áætlunargerðar sem voru stofnuð fyrir innbyggðu áætlunarvélina Supply Chain Management eru sett af stað á meðan valkosturinn **Nota fínstillingu skipulagningar** er stilltur á **Já** munu þær vinnslur ekki takast.</span><span class="sxs-lookup"><span data-stu-id="98a5b-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="98a5b-152">Samþætting við uppsetninguna</span><span class="sxs-lookup"><span data-stu-id="98a5b-152">Integration with the setup</span></span>

<span data-ttu-id="98a5b-153">Ef kveikt er á forskoðun fínstillingar skipulags er aðaláætlunargerð gerð með því að nota viðbótaráætlun fyrir fínstillingu skipulags.</span><span class="sxs-lookup"><span data-stu-id="98a5b-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="98a5b-154">Í þessu tilfelli verða niðurstöður og eiginleikar aðaláætlunargerðar fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="98a5b-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="98a5b-155">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="98a5b-155">Related resources</span></span>

[<span data-ttu-id="98a5b-156">Ákvæði og skilmálar fyrir forskoðunina</span><span class="sxs-lookup"><span data-stu-id="98a5b-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="98a5b-157">Yfirlit yfir fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="98a5b-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="98a5b-158">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="98a5b-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="98a5b-159">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="98a5b-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="98a5b-160">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="98a5b-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="98a5b-161">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="98a5b-161">Cancel a planning job</span></span>](cancel-planning-job.md)
