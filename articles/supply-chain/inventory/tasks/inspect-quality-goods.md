---
title: Kanna vörugæði
description: Í þessu efnisatriði er lýst hvernig á að vinna úr gæðapöntunum.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956135"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="2ec4c-103">Kanna vörugæði</span><span class="sxs-lookup"><span data-stu-id="2ec4c-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ec4c-104">Í þessu efnisatriði er lýst hvernig á að vinna úr gæðapöntunum.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="2ec4c-105">Gæðaskoðanir eru vanalega gerðar af gæðastarfsmanni.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="2ec4c-106">Ef stöðluð sýnigögn eru uppsett er hægt að nota þau til að ljúka ferlunum í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="2ec4c-107">Til að nota sýnigögnin skal velja lögaðilann *USMF* áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="2ec4c-108">Þú verður síðan að staðfesta innkaupapöntun *000016* og bóka innhreyfingarskjal afurðar.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="2ec4c-109">Gæðapöntun myndast sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="2ec4c-110">Skref 1: Velja gæðapöntun</span><span class="sxs-lookup"><span data-stu-id="2ec4c-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="2ec4c-111">Fylgja skal eftirfarandi skrefum til að velja gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="2ec4c-112">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="2ec4c-113">Veldu gæðapöntunina sem var búin til áður en þú hófst þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="2ec4c-114">Skref 2: Skrá niðurstöður prófunar</span><span class="sxs-lookup"><span data-stu-id="2ec4c-114">Step 2: Record test results</span></span>

<span data-ttu-id="2ec4c-115">Fylgja skal eftirfarandi skrefum til að skrá niðurstöður prófunar.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="2ec4c-116">Veldu **Niðurstöður**.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-116">Select **Results**.</span></span>
1. <span data-ttu-id="2ec4c-117">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-117">Select **Edit**.</span></span>
1. <span data-ttu-id="2ec4c-118">Í reitnum **Niðurstöðumagn** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="2ec4c-119">Í reitnum **Útkoma** skal velja æskilega skrá.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="2ec4c-120">Í þessu dæmi byggist niðurstaðan á fyrirframskilgreindri útkomu.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="2ec4c-121">Yfirleitt er skráð ítarlegri niðurstaða prófunar á borð við stærð eða aðra mælivídd.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="2ec4c-122">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-122">Select **Save**.</span></span>
1. <span data-ttu-id="2ec4c-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="2ec4c-124">Skref 3: Staðfesta gæðapöntunina</span><span class="sxs-lookup"><span data-stu-id="2ec4c-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="2ec4c-125">Til að staðfesta gæðapöntunina skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="2ec4c-126">Veldu **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-126">Select **Validate**.</span></span>
1. <span data-ttu-id="2ec4c-127">Í reitnum **Staðfest af** skal velja notandann sem sér um skoðunina.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="2ec4c-128">Veljið **Velja**.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-128">Select **Select**.</span></span>
1. <span data-ttu-id="2ec4c-129">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-129">Select **OK**.</span></span>
1. <span data-ttu-id="2ec4c-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2ec4c-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
