---
title: Breyta eftirspurnarspá handvirkt
description: Þessi verklýsing sýnir hvernig á að breyta spá fyrir vöru.
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec1edb861619bae2ae3c211720b55e170b83ec9
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916623"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="33c6f-103">Breyta eftirspurnarspá handvirkt</span><span class="sxs-lookup"><span data-stu-id="33c6f-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33c6f-104">Þessi verklýsing sýnir hvernig á að breyta spá fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="33c6f-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="33c6f-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="33c6f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="33c6f-106">Þessi skrá er ætluð fyrir framleiðslustjóri.</span><span class="sxs-lookup"><span data-stu-id="33c6f-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="33c6f-107">Breyta spá fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="33c6f-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="33c6f-108">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="33c6f-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="33c6f-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="33c6f-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="33c6f-110">Velja vöruna sem ætlunin er að breyta spánni.</span><span class="sxs-lookup"><span data-stu-id="33c6f-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="33c6f-111">Til dæmis er hægt að velja vöru D0001.</span><span class="sxs-lookup"><span data-stu-id="33c6f-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="33c6f-112">Í **Aðgerðarrúðunni** er smellt á **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="33c6f-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="33c6f-113">Smellið á **Eftirspurnarspá**.</span><span class="sxs-lookup"><span data-stu-id="33c6f-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="33c6f-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="33c6f-114">In the list, mark the selected row.</span></span> <span data-ttu-id="33c6f-115">Ef það eru engar spárlínur skal stofna nýja línu með því að smella á Nýtt á slá forrits.</span><span class="sxs-lookup"><span data-stu-id="33c6f-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="33c6f-116">Í reitnum **Sölumagn** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="33c6f-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="33c6f-117">Þetta númer stendur fyrir spáð magn vörunnar.</span><span class="sxs-lookup"><span data-stu-id="33c6f-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="33c6f-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33c6f-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="33c6f-119">Breyta spá í Excel</span><span class="sxs-lookup"><span data-stu-id="33c6f-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="33c6f-120">Smelltu á **Opna** í Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="33c6f-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="33c6f-121">Smelltu á **Breyta eftirspurnarspá** í Excel.</span><span class="sxs-lookup"><span data-stu-id="33c6f-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="33c6f-122">Í Excel, hægt að bæta við, eyða og breyta spárlínum eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="33c6f-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="33c6f-123">Ef ekki er hægt að sjá gögnin í Excel, þarf að skrá sig inn í Microsoft Dynamics 365 for Finance and Operations Enterprise edition, með "Halda mér innskráðum/innskráðri" valkosturinn virk og þarf að treysta gagnatenginarforritið.</span><span class="sxs-lookup"><span data-stu-id="33c6f-123">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

