---
title: "Stjórna Birgðir verslunar"
description: "Þessi grein lýsir gerðum skjala sem hægt er að nota til að stýra birgðum."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fd37bcd7155c61492f5f4990685203ea97bca36
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="b3721-103">Stjórna Birgðir verslunar</span><span class="sxs-lookup"><span data-stu-id="b3721-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b3721-104">Þessi grein lýsir gerðum skjala sem hægt er að nota til að stýra birgðum.</span><span class="sxs-lookup"><span data-stu-id="b3721-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="b3721-105">Hægt er að nota eftirfarandi gerðir af skjölum til að stjórna birgðum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="b3721-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="b3721-106">Innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="b3721-106">Purchase orders</span></span>
<span data-ttu-id="b3721-107">Innkaupapantanir eru stofnaðar á aðalskrifstofu.</span><span class="sxs-lookup"><span data-stu-id="b3721-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="b3721-108">Ef vöruhús smásölu er innifalið í haus innkaupapöntunar er hægt að taka við pöntuninni í verslun með því að nota Modern POS (MPOS) eða Cloud POS í Microsoft Dynamics 365 for Operations - Retail.</span><span class="sxs-lookup"><span data-stu-id="b3721-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="b3721-109">Eftir að umbeðið magn hefur verið móttekið í versluninni er hægt að vista það staðbundið fyrir frekari breytingar.</span><span class="sxs-lookup"><span data-stu-id="b3721-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="b3721-110">Einnig er hægt að ráðstafa magninu og senda það á aðalskrifstofu.</span><span class="sxs-lookup"><span data-stu-id="b3721-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="b3721-111">Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Retail í reitnum **Móttaka núna** á innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="b3721-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="b3721-112">Flutningspantanir</span><span class="sxs-lookup"><span data-stu-id="b3721-112">Transfer orders</span></span>
<span data-ttu-id="b3721-113">Flutningspöntun getur tilgreint að ákveðin verslun sé staðsetning sem hægt er að senda vörurnar úr.</span><span class="sxs-lookup"><span data-stu-id="b3721-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="b3721-114">Í þessu tilfelli birtist flutningspöntun í verslun sem beiðni um tiltekt í MPOS eða Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="b3721-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="b3721-115">Eftir að umbeðið magn hefur verið tekið til er því ráðstafað og sent til aðalskrifstofu.</span><span class="sxs-lookup"><span data-stu-id="b3721-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="b3721-116">Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Retail í reitnum **Senda núna** á flutningspöntuninni.</span><span class="sxs-lookup"><span data-stu-id="b3721-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="b3721-117">Flutningspöntun getur tilgreint að ákveðin verslun sé staðsetning sem hægt er að senda vörurnar til.</span><span class="sxs-lookup"><span data-stu-id="b3721-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="b3721-118">Í þessu tilfelli birtist flutningspöntun í verslun sem beiðni um móttöku í MPOS eða Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="b3721-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="b3721-119">Eftir að umbeðið magn hefur verið móttekið í versluninni er hægt að vista það staðbundið fyrir frekari breytingar.</span><span class="sxs-lookup"><span data-stu-id="b3721-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="b3721-120">Einnig er hægt að ráðstafa magninu og senda það á aðalskrifstofu.</span><span class="sxs-lookup"><span data-stu-id="b3721-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="b3721-121">Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Retail í reitnum **Móttaka núna** á flutningspöntuninni.</span><span class="sxs-lookup"><span data-stu-id="b3721-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="b3721-122">Birgðatalning</span><span class="sxs-lookup"><span data-stu-id="b3721-122">Stock counts</span></span>
<span data-ttu-id="b3721-123">Birgðatalningar geta verið annaðhvort áætlaðar eða óskipulagðar.</span><span class="sxs-lookup"><span data-stu-id="b3721-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="b3721-124">Áætluð birgðatalning – Þessar birgðatalningar eru gerðar að frumkvæði aðalskrifstofunnar og það er hún sem ákveður hvaða vörur á að telja.</span><span class="sxs-lookup"><span data-stu-id="b3721-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="b3721-125">Aðalskrifstofa útbýr talningarskjal og sendir versluninni það og þar eru upplýsingar um birgðastöðu færðar inn í MPOS eða Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="b3721-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="b3721-126">Óundirbúin birgðatalning er hafin í verslun og magn raunbirgða á lager er uppfært í annaðhvort MPOS eða Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="b3721-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="b3721-127">Ólíkt áætlaðri birgðatalningu hafa óundirbúnar birgðatalningar ekki fyrirfram skilgreindan lista yfir vörur.</span><span class="sxs-lookup"><span data-stu-id="b3721-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="b3721-128">Þegar birgðatalningu af annarri hvorri gerð er lokið er henni ráðstafað og send til aðalskrifstofu.</span><span class="sxs-lookup"><span data-stu-id="b3721-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="b3721-129">Á aðalskrifstofu er talningin villuleituð og bókuð.</span><span class="sxs-lookup"><span data-stu-id="b3721-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="b3721-130">Birgðauppfletting</span><span class="sxs-lookup"><span data-stu-id="b3721-130">Inventory lookup</span></span>
<span data-ttu-id="b3721-131">Gildandi magn vöru á lager fyrir margar verslanir og vöruhús má skoða á síðunni Uppflettisvæði birgða.</span><span class="sxs-lookup"><span data-stu-id="b3721-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="b3721-132">Fyrir utan núverandi lagermagn má skoða tiltækt magn loforðs (ATP) um fyrir hverja einstaka verslun.</span><span class="sxs-lookup"><span data-stu-id="b3721-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="b3721-133">Til að gera það skal velja þá verslun sem á að skoða ATP fyrir og smella svo á **Sýna framboð verslunar**.</span><span class="sxs-lookup"><span data-stu-id="b3721-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





