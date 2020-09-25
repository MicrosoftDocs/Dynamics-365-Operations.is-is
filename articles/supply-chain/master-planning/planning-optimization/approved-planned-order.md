---
title: Samþykkja tillögur
description: Þetta efnisatriði lýsir samþykki áætlaðra pantana sem eru studdar í Fínstillingu skipulagningar.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759689"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="0639e-103">Samþykkja tillögur</span><span class="sxs-lookup"><span data-stu-id="0639e-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0639e-104">Í þessu efnisatriði eru veittar upplýsingar um hvernig uppfæra eigi stöðu áætlaðra pantana í Fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="0639e-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="0639e-105">Athugið að samþykki á áætluðum pöntunum er valfrjálst skref, og er eitt skref í því að stofna staðfesta pöntun úr áætlaðri pöntun.</span><span class="sxs-lookup"><span data-stu-id="0639e-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="0639e-106">Mælt er með því að samþykkja breyttar áætlaðar pantanir, annars verða breytingarnar hunsaðar og yfirskrifaðar af næstu áætlunarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="0639e-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Áætlað pöntunarflæði](media/approved-planned-orders-1.png)

<span data-ttu-id="0639e-108">Reiturinn **Staða** hjálpar til við að fylgjast með framvindu með eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="0639e-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="0639e-109">**Óunnið:** Þegar aðaláætlunargerð myndar áætlaðar pantanir, hafa áætlaðar pantanir stöðuna *Óunnið*.</span><span class="sxs-lookup"><span data-stu-id="0639e-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="0639e-110">Áætluðum pöntunum með þessa stöðu verður eytt við næstu áætlunarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="0639e-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="0639e-111">**Lokið:** Ef þú ákveður að staðfesta ekki áætlaða pöntun geturðu breytt stöðunni í *Lokið* til að gefa til kynna að þú hafir lokið við að meta þessa áætluðu pöntun.</span><span class="sxs-lookup"><span data-stu-id="0639e-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="0639e-112">Athugið að stöðurnar *Ómeðhöndlað* og *Lokið* er meðhöndlaðar eins af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="0639e-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="0639e-113">**Samþykkt:** Ef þú vilt halda breytingum eða ætlar að staðfesta áætlaða pöntun skaltu breyta stöðunni í *Samþykkt*.</span><span class="sxs-lookup"><span data-stu-id="0639e-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="0639e-114">Áætlaðar pantanir með stöðuna *Samþykkt* eru hugsaðar sem fastar og eru áætlaðar fyrir aðaláætlanagerð, þannig að þeim er ekki breytt eða þeim eytt í síðari aðaláætlunarkeyrslum.</span><span class="sxs-lookup"><span data-stu-id="0639e-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="0639e-115">Til að ná þessu afritar áætlunargrunnurinn *Samþykktar* áætlaðar pantanir úr gömlu áætlunarútgáfunni yfir í nýju áætlunarútgáfuna við aðalskipulagningu.</span><span class="sxs-lookup"><span data-stu-id="0639e-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="0639e-116">Athugið að *Samþykktar* áætlaðar pantanir eru aðeins hugsaðar sem framboð innan tiltekinnar aðaláætlunar.</span><span class="sxs-lookup"><span data-stu-id="0639e-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="0639e-117">Hægt er að stjórna áætluðum pöntunum úr vinnusvæðinu **Aðaláætlanagerð**, úr listanum **Áætluð pöntun** eða listunum **Áætlaðar framleiðslupantanir**, **Áætlaðar innkaupapantanir**, og **Flutningsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="0639e-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
