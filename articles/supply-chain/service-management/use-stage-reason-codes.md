---
title: Nota ástæðukóða stigs
description: Notaður er ástæðukóði til þess að gefa til kynna hvers vegna hætt hefur verið við þjónustustigssamning (SLA) eða hvers vegna þjónustupöntun hefur farið hefur verið framúr tímamörkum sem voru tilgreind í SLA.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33fa7e5f08f09fe109d0507d686315d01e043928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557757"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="a9f41-103">Nota ástæðukóða stigs</span><span class="sxs-lookup"><span data-stu-id="a9f41-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a9f41-104">Notaður er ástæðukóði til þess að gefa til kynna hvers vegna hætt hefur verið við þjónustustigssamning (SLA) eða hvers vegna þjónustupöntun hefur farið hefur verið framúr tímamörkum sem voru tilgreind í SLA.</span><span class="sxs-lookup"><span data-stu-id="a9f41-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="a9f41-105">Einnig er hægt að tilgreina að ástæðukóða sé krafist þegar hætt er við SLA eða þegar farið er yfir tímamörkin sem eru tilgreind í SLA fyrir þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="a9f41-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="a9f41-106">Ef búið er að tilgreina að ástæðukóða sé krafist, verður að færa inn ástæðukóða við eftirfarandi aðstæður:</span><span class="sxs-lookup"><span data-stu-id="a9f41-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="a9f41-107">Þegar þjónustupöntun er flutt á stig þar sem tímaskráningu er hætt, þvert á það sem kveðið er á um í SLA fyrir þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="a9f41-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="a9f41-108">Þegar þjónustupöntunin er staðfest.</span><span class="sxs-lookup"><span data-stu-id="a9f41-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="a9f41-109">Þegar tímaskráning er stöðvuð handvirkt.</span><span class="sxs-lookup"><span data-stu-id="a9f41-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="a9f41-110">Setja upp ástæðukóða</span><span class="sxs-lookup"><span data-stu-id="a9f41-110">Set up reason codes</span></span>

1.  <span data-ttu-id="a9f41-111">Smelltu á **Þjónustukerfi** \> **Uppsetning** \> **Þjónustupantanir** \> **Stig ástæðukóðar**.</span><span class="sxs-lookup"><span data-stu-id="a9f41-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="a9f41-112">Í skjámyndinni **Stig ástæðukóða** er smellt á **Nýtt** til að stofna nýjan ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="a9f41-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="a9f41-113">Í reitnum **Stig ástæðukóða** skal slá inn einkvæmt stig ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="a9f41-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="a9f41-114">Í reitnum **Lýsing** skal slá inn lýsingu á stigi ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="a9f41-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="a9f41-115">Skjámyndinni er lokað til að vista breytingar.</span><span class="sxs-lookup"><span data-stu-id="a9f41-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="a9f41-116">Krefjast ástæðukóða þegar hætt er við þjónustustigssamning</span><span class="sxs-lookup"><span data-stu-id="a9f41-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="a9f41-117">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Færibreytur þjónustustjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="a9f41-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="a9f41-118">Í skjámyndinni **Færibreytur þjónustustjórnunar** skal smella á tengilinn **Almennt** og velja síðan gátreitinn **Ástæðukóði afturköllunar**.</span><span class="sxs-lookup"><span data-stu-id="a9f41-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="a9f41-119">Krefjast ástæðukóða þegar þjónustupöntun fer fram úr settum tímamörkum í þjónustustigssamningi</span><span class="sxs-lookup"><span data-stu-id="a9f41-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="a9f41-120">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Færibreytur þjónustustjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="a9f41-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="a9f41-121">Í skjámyndinni **Færibreytur þjónustustjórnunar** skal smella á tengilinn **Almennt** og velja síðan gátreitinn **Ástæðukóði fyrir að fara yfir á tíma**.</span><span class="sxs-lookup"><span data-stu-id="a9f41-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9f41-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a9f41-122">See also</span></span>

[<span data-ttu-id="a9f41-123">Hefja og stöðva tímaskráningu fyrir þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="a9f41-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


