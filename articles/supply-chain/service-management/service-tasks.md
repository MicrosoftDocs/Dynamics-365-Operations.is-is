---
title: Yfirlit yfir þjónustuverk
description: Notið þjónustuverk til að lýsa verkinu sem á að ljúka í þjónustupöntun. Bæði tæknimenn og viðskiptavinir geta séð þessar upplýsingar.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebad3a5fdd65155eb822dcd69a1d2624a1891337
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835823"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="8ee8d-104">Yfirlit yfir þjónustuverk</span><span class="sxs-lookup"><span data-stu-id="8ee8d-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ee8d-105">Notið þjónustuverk til að lýsa verkinu sem á að ljúka í þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="8ee8d-106">Bæði tæknimenn og viðskiptavinir geta séð þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="8ee8d-107">Þjónustuverk eru stofnuð í skjámyndinni **Þjónustuverk** og hægt er að tengja þau við tiltekinn þjónustusamning eða þjónustupöntun með því að stofna þjónustuverkatengsl.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="8ee8d-108">Í hvert skipti sem þjónustuverkatengsl er stofnað er hægt að stofna eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8ee8d-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="8ee8d-109">Innri athugasemdir fyrir verkið, t.d. nákvæmar tæknilegar beiðnir fyrir verkið sem eru nauðsynlegar fyrir tæknimanninn.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="8ee8d-110">Ytri athugasemdir sem viðskiptavinurinn getur séð.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-110">External notes that the customer can see.</span></span> <span data-ttu-id="8ee8d-111">Þær kunna að innihalda almenna útskýringu á verkinu sem verið er að vinna samkvæmt samningi á milli viðskiptavinar og þjónustufyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="8ee8d-112">Um leið og búið er setja upp þjónustuverkatengsl á milli þjónustuverks og þjónustupöntunar eða þjónustusamnings er hægt að tilgreina þetta þjónustuverk þegar stofnaðar eru þjónustupöntunarlínur eða þjónustusamningslínur fyrir opnu þjónustupöntunina eða þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="8ee8d-113">Þegar þjónustupantanir eru stofnaðar úr þjónustusamningi er hægt að nota þjónustuverk sem tengd eru þjónustusamningslínunum til að flokka þjónustupöntunarlínur í þjónustupantanir.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="8ee8d-114">Stofna þjónustuverk</span><span class="sxs-lookup"><span data-stu-id="8ee8d-114">Create a service task</span></span>

1. <span data-ttu-id="8ee8d-115">Smellið á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuverk**.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="8ee8d-116">Stofnið nýja línu.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-116">Create a new line.</span></span>
3. <span data-ttu-id="8ee8d-117">Færið inn kenni þjónustu og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="8ee8d-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8ee8d-118">Example</span></span>

<span data-ttu-id="8ee8d-119">Tæknimaður verður að ljúka tveimur verkum á gírkassa (þjónustuhluti GB-1234) hjá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="8ee8d-120">Þjónustusamningur er stofnaður fyrir viðskiptavininn og nokkrar færslur eru tengdar verkunum.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="8ee8d-121">Þjónustusamningurinn og þjónustusamningslínurnar fyrir verkin tvö eru eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8ee8d-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="8ee8d-122">Þjónustusamningur</span><span class="sxs-lookup"><span data-stu-id="8ee8d-122">Service agreement</span></span>

| <span data-ttu-id="8ee8d-123">Verkefni</span><span class="sxs-lookup"><span data-stu-id="8ee8d-123">Project</span></span> | <span data-ttu-id="8ee8d-124">Þjónustusamningur</span><span class="sxs-lookup"><span data-stu-id="8ee8d-124">Service agreement</span></span> | <span data-ttu-id="8ee8d-125">lýsing</span><span class="sxs-lookup"><span data-stu-id="8ee8d-125">Description</span></span>                                  | <span data-ttu-id="8ee8d-126">Hópur</span><span class="sxs-lookup"><span data-stu-id="8ee8d-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="8ee8d-127">9012</span><span class="sxs-lookup"><span data-stu-id="8ee8d-127">9012</span></span>    | <span data-ttu-id="8ee8d-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="8ee8d-128">000008\_001</span></span>       | <span data-ttu-id="8ee8d-129">Skoðun og reglubundin skipti – GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="8ee8d-130">Bónusgreiðsla</span><span class="sxs-lookup"><span data-stu-id="8ee8d-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="8ee8d-131">Þjónustusamningslínur</span><span class="sxs-lookup"><span data-stu-id="8ee8d-131">Service agreement lines</span></span>

| <span data-ttu-id="8ee8d-132">lýsing</span><span class="sxs-lookup"><span data-stu-id="8ee8d-132">Description</span></span>             | <span data-ttu-id="8ee8d-133">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="8ee8d-133">Transaction type</span></span> | <span data-ttu-id="8ee8d-134">Þjónustuhlutur</span><span class="sxs-lookup"><span data-stu-id="8ee8d-134">Service object</span></span> | <span data-ttu-id="8ee8d-135">Þjónustuverk</span><span class="sxs-lookup"><span data-stu-id="8ee8d-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="8ee8d-136">Skoðun og hreinsun</span><span class="sxs-lookup"><span data-stu-id="8ee8d-136">Inspection and cleaning</span></span> | <span data-ttu-id="8ee8d-137">Vinnustund</span><span class="sxs-lookup"><span data-stu-id="8ee8d-137">Hour</span></span>             | <span data-ttu-id="8ee8d-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-138">GB-1234</span></span>        | <span data-ttu-id="8ee8d-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-139">I/C - GB1234</span></span> |
| <span data-ttu-id="8ee8d-140">Ferðir</span><span class="sxs-lookup"><span data-stu-id="8ee8d-140">Travel</span></span>                  | <span data-ttu-id="8ee8d-141">Expense</span><span class="sxs-lookup"><span data-stu-id="8ee8d-141">Expense</span></span>          | <span data-ttu-id="8ee8d-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-142">GB-1234</span></span>        | <span data-ttu-id="8ee8d-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-143">I/C - GB1234</span></span> |
| <span data-ttu-id="8ee8d-144">Efni</span><span class="sxs-lookup"><span data-stu-id="8ee8d-144">Materials</span></span>               | <span data-ttu-id="8ee8d-145">vara</span><span class="sxs-lookup"><span data-stu-id="8ee8d-145">Item</span></span>             | <span data-ttu-id="8ee8d-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-146">GB-1234</span></span>        | <span data-ttu-id="8ee8d-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-147">I/C - GB1234</span></span> |
| <span data-ttu-id="8ee8d-148">Reglubundin skipti</span><span class="sxs-lookup"><span data-stu-id="8ee8d-148">Routine replacement</span></span>     | <span data-ttu-id="8ee8d-149">Vinnustund</span><span class="sxs-lookup"><span data-stu-id="8ee8d-149">Hour</span></span>             | <span data-ttu-id="8ee8d-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-150">GB-1234</span></span>        | <span data-ttu-id="8ee8d-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-151">RR - GB1234</span></span>  |
| <span data-ttu-id="8ee8d-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="8ee8d-152">GR-1</span></span>                    | <span data-ttu-id="8ee8d-153">vara</span><span class="sxs-lookup"><span data-stu-id="8ee8d-153">Item</span></span>             | <span data-ttu-id="8ee8d-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-154">GB-1234</span></span>        | <span data-ttu-id="8ee8d-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-155">RR - GB1234</span></span>  |
| <span data-ttu-id="8ee8d-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="8ee8d-156">GR-5</span></span>                    | <span data-ttu-id="8ee8d-157">vara</span><span class="sxs-lookup"><span data-stu-id="8ee8d-157">Item</span></span>             | <span data-ttu-id="8ee8d-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-158">GB-1234</span></span>        | <span data-ttu-id="8ee8d-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-159">RR - GB1234</span></span>  |

<span data-ttu-id="8ee8d-160">Tvö þjónustuverk eru tengd þjónustusamningslínunum fyrir verkin tvö.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="8ee8d-161">Þjónustuverkin stjórna færslunum sem tilheyra hvoru verki.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="8ee8d-162">Í fyrsta lagi auðkennir þjónustuverkið I/C - GB1234 allar þjónustusamningslínur sem tengjast skoðun og hreinsun á hlut GB-1234.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="8ee8d-163">Í öðru lagi auðkennir RR - GB1234 allar samningslínur sem tengjast lokum á reglubundnum skiptum.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="8ee8d-164">Þjónustuverkatengslin sem tengja þjónustuverkin við tiltekna samninga eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="8ee8d-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="8ee8d-165">Þjónustuverk</span><span class="sxs-lookup"><span data-stu-id="8ee8d-165">Service tasks</span></span>

| <span data-ttu-id="8ee8d-166">Þjónustuverkliður</span><span class="sxs-lookup"><span data-stu-id="8ee8d-166">Service task</span></span> | <span data-ttu-id="8ee8d-167">Lýsing</span><span class="sxs-lookup"><span data-stu-id="8ee8d-167">Description</span></span>                             | <span data-ttu-id="8ee8d-168">Innri athugasemd</span><span class="sxs-lookup"><span data-stu-id="8ee8d-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="8ee8d-169">Ytri athugasemd</span><span class="sxs-lookup"><span data-stu-id="8ee8d-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="8ee8d-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-170">I/C - GB1234</span></span> | <span data-ttu-id="8ee8d-171">Skoðun á gírkassa GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="8ee8d-172">Sjónræn og vélræn skoðun og hreinsun gírkassa GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="8ee8d-173">Reglubundin skoðun á gírkassa</span><span class="sxs-lookup"><span data-stu-id="8ee8d-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="8ee8d-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-174">RR - GB1234</span></span>  | <span data-ttu-id="8ee8d-175">Reglubundin skipti á hlutum í GB-1234</span><span class="sxs-lookup"><span data-stu-id="8ee8d-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="8ee8d-176">Reglubundin þjónustuskipti á GR-1 og GR-5 íhlutunum (fyrir gírkassa framleidda fyrir 2002, einnig þarf að skipta út GR-2 íhlutnum)</span><span class="sxs-lookup"><span data-stu-id="8ee8d-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="8ee8d-177">Reglubundin skipti á hlutum</span><span class="sxs-lookup"><span data-stu-id="8ee8d-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="8ee8d-178">Þjónustuflokkapöntun</span><span class="sxs-lookup"><span data-stu-id="8ee8d-178">Group service orders</span></span>

<span data-ttu-id="8ee8d-179">Þegar þjónustupantanir eru stofnaðar sjálfvirkt er hægt að nota þjónustuverk sem flokkunarskilyrði.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="8ee8d-180">Til að flokka þjónustupantanir eftir þjónustuverkum þarf að tilgreina í þjónustusamningnum að þjónustupantanir sem eru byggðar á þjónustusamningnum eigi að flokka eftir þjónustuverkskenni sem fyrsta flokkunarskilyrði.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="8ee8d-181">**Flokka eftir þjónustuverki**</span><span class="sxs-lookup"><span data-stu-id="8ee8d-181">**Group by service task**</span></span>

1. <span data-ttu-id="8ee8d-182">Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="8ee8d-183">Í flipanum **Uppsetning** skal velja **Eftir þjónustuverki** í reitnum **Sameina þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]