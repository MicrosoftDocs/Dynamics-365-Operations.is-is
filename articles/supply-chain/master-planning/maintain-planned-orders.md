---
title: "Viðhalda tillögum"
description: "Þessi grein gefur upplýsingar um hvernig á að stjórna áætluðum pöntunum. Hún lýsir því hvernig hægt er að uppfæra stöðu áætlaðra pantana, staðfesta þær og sía fyrir áætluðum pöntunum sem hafa sömu stöðu og valin áætluð pöntun."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c63fb039fc3bda00073c3e2a808a06b1d745a786
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="1542f-104">Viðhalda tillögum</span><span class="sxs-lookup"><span data-stu-id="1542f-104">Maintain planned orders</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1542f-105">Þessi grein gefur upplýsingar um hvernig á að stjórna áætluðum pöntunum.</span><span class="sxs-lookup"><span data-stu-id="1542f-105">This article provides information about how to manage planned orders.</span></span> <span data-ttu-id="1542f-106">Hún lýsir því hvernig hægt er að uppfæra stöðu áætlaðra pantana, staðfesta þær og sía fyrir áætluðum pöntunum sem hafa sömu stöðu og valin áætluð pöntun.</span><span class="sxs-lookup"><span data-stu-id="1542f-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="1542f-107">Hægt er að stjórna áætluðum pöntunum úr vinnusvæðinu **Aðaláætlanagerð**, úr listanum **Áætluð pöntun** eða listunum **Áætlaðar framleiðslupantanir**, **Áætlaðar innkaupapantanir**, og **Flutningsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="1542f-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="1542f-108">Hægt er að nota svæðið **Staða** til að aðstoða við að rekja framgang.</span><span class="sxs-lookup"><span data-stu-id="1542f-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="1542f-109">Eftirtalin gildi eru notuð:</span><span class="sxs-lookup"><span data-stu-id="1542f-109">The following values are used:</span></span>

-   <span data-ttu-id="1542f-110">Þegar aðaláætlunagerð°myndar áætlaðar pantanir, hafa áætlaðar pantanir stöðuna **Óunnið**.</span><span class="sxs-lookup"><span data-stu-id="1542f-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="1542f-111">Þegar valið er að staðfesta ekki áætlaða pöntun getur hún fengið stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="1542f-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="1542f-112">Þegar valið er að staðfesta áætlaða pöntun getur hún fengið stöðuna **Samþykkt**.</span><span class="sxs-lookup"><span data-stu-id="1542f-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="1542f-113">Sú staða°gefur til kynna að samþykkt hefur verið að staðfesta pöntunina en það hefur enn ekki verið gert.</span><span class="sxs-lookup"><span data-stu-id="1542f-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="1542f-114">**Ábending:** Áætluð pöntun sem er samþykkt er flutt, í núverandi stöðu, í næsta útreikning°aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="1542f-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="1542f-115">Hægt er að staðfesta áætlaðar pantanir með því að smella á **Staðfest**.</span><span class="sxs-lookup"><span data-stu-id="1542f-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="1542f-116">Hægt er að staðfesta eftirfarandi áætlaðar pantanir:</span><span class="sxs-lookup"><span data-stu-id="1542f-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="1542f-117">Áætlaða pöntunin sem er valin.</span><span class="sxs-lookup"><span data-stu-id="1542f-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="1542f-118">Margar áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="1542f-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="1542f-119">Áætlaðar pantanir sem myndaðar eru með niðurbroti af síðunni **Niðurbrot**.</span><span class="sxs-lookup"><span data-stu-id="1542f-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="1542f-120">Smellið á **Áætlaðar pantanir**, veljið pöntunina og smellið því næst á **Staðfest**.</span><span class="sxs-lookup"><span data-stu-id="1542f-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="1542f-121">Þegar áætluð pöntun er staðfest er hún færð í pöntunarhluta í viðeigandi einingu.</span><span class="sxs-lookup"><span data-stu-id="1542f-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> <span data-ttu-id="1542f-122">**Ábending:**Með því að hægrismella á áætlaða pöntun með ákveðna stöðu er hægt að sía fyrir aðrar áætlaðar pantanir með sömu stöðu.</span><span class="sxs-lookup"><span data-stu-id="1542f-122">**Note:** You can right-click a planned order that has a particular status and filter for other planned orders that have the same status.</span></span> <span data-ttu-id="1542f-123">Þessi aðgerð er gagnleg ef, til dæmis, óskað er að sía fyrir allar áætlaðar pantanir sem hafa stöðuna **Samþykkt**, svo síðan sé hægt að staðfesta þær.</span><span class="sxs-lookup"><span data-stu-id="1542f-123">This functionality is useful if, for example, you want to filter for all planned orders that have a status of **Approved**, so that you can then firm them.</span></span>

<a name="see-also"></a><span data-ttu-id="1542f-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1542f-124">See also</span></span>
--------

[<span data-ttu-id="1542f-125">Aðaláætlanir</span><span class="sxs-lookup"><span data-stu-id="1542f-125">Master plans</span></span>](master-plans.md)




