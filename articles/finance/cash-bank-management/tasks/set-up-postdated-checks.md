---
title: Setja upp fyrirframdagsettar ávísanir
description: Í þessu efnisatriði er útskýrt hvernig á að tilgreina hvort eigi að bóka bókarfærslur fyrir fyrirframdagsettar ávísanir og hvaða bókunarbækur sem nota á fyrir færslur og lánardrottnagreiðslur.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141109"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="546be-103">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="546be-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="546be-104">Í þessu efnisatriði er útskýrt hvernig á að tilgreina hvort eigi að bóka bókarfærslur fyrir fyrirframdagsettar ávísanir og hvaða bókunarbækur sem nota á fyrir færslur og lánardrottnagreiðslur.</span><span class="sxs-lookup"><span data-stu-id="546be-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="546be-105">Einnig er hægt að tilgreina millireikninga fyrir útgefnar ávísanir, mótteknar ávísanir og staðgreiðsluskatt.</span><span class="sxs-lookup"><span data-stu-id="546be-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="546be-106">Fyrirframdagsettar ávísanir sem eru gefnar út til að gera og móttaka greiðslur í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="546be-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="546be-107">Hægt er að tilgreina hvort ávísunin verði að koma fram í bókhaldsbókum fyrir gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="546be-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="546be-108">Hlutverk þessa ferlis er fjárreiðustjóri.</span><span class="sxs-lookup"><span data-stu-id="546be-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="546be-109">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="546be-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="546be-110">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="546be-110">Set up postdated checks</span></span>
1. <span data-ttu-id="546be-111">Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="546be-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="546be-112">Smellið á flipann Fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="546be-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="546be-113">Veldu eða hreinsaðu gátreitinn Virkja fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="546be-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="546be-114">Velja eða hreinsa gátreitinn Bóka bókarfærslur fyrir fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="546be-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="546be-115">Í reitnum Millireikningur fyrir útgefnar ávísanir skal tilgreina þau gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="546be-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="546be-116">Tilgreinið gildin sem óskað er eftir í reitinn Millireikningur fyrir mótteknar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="546be-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="546be-117">Í reitinn Almenn færslubók fyrir jöfnun færslna skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="546be-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="546be-118">Í reitinn Millifæra fyrirframdagsettar ávísanir á þessa færslubók lánardrottins skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="546be-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="546be-119">Í reitnum Millireikningur staðgreiðsluskatts skal tilgreina þau gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="546be-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="546be-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="546be-120">Click Save.</span></span>
11. <span data-ttu-id="546be-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="546be-121">Close the page.</span></span>
12. <span data-ttu-id="546be-122">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="546be-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="546be-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="546be-123">Click New.</span></span>
14. <span data-ttu-id="546be-124">Færa inn gildi í svæðinu greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="546be-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="546be-125">Velja skal bókunarkostinn Millireikning fyrirframdagsettrar ávísunar til að tilgreina að upphæð ávísunarinnar er bókuð á millireikning.</span><span class="sxs-lookup"><span data-stu-id="546be-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="546be-126">Veljið 'Banki' í svæðinu gerð lykils.</span><span class="sxs-lookup"><span data-stu-id="546be-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="546be-127">Mótlykill greiðslumáta verður banki.</span><span class="sxs-lookup"><span data-stu-id="546be-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="546be-128">Í reitnum Greiðslulykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="546be-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="546be-129">Veldu reikninginn sem er notaður til að draga reikningsupphæðina frá.</span><span class="sxs-lookup"><span data-stu-id="546be-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="546be-130">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="546be-130">Click Save.</span></span>
19. <span data-ttu-id="546be-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="546be-131">Close the page.</span></span>

