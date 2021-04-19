---
title: Þjónustupöntunarstig
description: Með því að skilgreina stig fyrir þjónustupöntun og úthluta þeim til starfsmanna, stjórnarðu flæði þjónustupantana með þeim verkefnum sem ýmsir einstaklingar sinna í þjónustufyrirtækinu.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817510"
---
# <a name="service-order-stages"></a><span data-ttu-id="a41cb-103">Þjónustupöntunarstig</span><span class="sxs-lookup"><span data-stu-id="a41cb-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a41cb-104">Þú getur sett upp stig fyrir þjónustupöntun til þess að skilgreina verkefni sem þarf að ljúka, í hvaða röð þeim er lokið og starfsmenn sem bera ábyrgð á því að ljúka þeim.</span><span class="sxs-lookup"><span data-stu-id="a41cb-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="a41cb-105">Með því að skilgreina í stiganna fyrir þjónustupöntun og úthlutun þess á starfsmönnum, hægt að stýra flæði þjónustupöntunar gegnum verkefnum sem mismunandi unnin þjónustufyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="a41cb-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="a41cb-106">Röð stiga verður að innihalda frumstig.</span><span class="sxs-lookup"><span data-stu-id="a41cb-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="a41cb-107">Einnig er hægt að skilgreina aðgerðir sem eru leyfðar á hverju stigi.</span><span class="sxs-lookup"><span data-stu-id="a41cb-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="a41cb-108">Til dæmis, ef þú hreinsar gátreitinn **Bóka** fyrir öll stig nema síðasta stigið, er komið í veg fyrir að þjónustupantanir séu bókaðar áður en þjónustupantanir eru unnar í gegnum öll stigin.</span><span class="sxs-lookup"><span data-stu-id="a41cb-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="a41cb-109">Leiðaskil í þjónustupantanastig</span><span class="sxs-lookup"><span data-stu-id="a41cb-109">Branching in service order stages</span></span>

<span data-ttu-id="a41cb-110">Þegar sett er upp þjónustustig, er hægt að stofna marga valkosti eða greinar, til að velja úr fyrir næsta stig þjónustupöntunar.</span><span class="sxs-lookup"><span data-stu-id="a41cb-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="a41cb-111">Öll útibú sem þú stofnar eru til að velja úr þegar fyrsta áfanga er lokið.</span><span class="sxs-lookup"><span data-stu-id="a41cb-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="a41cb-112">T.d. setja upp **Áætlanagerð** sem frumstig.</span><span class="sxs-lookup"><span data-stu-id="a41cb-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="a41cb-113">Stofna stigin með heitinu **í vinnslu** og **hætta Við**, og veljið síðan **Áætlanagerðar** sem yfirstig fyrir þær.</span><span class="sxs-lookup"><span data-stu-id="a41cb-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="a41cb-114">Þú úthlutar stiginu **Áætlanagerð** til sölupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="a41cb-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="a41cb-115">Þegar stig fjárhagsáætlunargerðar fyrir sölupöntunina er lokið er hægt að velja á **í vinnslu** áfangi ef sölupöntunin er tilbúið til að vinna eða er hægt að velja á **hætta Við** áfangi ef hætt er við sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a41cb-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="a41cb-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a41cb-116">See also</span></span>

[<span data-ttu-id="a41cb-117">Setja upp stig þjónustupantana</span><span class="sxs-lookup"><span data-stu-id="a41cb-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="a41cb-118">Breyta þjónustupöntunarstigi</span><span class="sxs-lookup"><span data-stu-id="a41cb-118">Change the service order stage</span></span>](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]