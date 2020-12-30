---
title: Hefja framleiðslupöntun
description: Þessi verklýsing sýnir hvernig framleiðslupöntun er hafin í vinnslusal.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47915a93151b1adc99ddb4e3facb29bf8db49dd6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430253"
---
# <a name="start-a-production-order"></a><span data-ttu-id="f221e-103">Hefja framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="f221e-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f221e-104">Þessi verklýsing sýnir hvernig framleiðslupöntun er hafin í vinnslusal.</span><span class="sxs-lookup"><span data-stu-id="f221e-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="f221e-105">Tíma- og efnisnotkun er skráð í þessa vinnslu.</span><span class="sxs-lookup"><span data-stu-id="f221e-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="f221e-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="f221e-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f221e-107">Þetta er fimmta ferlið af sjö sem útskýrir lífsferil pöntunar í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="f221e-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="f221e-108">Hefja framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="f221e-108">Start a production order</span></span>
1. <span data-ttu-id="f221e-109">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="f221e-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="f221e-110">Veljið framleiðslupöntun sem hefur stöðuna Losað.</span><span class="sxs-lookup"><span data-stu-id="f221e-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="f221e-111">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f221e-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="f221e-112">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="f221e-112">Click Start.</span></span>
    * <span data-ttu-id="f221e-113">Á þessari síðu er hægt að staðfesta upphaf framleiðslupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="f221e-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="f221e-114">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="f221e-114">Click the General tab.</span></span>
5. <span data-ttu-id="f221e-115">Í af rekstri.</span><span class="sxs-lookup"><span data-stu-id="f221e-115">In the From Oper.</span></span> <span data-ttu-id="f221e-116">Nei.</span><span class="sxs-lookup"><span data-stu-id="f221e-116">No.</span></span> <span data-ttu-id="f221e-117">skal færa inn ‚10‘.</span><span class="sxs-lookup"><span data-stu-id="f221e-117">field, enter '10'.</span></span>
6. <span data-ttu-id="f221e-118">Veljið ‚Alltaf‘ í reitnum Sjálfvirk leiðarnotkun.</span><span class="sxs-lookup"><span data-stu-id="f221e-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="f221e-119">Smellt er á gátreitinn Bóka leiðarspjald núna.</span><span class="sxs-lookup"><span data-stu-id="f221e-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="f221e-120">Veljið ‚Alltaf‘ í reitnum Sjálfvirk uppskriftarnotkun.</span><span class="sxs-lookup"><span data-stu-id="f221e-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="f221e-121">Smellt er í gátreitinn Bóka tiltektarlista núna.</span><span class="sxs-lookup"><span data-stu-id="f221e-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="f221e-122">Smellt er í gátreitinn Prenta tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="f221e-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="f221e-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f221e-123">Click OK.</span></span>
    * <span data-ttu-id="f221e-124">Þetta er prentaði tiltektarlistinn sem sýnir efni sem notað er fyrir framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="f221e-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="f221e-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f221e-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="f221e-126">Sannprófa tiltektarlistann</span><span class="sxs-lookup"><span data-stu-id="f221e-126">Validate the picking list</span></span>
1. <span data-ttu-id="f221e-127">Smellið á „Skoða“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f221e-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="f221e-128">Smellt er á tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="f221e-128">Click Picking list.</span></span>
3. <span data-ttu-id="f221e-129">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f221e-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f221e-130">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f221e-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f221e-131">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="f221e-131">Click Edit.</span></span>
6. <span data-ttu-id="f221e-132">Í reitnum Notkun skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f221e-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="f221e-133">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="f221e-133">Click Post.</span></span>
8. <span data-ttu-id="f221e-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f221e-134">Click OK.</span></span>
    * <span data-ttu-id="f221e-135">Í færslubók tiltektarlista er efni sem er notað í framleiðslupöntuninni bókað.</span><span class="sxs-lookup"><span data-stu-id="f221e-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="f221e-136">Áður en færslubókin er bókuð er hægt að gera leiðréttingar ef munur er á áætluðu magni og raunverulega notuðu magni.</span><span class="sxs-lookup"><span data-stu-id="f221e-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="f221e-137">Smellt er á flipann GridPanel.</span><span class="sxs-lookup"><span data-stu-id="f221e-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="f221e-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f221e-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="f221e-139">Sannprófa færslubók leiðarspjalda</span><span class="sxs-lookup"><span data-stu-id="f221e-139">Verify the route card journal</span></span>
1. <span data-ttu-id="f221e-140">Smellið á „Skoða“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f221e-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="f221e-141">Smellt er á Leiðarspjald.</span><span class="sxs-lookup"><span data-stu-id="f221e-141">Click Route card.</span></span>
3. <span data-ttu-id="f221e-142">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f221e-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f221e-143">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f221e-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f221e-144">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="f221e-144">Click Edit.</span></span>
6. <span data-ttu-id="f221e-145">Í reitnum Vinnustundir skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="f221e-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="f221e-146">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="f221e-146">Click Post.</span></span>
8. <span data-ttu-id="f221e-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f221e-147">Click OK.</span></span>
    * <span data-ttu-id="f221e-148">Í færslubók leiðarspjalda er tími sem er eytt í staðar aðgerðir skráður.</span><span class="sxs-lookup"><span data-stu-id="f221e-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="f221e-149">Einnig er hægt að tilkynna gallað og ógallað magn.</span><span class="sxs-lookup"><span data-stu-id="f221e-149">Good and error quantity can also be reported.</span></span>  
