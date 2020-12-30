---
title: Spár, verkbeiðnir og verk
description: Þetta efni útskýrir spár og samþættingu verkbeiðni við verkefnastjórnun og bókhaldseininguna í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9e6d20d1538ea68570d6dcc49da001ad76b8042b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430221"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="ba7b2-103">Spár, verkbeiðnir og verk</span><span class="sxs-lookup"><span data-stu-id="ba7b2-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ba7b2-104">Í eignastjórnun hjálpar samþætting við eininguna **Verkefnisstjórnun og bókhald** við að hámarka kostnaðareftirlit, svo að notendur geta fylgst með kostnaði við spár um gerð viðhaldsverka og verkbeiðnivinnslur.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-104">In Asset Management, integration with the **Project management and accounting** module helps optimize cost control, so that users can track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="ba7b2-105">Rakning á spám um gerðir viðhaldsverka krefst tveggja stillinga:</span><span class="sxs-lookup"><span data-stu-id="ba7b2-105">Tracking of maintenance job type forecasts requires two settings:</span></span>

1. <span data-ttu-id="ba7b2-106">Veldu verkefni í **Eignastýring** > **Uppsetning** > **Breytur eignastýringar**, og síðan á flipanum **Eignir** > á flýtiflipanum **Verkefni**, í reitnum **Verkefni viðhaldsspá**, veldu verkefni.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-106">Select a project in **Asset management** > **Setup** > **Asset management parameters**, and then, on the **Assets** tab > on the **Project** FastTab, in the **Maintenance forecast project** field, select a project.</span></span>

2. <span data-ttu-id="ba7b2-107">Þegar þú stofnar sjálfgefna línu gerðar viðhaldsstarfs er aðgerðarnúmer sjálfkrafa stofnað fyrir línuna á síðunni **Sjálfgefin tegund viðhaldsverka** (**Eignastjórnun** > **Uppsenting** > **Vinnslur** > **Sjálfgefnar gerðir viðhaldsverka**).</span><span class="sxs-lookup"><span data-stu-id="ba7b2-107">When you create a maintenance job type default line, an activity number is automatically created for the line on the **Maintenance job type defaults** page (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="ba7b2-108">Spár um gerðir viðhaldsverka þjóna tvennum tilgangi:</span><span class="sxs-lookup"><span data-stu-id="ba7b2-108">Maintenance job type forecasts serve two purposes:</span></span> 

- <span data-ttu-id="ba7b2-109">Þú getur fylgst með kostnaði við spár um gerðir viðhaldsverka í einingunni **Verkefnisstjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-109">You can track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> 
- <span data-ttu-id="ba7b2-110">Spár eru færðar sjálfkrafa yfir í verkbeiðnaverkefni þegar þú velur tegund viðhalds í verkbeiðnivinnslu.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-110">Forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="ba7b2-111">Til að fylgjast með kostnaði við verkbeiðnavinnslur verður þú fyrst að setja upp verkbeiðnaverkefni.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-111">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="ba7b2-112">Frekari upplýsingar eru í [Verkuppsetning verkbeiðni](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ba7b2-112">For more information, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="ba7b2-113">Verkbeiðnaverkefni</span><span class="sxs-lookup"><span data-stu-id="ba7b2-113">Work order job projects</span></span>

<span data-ttu-id="ba7b2-114">Þegar þú býrð til verkbeiðnivinnslu í verkbeiðni ræðst verkbeiðniverkefnið af uppsetningu foreldraverkefnis fyrir verkbeiðnir á síðunni **Verkuppsetning verkbeiðni** (**Eignastjórnun** > **Uppsetning** > **Verkbeiðni** > **Uppsetning verkefnis**).</span><span class="sxs-lookup"><span data-stu-id="ba7b2-114">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders on the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>

<span data-ttu-id="ba7b2-115">Verkbeiðnaverkefni eru mynduð með því að nota samsetningu af eftirfarandi upplýsingum um verkbeiðni:</span><span class="sxs-lookup"><span data-stu-id="ba7b2-115">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="ba7b2-116">Verkbeiðnigerðin sem valin var í verkbeiðninni</span><span class="sxs-lookup"><span data-stu-id="ba7b2-116">The work order type selected on the work order</span></span> 
- <span data-ttu-id="ba7b2-117">Virk staðsetning sem tengist eigninni í verkpöntunarvinnslunni</span><span class="sxs-lookup"><span data-stu-id="ba7b2-117">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="ba7b2-118">Eignagerðin sem tengist eigninni í verkpöntunarvinnslunni</span><span class="sxs-lookup"><span data-stu-id="ba7b2-118">The asset type that is related to the asset on the work order job</span></span>  
- <span data-ttu-id="ba7b2-119">Áætlaðir upphafs- og lokatímar sem eru stilltir í verkbeiðninni</span><span class="sxs-lookup"><span data-stu-id="ba7b2-119">The expected start and end times that are set on the work order</span></span>  

<span data-ttu-id="ba7b2-120">Sumar þessara upplýsinga er hugsanlega ekki að finna í vinnupöntun.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-120">Some of this information might not be found on a work order.</span></span> <span data-ttu-id="ba7b2-121">Þess vegna er leitin að yfirverki verkbeiðni gerð með því að nota fyrirliggjandi samsetningu gagna og velja verkefnisauðkenni sem samsvarar gögnum um verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-121">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds to work order data.</span></span>

<span data-ttu-id="ba7b2-122">Til dæmis, á eftirfarandi mynd, vegna þess hvernig eignategundin **Vörubíll vél** er sett upp, verður hver vinnupöntunarvinna sem er búin til með eignategundinni **Vörubíll vél** að vera undirverkefni verkefnis ID 000186.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-122">For example, in the following illustration, because of the way that the **Truck Engine** asset type is set up, every work order job that is created with the **Truck Engine** asset type will be a sub-project of project ID 000186.</span></span>

![Mynd 1](media/01-integration-to-pma.png)

<span data-ttu-id="ba7b2-124">Tilgangurinn með auðkenni verkefnisins í vinnupöntunarstörfinu, og tilheyrandi athafnanúmeri, er að rekja kostnað sem er tengdur vinnu pöntunarstarfinu og eigninni sem er valin á það, í einingunni **Verkefnisstjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-124">The purpose of the project ID on the work order job, and the related activity number, is to track costs that are related to the work order job, and the asset that is selected on it, in the **Project management and accounting** module.</span></span> <span data-ttu-id="ba7b2-125">(Til að skoða auðkenni verkefnisins og aðgerðarnúmerið, veldu **Eignastýring** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** og veldu síðan verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-125">(To view the project ID and activity number, select **Asset management** > **Common** > **Work orders** > **All work orders**, and then select the work order.</span></span> <span data-ttu-id="ba7b2-126">Á flýtiflipanum **Línulýsing** sýnir reiturinn **Verkkenni** auðkenni verksins og reiturinn **Aðgerðarnúmer** sýnir númer aðgerðar.) Sjá frekari upplýsingar um kostnaðarstýringu í eignastýringu [Stjórnun kostnaðar og dagsetningar](../controlling-and-reporting/cost-and-date-control.md).</span><span class="sxs-lookup"><span data-stu-id="ba7b2-126">On the **Line details** FastTab, the **Project ID** field shows the project ID, and the **Activity number** field shows the activity number.) For more information about cost control in Asset Management, see [Cost and date control](../controlling-and-reporting/cost-and-date-control.md).</span></span>

<span data-ttu-id="ba7b2-127">Eftirfarandi mynd sýnir myndrænt yfirlit yfir verkbeiðniverk og skyldar aðgerðir verkefnis.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-127">The following illustration shows a graphical overview of work order projects and related project activities.</span></span>

![Mynd 2](media/02-integration-to-pma.png)

<span data-ttu-id="ba7b2-129">Þegar ný verkbeiðnivinnsla er mynduð í verkbeiðni er verkbeiðniverk sjálfkrafa búið til fyrir vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-129">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="ba7b2-130">Fjárhagslegar víddir eignarinnar sem tengjast vinnslu á verkbeiðni eru sjálfkrafa fluttar yfir í verkbeiðniverkið.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-130">The financial dimensions for the asset that is related to the work order job are automatically transferred to the work order project.</span></span>

<span data-ttu-id="ba7b2-131">Verkefnastarfsemin sem er búin til vegna vinnslu á verkbeiðni hefur tengdar upplýsingar sem fylgja henni.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-131">The project activity that is created for a work order job has related information attached to it.</span></span> <span data-ttu-id="ba7b2-132">Þessar upplýsingar snúast um gerð viðhaldsverka, gerðarafbrigði viðhaldsverka og viðskipti.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-132">This information is about the maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="ba7b2-133">Þau eru gagnleg ef þú býrð til dæmis til innkaupapöntun úr verkbeiðni (sjá [Innkaup](../work-orders/procurement.md)), eða ef þú notar eininguna **Verkefnisstjórnun og bókhald** fyrir tímaskráningu.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-133">It's useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>

<span data-ttu-id="ba7b2-134">Ef eignin var sett upp á virkri staðsetningu en er seinna sett upp á annarri virkri staðsetningu, eru fjárhagsvíddir sem tengjast nýju virku staðsetningunni sjálfkrafa uppfærðar á eigninni.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-134">If the asset was installed on a functional location but is later installed on a different functional location, the financial dimensions that are related to the new functional location are automatically updated on the asset.</span></span> <span data-ttu-id="ba7b2-135">Síðan, þegar þú býrð til verkbeiðnivinnslu fyrir eignina fær verkbeiðniverkið fyrir verkbeiðnivinnsluna sjálfkrafa fjárhagsvíddirnar sem nú tengjast eigninni.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-135">Then, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="ba7b2-136">Þar af leiðandi, þegar þú notar virkar staðsetningar er alltaf hægt að rekja kostnað á virkum staðsetningum þar sem eign var sett upp á hverjum tíma.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-136">Therefore, when you use functional locations, costs can always be tracked on the functional locations that an asset was installed on at any given time.</span></span> <span data-ttu-id="ba7b2-137">Sjálfvirk uppfærsla fjárhagsvídda tryggir fullkominn rekjanleika kostnaðar við stjórnun og skýrslugerð verkefna.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-137">The automatic update of financial dimensions helps guarantee complete traceability of costs for project control and reporting.</span></span>

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="ba7b2-138">Verkbeiðniverk, líftímastöður verkbeiðnil, verkþrep og gerðir verka</span><span class="sxs-lookup"><span data-stu-id="ba7b2-138">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="ba7b2-139">Til að tryggja að líftímastöður verkbeiðna og tengdra verkstiga á verkbeiðnum séu notaðar rétt skaltu íhuga tengsl varðandi við eininguna **Verkefnisstjórnun og bókhald**:</span><span class="sxs-lookup"><span data-stu-id="ba7b2-139">To help guarantee that work order lifecycle states and related project stages on work orders are used correctly, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="ba7b2-140">Í einingunni **Verkefnisstjórnun og bókhald** eru verkstig sett upp á verkgerðum á síðunni **Færibreytum verkefnisstjórnunar og bókhalds**.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-140">In the **Project management and accounting** module, project stages are set up on project types on the **Project management and accounting parameters** page.</span></span>  
- <span data-ttu-id="ba7b2-141">Á síðunni **Færibreytur verkefnisstjórnunar og bókhalds** notarðu gátreitina til að velja viðeigandi verkgerðirnar fyrir allar verkgerðirnar sem þú ætlar að nota.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-141">On the **Project management and accounting parameters** page, use the check boxes to select relevant project stages for all the project types that you will use.</span></span> <span data-ttu-id="ba7b2-142">Á eftirfarandi myndum hafa fimm stig (**Stofnað**, **Áætlað**, **Tímaáætlað**, **Í ferli** og **Lokið**) verið valin fyrir verkgerðirnar **Tími og efni** og **Innra**.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-142">In the following illustrations, five stages (**Created**, **Estimated**, **Scheduled**, **In process**, and **Finished**) have been selected for the **Time and material** and **Internal** project types.</span></span> <span data-ttu-id="ba7b2-143">Þessi fimm stig eru mikilvæg bæði fyrir vinnslur innra viðhaldsvinnlsa og viðhaldsþjónustu.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-143">Those five stages are relevant to both internal maintenance jobs and service maintenance jobs.</span></span>
- <span data-ttu-id="ba7b2-144">Í einingunni **Eignastýring** eru verkefnategundir skilgreindar af verkefnahópunum sem þú settir upp á síðunni **Uppsetning vinnuverkefna** > **Verkefnahópur** flipanum (**Eignastýring** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verkefnis**).</span><span class="sxs-lookup"><span data-stu-id="ba7b2-144">In the **Asset Management** module, project types are defined by the project groups that you set up on the **Work order project setup** page > **Project group** tab (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  
- <span data-ttu-id="ba7b2-145">Verkhóparnir sem eru settir upp á síðunni **Uppsetning verkbeiðniverks** eru notaðir þegar þú býrð til verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-145">The project groups that are set up on the **Work order project setup** page are used when you create work orders.</span></span> <span data-ttu-id="ba7b2-146">Þegar verkbeiðni er stofnuð er verkbeiðniverk sjálfkrafa búið til fyrir verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-146">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="ba7b2-147">Í hvert skipti sem líftímastaða verkbeiðni verða að hafa tengt verkefnastig.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-147">Every work order lifecycle state must have a related project stage.</span></span>  
- <span data-ttu-id="ba7b2-148">Verkstigið sem tengist líftímastöðu verkbeiðni verður að skilgreina sem virkt stig fyrir verkhópinn sem er skilgreindur í verkbeiðniverkinu.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-148">The project stage that is related to a work order lifecycle state must be defined as an active stage for the project group that is defined in the work order project.</span></span> <span data-ttu-id="ba7b2-149">Verk verkbeiðninnar er sjálfkrafa myndað í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-149">The work order project is automatically created on a work order.</span></span>
- <span data-ttu-id="ba7b2-150">Þegar þú býrð til nýja verkbeiðni er sjálfvirk úthlutun á verkbeiðniverki byggð á uppsetningunni á síðunni **Verkuppsetning verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-150">When you create a new work order, the automatic allocation of a work order project is based on the setup on the **Work order project setup** page.</span></span>  

<span data-ttu-id="ba7b2-151">Eftirfarandi myndir sýna tengingar milli verkhópa í verkbeiðni, tengdar verkgerðir, verkstig og líftímastöður verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-151">The following illustrations show the associations between work order project groups, related project types, project stages, and work order lifecycle states.</span></span>

![Mynd 3](media/03-integration-to-pma.png)

![Mynd 4](media/04-integration-to-pma.png)

![Mynd 5](media/05-integration-to-pma.png)

<span data-ttu-id="ba7b2-155">Nánari upplýsingar um hvernig setja skal upp verk verkbeiðna er að finna í [Verkuppsetning verkbeiðni](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ba7b2-155">For information about how to set up work order projects, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span> <span data-ttu-id="ba7b2-156">Upplýsingar um hvernig skal stofna líftímastöður verkbeiðna er að finna í [Líftímastöður verkbeiðna](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="ba7b2-156">For information about how to create work order lifecycle states, see [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md).</span></span>

<span data-ttu-id="ba7b2-157">Eftirfarandi mynd sýnir myndrænt yfirlit yfir hin ýmsu verkefni sem eru búin til í einingunni **Eignastýring** til að gera samþættingu við eininguna **Verkefnisstjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-157">The following illustration shows a graphical overview of the various projects that are created in the **Asset management** module to enable integration with the **Project management and accounting** module.</span></span> <span data-ttu-id="ba7b2-158">Það sýnir einnig verkferla sem verkefnin tengjast.</span><span class="sxs-lookup"><span data-stu-id="ba7b2-158">It also shows the work processes that the projects are related to.</span></span>

![Mynd 6](media/06-integration-to-pma.png)

