---
title: Stofna og vinna úr samræmi
description: Notaðu þetta ferli til að framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "336291"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="b6afa-103">Stofna og vinna úr samræmi</span><span class="sxs-lookup"><span data-stu-id="b6afa-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6afa-104">Notaðu þetta ferli til að framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="b6afa-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="b6afa-105">Hægt er að keyra þessa skráningu í sýnifyrirtækinu USMF og nota ráðlögð gildi.</span><span class="sxs-lookup"><span data-stu-id="b6afa-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="b6afa-106">Þetta ferli er yfirleitt framkvæmt af starfsmanni á sviði gæða.</span><span class="sxs-lookup"><span data-stu-id="b6afa-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="b6afa-107">Frumskilyrði er að keyra verkskráninguna ‚Skoða gæði vara‘.</span><span class="sxs-lookup"><span data-stu-id="b6afa-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="b6afa-108">Til að keyra samþykki á ósamkvæmi verður notandi sem keyrir verkskráninguna að hafa „Heiti“ úthlutað á síðunni Notendur.</span><span class="sxs-lookup"><span data-stu-id="b6afa-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="b6afa-109">Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.</span><span class="sxs-lookup"><span data-stu-id="b6afa-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="b6afa-110">Velja gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="b6afa-110">Select a quality order</span></span>
1. <span data-ttu-id="b6afa-111">Fara á Gæðapantanir.</span><span class="sxs-lookup"><span data-stu-id="b6afa-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="b6afa-112">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b6afa-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b6afa-113">Veldu gæðapöntunina sem var stofnuð úr verkskráningunni „Skoða gæði vara“.</span><span class="sxs-lookup"><span data-stu-id="b6afa-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="b6afa-114">Stofna ósamkvæmistilvik</span><span class="sxs-lookup"><span data-stu-id="b6afa-114">Create a nonconformance</span></span>
1. <span data-ttu-id="b6afa-115">Smellt er á Fyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="b6afa-115">Click Inquiries.</span></span>
2. <span data-ttu-id="b6afa-116">Smellt er á Ósamkvæmnistilvik.</span><span class="sxs-lookup"><span data-stu-id="b6afa-116">Click Non conformances.</span></span>
3. <span data-ttu-id="b6afa-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b6afa-117">Click New.</span></span>
4. <span data-ttu-id="b6afa-118">Í reitnum Vandamálagerðir skal smella a fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b6afa-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b6afa-119">Veldu vandamálið sem fannst við eftirlitsferlið.</span><span class="sxs-lookup"><span data-stu-id="b6afa-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="b6afa-120">Í reitnum Vandamálagerðir skal smella a fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b6afa-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b6afa-121">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b6afa-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b6afa-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b6afa-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b6afa-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b6afa-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="b6afa-124">Samþykkja/hafna ósamkvæmistilviki</span><span class="sxs-lookup"><span data-stu-id="b6afa-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="b6afa-125">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="b6afa-125">Click Functions.</span></span>
2. <span data-ttu-id="b6afa-126">Smellt er á Samþykkja ósamkvæmnistilvik.</span><span class="sxs-lookup"><span data-stu-id="b6afa-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="b6afa-127">Í þessu dæmi samþykkirðu ósamkvæmina.</span><span class="sxs-lookup"><span data-stu-id="b6afa-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="b6afa-128">Hægt er að tengja samþykkta ósamkvæmi tengdri virkni til að skrá vinnu sem er lokið sem hluti af afgreiðslu ósamkvæmi og, eins og í þessari verkskráningu, vinnslu á afgreiðslu leiðréttinga.</span><span class="sxs-lookup"><span data-stu-id="b6afa-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="b6afa-129">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="b6afa-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="b6afa-130">Stofna leiðréttingaraðgerð</span><span class="sxs-lookup"><span data-stu-id="b6afa-130">Create a correction action</span></span>
1. <span data-ttu-id="b6afa-131">Smellt er á Leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="b6afa-131">Click Corrections.</span></span>
2. <span data-ttu-id="b6afa-132">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b6afa-132">Click New.</span></span>
3. <span data-ttu-id="b6afa-133">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b6afa-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b6afa-134">Í reitnum Starfsmannanúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b6afa-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b6afa-135">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b6afa-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b6afa-136">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="b6afa-136">Click Select.</span></span>
7. <span data-ttu-id="b6afa-137">Smellt er á Hengja við.</span><span class="sxs-lookup"><span data-stu-id="b6afa-137">Click Attach.</span></span>
    * <span data-ttu-id="b6afa-138">Stofna athugasemd um leiðréttinguna.</span><span class="sxs-lookup"><span data-stu-id="b6afa-138">Create a note about the correction.</span></span> <span data-ttu-id="b6afa-139">Fyrir þetta dæmi er aðgerð að hafa samband við lánardrottininn til að  ræða ósamkvæmitilvikið.</span><span class="sxs-lookup"><span data-stu-id="b6afa-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="b6afa-140">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b6afa-140">Click New.</span></span>
9. <span data-ttu-id="b6afa-141">Smellt er á Athugasemd.</span><span class="sxs-lookup"><span data-stu-id="b6afa-141">Click Note.</span></span>
    * <span data-ttu-id="b6afa-142">Athugaðu að, eftir því hvernig uppsetning skýrslunnar er, hægt er að prenta mismunandi skjalategundir á skýrslum sem eru tengdar stjórnun á ósamkvæmi.</span><span class="sxs-lookup"><span data-stu-id="b6afa-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="b6afa-143">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="b6afa-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="b6afa-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6afa-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="b6afa-145">Viðhalda leiðréttingu</span><span class="sxs-lookup"><span data-stu-id="b6afa-145">Maintain a correction</span></span>
1. <span data-ttu-id="b6afa-146">Smellt er á Merkja sem lokið.</span><span class="sxs-lookup"><span data-stu-id="b6afa-146">Click Mark complete.</span></span>
2. <span data-ttu-id="b6afa-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b6afa-147">Click OK.</span></span>
3. <span data-ttu-id="b6afa-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6afa-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="b6afa-149">Loka ósamkvæmistilviki</span><span class="sxs-lookup"><span data-stu-id="b6afa-149">Close a nonconformance</span></span>
1. <span data-ttu-id="b6afa-150">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="b6afa-150">Click Functions.</span></span>
2. <span data-ttu-id="b6afa-151">Smellt er á Loka ósamkvæmnistilviki.</span><span class="sxs-lookup"><span data-stu-id="b6afa-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="b6afa-152">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="b6afa-152">Click Yes.</span></span>
4. <span data-ttu-id="b6afa-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6afa-153">Close the page.</span></span>
5. <span data-ttu-id="b6afa-154">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6afa-154">Close the page.</span></span>
