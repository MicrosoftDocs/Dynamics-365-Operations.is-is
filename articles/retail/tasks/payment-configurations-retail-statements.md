--- 
title: " Skilgreiningar greiðslna fyrir smásöluyfirlit"
description: "Þetta ferli sýnir skilgreiningar fyrir greiðsluaðferðir Smásöluverslunar sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9bbc0367e88f86ae7fdbf7c4fec89eff78478cac
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="c35dd-103"> Skilgreiningar greiðslna fyrir smásöluyfirlit</span><span class="sxs-lookup"><span data-stu-id="c35dd-103">Payment configurations for Retail statements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c35dd-104">Þetta ferli sýnir skilgreiningar fyrir greiðsluaðferðir Smásöluverslunar sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð.</span><span class="sxs-lookup"><span data-stu-id="c35dd-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="c35dd-105">Þessi skráning notar sýnigögn USRT fyrirtækið .</span><span class="sxs-lookup"><span data-stu-id="c35dd-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="c35dd-106">Fara í Smásölu og viðskipti > rásir > smásöluverslanir > allar smásöluverslanir.</span><span class="sxs-lookup"><span data-stu-id="c35dd-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="c35dd-107">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c35dd-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c35dd-108">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c35dd-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c35dd-109">Í aðgerðasvæðinu er smellt á setja upp.</span><span class="sxs-lookup"><span data-stu-id="c35dd-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="c35dd-110">Smellt er á greiðsluhætti.</span><span class="sxs-lookup"><span data-stu-id="c35dd-110">Click Payment methods.</span></span>
6. <span data-ttu-id="c35dd-111">Stækka eða fella saman bókunarhlutann.</span><span class="sxs-lookup"><span data-stu-id="c35dd-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="c35dd-112">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="c35dd-112">Click Edit.</span></span>
    * <span data-ttu-id="c35dd-113">Veljið hvort upphæðir sem móttekna fyrir þennan greiðslumáta skuli bókuð í fjárhagslykil eða bankareikning.</span><span class="sxs-lookup"><span data-stu-id="c35dd-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="c35dd-114">Veljið lykilinn sem bóka á upphæðir á sem móttekið er fyrir þennan greiðsluhátt.</span><span class="sxs-lookup"><span data-stu-id="c35dd-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="c35dd-115">Veljið lykil til að bóka mögulegar mismun á milli mótteknar heildarfærsluupphæð og talda upphæð fyrir þennan greiðsluhátt.</span><span class="sxs-lookup"><span data-stu-id="c35dd-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="c35dd-116">Í þessu svæði er hægt að færa inn hvenær upphæðamismunur skal bóka upphæð í annan lykil.</span><span class="sxs-lookup"><span data-stu-id="c35dd-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="c35dd-117">Hægt er að nota þetta til að rekja mikinn mismun.</span><span class="sxs-lookup"><span data-stu-id="c35dd-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="c35dd-118">Veljið lykil til að bóka mögulegar mismun á milli mótteknar heildarfærsluupphæð og talda upphæð fyrir þennan greiðsluhátt þegar það fer yfir gildið sem er skilgreint í „hámarks mismunur upphæðar“ reit.</span><span class="sxs-lookup"><span data-stu-id="c35dd-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="c35dd-119">Veljið "Já" til að bóka upphæðir peningaflutningur í banka á aðskilda lykla.</span><span class="sxs-lookup"><span data-stu-id="c35dd-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="c35dd-120">Í þessu svæði er hægt að velja hvort upphæðir peningaflutningur í banka skuli bókuð í fjárhagslykil eða bankareikning.</span><span class="sxs-lookup"><span data-stu-id="c35dd-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="c35dd-121">Veljið lykilinn sem á að bóka upphæðir peningaflutningur í banka í.</span><span class="sxs-lookup"><span data-stu-id="c35dd-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="c35dd-122">Velja skal bankafærslugerð sem nota á við bókun peningaflutningur í banka á bankareikning.</span><span class="sxs-lookup"><span data-stu-id="c35dd-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="c35dd-123">Veljið "Já" til að bóka upphæðir í öryggisskáp á aðskildum lykli.</span><span class="sxs-lookup"><span data-stu-id="c35dd-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="c35dd-124">Veljið hvort upphæðir í öryggisskáp skuli bókuð í fjárhagslykil eða bankareikning.</span><span class="sxs-lookup"><span data-stu-id="c35dd-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="c35dd-125">Veljið lykilinn sem á að bóka upphæðir í öryggisskáp í.</span><span class="sxs-lookup"><span data-stu-id="c35dd-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="c35dd-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c35dd-126">Click Save.</span></span>


