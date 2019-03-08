---
title: Úthluta lífferilsstaða afurðar til útgefins afurðasniðmáts
description: Þetta ferli sýnir hvernig á að úthluta lífferilsstöðu afurðar á útgefið afurðasniðmát og afbrigði þess.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd9d40bb331b9e024617c8be55330dfce8ba1cc6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "309473"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="955aa-103">Úthluta lífferilsstaða afurðar til útgefins afurðasniðmáts</span><span class="sxs-lookup"><span data-stu-id="955aa-103">Assign a product lifecycle state to a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="955aa-104">Þetta ferli sýnir hvernig á að úthluta lífferilsstöðu afurðar á útgefið afurðasniðmát og afbrigði þess.</span><span class="sxs-lookup"><span data-stu-id="955aa-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="955aa-105">Forkröfur: Spila þarf verkefnaleiðbeiningarnar „Búa til nýja lífferlisstöðu vöru“ fyrst til að ganga úr skugga um að a.m.k. ein lífferlisstaða afurðar sé stofuað áður en hægt er að spila þessar verkefnaleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="955aa-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="955aa-106">Finna útgefið afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="955aa-106">Find a released product master</span></span>
1. <span data-ttu-id="955aa-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="955aa-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="955aa-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="955aa-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="955aa-109">Afurðarsniðmát er með Undirgerð afurðar afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="955aa-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="955aa-110">Uppfæra lífferilsstöðu</span><span class="sxs-lookup"><span data-stu-id="955aa-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="955aa-111">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="955aa-111">Click Edit.</span></span>
2. <span data-ttu-id="955aa-112">Sláið inn eða veljið gildi í reitnum Lífferilsstaða afurðar.</span><span class="sxs-lookup"><span data-stu-id="955aa-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="955aa-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="955aa-113">Click Save.</span></span>
4. <span data-ttu-id="955aa-114">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="955aa-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="955aa-115">Ef Já er valið eru allar tengd útgefin afurðarafbrigði sem hafa sömu upphaflegu stöðu og valin útgefin afurðarsniðmát einnig uppfærð í nýja lífferlisstöðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="955aa-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="955aa-116">Ef Nei er valið halda öll afbrigði raunástandi sínu.</span><span class="sxs-lookup"><span data-stu-id="955aa-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="955aa-117">Afbrigði sem hafa mismunandi lífferlisstöðu afurðar frá útgefnu afurðarsniðmáti eru ekki uppfærð.</span><span class="sxs-lookup"><span data-stu-id="955aa-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="955aa-118">Staðfestu lífferilsstöðu afurðarafbrigða</span><span class="sxs-lookup"><span data-stu-id="955aa-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="955aa-119">Smella á Útgefin afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="955aa-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="955aa-120">Athugið að öll afbrigði hafa erft valda lífferlisstöðu úr útgefnu afurðarsniðmáti.</span><span class="sxs-lookup"><span data-stu-id="955aa-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="955aa-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="955aa-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="955aa-122">Sláið inn eða veljið gildi í reitnum Lífferilsstaða afurðar.</span><span class="sxs-lookup"><span data-stu-id="955aa-122">In the Product lifecycle state field, enter or select a value.</span></span>

