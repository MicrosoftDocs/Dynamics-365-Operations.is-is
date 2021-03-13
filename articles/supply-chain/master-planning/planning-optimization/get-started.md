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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a41f69958d84fb67b7cd8b6b4c7de38da23552f3
ms.sourcegitcommit: 2b76d4443b2867205db156648125a894f395a495
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2021
ms.locfileid: "5091086"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="378b9-103">Hafist handa með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="378b9-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="378b9-104">Eins og hefur [áður verið tilkynnt](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), er á dagskrá að fínstilling skipulagningar takið við af núverandi innbyggðri vél aðaláætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="378b9-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="378b9-105">Ef verið er að nota innbyggða vél aðaláætlanagerðar, ætti að huga að flutningi yfir í fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="378b9-106">Mikilvægt er að hefja flutningsferlið strax vegna þess að aðgerðir þínar kunna að verða fyrir áhrifum þegar úreldingu er framfylgt.</span><span class="sxs-lookup"><span data-stu-id="378b9-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="378b9-107">Til að koma í veg fyrir vandamál í síðustu stundu þegar úreldingu er framfylgt, mælum við eindregið með því að þú ljúkir við flutninginn fyrir 1. desember 2020.</span><span class="sxs-lookup"><span data-stu-id="378b9-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="378b9-108">Sem stendur styður virknin fyrir fínstillingu skipulagningar ekki alla eiginleika sem eru í boði í vél áætlanagerðar sem er byggð inn í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="378b9-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="378b9-109">Þess vegna er mikilvægt að þú metir hvort eiginleikasettið sem nú er fáanlegt í fínstillingu skipulagsins uppfylli kröfur þínar.</span><span class="sxs-lookup"><span data-stu-id="378b9-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="378b9-110">Ekki er kveikt á virkni fyrir fínstillingu skipulagningar að sjálfgefnu sem stendur í Dynamics Lifecycle Services, þannig að þú hefur tækifæri til að meta stöðuna áður en kveikt er á eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="378b9-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="378b9-111">Þú þarft að biðja um undantekningu á flutningi yfir í fínstillingu skipulagningar ef ferli aðaláætlanagerðar felur ekki í sér framleiðslu (áætlaðar framleiðslupantanir sem aðaláætlanagerðin býr til) og þú þarft að nota innbyggða vél aðaláætlanagerðar í útgáfu sem er nýrri en 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="378b9-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="378b9-112">Frá og með útgáfu 10.0.16 verður sýnd villa í umhverfum þegar innbyggð aðaláætlanagerð er keyrð án þess að búa til áætlaðar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="378b9-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="378b9-113">Nota ætti fínstillingu skipulagningar fyrir allar nýjar uppsetningar sem búa ekki til áætlaðar framleiðslupantanir meðan á aðaláætlanagerð stendur.</span><span class="sxs-lookup"><span data-stu-id="378b9-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="378b9-114">Eigendur núverandi umhverfa sem keyra innbyggða vél aðaláætlanagerðar án þess að búa til áætlaðar framleiðslupantanir, fá tölvupóst með upplýsingum um undantekningarferlið.</span><span class="sxs-lookup"><span data-stu-id="378b9-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="378b9-115">Við mælum með því að þú vinnir með samstarfsaðila til að meta og leggja drög að flutningnum yfir í Fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="378b9-116">Áður en þú kveikir á fínstillingu skipulags mælum við eindregið með því að þú metir niðurstöður greiningar á fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="378b9-117">Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="378b9-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="378b9-118">Til ráðstöfunar</span><span class="sxs-lookup"><span data-stu-id="378b9-118">Availability</span></span>

<span data-ttu-id="378b9-119">Fínstilling áætlanagerðar er í boði í eftirfarandi Azure-svæðum: Bandaríkin, Kanada, Evrópa, Bretland og Ástralía og Asíu-Kyrrahafi.</span><span class="sxs-lookup"><span data-stu-id="378b9-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="378b9-120">Ef reynt er að setja upp innbæturnar á öðru svæði birtir LCS skilaboð um að svæðið sé ekki stutt.</span><span class="sxs-lookup"><span data-stu-id="378b9-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="378b9-121">Athugið að fínstilling áætlanagerðar styður ekki uppsetningu á staðnum á Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="378b9-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="378b9-122">Leyfisveiting</span><span class="sxs-lookup"><span data-stu-id="378b9-122">Licensing</span></span>

<span data-ttu-id="378b9-123">Ef þú getur keyrt aðalskipulagningu með því að nota núverandi leyfi þitt þarftu ekki að kaupa viðbótarleyfi til að byrja að nota fínstillingu skipulagsins.</span><span class="sxs-lookup"><span data-stu-id="378b9-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="378b9-124">Setja upp og virkja fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="378b9-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="378b9-125">Til að nota Fínstilling skipulagningar verður að ganga úr skugga um að kerfið sé með allar forkröfur í lagi og virkja svo leyfislykil þess og setja upp Viðbót fyrir Fínstillingu skipulagningar fyrir Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="378b9-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="378b9-126">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="378b9-126">Prerequisites</span></span>

<span data-ttu-id="378b9-127">Áður en viðbót fyri Fínstillingu skipulagningar er settu upp verður eftirfarandi að vera til staðar:</span><span class="sxs-lookup"><span data-stu-id="378b9-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="378b9-128">Nauðsynlegt er að keyra Supply Chain Management á öflugu LCS virkt umhverfi, á stigi 2 eða hærra (ekki OneBox-umhverfi), með Dynamics 365 Supply Chain Management útgáfu 10.0.7 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="378b9-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="378b9-129">Ef reynt er að setja upp viðbótina í OneBox-umhverfi verður uppsetningunni ekki lokið og því verður að hætta við uppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="378b9-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="378b9-130">Kerfið verður að vera sett upp fyrir Power Platform samþættingu.</span><span class="sxs-lookup"><span data-stu-id="378b9-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="378b9-131">Frekari upplýsingar er að finna [Forsendur fyrir uppsetningu viðbóta](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) og [Setja upp innbætur](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span><span class="sxs-lookup"><span data-stu-id="378b9-131">For more information, see [Prerequisites for setting up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) and [Set up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="378b9-132">Virkja leyfi Fínstillingar skipulagningar</span><span class="sxs-lookup"><span data-stu-id="378b9-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="378b9-133">Til að nota Fínstillingu skipulagningar verður að virkja skilgreiningarlykilinn.</span><span class="sxs-lookup"><span data-stu-id="378b9-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="378b9-134">Þannig er það gert:</span><span class="sxs-lookup"><span data-stu-id="378b9-134">To do so:</span></span>

1. <span data-ttu-id="378b9-135">Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="378b9-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="378b9-136">Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.</span><span class="sxs-lookup"><span data-stu-id="378b9-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="378b9-137">Í flipanum **Skilgreiningarlyklar** skal velja gátreitinn fyrir **Fínstilling skipulagningar**.</span><span class="sxs-lookup"><span data-stu-id="378b9-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="378b9-138">Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="378b9-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="378b9-139">Setjið upp innbótina Fínstilling skipulagningar</span><span class="sxs-lookup"><span data-stu-id="378b9-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="378b9-140">Setja verður upp viðbótina frá LCS verkinu og kveikt á virkni fínstillingar skipulagningar úr notendaviðmóti (UI) Supply Chain Management notandaviðmóti.</span><span class="sxs-lookup"><span data-stu-id="378b9-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="378b9-141">Til að setja upp viðbót Fínstillingar skipulagningar:</span><span class="sxs-lookup"><span data-stu-id="378b9-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="378b9-142">Skráðu þig inn á LCS og opnaðu viðkomandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="378b9-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="378b9-143">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="378b9-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="378b9-144">Flettu niður að flýtiflipanum **Umhverfisinnbætur**.</span><span class="sxs-lookup"><span data-stu-id="378b9-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="378b9-145">Veldu **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="378b9-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="378b9-146">Veldu **Fínstillingu skipulagningar**.</span><span class="sxs-lookup"><span data-stu-id="378b9-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="378b9-147">Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="378b9-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="378b9-148">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="378b9-148">Select **Install**.</span></span>
1. <span data-ttu-id="378b9-149">Á flýtiflipanum **Umhverfisviðbætur** ættir þú að sjá að hagræðing skipulags er að setja upp.</span><span class="sxs-lookup"><span data-stu-id="378b9-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="378b9-150">Eftir nokkrar mínútur ætti **Setur upp** að breytast í **Uppsett** (þú gætir þurft að endurnýja síðuna).</span><span class="sxs-lookup"><span data-stu-id="378b9-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="378b9-151">Þegar það er sett upp ertu tilbúinn til að virkja hagræðingu skipulags í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="378b9-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="378b9-152">Aðaltilgangurinn með því að setja upp viðbót fyrir fínstillingu skipulagningar er að tengja þjónustuna og umhverfið.</span><span class="sxs-lookup"><span data-stu-id="378b9-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="378b9-153">Þess vegna þarf að setja viðbótina upp sérstaklega í hverju umhverfi þar sem nota á fínstillingu skipulagningar, óháð því hvaða kóði er fluttur á milli umhverfanna.</span><span class="sxs-lookup"><span data-stu-id="378b9-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="378b9-154">Samþætta Fínstillingu skipulagningar við kerfið</span><span class="sxs-lookup"><span data-stu-id="378b9-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="378b9-155">Til að stilla hvort nota eigi innbótina fínstilling skipulagningara fyrir aðaláætlanagerð, farðu í **Aðaláætlanargerð** \> **Uppsetning** \> **Færibreytur fínstillingar skipulagningar**.</span><span class="sxs-lookup"><span data-stu-id="378b9-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="378b9-156">Staða tengingar</span><span class="sxs-lookup"><span data-stu-id="378b9-156">Connection status</span></span>

<span data-ttu-id="378b9-157">Staða tengingarinnar gefur til kynna núverandi stöðu tengingarinnar milli Supply Chain Management og þjónustunnar Fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="378b9-158">Eftirfarandi tafla sýnir hugsanleg gildi.</span><span class="sxs-lookup"><span data-stu-id="378b9-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="378b9-159">Staða tengingar</span><span class="sxs-lookup"><span data-stu-id="378b9-159">Connection status</span></span> | <span data-ttu-id="378b9-160">Lýsing</span><span class="sxs-lookup"><span data-stu-id="378b9-160">Description</span></span> | <span data-ttu-id="378b9-161">Er hægt að nota fínstillingu skipulagningar?</span><span class="sxs-lookup"><span data-stu-id="378b9-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="378b9-162">Tengt</span><span class="sxs-lookup"><span data-stu-id="378b9-162">Connected</span></span> | <span data-ttu-id="378b9-163">Tengingu hafa verið komið á milli þjónustunnar fínstilling skipulagningar og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="378b9-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="378b9-164">Já</span><span class="sxs-lookup"><span data-stu-id="378b9-164">Yes</span></span> |
| <span data-ttu-id="378b9-165">Tengir</span><span class="sxs-lookup"><span data-stu-id="378b9-165">Enabling connection</span></span> | <span data-ttu-id="378b9-166">Nú stendur yfir beiðni um að kveikja á tengingunni við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="378b9-167">Nr</span><span class="sxs-lookup"><span data-stu-id="378b9-167">No</span></span> |
| <span data-ttu-id="378b9-168">Aftengt</span><span class="sxs-lookup"><span data-stu-id="378b9-168">Disconnected</span></span> | <span data-ttu-id="378b9-169">Engin tenging er við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="378b9-170">Hægt er að kveikja á tengingunni úr LCS, eins og lýst er fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="378b9-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="378b9-171">Nr</span><span class="sxs-lookup"><span data-stu-id="378b9-171">No</span></span> |
| <span data-ttu-id="378b9-172">Aftengir</span><span class="sxs-lookup"><span data-stu-id="378b9-172">Disabling connection</span></span> | <span data-ttu-id="378b9-173">Nú stendur yfir beiðni um að slökkva á tengingunni við þjónustuna fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="378b9-174">Nr</span><span class="sxs-lookup"><span data-stu-id="378b9-174">No</span></span> |
| <span data-ttu-id="378b9-175">Sækir stöðu</span><span class="sxs-lookup"><span data-stu-id="378b9-175">Getting status</span></span> | <span data-ttu-id="378b9-176">Kerfið bíður eftir stöðuupplýsingum úr þjónustunni fínstilling skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="378b9-177">Nr</span><span class="sxs-lookup"><span data-stu-id="378b9-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="378b9-178">Valkosturinn Nota fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="378b9-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="378b9-179">Stilling á valkostinum **Nota fínstillingu skipulags** ákvarðar hvaða áætlunarvél er notuð við aðaláætlanagerð:</span><span class="sxs-lookup"><span data-stu-id="378b9-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="378b9-180">**Já** - Fínstilling skipulags er notuð við aðaláætlungargerð.</span><span class="sxs-lookup"><span data-stu-id="378b9-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="378b9-181">**Nei** - Innbyggða áætlunarvélin Supply Chain Management er notuð til aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="378b9-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="378b9-182">Ef fyrirliggjandi runuvinnslur áætlunargerðar sem voru stofnuð fyrir innbyggðu áætlunarvélina Supply Chain Management eru sett af stað á meðan valkosturinn **Nota fínstillingu skipulagningar** er stilltur á **Já** munu þær vinnslur ekki takast.</span><span class="sxs-lookup"><span data-stu-id="378b9-182">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="378b9-183">Samþætting við uppsetninguna</span><span class="sxs-lookup"><span data-stu-id="378b9-183">Integration with the setup</span></span>

<span data-ttu-id="378b9-184">Ef kveikt er á fínstillingu áætlanagerðar er aðaláætlanagerð lokið með því að nota viðbót fyrir fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="378b9-184">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="378b9-185">Í þessu tilfelli verða niðurstöður og eiginleikar aðaláætlunargerðar fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="378b9-185">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="378b9-186">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="378b9-186">Additional resources</span></span>

[<span data-ttu-id="378b9-187">Ákvæði og skilmálar fyrir forskoðunina</span><span class="sxs-lookup"><span data-stu-id="378b9-187">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="378b9-188">Yfirlit yfir fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="378b9-188">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="378b9-189">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="378b9-189">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="378b9-190">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="378b9-190">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="378b9-191">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="378b9-191">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="378b9-192">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="378b9-192">Cancel a planning job</span></span>](cancel-planning-job.md)
