--- 
title: "Uppfæra kanban-stöðu"
description: "Þegar kanban er tæmt fyrir mistök eða móttekið kanban þarf að vera tæmt, þarf að uppfæra stöðu kanban."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3c2b5a5fbfc5bd83cc68ffafaa243dac9244c003
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="update-kanban-status"></a><span data-ttu-id="efc91-103">Uppfæra kanban-stöðu</span><span class="sxs-lookup"><span data-stu-id="efc91-103">Update kanban status</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="efc91-104">Þegar kanban er tæmt fyrir mistök eða móttekið kanban þarf að vera tæmt, þarf að uppfæra stöðu kanban.</span><span class="sxs-lookup"><span data-stu-id="efc91-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="efc91-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="efc91-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="efc91-106">Þetta ferli er ætluð fyrir verkstæðisstjóri</span><span class="sxs-lookup"><span data-stu-id="efc91-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="efc91-107">Finna kanban</span><span class="sxs-lookup"><span data-stu-id="efc91-107">Find the kanban.</span></span>
1. <span data-ttu-id="efc91-108">Fara í framleiðslustýringar > Kanban >Kanbans.</span><span class="sxs-lookup"><span data-stu-id="efc91-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="efc91-109">Opna dálkasía stöðu efnismeðhöndlunareiningu.</span><span class="sxs-lookup"><span data-stu-id="efc91-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="efc91-110">Smellið á „Hreinsa“.</span><span class="sxs-lookup"><span data-stu-id="efc91-110">Click Clear.</span></span>
    * <span data-ttu-id="efc91-111">Þetta endurstillir síurnar.</span><span class="sxs-lookup"><span data-stu-id="efc91-111">This resets the filters.</span></span>  
4. <span data-ttu-id="efc91-112">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="efc91-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="efc91-113">Til dæmis, sía á svæðið kortanúmer með gildið ‚000149'.</span><span class="sxs-lookup"><span data-stu-id="efc91-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="efc91-114">Breyta tæmt í Móttekið</span><span class="sxs-lookup"><span data-stu-id="efc91-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="efc91-115">Smella á Bakfæra auða afgreiðslueiningu</span><span class="sxs-lookup"><span data-stu-id="efc91-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="efc91-116">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="efc91-116">Click OK.</span></span>
    * <span data-ttu-id="efc91-117">Athugið að staða Efnismeðhöndlunareiningar er Móttekin.</span><span class="sxs-lookup"><span data-stu-id="efc91-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="efc91-118">Breyta móttekið í Tæmt</span><span class="sxs-lookup"><span data-stu-id="efc91-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="efc91-119">Smella á Tómt kanban</span><span class="sxs-lookup"><span data-stu-id="efc91-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="efc91-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="efc91-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="efc91-121">Athugið að staða Efnismeðhöndlunareiningar er Tæmd</span><span class="sxs-lookup"><span data-stu-id="efc91-121">Notice that the Handling unit status is Emptied.</span></span>  


