---
title: Undirbúa kanban-vinnslu ferlis þegar efni er tiltækt fyrir vinnuflokk
description: Þetta verk leggur áherslu á undirbúning kanban-vinnslu þegar allt efni er tiltækt fyrir vinnuflokkur.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12773cc6d94a34197084c8fe12c90167d4dca62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977764"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="f3d0f-103">Undirbúa kanban-vinnslu ferlis þegar efni er tiltækt fyrir vinnuflokk</span><span class="sxs-lookup"><span data-stu-id="f3d0f-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3d0f-104">Þetta verk leggur áherslu á undirbúning kanban-vinnslu þegar allt efni er tiltækt fyrir vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="f3d0f-105">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f3d0f-106">Þetta verk er ætluð fyrir á starfsmaður á vél.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="f3d0f-107">Fara í Kanban-spjald fyrir vinnslukenni verks</span><span class="sxs-lookup"><span data-stu-id="f3d0f-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="f3d0f-108">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f3d0f-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f3d0f-110">Veljið vinnuflokkur 1250 og smella á í lagi.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="f3d0f-111">Í listanum skal velja línu 4.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="f3d0f-112">Í fyrirtæki sýnigögn Kanban 000329 í röð 4 er fyrsta vinnslan sem er enn ekki lokið enn.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="f3d0f-113">Víxla útvíkkun á liðnum tiltektarlisti.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="f3d0f-114">Staðfestið að birgðastaða sé tiltæk fyrir allar vörur í tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="f3d0f-115">Ef valdar eru margar vinnslur tiltektarlista, sýna tiltektarlisti samtölu allra vara sem þarf fyrir valdar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="f3d0f-116">Smellt er á Undirbúa.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-116">Click Prepare.</span></span>
    * <span data-ttu-id="f3d0f-117">Undirbúningsferli er nú lokið.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-117">The preparation process is now completed.</span></span> <span data-ttu-id="f3d0f-118">Valinn gátreitur fyrir allar línur í tiltektarlistanum tilgreinir birgðastaða er tiltekin.</span><span class="sxs-lookup"><span data-stu-id="f3d0f-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

