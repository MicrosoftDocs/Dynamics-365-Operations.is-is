---
title: Fjarlægja kanban-vinnslu úr áætlun
description: Þetta ferli leggur áherslu á fjarlægir í áætluðu kanban-vinnslu úr áætlun með bakfæra staða vinnslu aftur yfir í Ekki áætluð.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4d994be5c6bb1edc6f0fc64494a19a5babf72ae
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571976"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="fd507-103">Fjarlægja kanban-vinnslu úr áætlun</span><span class="sxs-lookup"><span data-stu-id="fd507-103">Remove a kanban job from the schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd507-104">Þetta ferli leggur áherslu á fjarlægir í áætluðu kanban-vinnslu úr áætlun með bakfæra staða vinnslu aftur yfir í Ekki áætluð.</span><span class="sxs-lookup"><span data-stu-id="fd507-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="fd507-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="fd507-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fd507-106">Þetta ferli er ætluð fyrir yfirmaður vinnusals eða framleiðslustjóri.</span><span class="sxs-lookup"><span data-stu-id="fd507-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="fd507-107">Leita í áætluðu kanban-vinnslu</span><span class="sxs-lookup"><span data-stu-id="fd507-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="fd507-108">Fara í Framleiðslustýringar > Kanban > Áætlun kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="fd507-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="fd507-109">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="fd507-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fd507-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="fd507-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fd507-111">Velja vinnuflokkur 1250.</span><span class="sxs-lookup"><span data-stu-id="fd507-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="fd507-112">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="fd507-112">Click Select.</span></span>
5. <span data-ttu-id="fd507-113">Í svæði Birta staða vinnslu, velja "Áætlað".</span><span class="sxs-lookup"><span data-stu-id="fd507-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="fd507-114">Fjarlægja áætlaðar kanban-vinnslu úr áætlun</span><span class="sxs-lookup"><span data-stu-id="fd507-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="fd507-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="fd507-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fd507-116">Veljið vinnslu sem er með stöðuna Áætluð vinnsla, t.d. með vinnsla frá 19 Desember 2012</span><span class="sxs-lookup"><span data-stu-id="fd507-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="fd507-117">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="fd507-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="fd507-118">Smellt er á snúa aftur staða vinnslu.</span><span class="sxs-lookup"><span data-stu-id="fd507-118">Click Revert job status.</span></span>
4. <span data-ttu-id="fd507-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fd507-119">Click OK.</span></span>
    * <span data-ttu-id="fd507-120">Þetta er bakfæra stöðu vinnslunnar úr "Áætlað" í 'Ekki áætluð' og fjarlægja hana úr spjald ferli.</span><span class="sxs-lookup"><span data-stu-id="fd507-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

