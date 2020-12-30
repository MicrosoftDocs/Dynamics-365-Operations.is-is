---
title: Stofna og vinna úr samræmi
description: Þetta efni útskýrir hvernig eigi að framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430597"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="070e7-103">Stofna og vinna úr samræmi</span><span class="sxs-lookup"><span data-stu-id="070e7-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="070e7-104">Þetta efni útskýrir hvernig eigi að framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="070e7-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="070e7-105">Hægt er að keyra þessa skráningu í sýnifyrirtækinu USMF og nota ráðlögð gildi.</span><span class="sxs-lookup"><span data-stu-id="070e7-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="070e7-106">Þetta ferli er yfirleitt framkvæmt af starfsmanni á sviði gæða.</span><span class="sxs-lookup"><span data-stu-id="070e7-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="070e7-107">Sem frumskilyrði skaltu ljúka leiðbeiningunum í [Kanna vörugæði](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="070e7-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="070e7-108">Til að keyra samþykki á ósamkvæmi verður notandi sem keyrir verkskráninguna að hafa „Heiti“ úthlutað á síðunni Notendur.</span><span class="sxs-lookup"><span data-stu-id="070e7-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="070e7-109">Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.</span><span class="sxs-lookup"><span data-stu-id="070e7-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="070e7-110">Velja gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="070e7-110">Select a quality order</span></span>
1. <span data-ttu-id="070e7-111">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastjórnun > Reglubundin verkefni > Gæðastjórnun > Gæðapantanir**.</span><span class="sxs-lookup"><span data-stu-id="070e7-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="070e7-112">Í listaum velurðu gæðapöntunina sem var stofnuð í [Kanna vörugæði](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="070e7-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="070e7-113">Stofna ósamkvæmistilvik</span><span class="sxs-lookup"><span data-stu-id="070e7-113">Create a nonconformance</span></span>
1. <span data-ttu-id="070e7-114">Á aðgerðasvæðinu skal velja **Fyrirspurnir**.</span><span class="sxs-lookup"><span data-stu-id="070e7-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="070e7-115">Veldu **Ósamkvæmnitilvik**.</span><span class="sxs-lookup"><span data-stu-id="070e7-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="070e7-116">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="070e7-116">Select **New**.</span></span>
4. <span data-ttu-id="070e7-117">Í fellivalmyndinni **Gerð vandamáls** velurðu vandamálið sem fannst við skoðunarferlið.</span><span class="sxs-lookup"><span data-stu-id="070e7-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="070e7-118">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="070e7-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="070e7-119">Samþykkja/hafna ósamkvæmistilviki</span><span class="sxs-lookup"><span data-stu-id="070e7-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="070e7-120">Veljið **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="070e7-120">Select **Functions**.</span></span>
2. <span data-ttu-id="070e7-121">Veldu **Samþykkja ósamkvæmni**.</span><span class="sxs-lookup"><span data-stu-id="070e7-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="070e7-122">Í þessu dæmi samþykkirðu ósamkvæmina.</span><span class="sxs-lookup"><span data-stu-id="070e7-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="070e7-123">Hægt er að tengja samþykkta ósamkvæmi tengdri virkni til að skrá vinnu sem er lokið sem hluti af afgreiðslu ósamkvæmi og, eins og í þessu efni, vinnslu á afgreiðslu leiðréttinga.</span><span class="sxs-lookup"><span data-stu-id="070e7-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="070e7-124">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="070e7-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="070e7-125">Stofna leiðréttingaraðgerð</span><span class="sxs-lookup"><span data-stu-id="070e7-125">Create a correction action</span></span>
1. <span data-ttu-id="070e7-126">Veldu **Leiðréttingar**.</span><span class="sxs-lookup"><span data-stu-id="070e7-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="070e7-127">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="070e7-127">Select **New**.</span></span>
3. <span data-ttu-id="070e7-128">Í reitnum **Númer starfsmanns** í nýju línunni velurðu skrána sem óskað er eftir af fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="070e7-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="070e7-129">Smellið á **Velja**.</span><span class="sxs-lookup"><span data-stu-id="070e7-129">Click **Select**.</span></span>
5. <span data-ttu-id="070e7-130">Veldu **Hengja við**.</span><span class="sxs-lookup"><span data-stu-id="070e7-130">Select **Attach**.</span></span> <span data-ttu-id="070e7-131">Stofna athugasemd um leiðréttinguna.</span><span class="sxs-lookup"><span data-stu-id="070e7-131">Create a note about the correction.</span></span> <span data-ttu-id="070e7-132">Fyrir þetta dæmi er aðgerð að hafa samband við lánardrottininn til að ræða ósamkvæmitilvikið.</span><span class="sxs-lookup"><span data-stu-id="070e7-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="070e7-133">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="070e7-133">Select **New**.</span></span>
7. <span data-ttu-id="070e7-134">Veljið **Athugasemd**.</span><span class="sxs-lookup"><span data-stu-id="070e7-134">Select **Note**.</span></span> <span data-ttu-id="070e7-135">Eftir því hvernig uppsetning skýrslunnar er, hægt er að prenta mismunandi skjalategundir á skýrslum sem eru tengdar stjórnun á ósamkvæmi.</span><span class="sxs-lookup"><span data-stu-id="070e7-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="070e7-136">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="070e7-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="070e7-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="070e7-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="070e7-138">Viðhalda leiðréttingu</span><span class="sxs-lookup"><span data-stu-id="070e7-138">Maintain a correction</span></span>
1. <span data-ttu-id="070e7-139">Velja **Merka sem lokið**.</span><span class="sxs-lookup"><span data-stu-id="070e7-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="070e7-140">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="070e7-140">Select **OK**.</span></span>
3. <span data-ttu-id="070e7-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="070e7-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="070e7-142">Loka ósamkvæmistilviki</span><span class="sxs-lookup"><span data-stu-id="070e7-142">Close a nonconformance</span></span>
1. <span data-ttu-id="070e7-143">Veljið **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="070e7-143">Select **Functions**.</span></span>
2. <span data-ttu-id="070e7-144">Veldu **Loka ósamkvæmni**.</span><span class="sxs-lookup"><span data-stu-id="070e7-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="070e7-145">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="070e7-145">Select **Yes**.</span></span>
4. <span data-ttu-id="070e7-146">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="070e7-146">Close the pages.</span></span>
