--- 
title: "Ljúka framleiðslupöntun"
description: "Þetta ferli sýnir hvernig á að ljúka framleiðslupöntun."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 75b91ea330258a5b57e9e58cb32539d57e458f28
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="end-a-production-order"></a><span data-ttu-id="d77fc-103">Ljúka framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="d77fc-103">End a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d77fc-104">Þetta ferli sýnir hvernig á að ljúka framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="d77fc-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="d77fc-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="d77fc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d77fc-106">Þetta er síðasta ferli af sjö sem útskýrir lífsferil pöntunar í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="d77fc-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="d77fc-107">Ljúka framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="d77fc-107">End a production order</span></span>
1. <span data-ttu-id="d77fc-108">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="d77fc-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="d77fc-109">Veljið framleiðslupöntun sem hefur stöðuna Tilgreint sem tilbúið.</span><span class="sxs-lookup"><span data-stu-id="d77fc-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="d77fc-110">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="d77fc-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="d77fc-111">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="d77fc-111">Click End.</span></span>
    * <span data-ttu-id="d77fc-112">Á þessari síðu er hægt að staðfesta að það eigi að ljúka framleiðslupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="d77fc-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="d77fc-113">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="d77fc-113">Click the General tab.</span></span>
5. <span data-ttu-id="d77fc-114">Dagsetning er rituð í reitinn Dagetning.</span><span class="sxs-lookup"><span data-stu-id="d77fc-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="d77fc-115">Í reitnum Úrkastsaðferð skal velja ‚Úthlutun‘.</span><span class="sxs-lookup"><span data-stu-id="d77fc-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="d77fc-116">Þegar úthlutunaraðferð er valin er kostnaði við úrkastsefni bætt við fullbúnar vörur.</span><span class="sxs-lookup"><span data-stu-id="d77fc-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="d77fc-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d77fc-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="d77fc-118">Villuleita niðurstöður útreikninga</span><span class="sxs-lookup"><span data-stu-id="d77fc-118">Validate calculation results</span></span>
1. <span data-ttu-id="d77fc-119">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="d77fc-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="d77fc-120">Skoða kostnaðarsamanburð</span><span class="sxs-lookup"><span data-stu-id="d77fc-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="d77fc-121">Þegar framleiðslupöntuninni er lokið er hægt að bera saman áætlað kostnaðarverð við raunkostnaðarverð til að fá yfirlit yfir frávik í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="d77fc-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  


