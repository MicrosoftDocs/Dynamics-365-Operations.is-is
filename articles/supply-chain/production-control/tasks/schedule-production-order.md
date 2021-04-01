---
title: Áætla framleiðslupöntun
description: Þessi verklýsing sýnir hvernig á að raða framleiðslupöntun.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93ec5bd6984dd1a8f970834070fd77873078b3b0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237132"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="fec95-103">Áætla framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="fec95-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fec95-104">Þessi verklýsing sýnir hvernig á að raða framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="fec95-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="fec95-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="fec95-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fec95-106">Þetta er þriðja ferli úr sjö sem útskýrir lífsferil pöntun í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="fec95-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="fec95-107">Áætla framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="fec95-107">Schedule a production order</span></span>
1. <span data-ttu-id="fec95-108">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="fec95-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="fec95-109">Veljið framleiðslupöntun sem hefur stöðuna Áætlað.</span><span class="sxs-lookup"><span data-stu-id="fec95-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="fec95-110">Í Aðgerðarrúðunni er smellt á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="fec95-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="fec95-111">Smella á Áætla verk.</span><span class="sxs-lookup"><span data-stu-id="fec95-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="fec95-112">Færibreytur fyrir röðun eru settar upp á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="fec95-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="fec95-113">Hægt er að setja upp færibreytur fyrir tilteknir notendur eða alla notendur.</span><span class="sxs-lookup"><span data-stu-id="fec95-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="fec95-114">Í reitnum röðunarstefna er valið: „áfram frá deginum í dag“.</span><span class="sxs-lookup"><span data-stu-id="fec95-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="fec95-115">Dagsetning er rituð í reitinn röðunardagsetning.</span><span class="sxs-lookup"><span data-stu-id="fec95-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="fec95-116">Veldu eða hreinsaðu gátreitinn takmörkuð afkastaveita.</span><span class="sxs-lookup"><span data-stu-id="fec95-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="fec95-117">Veldu eða hreinsaðu gátreitinn takmarkað efni.</span><span class="sxs-lookup"><span data-stu-id="fec95-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="fec95-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fec95-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="fec95-119">Skoða niðurstöður röðunar</span><span class="sxs-lookup"><span data-stu-id="fec95-119">View the scheduling results</span></span>
1. <span data-ttu-id="fec95-120">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="fec95-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="fec95-121">Smellt er á Allar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="fec95-121">Click All jobs.</span></span>
    * <span data-ttu-id="fec95-122">Þessi síða sýnir raðaðar vinnslur sem hafa nýlega verið mynduð.</span><span class="sxs-lookup"><span data-stu-id="fec95-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="fec95-123">Útvíkka eða draga saman hlutann röðun.</span><span class="sxs-lookup"><span data-stu-id="fec95-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="fec95-124">Í flýtiflipanum Röðun, er hægt að skoða áætlaða dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="fec95-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="fec95-125">Smellt er á Fyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="fec95-125">Click Inquiries.</span></span>
5. <span data-ttu-id="fec95-126">Smellt er á álag.</span><span class="sxs-lookup"><span data-stu-id="fec95-126">Click Capacity load.</span></span>
    * <span data-ttu-id="fec95-127">síðan álag birtir afkastagetu sem er frátekið með vinnsluröðun, fjölda stunda sem eru nú teknar frá í tilfang, og fjölda stunda sem eftir eru tiltækar fyrir vinnsluröðun á tilföng.</span><span class="sxs-lookup"><span data-stu-id="fec95-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="fec95-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="fec95-128">Close the page.</span></span>
7. <span data-ttu-id="fec95-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="fec95-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]