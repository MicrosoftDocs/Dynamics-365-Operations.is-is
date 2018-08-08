--- 
title: "Bæta skorðu á segð við afbrigðalíkan afurðar"
description: "Þessi verklýsing sýnir hvernig hægt er að bæta nýjum skorðusegð við afbrigðalíkani afurðar."
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9c76669532333450b8f73fb0f4f7397ac8f1ee4e
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="22b62-103">Bæta skorðu á segð við afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="22b62-103">Add an expression constraint to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22b62-104">Þessi verklýsing sýnir hvernig hægt er að bæta nýjum skorðusegð við afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="22b62-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="22b62-105">Hún sýnir hvernig er hægt að gefa fyrirmæli sem um að hornvörn verður að nota í hátalara ef notandinn hefur valið sé framgrill í málmi.</span><span class="sxs-lookup"><span data-stu-id="22b62-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="22b62-106">Ferlið notar hágæða hátalaraíhlut fyrir USMF sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="22b62-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="22b62-107">Stofna segð töfluskorðu</span><span class="sxs-lookup"><span data-stu-id="22b62-107">Create an expression constraint</span></span>
1. <span data-ttu-id="22b62-108">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="22b62-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="22b62-109">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="22b62-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="22b62-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="22b62-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="22b62-111">Þetta dæmi nota hágæða hátalara líkanið.</span><span class="sxs-lookup"><span data-stu-id="22b62-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="22b62-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="22b62-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="22b62-113">Stækka skorðuhluti.</span><span class="sxs-lookup"><span data-stu-id="22b62-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="22b62-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="22b62-114">Click Add.</span></span>
7. <span data-ttu-id="22b62-115">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="22b62-115">Click Create.</span></span>
8. <span data-ttu-id="22b62-116">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="22b62-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="22b62-117">Færa inn segð</span><span class="sxs-lookup"><span data-stu-id="22b62-117">Enter expression</span></span>
1. <span data-ttu-id="22b62-118">Smella á Breyta segð.</span><span class="sxs-lookup"><span data-stu-id="22b62-118">Click Edit expression.</span></span>
    * <span data-ttu-id="22b62-119">Ef notendaviðmótinu í verkinu á skráningu á þessu stigi er aflæsa, má nota IntelliSense og lista yfir tákn til að byggja skorðusegð.</span><span class="sxs-lookup"><span data-stu-id="22b62-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="22b62-120">Færið inn í svæðið ConstraintBody 'Implies [FrontGrill == "Metal", CornerProtection] '.</span><span class="sxs-lookup"><span data-stu-id="22b62-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="22b62-121">Rökhugsun á bakvið þessa segð segir: Ef Framgrill er úr málmi, þá verður að velja valkostinn hornvörn.</span><span class="sxs-lookup"><span data-stu-id="22b62-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="22b62-122">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="22b62-122">Click Validate.</span></span>
    * <span data-ttu-id="22b62-123">Villuleita aðgerð keyrir gegnum skorðusegð og athugar málskipanarvilla.</span><span class="sxs-lookup"><span data-stu-id="22b62-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="22b62-124">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="22b62-124">Click Close.</span></span>
5. <span data-ttu-id="22b62-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="22b62-125">Click OK.</span></span>


