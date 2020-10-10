---
title: Byrjaðu með hagræðingu skipulags
description: Þetta efnisatriði útskýrir hvernig skuli hefja notkun á virkninni Fínstilling skipulagningar.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887265"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="96406-103">Byrjaðu með hagræðingu skipulags</span><span class="sxs-lookup"><span data-stu-id="96406-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96406-104">Virkni fínstillingar áætlunar styður ekki eins og er alla þá eiginleika sem eru fáanlegir í áætlunarvélinni sem er innbyggð í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="96406-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="96406-105">Þess vegna er mikilvægt að þú metir hvort eiginleikasettið sem nú er fáanlegt í fínstillingu skipulagsins uppfylli kröfur þínar.</span><span class="sxs-lookup"><span data-stu-id="96406-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="96406-106">Sjálfgefið er að ekki er kveikt á virkni fínstillingar skipulagningar í Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="96406-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="96406-107">Þess vegna hefurðu tækifæri til að gera úttektina áður en kveikt er á henni.</span><span class="sxs-lookup"><span data-stu-id="96406-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="96406-108">Að lokum mun fínstilling skipulagningar koma í stað núverandi innbyggðrar áætlunarvélar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="96406-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="96406-109">Áður en þú kveikir á fínstillingu skipulags mælum við eindregið með því að þú metir niðurstöður greiningar á fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="96406-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="96406-110">Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="96406-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="96406-111">Til ráðstöfunar</span><span class="sxs-lookup"><span data-stu-id="96406-111">Availability</span></span>
<span data-ttu-id="96406-112">Fínstilling áætlanagerðar er í boði í eftirfarandi Azure-svæðum: Bandaríkin, Kanada, Evrópa, Bretland og Ástralía.</span><span class="sxs-lookup"><span data-stu-id="96406-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="96406-113">Ef reynt er að setja upp innbæturnar á öðru svæði birtir LCS skilaboð um að svæðið sé ekki stutt.</span><span class="sxs-lookup"><span data-stu-id="96406-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="96406-114">Athugið að fínstilling áætlanagerðar styður ekki uppsetningu á staðnum á Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="96406-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="96406-115">Leyfisveiting</span><span class="sxs-lookup"><span data-stu-id="96406-115">Licensing</span></span>

<span data-ttu-id="96406-116">Ef þú getur keyrt aðalskipulagningu með því að nota núverandi leyfi þitt þarftu ekki að kaupa viðbótarleyfi til að byrja að nota fínstillingu skipulagsins.</span><span class="sxs-lookup"><span data-stu-id="96406-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="96406-117">Setja upp innbótina</span><span class="sxs-lookup"><span data-stu-id="96406-117">Install the add-in</span></span>

<span data-ttu-id="96406-118">Til að nota fínstillingu skipulagningar skaltu setja upp innbótina fínstilling skipulagningar fyrir Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="96406-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="96406-119">Þú getur fengið aðgang að viðbótinni frá LCS verkinu og kveikt á virkni fínstillingar skipulagningar úr notendaviðmóti (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="96406-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="96406-120">Þörf fyrir fínstillingu áætlanagerðar er öflugt LCS virkt umhverfi, á stigi 2 eða hærra (ekki OneBox-umhverfi), með Dynamics 365 Supply Chain Management útgáfu 10.0.7 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="96406-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="96406-121">Ef reynt er að setja upp viðbótina í OneBox-umhverfi verður uppsetningunni ekki lokið og því verður að hætta við uppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="96406-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="96406-122">Skráðu þig inn á LCS og opnaðu viðkomandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="96406-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="96406-123">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="96406-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="96406-124">Flettu niður að flýtiflipanum **Umhverfisinnbætur**.</span><span class="sxs-lookup"><span data-stu-id="96406-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="96406-125">Veldu **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="96406-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="96406-126">Veldu **Fínstillingu skipulagningar**.</span><span class="sxs-lookup"><span data-stu-id="96406-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="96406-127">Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="96406-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="96406-128">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="96406-128">Select **Install**.</span></span>
1. <span data-ttu-id="96406-129">Á flýtiflipanum **Umhverfisviðbætur** ættir þú að sjá að hagræðing skipulags er að setja upp.</span><span class="sxs-lookup"><span data-stu-id="96406-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="96406-130">Eftir nokkrar mínútur ætti **Setur upp** að breytast í **Uppsett** (þú gætir þurft að endurnýja síðuna).</span><span class="sxs-lookup"><span data-stu-id="96406-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="96406-131">Þegar það er sett upp ertu tilbúinn til að virkja hagræðingu skipulags í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="96406-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="96406-132">Samþætting fínstillingar skipulagningar</span><span class="sxs-lookup"><span data-stu-id="96406-132">Planning Optimization integration</span></span>

<span data-ttu-id="96406-133">Til að stilla hvort nota eigi innbótina fínstilling skipulagningara fyrir aðaláætlanagerð, farðu í **Aðaláætlanargerð** \> **Uppsetning** \> **Færibreytur fínstillingar skipulagningar**.</span><span class="sxs-lookup"><span data-stu-id="96406-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="96406-134">Staða tengingar</span><span class="sxs-lookup"><span data-stu-id="96406-134">Connection status</span></span>

<span data-ttu-id="96406-135">Staða tengingarinnar gefur til kynna núverandi stöðu tengingarinnar milli Supply Chain Management og þjónustunnar Fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="96406-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="96406-136">Eftirfarandi tafla sýnir hugsanleg gildi.</span><span class="sxs-lookup"><span data-stu-id="96406-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="96406-137">Staða tengingar</span><span class="sxs-lookup"><span data-stu-id="96406-137">Connection status</span></span> | <span data-ttu-id="96406-138">Lýsing</span><span class="sxs-lookup"><span data-stu-id="96406-138">Description</span></span> | <span data-ttu-id="96406-139">Er hægt að nota fínstillingu skipulagningar?</span><span class="sxs-lookup"><span data-stu-id="96406-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="96406-140">Tengt</span><span class="sxs-lookup"><span data-stu-id="96406-140">Connected</span></span> | <span data-ttu-id="96406-141">Tengingu hafa verið komið á milli þjónustunnar fínstilling skipulagningar og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="96406-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="96406-142">Já</span><span class="sxs-lookup"><span data-stu-id="96406-142">Yes</span></span> |
| <span data-ttu-id="96406-143">Tengir</span><span class="sxs-lookup"><span data-stu-id="96406-143">Enabling connection</span></span> | <span data-ttu-id="96406-144">Nú stendur yfir beiðni um að kveikja á tengingunni við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="96406-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="96406-145">Nr</span><span class="sxs-lookup"><span data-stu-id="96406-145">No</span></span> |
| <span data-ttu-id="96406-146">Aftengt</span><span class="sxs-lookup"><span data-stu-id="96406-146">Disconnected</span></span> | <span data-ttu-id="96406-147">Engin tenging er við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="96406-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="96406-148">Hægt er að kveikja á tengingunni úr LCS, eins og lýst er fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="96406-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="96406-149">Nr</span><span class="sxs-lookup"><span data-stu-id="96406-149">No</span></span> |
| <span data-ttu-id="96406-150">Aftengir</span><span class="sxs-lookup"><span data-stu-id="96406-150">Disabling connection</span></span> | <span data-ttu-id="96406-151">Nú stendur yfir beiðni um að slökkva á tengingunni við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="96406-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="96406-152">Nr</span><span class="sxs-lookup"><span data-stu-id="96406-152">No</span></span> |
| <span data-ttu-id="96406-153">Sækir stöðu</span><span class="sxs-lookup"><span data-stu-id="96406-153">Getting status</span></span> | <span data-ttu-id="96406-154">Kerfið bíður eftir stöðuupplýsingum úr þjónustunni fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="96406-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="96406-155">Nr</span><span class="sxs-lookup"><span data-stu-id="96406-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="96406-156">Valkosturinn Nota fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="96406-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="96406-157">Stilling á valkostinum **Nota fínstillingu skipulags** ákvarðar hvaða áætlunarvél er notuð við aðaláætlanagerð:</span><span class="sxs-lookup"><span data-stu-id="96406-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="96406-158">**Já** - Fínstilling skipulags er notuð við aðaláætlungargerð.</span><span class="sxs-lookup"><span data-stu-id="96406-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="96406-159">**Nei** - Innbyggða áætlunarvélin Supply Chain Management er notuð til aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="96406-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="96406-160">Ef fyrirliggjandi runuvinnslur áætlunargerðar sem voru stofnuð fyrir innbyggðu áætlunarvélina Supply Chain Management eru sett af stað á meðan valkosturinn **Nota fínstillingu skipulagningar** er stilltur á **Já** munu þær vinnslur ekki takast.</span><span class="sxs-lookup"><span data-stu-id="96406-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="96406-161">Samþætting við uppsetninguna</span><span class="sxs-lookup"><span data-stu-id="96406-161">Integration with the setup</span></span>

<span data-ttu-id="96406-162">Ef kveikt er á forskoðun fínstillingar skipulags er aðaláætlunargerð gerð með því að nota viðbótaráætlun fyrir fínstillingu skipulags.</span><span class="sxs-lookup"><span data-stu-id="96406-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="96406-163">Í þessu tilfelli verða niðurstöður og eiginleikar aðaláætlunargerðar fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="96406-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96406-164">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="96406-164">Additional resources</span></span>

[<span data-ttu-id="96406-165">Ákvæði og skilmálar fyrir forskoðunina</span><span class="sxs-lookup"><span data-stu-id="96406-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="96406-166">Yfirlit yfir fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="96406-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="96406-167">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="96406-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="96406-168">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="96406-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="96406-169">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="96406-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="96406-170">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="96406-170">Cancel a planning job</span></span>](cancel-planning-job.md)
