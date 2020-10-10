---
title: Gerðir verkbeiðni
description: Þetta efni útskýrir gerðir verkbeiðna í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e43908e3f13c9e4fd6fab6f1e17a171866b803
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888786"
---
# <a name="work-order-types"></a><span data-ttu-id="76429-103">Gerðir verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="76429-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="76429-104">Verkbeiðnagerðir eru notaðar til að flokka verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="76429-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="76429-105">Til dæmis gætir þú verið með verkbeiðnir sem tengjast fyrirbyggjandi viðhaldi eða leiðréttandi viðhaldi.</span><span class="sxs-lookup"><span data-stu-id="76429-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="76429-106">Gerð verkbeiðni skilgreinir tengsl við líftímalíkan verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="76429-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="76429-107">Líftímalíkan verkbeiðni skilgreinir þá líftímastöðu verkbeiðni sem er hægt að stilla á verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="76429-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="76429-108">(Dæmi um líftímastöður verkbeiðna eru **Stofnað**, **Í ferli** og **Lokið**.)</span><span class="sxs-lookup"><span data-stu-id="76429-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="76429-109">Nánari upplýsingar um líftímastöður verkbeiðna og verkefnastig, sjá [Líftímastöður verkbeiðna](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="76429-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="76429-110">Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Gerðir verkbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="76429-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="76429-111">Smellið á **Nýtt** til að stofna nýja gerð verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="76429-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="76429-112">Í reitnum **Gerð verkbeiðni** skal slá inn auðkenni fyrir gerð verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="76429-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="76429-113">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="76429-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="76429-114">Í reitnum **Líftímalíkan verkbeiðni** skaltu velja líftímalíkan.</span><span class="sxs-lookup"><span data-stu-id="76429-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="76429-115">Stilltu valkostinn **Einn viðhaldsstarfsmaður** á **Já** ef öll verkbeiðniverk sem tengjast verkbeiðni af þessari gerð ættu að vera áætluð til sama viðhaldsstarfsmanns.</span><span class="sxs-lookup"><span data-stu-id="76429-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="76429-116">Í reitnum **Gerð kostnaðar** velurðu **Leiðrétting**, **Fyrirbyggjandi** eða **Fjárfesting**, eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="76429-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="76429-117">Öll verkbeiðniverk í verkbeiðni verða að hafa sömu kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="76429-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="76429-118">Í hlutanum **Skylda** stillirðu viðeigandi valkosti á **Já** til að tilgreina hvaða bilanatengdar eða niðurtíma vegna viðhalds-tengdar upplýsingar er bætt við verkbeiðni af þessari gerð.</span><span class="sxs-lookup"><span data-stu-id="76429-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="76429-119">Valkostirnir í hlutanum **Skylda** tengjast valkostunum á flýtiflipanum **Staðfesta** á síðunni **Líftími verkbeiðna** (**Eignastýring** \> **Uppsetning** \> **Verkbeiðnir** \> **Líftímastöður**).</span><span class="sxs-lookup"><span data-stu-id="76429-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="76429-120">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="76429-120">Select **Save**.</span></span>

![Gerðir verkbeiðni](media/16-setup-for-work-orders.png)
