---
title: Uppfæra kanban-stöðu
description: Þegar kanban er tæmt fyrir mistök eða móttekið kanban þarf að vera tæmt, þarf að uppfæra stöðu kanban.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48dd5c3a878efb7413f461e76fde086030015b60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146676"
---
# <a name="update-kanban-status"></a><span data-ttu-id="52132-103">Uppfæra kanban-stöðu</span><span class="sxs-lookup"><span data-stu-id="52132-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52132-104">Þegar kanban er tæmt fyrir mistök eða móttekið kanban þarf að vera tæmt, þarf að uppfæra stöðu kanban.</span><span class="sxs-lookup"><span data-stu-id="52132-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="52132-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="52132-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="52132-106">Þetta ferli er ætluð fyrir verkstæðisstjóri</span><span class="sxs-lookup"><span data-stu-id="52132-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="52132-107">Finna kanban</span><span class="sxs-lookup"><span data-stu-id="52132-107">Find the kanban.</span></span>
1. <span data-ttu-id="52132-108">Fara í framleiðslustýringar > Kanban >Kanbans.</span><span class="sxs-lookup"><span data-stu-id="52132-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="52132-109">Opna dálkasía stöðu efnismeðhöndlunareiningu.</span><span class="sxs-lookup"><span data-stu-id="52132-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="52132-110">Smellið á „Hreinsa“.</span><span class="sxs-lookup"><span data-stu-id="52132-110">Click Clear.</span></span>
    * <span data-ttu-id="52132-111">Þetta endurstillir síurnar.</span><span class="sxs-lookup"><span data-stu-id="52132-111">This resets the filters.</span></span>  
4. <span data-ttu-id="52132-112">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="52132-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="52132-113">Til dæmis, sía á svæðið kortanúmer með gildið ‚000149'.</span><span class="sxs-lookup"><span data-stu-id="52132-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="52132-114">Breyta tæmt í Móttekið</span><span class="sxs-lookup"><span data-stu-id="52132-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="52132-115">Smella á Bakfæra auða afgreiðslueiningu</span><span class="sxs-lookup"><span data-stu-id="52132-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="52132-116">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52132-116">Click OK.</span></span>
    * <span data-ttu-id="52132-117">Athugið að staða Efnismeðhöndlunareiningar er Móttekin.</span><span class="sxs-lookup"><span data-stu-id="52132-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="52132-118">Breyta móttekið í Tæmt</span><span class="sxs-lookup"><span data-stu-id="52132-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="52132-119">Smella á Tómt kanban</span><span class="sxs-lookup"><span data-stu-id="52132-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="52132-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="52132-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="52132-121">Athugið að staða Efnismeðhöndlunareiningar er Tæmd</span><span class="sxs-lookup"><span data-stu-id="52132-121">Notice that the Handling unit status is Emptied.</span></span>  

