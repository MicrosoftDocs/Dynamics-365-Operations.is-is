--- 
title: "Setja upp skyldubundnar greiðslutilvísanir (Ísland)"
description: "Notið þetta ferli til að setja upp skyldubundna greiðslutilvísun fyrir sérstakan fjárhagslykil og bóka greiðslu."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 02/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Iceland
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 484f2e6f5213a2d55daa3d8292e80085abcb3e0d
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-mandatory-payment-references-iceland"></a><span data-ttu-id="04a60-103">Setja upp skyldubundnar greiðslutilvísanir (Ísland)</span><span class="sxs-lookup"><span data-stu-id="04a60-103">Set up mandatory payment references (Iceland)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04a60-104">Notið þetta ferli til að setja upp skyldubundna greiðslutilvísun fyrir sérstakan fjárhagslykil og bóka greiðslu.</span><span class="sxs-lookup"><span data-stu-id="04a60-104">Use this procedure to set up mandatory payment reference for a specific ledger account and post a payment.</span></span> <span data-ttu-id="04a60-105">Þegar fjárhagslykill er valin í færslubók verður að tilgreina tilvísun greiðslu fyrir færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="04a60-105">When you select the ledger account in the journal you must specify a payment reference for the journal line.</span></span>

<span data-ttu-id="04a60-106">Þessi skráning notar sýnigögn DEMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="04a60-106">This recording uses the DEMF demo company.</span></span> <span data-ttu-id="04a60-107">Þessi Virkni er eingöngu tiltæk fyrir lögaðila með aðalaðsetur á Íslandi.</span><span class="sxs-lookup"><span data-stu-id="04a60-107">This functionality is available for legal entities whose primary address is in Iceland.</span></span>

<span data-ttu-id="04a60-108">Þessi virkni er gjarnan notað af bókhaldarar , aðalbókarar, bókurum.</span><span class="sxs-lookup"><span data-stu-id="04a60-108">This functionality is typically used by accountants, accounting managers, accounting clerks.</span></span>


## <a name="set-up-the-main-account"></a><span data-ttu-id="04a60-109">Setja upp aðallykill</span><span class="sxs-lookup"><span data-stu-id="04a60-109">Set up the main account</span></span>
1. <span data-ttu-id="04a60-110">Fara í Fjárhagur > Bókhaldslyklar > Lyklar > Aðallyklar.</span><span class="sxs-lookup"><span data-stu-id="04a60-110">Go to General ledger > Chart of accounts > Accounts > Main accounts.</span></span>
2. <span data-ttu-id="04a60-111">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="04a60-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="04a60-112">Til dæmis, sía svæðið aðallykill með gildið '170150'.</span><span class="sxs-lookup"><span data-stu-id="04a60-112">For example, filter on the Main account field with a value of '170150'.</span></span>
3. <span data-ttu-id="04a60-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="04a60-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="04a60-114">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="04a60-114">Click Edit.</span></span>
5. <span data-ttu-id="04a60-115">Velja eða hreinsa sem gátreit Krefjast tilvísun greiðslu.</span><span class="sxs-lookup"><span data-stu-id="04a60-115">Select or clear the Require payment reference check box.</span></span>
6. <span data-ttu-id="04a60-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="04a60-116">Click Save.</span></span>

## <a name="create-a-payment-with-a-payment-reference"></a><span data-ttu-id="04a60-117">Greiðsla er stofnuð með tilvísun greiðslu</span><span class="sxs-lookup"><span data-stu-id="04a60-117">Create a payment with a payment reference</span></span>
1. <span data-ttu-id="04a60-118">Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="04a60-118">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="04a60-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="04a60-119">Click New.</span></span>
3. <span data-ttu-id="04a60-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="04a60-120">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="04a60-121">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="04a60-121">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="04a60-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="04a60-122">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="04a60-123">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="04a60-123">Click Lines.</span></span>
7. <span data-ttu-id="04a60-124">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="04a60-124">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="04a60-125">Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="04a60-125">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="04a60-126">Í reitnum Debet skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="04a60-126">In the Debit field, enter a number.</span></span>
10. <span data-ttu-id="04a60-127">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="04a60-127">In the Offset account field, specify the desired values.</span></span>
11. <span data-ttu-id="04a60-128">Smellið á flipann Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="04a60-128">Click the Payment tab.</span></span>
12. <span data-ttu-id="04a60-129">Færa inn gildi í greiðslutilvísunarsvæðið.</span><span class="sxs-lookup"><span data-stu-id="04a60-129">In the Payment reference field, type a value.</span></span>
13. <span data-ttu-id="04a60-130">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="04a60-130">Click Save.</span></span>
14. <span data-ttu-id="04a60-131">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="04a60-131">Click Post.</span></span>


