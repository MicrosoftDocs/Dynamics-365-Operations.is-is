---
title: Viðhaldsbeiðnir
description: Þetta efni veitir yfirlit um stjórnun viðhaldsbeiðna í eignastjórnun
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dceb179d0a17d8025d88c5945b9571de65c86449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838611"
---
# <a name="maintenance-requests"></a><span data-ttu-id="64084-103">Viðhaldsbeiðnir</span><span class="sxs-lookup"><span data-stu-id="64084-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="64084-104">Viðhaldsbeiðnir eru athugasemdir eða yfirlýsingar sem eru búnar til til að tilkynna stjórnanda eða skipuleggjanda um að eign gæti krafist viðhalds- eða viðgerðarstarfa, en án þess að búa til vinnupöntun.</span><span class="sxs-lookup"><span data-stu-id="64084-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="64084-105">Ef innihald viðhaldsbeiðni er talið gilt, þá er hægt að búa til viðhaldsbeiðni út frá viðhaldsbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="64084-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="64084-106">Hægt er að búa til viðhaldsbeiðnir fyrir hverja eign í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="64084-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="64084-107">Hægt er að búa til ýmsar viðhaldsbeiðnir, allt eftir því hvernig fyrirtæki þitt notar viðhaldsbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="64084-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="64084-108">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="64084-108">Here are some examples:</span></span>

- <span data-ttu-id="64084-109">Viðhaldsbeiðnir</span><span class="sxs-lookup"><span data-stu-id="64084-109">Maintenance requests</span></span>
- <span data-ttu-id="64084-110">Athugasemdir</span><span class="sxs-lookup"><span data-stu-id="64084-110">Notes</span></span>
- <span data-ttu-id="64084-111">Leiðréttingar eða viðbætur</span><span class="sxs-lookup"><span data-stu-id="64084-111">Corrections or enhancements</span></span>
- <span data-ttu-id="64084-112">Fjárfestingar</span><span class="sxs-lookup"><span data-stu-id="64084-112">Investments</span></span>
- <span data-ttu-id="64084-113">Depot viðgerð (þessi tegund er notuð þegar þú færð eignir frá öðrum stað svo þú getir sinnt viðhalds- eða viðgerðarstarfi og þú skilar síðan eigninni eftir að verkinu er lokið.)</span><span class="sxs-lookup"><span data-stu-id="64084-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="64084-114">Skoða viðhaldsbeiðnir</span><span class="sxs-lookup"><span data-stu-id="64084-114">View maintenance requests</span></span>

<span data-ttu-id="64084-115">Veldu til að skoða viðhaldsbeiðnir **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir**, **Virkar viðhaldsbeiðnir**, eða **Beiðnir mínar um viðhald á staðsetningu minni**.</span><span class="sxs-lookup"><span data-stu-id="64084-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="64084-116">Hver listasíða sýnir nokkrar upplýsingar sem tengjast viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Skoða viðhaldsbeiðnir](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="64084-118">Notaðu listasíðuna **Beiðnir mínar um viðhald á staðsetningu minni** til að skoða lista yfir viðhaldsbeiðnir sem innihalda annaðhvort virka staði sem þú ert skyldur sem starfsmaður eða eignir sem eru settar upp á starfrænum stöðum sem þú ert skyldur sem starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="64084-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="64084-119">(Sjá upplýsingar um hvernig á að setja upp starfshætti á viðhaldsstarfsmönnum [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) .)</span><span class="sxs-lookup"><span data-stu-id="64084-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="64084-120">Þrátt fyrir að upplýsingar um viðskiptareikninga séu tiltækar í þjónustustjórnun eigna (utanaðkomandi viðhald) eru þær ekki tiltækar í eignastýringu (innra viðhald).</span><span class="sxs-lookup"><span data-stu-id="64084-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="64084-121">Til að opna smáatriðið yfir plötuna á listasíðunni **Allar viðhaldsbeiðnir** velurðu tengil í hnitalínuyfirlitinu í dálkinum **Viðhaldsbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="64084-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Skoða upplýsingar um viðhaldsbeiðni](media/02-manage-maintenance-requests.png)

<span data-ttu-id="64084-123">Hnapparnir á aðgerðarglugganum eru skipulagðir á flipa.</span><span class="sxs-lookup"><span data-stu-id="64084-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="64084-124">Eftirfarandi tafla lýsir stuttlega hnöppunum sem tengjast eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="64084-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="64084-125">Heiti hnapps</span><span class="sxs-lookup"><span data-stu-id="64084-125">Button name</span></span>                      | <span data-ttu-id="64084-126">Lýsing</span><span class="sxs-lookup"><span data-stu-id="64084-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="64084-127">Breyta</span><span class="sxs-lookup"><span data-stu-id="64084-127">Edit</span></span>                             | <span data-ttu-id="64084-128">Breyta valinni viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="64084-129">Nýjar</span><span class="sxs-lookup"><span data-stu-id="64084-129">New</span></span>                              | <span data-ttu-id="64084-130">Stofna nýja viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="64084-131">Eyða</span><span class="sxs-lookup"><span data-stu-id="64084-131">Delete</span></span>                           | <span data-ttu-id="64084-132">Eyða valinni viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="64084-133">Verkbeiðnihópur</span><span class="sxs-lookup"><span data-stu-id="64084-133">Work order pool</span></span>                  | <span data-ttu-id="64084-134">Tengdu valda viðhaldsbeiðni við verkbeiðnasafn.</span><span class="sxs-lookup"><span data-stu-id="64084-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="64084-135">Verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="64084-135">Work order</span></span>                       | <span data-ttu-id="64084-136">Stofnaðu verkbeiðni byggða á valinni viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="64084-137">Bilun eignar</span><span class="sxs-lookup"><span data-stu-id="64084-137">Asset fault</span></span>                      | <span data-ttu-id="64084-138">Smelltu á **Eignabilanir**, þar sem þú getur búið til bilanaskráningu á valinni viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="64084-139">Verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="64084-139">Work orders</span></span>                      | <span data-ttu-id="64084-140">Sýna lista yfir allar viðhaldsbeiðnir sem tengjast völdum viðhaldsbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="64084-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="64084-141">Uppfæra stöðu viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="64084-141">Update maintenance request state</span></span> | <span data-ttu-id="64084-142">Uppfæra stöðu viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="64084-143">Kladdi líftímastöðu</span><span class="sxs-lookup"><span data-stu-id="64084-143">Lifecycle state log</span></span>              | <span data-ttu-id="64084-144">Skoða kladdaskrá sem sýnir líftímastöður valinnar viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="64084-145">Upplýsingar yfir viðhaldsbeiðnir</span><span class="sxs-lookup"><span data-stu-id="64084-145">Maintenance request details</span></span>      | <span data-ttu-id="64084-146">Prentaðu skýrslu sem sýnir upplýsingar um valda viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="64084-147">Senda lánseign</span><span class="sxs-lookup"><span data-stu-id="64084-147">Send loan asset</span></span>                  | <span data-ttu-id="64084-148">Veldu lánaeign sem ætti að koma tímabundið í staðinn fyrir þá eign sem er valin á valinni viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="64084-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="64084-149">Skila lánseign</span><span class="sxs-lookup"><span data-stu-id="64084-149">Return loan asset</span></span>                | <span data-ttu-id="64084-150">Skráðu lánaeignina sem að henni hafi verið skilað.</span><span class="sxs-lookup"><span data-stu-id="64084-150">Register the loan asset as returned.</span></span> |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]