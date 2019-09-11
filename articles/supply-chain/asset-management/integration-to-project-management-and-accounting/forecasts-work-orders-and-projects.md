---
title: Spár, verkbeiðnir og verk
description: Þetta efni útskýrir spár og samþættingu verkbeiðni við verkefnastjórnun og bókhaldseininguna í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886817"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="a0aee-103">Spár, verkbeiðnir og verk</span><span class="sxs-lookup"><span data-stu-id="a0aee-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a0aee-104">Í eignastjórnun er samþætting við eininguna **Verkefnisstjórnun og bókhald** gerð til að hámarka kostnaðareftirlit, sem gerir notendum kleift að fylgjast með kostnaði við spár um gerð viðhaldsverka og verkbeiðnivinnslur.</span><span class="sxs-lookup"><span data-stu-id="a0aee-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="a0aee-105">Til að rekja spár um gerðir viðhaldsverka verður að gera tvær stillingar:</span><span class="sxs-lookup"><span data-stu-id="a0aee-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="a0aee-106">Veldu verkefni á tenglinum **Eignastýring** > **Uppsetning** > **Færibreytur eignastýringar** > **Eignir** > flýtiflipanum **Verk** > reitnum **Verk viðhaldsspár**.</span><span class="sxs-lookup"><span data-stu-id="a0aee-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="a0aee-107">Í **Sjálfgefnar gerðir viðhaldsverka**, þegar þú býrð til sjálfgefna línu af gerð viðhaldsverks er aðgerðarnúmer sjálfkrafa búið til fyrir línuna (**Eignastýring** > **Uppsetning** > **Vinnslur** > **Sjálfgefnar gerðir viðhaldsverka**).</span><span class="sxs-lookup"><span data-stu-id="a0aee-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="a0aee-108">Spár um gerð viðhaldsverka þjóna tvennum tilgangi: Þú getur fylgst með kostnaði við spár um viðhaldsgerðir í einingunni **Verkefnisstjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="a0aee-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="a0aee-109">Ennfremur eru spár færðar sjálfkrafa yfir í verkbeiðnaverkefni þegar þú velur tegund viðhalds í verkbeiðnivinnslu.</span><span class="sxs-lookup"><span data-stu-id="a0aee-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="a0aee-110">Til að fylgjast með kostnaði við verkbeiðnavinnslur verður þú fyrst að setja upp verkbeiðnaverkefni.</span><span class="sxs-lookup"><span data-stu-id="a0aee-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="a0aee-111">Sjá kaflann [Uppsetning verkbeiðniverka](../setup-for-work-orders/work-order-project-setup.md) fyrir lýsingu á ferlinu.</span><span class="sxs-lookup"><span data-stu-id="a0aee-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="a0aee-112">Verkbeiðnaverkefni</span><span class="sxs-lookup"><span data-stu-id="a0aee-112">Work order job projects</span></span>

<span data-ttu-id="a0aee-113">Þegar þú býrð til verkbeiðnivinnslu í verkbeiðni ræðst verkbeiðniverkefnið af uppsetningu foreldraverkefnis fyrir verkbeiðnir í **Eignastjórnun** > **Uppsetning** > **Verkbeiðni** > **Uppsetning verkefnis**.</span><span class="sxs-lookup"><span data-stu-id="a0aee-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="a0aee-114">Verkbeiðnaverkefni eru mynduð með því að nota samsetningu af eftirfarandi upplýsingum um verkbeiðni:</span><span class="sxs-lookup"><span data-stu-id="a0aee-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="a0aee-115">Verkbeiðnigerðin sem valin var í verkbeiðninni</span><span class="sxs-lookup"><span data-stu-id="a0aee-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="a0aee-116">Virk staðsetning sem tengist eigninni í verkpöntunarvinnslunni</span><span class="sxs-lookup"><span data-stu-id="a0aee-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="a0aee-117">Eignagerð sem tengist eigninni í verkpöntunarvinnslunni</span><span class="sxs-lookup"><span data-stu-id="a0aee-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="a0aee-118">Áætlaður upphafs- og lokatími stilltur á verkbeiðnina</span><span class="sxs-lookup"><span data-stu-id="a0aee-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="a0aee-119">Hugsanlegt er að ekki séu allar upplýsingar sem nefndar eru hér að ofan að finna í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="a0aee-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="a0aee-120">Þess vegna er leitin að yfirverki verkbeiðni gerð með því að nota fyrirliggjandi samsetningu gagna og velja verkefnisauðkenni sem samsvarar gögnum um verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="a0aee-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="a0aee-121">Dæmi: Á myndinni hér að neðan þýðir uppsetning eignategundarinnar „Vél í vörubíl“ að hver verkbeiðnivinnsla sem er mynduð með þá eignagerð verður undirverkefni verkkennis „000186“.</span><span class="sxs-lookup"><span data-stu-id="a0aee-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![Mynd 1](media/01-integration-to-pma.png)

<span data-ttu-id="a0aee-123">Tilgangur verkkennis í verkbeiðnivinnslu og tengt númer verkþáttar (**Eignastjórnun** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** > veldu verkbeiðni í lista > flýtiflipann **Upplýsingar um línu** > reitnum **Verkkenni** og reitnum **Verkþáttanúmer**) er að fylgjast með kostnaði sem tengist verkbeiðnivinnslunni og eigninni sem er valin í verkbeiðnivinnslunni í einingunni **Verkefnisstjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="a0aee-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="a0aee-124">Á myndinni hér að neðan sérðu myndrænt yfirlit yfir verkbeiðniverk og skyldar aðgerðir verkefnis.</span><span class="sxs-lookup"><span data-stu-id="a0aee-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![Mynd 2](media/02-integration-to-pma.png)

<span data-ttu-id="a0aee-126">Þegar ný verkbeiðnivinnsla er mynduð í verkbeiðni er verkbeiðniverk sjálfkrafa búið til fyrir vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="a0aee-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="a0aee-127">Fjárhagslegar víddir eignarinnar sem tengjast vinnslu á verkbeiðni eru sjálfkrafa fluttar yfir í verkbeiðniverkið.</span><span class="sxs-lookup"><span data-stu-id="a0aee-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="a0aee-128">Verkþátturinn sem var stofnaður fyrir vinnslu verkbeiðni er með tengdar upplýsingar í viðhengi varðandi gerð viðhaldsverka, afbrigði af viðhaldsverkum og viðskipti.</span><span class="sxs-lookup"><span data-stu-id="a0aee-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="a0aee-129">Þessi gögn eru gagnleg ef þú býrð til dæmis til innkaupapöntun úr verkbeiðni (sjá [Innkaup](../work-orders/procurement.md)), eða ef þú notar eininguna **Verkefnisstjórnun og bókhald** fyrir tímaskráningu.</span><span class="sxs-lookup"><span data-stu-id="a0aee-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="a0aee-130">Ef eignin var sett upp á virkri staðsetningu og sú eign er seinna sett upp á annarri virkri staðsetningu, eru fjárhagsvíddir sem tengjast nýju virku staðsetningunni sjálfkrafa uppfærðar á eigninni.</span><span class="sxs-lookup"><span data-stu-id="a0aee-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="a0aee-131">Þar af leiðandi, þegar þú býrð til verkbeiðnivinnslu fyrir eignina fær verkbeiðniverkið fyrir verkbeiðnivinnsluna sjálfkrafa fjárhagsvíddirnar sem nú tengjast eigninni.</span><span class="sxs-lookup"><span data-stu-id="a0aee-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="a0aee-132">Þetta þýðir að þegar þú notar virkar staðsetningar er alltaf hægt að rekja kostnað á virkum staðsetningum þar sem eign var sett upp á hverjum tíma.</span><span class="sxs-lookup"><span data-stu-id="a0aee-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="a0aee-133">Sjálfvirk uppfærsla fjárhagsvídda tryggir fullkominn rekjanleika kostnaðar við stjórnun og skýrslugerð verkefna.</span><span class="sxs-lookup"><span data-stu-id="a0aee-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="a0aee-134">Verkbeiðniverk, líftímastöður verkbeiðnil, verkþrep og gerðir verka</span><span class="sxs-lookup"><span data-stu-id="a0aee-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="a0aee-135">Til að tryggja rétta notkun á líftímastöðum verkbeiðna og tengdum verkstigum á verkbeiðnum skaltu íhuga tengsl varðandi við eininguna **Verkefnisstjórnun og bókhald**:</span><span class="sxs-lookup"><span data-stu-id="a0aee-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="a0aee-136">Í einingunni **Verkefnisstjórnun og bókhald** eru verkstig sett upp á verkgerðum í **Færibreytum verkefnisstjórnunar og bókhalds**.</span><span class="sxs-lookup"><span data-stu-id="a0aee-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="a0aee-137">Í **Færibreytum verkefnisstjórnunar og bókhalds** skaltu muna að velja viðeigandi gátreiti verkstigs fyrir allar verkgerðirnar sem þú ætlar að nota.</span><span class="sxs-lookup"><span data-stu-id="a0aee-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="a0aee-138">Á myndinni hér að neðan hafa fimm stig **Stofnað** - **Áætlað** - **Tímaáætlað** - **Í ferli** - **Lokið** verið valin fyrir verkgerðirnar „Tími og efni“ og „Innra“.</span><span class="sxs-lookup"><span data-stu-id="a0aee-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="a0aee-139">Þessi fimm stig eru mikilvæg bæði fyrir vinnslur innra viðhalds og viðhaldsþjónustu.</span><span class="sxs-lookup"><span data-stu-id="a0aee-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="a0aee-140">Í **Eignastjórnun** eru verkgerðir skilgreindar af verkhópunum sem þú settir upp í skjámyndinni **Uppsetning verkbeiðniverks** > tenglinum **Verkflokkur**.</span><span class="sxs-lookup"><span data-stu-id="a0aee-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="a0aee-141">Vkerhóparnir sem eru settir upp í **Uppsetning verkbeiðniverks** eru notaðir þegar þú býrð til verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="a0aee-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="a0aee-142">Þegar verkbeiðni er stofnuð er verkbeiðniverk sjálfkrafa búið til fyrir verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="a0aee-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="a0aee-143">Líftímastöður verkbeiðni verða allar að hafa tengt verkefnastig.</span><span class="sxs-lookup"><span data-stu-id="a0aee-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="a0aee-144">Verkstigið sem tengist líftímastöðu verkbeiðni verður að skilgreina sem virkt stig fyrir verkhópinn sem skilgreindur er í verkbeiðniverkinu.</span><span class="sxs-lookup"><span data-stu-id="a0aee-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="a0aee-145">Verk verkbeiðninnar er sjálfkrafa myndað í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="a0aee-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="a0aee-146">Þegar þú býrð til nýja verkbeiðni er sjálfvirk úthlutun á verkbeiðniverki byggð á uppsetningunni í **Verkuppsetningu verkbeiðni** (**Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verkefnis**).</span><span class="sxs-lookup"><span data-stu-id="a0aee-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="a0aee-147">Tengingar milli verkhópa í verkbeiðni, tengdar verkgerðir, verkstig og líftímastöður verkbeiðna eru sýndar á myndunum hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="a0aee-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![Mynd 3](media/03-integration-to-pma.png)

![Mynd 4](media/04-integration-to-pma.png)

![Mynd 5](media/05-integration-to-pma.png)

<span data-ttu-id="a0aee-151">Sjá [Uppsetning verkbeiðniverka](../setup-for-work-orders/work-order-project-setup.md) varðandi hvernig eigi að setja upp verkbeiðniverk og [Líftímastöður verkbeiðna](../setup-for-work-orders/work-order-lifecycle-states.md) varðandi hvernig eigi að búa til líftímastöður verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="a0aee-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="a0aee-152">Myndin hér að neðan sýnir myndrænt yfirlit yfir hin ýmsu verkefni sem eru búin til í einingunni **Eignastjórnun** til að leyfa samþættingu við eininguna **Verkefnisstjórnun og bókhald**, svo og vinnuferlum sem verkefnin tengjast.</span><span class="sxs-lookup"><span data-stu-id="a0aee-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![Mynd 6](media/06-integration-to-pma.png)

