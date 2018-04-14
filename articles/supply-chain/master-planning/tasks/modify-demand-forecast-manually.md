--- 
title: "Breyta eftirspurnarspá handvirkt"
description: "Þessi verklýsing sýnir hvernig á að breyta spá fyrir vöru."
author: YuyuScheller
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6fd59d3f6c3a5926a2191a89dd682154714c9fa1
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="f9eea-103">Breyta eftirspurnarspá handvirkt</span><span class="sxs-lookup"><span data-stu-id="f9eea-103">Modify a demand forecast manually</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9eea-104">Þessi verklýsing sýnir hvernig á að breyta spá fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="f9eea-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="f9eea-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="f9eea-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f9eea-106">Þessi skrá er ætluð fyrir framleiðslustjóri.</span><span class="sxs-lookup"><span data-stu-id="f9eea-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="f9eea-107">Breyta spá fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="f9eea-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="f9eea-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="f9eea-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f9eea-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f9eea-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f9eea-110">Velja vöruna sem ætlunin er að breyta spánni.</span><span class="sxs-lookup"><span data-stu-id="f9eea-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="f9eea-111">Til dæmis er hægt að velja vöru D0001.</span><span class="sxs-lookup"><span data-stu-id="f9eea-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="f9eea-112">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f9eea-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="f9eea-113">Smellið á „Eftirspurnarspá“.</span><span class="sxs-lookup"><span data-stu-id="f9eea-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="f9eea-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f9eea-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f9eea-115">Ef það eru engar spárlínur skal stofna nýja línu með því að</span><span class="sxs-lookup"><span data-stu-id="f9eea-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="f9eea-116">smella á Nýtt á slá forrits.</span><span class="sxs-lookup"><span data-stu-id="f9eea-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="f9eea-117">Í reitnum sölumagn, skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f9eea-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="f9eea-118">Þetta númer stendur fyrir spáð magn vörunnar.</span><span class="sxs-lookup"><span data-stu-id="f9eea-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="f9eea-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f9eea-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="f9eea-120">Breyta spá í Excel</span><span class="sxs-lookup"><span data-stu-id="f9eea-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="f9eea-121">Smellt er á Opna í Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="f9eea-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="f9eea-122">Smella á Breyta Eftirspurnarspár í Excel.</span><span class="sxs-lookup"><span data-stu-id="f9eea-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="f9eea-123">Í Excel, hægt að bæta við, eyða og breyta spárlínum eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="f9eea-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="f9eea-124">Ef ekki er hægt að sjá gögnin í Excel, þarf að skrá sig inn í Microsoft Dynamics 365 for Finance and Operations með valkostinum "Halda mér innskráðum/innskráðri" virkum og það þarf að treysta á gagnatengingarforritið.</span><span class="sxs-lookup"><span data-stu-id="f9eea-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


