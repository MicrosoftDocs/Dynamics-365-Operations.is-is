---
title: Skipta eign
description: Þetta efni útskýrir hvernig skal skipta hlutfalli einnar eignabókar á nýtt eignabók.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000294"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="4d7a2-103">Skipta eign</span><span class="sxs-lookup"><span data-stu-id="4d7a2-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d7a2-104">Þetta efni útskýrir hvernig skal skipta hlutfalli einnar eignabókar á nýtt eignabók.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="4d7a2-105">Það notar hlutverk Bókhaldara og sýnigögn USMF.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="4d7a2-106">Búa til nýja eign</span><span class="sxs-lookup"><span data-stu-id="4d7a2-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="4d7a2-107">Í yfirlitssvæðinu opnarðu **Einingar \> Eignir \> Eignir \> Eignir**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="4d7a2-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-108">Select **New**.</span></span>
3. <span data-ttu-id="4d7a2-109">Í reitnum **Eignaflokkur** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="4d7a2-110">Athugið númer eignar til að nota seinna í ferlinu skipta.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="4d7a2-111">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="4d7a2-112">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="4d7a2-113">Skipta eign</span><span class="sxs-lookup"><span data-stu-id="4d7a2-113">Split a fixed asset</span></span>

<span data-ttu-id="4d7a2-114">Áður en afskrifaðri eign er skipt ætti að breyta stöðu eignabókar handvirkt úr **Lokað** í **Opin**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="4d7a2-115">Þetta skref er áskilið vegna þess að staða bókar verður að vera **Opin** ef bóka þarf færslur fyrir eignina (til dæmis fyrir afskráning sölu).</span><span class="sxs-lookup"><span data-stu-id="4d7a2-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="4d7a2-116">Eftir að stöðu eignabókar er breytt skal fylgja þessum skrefum til að skipta eigninni.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="4d7a2-117">Finna og veljið tengil í eignir sem skipta á í listanum.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="4d7a2-118">Veldu **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-118">Select **Books**.</span></span> <span data-ttu-id="4d7a2-119">Veljið bók til að skipta á nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="4d7a2-120">Veljið **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-120">Select **Functions**.</span></span>
4. <span data-ttu-id="4d7a2-121">Velu **Skipta eign**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="4d7a2-122">Sláðu inn eða veldu gildi í reitnum **Á eign**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="4d7a2-123">Í reitnum **Til bókar** skal velja fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4d7a2-124">Færa inn dagsetningu í reitinn **Færsludagsetning**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="4d7a2-125">Færið inn tölu í reitnum **Prósenta**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="4d7a2-126">Sláið inn eða veljið gildi í reitnum **Heiti færslubókar**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="4d7a2-127">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="4d7a2-128">Bókið færslubókarfærsla.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-128">Post the journal transaction</span></span>

1. <span data-ttu-id="4d7a2-129">Í yfirlitssvæðinu opnarðu **Einingar \> Eignir \> Færslubókarfærslur \> Eignabækur**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="4d7a2-130">Veljið færslubók sem er stofnuð með skipta ferlinu á listanum.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="4d7a2-131">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-131">Select **Lines**.</span></span>

    - <span data-ttu-id="4d7a2-132">Staðfestið stofnaðar færslubókarlínur .</span><span class="sxs-lookup"><span data-stu-id="4d7a2-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="4d7a2-133">Leiðrétting kaupvirðisfærsla er stofnuð fyrir upprunalegu eignina til að minnka virði eftir prósentu sem tilgreind er við að skipta ferlinu.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="4d7a2-134">Kaupfærsla er stofnuð fyrir nýju eignina fyrir sömu upphæð.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="4d7a2-135">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="4d7a2-135">Select **Post**.</span></span>
