---
title: Biðgeymslusvæði fyrir ósamkvæmi
description: Í þessu efnisatriði er lýst hvernig á að stofna og nota biðgeymslusvæði fyrir ósamkvæmni.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956703"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="15cea-103">Biðgeymslusvæði fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="15cea-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15cea-104">Í þessu efnisatriði er lýst hvernig á að stofna og nota biðgeymslusvæði fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="15cea-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="15cea-105">Skjámyndin **Biðgeymslusvæði** er notuð til að skilgreina svæði sem hægt er að úthluta á ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="15cea-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="15cea-106">Þegar ósamkvæmni er stofnuð er hægt að stilla reitina **Biðgeymslusvæði** og **Gerð biðgeymslu** í flipanum **Almennt** á síðunni **Ósamkvæmni**.</span><span class="sxs-lookup"><span data-stu-id="15cea-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="15cea-107">Reiturinn **Biðgeymslusvæði** tilgreinir yfirleitt svæðið eða staðsetninguna þar sem varan er staðsett.</span><span class="sxs-lookup"><span data-stu-id="15cea-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="15cea-108">Reiturinn **Gerð biðgeymslu** skilgreinir vöruna sem annaðhvort *Takmörkuð notkun* eða *Ónothæf*.</span><span class="sxs-lookup"><span data-stu-id="15cea-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="15cea-109">Þegar skýrsla um ósamkvæmni eða leiðréttingar er prentuð vegna ósamkvæmni, er hægt að skoða biðgeymslusvæðið þar sem varan er staðsett.</span><span class="sxs-lookup"><span data-stu-id="15cea-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="15cea-110">Einnig er hægt að prenta ósamkvæmnismerki fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="15cea-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="15cea-111">Þessi skýrsla sýnir úthlutað biðgeymslusvæði og upplýsingar um notkun til að veita leiðsögn um hvernig gallað efni á að vera meðhöndlað.</span><span class="sxs-lookup"><span data-stu-id="15cea-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="15cea-112">Biðgeymslusvæðin gætu samsvarað birgðastaðsetningum eða rekstrartilföngum.</span><span class="sxs-lookup"><span data-stu-id="15cea-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="15cea-113">Dæmi um biðgeymslusvæði</span><span class="sxs-lookup"><span data-stu-id="15cea-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="15cea-114">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="15cea-114">Example 1</span></span>

<span data-ttu-id="15cea-115">Þú vinnur hjá fyrirtæki sem framleiðir og dreifir raftækjum á borð við sjónvörp, hátalara og margmiðlunarspilara.</span><span class="sxs-lookup"><span data-stu-id="15cea-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="15cea-116">Í þessu tilfelli er hægt að stilla biðgeymslusvæði til að endurspegla hverja vörutegund.</span><span class="sxs-lookup"><span data-stu-id="15cea-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="15cea-117">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="15cea-117">Example 2</span></span>

<span data-ttu-id="15cea-118">Þrjú hólf og tveir rekkar eru notaðir til að geyma vörur sem eru ósamkvæm.</span><span class="sxs-lookup"><span data-stu-id="15cea-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="15cea-119">Í þessu tilfelli er hægt að stilla fimm biðgeymslusvæði, eitt fyrir hvert hólf og hvern rekka.</span><span class="sxs-lookup"><span data-stu-id="15cea-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="15cea-120">Búa til biðgeymslusvæði</span><span class="sxs-lookup"><span data-stu-id="15cea-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="15cea-121">Fara í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Biðgeymslusvæði**.</span><span class="sxs-lookup"><span data-stu-id="15cea-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="15cea-122">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="15cea-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="15cea-123">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="15cea-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="15cea-124">**Biðgeymslusvæði** – Færið inn einkvæmt kenni eða heiti fyrir biðgeymslusvæðið.</span><span class="sxs-lookup"><span data-stu-id="15cea-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="15cea-125">**Lýsing** – Færið inn ítarlega lýsingu á biðgeymslunni.</span><span class="sxs-lookup"><span data-stu-id="15cea-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="15cea-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="15cea-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15cea-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="15cea-127">Additional resources</span></span>

- [<span data-ttu-id="15cea-128">Gæðastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="15cea-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="15cea-129">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="15cea-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="15cea-130">Starfsmenn ábyrgir fyrir samþykki ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="15cea-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="15cea-131">Gerðir vandamála fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="15cea-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="15cea-132">Gerðir greininga fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="15cea-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="15cea-133">Gæðagjöld fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="15cea-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="15cea-134">Aðgerðir fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="15cea-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="15cea-135">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="15cea-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
