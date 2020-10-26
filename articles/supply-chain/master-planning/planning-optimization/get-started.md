---
title: Byrjaðu með hagræðingu skipulags
description: Þetta efnisatriði útskýrir hvernig skuli hefja notkun á virkninni Fínstilling skipulagningar.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
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
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973477"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="cf527-103">Hafist handa með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="cf527-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf527-104">Eins og hefur [áður verið tilkynnt](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), er á dagskrá að fínstilling skipulagningar takið við af núverandi innbyggðri vél aðaláætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="cf527-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="cf527-105">Ef verið er að nota innbyggða vél aðaláætlanagerðar, ætti að huga að flutningi yfir í fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cf527-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="cf527-106">Mikilvægt er að hefja flutningsferlið strax vegna þess að aðgerðir þínar kunna að verða fyrir áhrifum þegar úreldingu er framfylgt.</span><span class="sxs-lookup"><span data-stu-id="cf527-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="cf527-107">Til að koma í veg fyrir vandamál í síðustu stundu þegar úreldingu er framfylgt, mælum við eindregið með því að þú ljúkir við flutninginn fyrir 1. desember 2020.</span><span class="sxs-lookup"><span data-stu-id="cf527-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="cf527-108">Sem stendur styður virknin fyrir fínstillingu skipulagningar ekki alla eiginleika sem eru í boði í vél áætlanagerðar sem er byggð inn í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf527-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="cf527-109">Þess vegna er mikilvægt að þú metir hvort eiginleikasettið sem nú er fáanlegt í fínstillingu skipulagsins uppfylli kröfur þínar.</span><span class="sxs-lookup"><span data-stu-id="cf527-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="cf527-110">Ekki er kveikt á virkni fyrir fínstillingu skipulagningar að sjálfgefnu sem stendur í Dynamics Lifecycle Services, þannig að þú hefur tækifæri til að meta stöðuna áður en kveikt er á eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="cf527-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="cf527-111">Þú þarft að biðja um undantekningu á flutningi yfir í fínstillingu skipulagningar ef ferli aðaláætlanagerðar felur ekki í sér framleiðslu (áætlaðar framleiðslupantanir sem aðaláætlanagerðin býr til) og þú þarft að nota innbyggða vél aðaláætlanagerðar í útgáfu sem er nýrri en 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="cf527-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="cf527-112">Frá og með útgáfu 10.0.16 verður sýnd villa í umhverfum þegar innbyggð aðaláætlanagerð er keyrð án þess að búa til áætlaðar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="cf527-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="cf527-113">Nota ætti fínstillingu skipulagningar fyrir allar nýjar uppsetningar sem búa ekki til áætlaðar framleiðslupantanir meðan á aðaláætlanagerð stendur.</span><span class="sxs-lookup"><span data-stu-id="cf527-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="cf527-114">Eigendur núverandi umhverfa sem keyra innbyggða vél aðaláætlanagerðar án þess að búa til áætlaðar framleiðslupantanir, fá tölvupóst með upplýsingum um undantekningarferlið.</span><span class="sxs-lookup"><span data-stu-id="cf527-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="cf527-115">Við mælum með því að þú vinnir með samstarfsaðila til að meta og leggja drög að flutningnum yfir í Fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cf527-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="cf527-116">Áður en þú kveikir á fínstillingu skipulags mælum við eindregið með því að þú metir niðurstöður greiningar á fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cf527-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="cf527-117">Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cf527-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="cf527-118">Til ráðstöfunar</span><span class="sxs-lookup"><span data-stu-id="cf527-118">Availability</span></span>
<span data-ttu-id="cf527-119">Fínstilling áætlanagerðar er í boði í eftirfarandi Azure-svæðum: Bandaríkin, Kanada, Evrópa, Bretland og Ástralía.</span><span class="sxs-lookup"><span data-stu-id="cf527-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="cf527-120">Ef reynt er að setja upp innbæturnar á öðru svæði birtir LCS skilaboð um að svæðið sé ekki stutt.</span><span class="sxs-lookup"><span data-stu-id="cf527-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="cf527-121">Athugið að fínstilling áætlanagerðar styður ekki uppsetningu á staðnum á Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf527-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="cf527-122">Leyfisveiting</span><span class="sxs-lookup"><span data-stu-id="cf527-122">Licensing</span></span>

<span data-ttu-id="cf527-123">Ef þú getur keyrt aðalskipulagningu með því að nota núverandi leyfi þitt þarftu ekki að kaupa viðbótarleyfi til að byrja að nota fínstillingu skipulagsins.</span><span class="sxs-lookup"><span data-stu-id="cf527-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="cf527-124">Setja upp innbótina</span><span class="sxs-lookup"><span data-stu-id="cf527-124">Install the add-in</span></span>

<span data-ttu-id="cf527-125">Til að nota fínstillingu skipulagningar skaltu setja upp innbótina fínstilling skipulagningar fyrir Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf527-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cf527-126">Þú getur fengið aðgang að viðbótinni frá LCS verkinu og kveikt á virkni fínstillingar skipulagningar úr notendaviðmóti (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf527-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="cf527-127">Þörf fyrir fínstillingu áætlanagerðar er öflugt LCS virkt umhverfi, á stigi 2 eða hærra (ekki OneBox-umhverfi), með Dynamics 365 Supply Chain Management útgáfu 10.0.7 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="cf527-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="cf527-128">Ef reynt er að setja upp viðbótina í OneBox-umhverfi verður uppsetningunni ekki lokið og því verður að hætta við uppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="cf527-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="cf527-129">Skráðu þig inn á LCS og opnaðu viðkomandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="cf527-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="cf527-130">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="cf527-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="cf527-131">Flettu niður að flýtiflipanum **Umhverfisinnbætur**.</span><span class="sxs-lookup"><span data-stu-id="cf527-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="cf527-132">Veldu **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="cf527-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="cf527-133">Veldu **Fínstillingu skipulagningar**.</span><span class="sxs-lookup"><span data-stu-id="cf527-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="cf527-134">Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="cf527-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="cf527-135">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="cf527-135">Select **Install**.</span></span>
1. <span data-ttu-id="cf527-136">Á flýtiflipanum **Umhverfisviðbætur** ættir þú að sjá að hagræðing skipulags er að setja upp.</span><span class="sxs-lookup"><span data-stu-id="cf527-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="cf527-137">Eftir nokkrar mínútur ætti **Setur upp** að breytast í **Uppsett** (þú gætir þurft að endurnýja síðuna).</span><span class="sxs-lookup"><span data-stu-id="cf527-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="cf527-138">Þegar það er sett upp ertu tilbúinn til að virkja hagræðingu skipulags í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf527-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="cf527-139">Samþætting fínstillingar skipulagningar</span><span class="sxs-lookup"><span data-stu-id="cf527-139">Planning Optimization integration</span></span>

<span data-ttu-id="cf527-140">Til að stilla hvort nota eigi innbótina fínstilling skipulagningara fyrir aðaláætlanagerð, farðu í **Aðaláætlanargerð** \> **Uppsetning** \> **Færibreytur fínstillingar skipulagningar**.</span><span class="sxs-lookup"><span data-stu-id="cf527-140">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="cf527-141">Staða tengingar</span><span class="sxs-lookup"><span data-stu-id="cf527-141">Connection status</span></span>

<span data-ttu-id="cf527-142">Staða tengingarinnar gefur til kynna núverandi stöðu tengingarinnar milli Supply Chain Management og þjónustunnar Fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cf527-142">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="cf527-143">Eftirfarandi tafla sýnir hugsanleg gildi.</span><span class="sxs-lookup"><span data-stu-id="cf527-143">The following table shows the possible values.</span></span>

| <span data-ttu-id="cf527-144">Staða tengingar</span><span class="sxs-lookup"><span data-stu-id="cf527-144">Connection status</span></span> | <span data-ttu-id="cf527-145">Lýsing</span><span class="sxs-lookup"><span data-stu-id="cf527-145">Description</span></span> | <span data-ttu-id="cf527-146">Er hægt að nota fínstillingu skipulagningar?</span><span class="sxs-lookup"><span data-stu-id="cf527-146">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="cf527-147">Tengt</span><span class="sxs-lookup"><span data-stu-id="cf527-147">Connected</span></span> | <span data-ttu-id="cf527-148">Tengingu hafa verið komið á milli þjónustunnar fínstilling skipulagningar og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf527-148">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="cf527-149">Já</span><span class="sxs-lookup"><span data-stu-id="cf527-149">Yes</span></span> |
| <span data-ttu-id="cf527-150">Tengir</span><span class="sxs-lookup"><span data-stu-id="cf527-150">Enabling connection</span></span> | <span data-ttu-id="cf527-151">Nú stendur yfir beiðni um að kveikja á tengingunni við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cf527-151">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="cf527-152">Nr</span><span class="sxs-lookup"><span data-stu-id="cf527-152">No</span></span> |
| <span data-ttu-id="cf527-153">Aftengt</span><span class="sxs-lookup"><span data-stu-id="cf527-153">Disconnected</span></span> | <span data-ttu-id="cf527-154">Engin tenging er við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cf527-154">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="cf527-155">Hægt er að kveikja á tengingunni úr LCS, eins og lýst er fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="cf527-155">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="cf527-156">Nr</span><span class="sxs-lookup"><span data-stu-id="cf527-156">No</span></span> |
| <span data-ttu-id="cf527-157">Aftengir</span><span class="sxs-lookup"><span data-stu-id="cf527-157">Disabling connection</span></span> | <span data-ttu-id="cf527-158">Nú stendur yfir beiðni um að slökkva á tengingunni við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cf527-158">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="cf527-159">Nr</span><span class="sxs-lookup"><span data-stu-id="cf527-159">No</span></span> |
| <span data-ttu-id="cf527-160">Sækir stöðu</span><span class="sxs-lookup"><span data-stu-id="cf527-160">Getting status</span></span> | <span data-ttu-id="cf527-161">Kerfið bíður eftir stöðuupplýsingum úr þjónustunni fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cf527-161">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="cf527-162">Nr</span><span class="sxs-lookup"><span data-stu-id="cf527-162">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="cf527-163">Valkosturinn Nota fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="cf527-163">The Use Planning Optimization option</span></span>

<span data-ttu-id="cf527-164">Stilling á valkostinum **Nota fínstillingu skipulags** ákvarðar hvaða áætlunarvél er notuð við aðaláætlanagerð:</span><span class="sxs-lookup"><span data-stu-id="cf527-164">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="cf527-165">**Já** - Fínstilling skipulags er notuð við aðaláætlungargerð.</span><span class="sxs-lookup"><span data-stu-id="cf527-165">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="cf527-166">**Nei** - Innbyggða áætlunarvélin Supply Chain Management er notuð til aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="cf527-166">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="cf527-167">Ef fyrirliggjandi runuvinnslur áætlunargerðar sem voru stofnuð fyrir innbyggðu áætlunarvélina Supply Chain Management eru sett af stað á meðan valkosturinn **Nota fínstillingu skipulagningar** er stilltur á **Já** munu þær vinnslur ekki takast.</span><span class="sxs-lookup"><span data-stu-id="cf527-167">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="cf527-168">Samþætting við uppsetninguna</span><span class="sxs-lookup"><span data-stu-id="cf527-168">Integration with the setup</span></span>

<span data-ttu-id="cf527-169">Ef kveikt er á forskoðun fínstillingar skipulags er aðaláætlunargerð gerð með því að nota viðbótaráætlun fyrir fínstillingu skipulags.</span><span class="sxs-lookup"><span data-stu-id="cf527-169">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="cf527-170">Í þessu tilfelli verða niðurstöður og eiginleikar aðaláætlunargerðar fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="cf527-170">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf527-171">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cf527-171">Additional resources</span></span>

[<span data-ttu-id="cf527-172">Ákvæði og skilmálar fyrir forskoðunina</span><span class="sxs-lookup"><span data-stu-id="cf527-172">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="cf527-173">Yfirlit yfir fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="cf527-173">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="cf527-174">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="cf527-174">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="cf527-175">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="cf527-175">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="cf527-176">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="cf527-176">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="cf527-177">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="cf527-177">Cancel a planning job</span></span>](cancel-planning-job.md)
