---
title: Villustjórnun
description: Þetta efni skýrir villustjórnun í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 72d6c8d750a5a0903017b4c77b3ce5d9521cf99b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430236"
---
# <a name="fault-management"></a><span data-ttu-id="40f2a-103">Villustjórnun</span><span class="sxs-lookup"><span data-stu-id="40f2a-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="40f2a-104">Í eignastjórnun geturðu notað villuhönnuðinn til að setja upp bilunareinkenni, bilunarsvæði og bilunargerðir á eignategundum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="40f2a-105">Á þennan hátt geturðu stjórnað göllum sem eru greindar á eignum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="40f2a-106">Að auki er hægt að skrá bilunarástæður og ábendingar til að laga bilanir í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="40f2a-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="40f2a-107">Ferlið til skráningar og stjórnunar á villum samanstendur af þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="40f2a-108">Búðu til lista yfir bilunareinkenni, bilunarsvæði og bilunargerðir sem gætu komið fram á eignagerðum þínum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="40f2a-109">Settu upp einkenni, bilunarsvæði og villugerðir hjá bilunarhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="40f2a-110">Hér eru nokkur dæmi til að hjálpa þér að skilja muninn á bilunareinkennum, bilunarsvæðum og bilunargerðum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="40f2a-111">**Einkenni bilana:**</span><span class="sxs-lookup"><span data-stu-id="40f2a-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="40f2a-112">Ójafnvægisspenna</span><span class="sxs-lookup"><span data-stu-id="40f2a-112">Unbalanced voltages</span></span>
- <span data-ttu-id="40f2a-113">Skammhlaup</span><span class="sxs-lookup"><span data-stu-id="40f2a-113">Short circuit</span></span>
- <span data-ttu-id="40f2a-114">Hávaði</span><span class="sxs-lookup"><span data-stu-id="40f2a-114">Noise</span></span>
- <span data-ttu-id="40f2a-115">Leki</span><span class="sxs-lookup"><span data-stu-id="40f2a-115">Leak</span></span>
- <span data-ttu-id="40f2a-116">Titringur</span><span class="sxs-lookup"><span data-stu-id="40f2a-116">Vibrations</span></span>

<span data-ttu-id="40f2a-117">**Bilunarsvæði:**</span><span class="sxs-lookup"><span data-stu-id="40f2a-117">**Fault areas:**</span></span>

- <span data-ttu-id="40f2a-118">Rafmagns</span><span class="sxs-lookup"><span data-stu-id="40f2a-118">Electrical</span></span>
- <span data-ttu-id="40f2a-119">Vélrænn</span><span class="sxs-lookup"><span data-stu-id="40f2a-119">Mechanical</span></span>
- <span data-ttu-id="40f2a-120">Vökvakerfi</span><span class="sxs-lookup"><span data-stu-id="40f2a-120">Hydraulic</span></span>
- <span data-ttu-id="40f2a-121">Loftknúið</span><span class="sxs-lookup"><span data-stu-id="40f2a-121">Pneumatic</span></span>

<span data-ttu-id="40f2a-122">**Gerðir bilana:**</span><span class="sxs-lookup"><span data-stu-id="40f2a-122">**Fault types:**</span></span>

- <span data-ttu-id="40f2a-123">Gallað aðalsáturvaf</span><span class="sxs-lookup"><span data-stu-id="40f2a-123">Faulty main stator winding</span></span>
- <span data-ttu-id="40f2a-124">Gölluð díóða</span><span class="sxs-lookup"><span data-stu-id="40f2a-124">Faulty diode</span></span>
- <span data-ttu-id="40f2a-125">Óhreint vaf</span><span class="sxs-lookup"><span data-stu-id="40f2a-125">Dirty windings</span></span>
- <span data-ttu-id="40f2a-126">Gallaður rafall</span><span class="sxs-lookup"><span data-stu-id="40f2a-126">Defective generator</span></span>
- <span data-ttu-id="40f2a-127">Gallaður skynjari</span><span class="sxs-lookup"><span data-stu-id="40f2a-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="40f2a-128">Stofna bilunareinkenni</span><span class="sxs-lookup"><span data-stu-id="40f2a-128">Create fault symptoms</span></span>

<span data-ttu-id="40f2a-129">Fylgdu þessum skrefum til að búa til lista yfir einkenni sem hægt er að nota í villuhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="40f2a-130">Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunareinkenni**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="40f2a-131">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="40f2a-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="40f2a-132">Í reitinn **Bilunareinkenni** reitinn skal slá inn heiti fyrir bilunareinkennið.</span><span class="sxs-lookup"><span data-stu-id="40f2a-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="40f2a-133">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="40f2a-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="40f2a-134">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="40f2a-135">Stofna bilunarsvæði</span><span class="sxs-lookup"><span data-stu-id="40f2a-135">Create fault areas</span></span>

<span data-ttu-id="40f2a-136">Fylgdu þessum skrefum til að búa til lista yfir svæði eða staðsetningar sem hægt er að nota í villuhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="40f2a-137">Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="40f2a-138">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="40f2a-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="40f2a-139">Í reitinn **Bilunarsvæði** skal slá inn heiti fyrir bilunarsvæðið.</span><span class="sxs-lookup"><span data-stu-id="40f2a-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="40f2a-140">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="40f2a-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="40f2a-141">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="40f2a-142">Stofna biðunargerðir</span><span class="sxs-lookup"><span data-stu-id="40f2a-142">Create fault types</span></span>

<span data-ttu-id="40f2a-143">Fylgdu þessum skrefum til að búa til lista yfir bilunargerðir sem hægt er að nota í villuhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="40f2a-144">Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunargerðir**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="40f2a-145">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="40f2a-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="40f2a-146">Í reitnum **Bilunartegund** skal slá inn heiti á bilunargerð.</span><span class="sxs-lookup"><span data-stu-id="40f2a-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="40f2a-147">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="40f2a-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="40f2a-148">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="40f2a-149">Settu upp bilunarhönnuðinn</span><span class="sxs-lookup"><span data-stu-id="40f2a-149">Set up the fault designer</span></span>

<span data-ttu-id="40f2a-150">Í bilunarhönnuðinum seturðu upp bilunargögn um eignagerðir.</span><span class="sxs-lookup"><span data-stu-id="40f2a-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="40f2a-151">Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunarhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="40f2a-152">Í vinstri glugganum velurðu þá gerð eigna sem á að setja upp bilanaskrá fyrir.</span><span class="sxs-lookup"><span data-stu-id="40f2a-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="40f2a-153">Á flýtiflipanum **Bilunareinkenni** velurðu **Bæta við línu** og síðan bilunareinkenni í reitnum **Bilunareinkenni**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="40f2a-154">Á flýtiflipanum **Bilunarsvæði** velurðu **Bæta við línu** og síðan bilunarsvæði í reitnum **Bilunarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="40f2a-155">Á flýtiflipanum **Bilunartegund** velurðu **Bæta við línu** og síðan bilunartegund í reitnum **Bilunartegund**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="40f2a-156">Til að stofna samsetningar af öllum fyrirliggjandi bilanaeinkennum, -svæðum og -gerðum á fljótlegan hátt fyrir valda eignagerð skaltu velja **Stofna bilanasamsetningar**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="40f2a-157">Þessi aðgerð er gagnleg ef þú hefur bætt við mörgum bilunareinkennum, -svæðum og -gerðum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="40f2a-158">Það er auðveldara að eyða línunum fyrir samsetningar sem ekki eiga við eignagerðina en að búa til nýjar línur handvirkt.</span><span class="sxs-lookup"><span data-stu-id="40f2a-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="40f2a-159">Veldu til að afrita uppsetningu bilanaeinkenna, -svæða og -gerða frá einni eignategund til valinnar eignartegundar **Afrita úr eignategund**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="40f2a-160">Veldu **Vista** til að vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="40f2a-160">Select **Save** to save your changes.</span></span>

![Síða bilunarhönnuðar](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="40f2a-162">Stofna orsakir bilunar</span><span class="sxs-lookup"><span data-stu-id="40f2a-162">Create fault causes</span></span>

<span data-ttu-id="40f2a-163">Fylgdu þessum skrefum til að búa til lista yfir þekktar orsakir bilunar sem hægt er að bæta við vinnupöntun eða viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="40f2a-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="40f2a-164">Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Orsakir bilunar**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="40f2a-165">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="40f2a-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="40f2a-166">Í reitnum **Orsakir bilunar** skal slá inn heiti á orsakir bilunar.</span><span class="sxs-lookup"><span data-stu-id="40f2a-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="40f2a-167">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="40f2a-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="40f2a-168">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="40f2a-169">Búðu til bilunarúrræði</span><span class="sxs-lookup"><span data-stu-id="40f2a-169">Create fault remedies</span></span>

<span data-ttu-id="40f2a-170">Fylgdu þessum skrefum til að búa til lista yfir uppástungur að úrræðum og viðgerðum sem hægt er að bæta við vinnupöntun eða viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="40f2a-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="40f2a-171">Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunarúrræði**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="40f2a-172">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="40f2a-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="40f2a-173">Í reitinn **Bilunarúrræði** skal slá inn heiti fyrir bilunarúrræðið.</span><span class="sxs-lookup"><span data-stu-id="40f2a-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="40f2a-174">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="40f2a-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="40f2a-175">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="40f2a-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="40f2a-176">Þú getur breytt nöfnum á bilanaeinkennum þínum, -svæðum, -gerðum, -orsökum og -úrræðum eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="40f2a-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="40f2a-177">Nafnabreytingarnar endurspeglast sjálfkrafa í tengdum bilaskráningum.</span><span class="sxs-lookup"><span data-stu-id="40f2a-177">The name changes are automatically reflected in the related fault registrations.</span></span>
