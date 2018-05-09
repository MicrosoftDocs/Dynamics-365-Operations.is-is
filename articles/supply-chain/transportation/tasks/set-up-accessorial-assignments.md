--- 
title: "Setja upp úthlutun á aukaþjónustu"
description: "Þessi verklýsing sýnir hvernig á að setja upp aukalegu úthlutun."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d3e49b4f4d8869790187a4f8c0b7d0129f5772d6
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="11166-103">Setja upp úthlutun á aukaþjónustu</span><span class="sxs-lookup"><span data-stu-id="11166-103">Set up accessorial assignments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="11166-104">Þessi verklýsing sýnir hvernig á að setja upp aukalegu úthlutun.</span><span class="sxs-lookup"><span data-stu-id="11166-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="11166-105">Þetta er yfirleitt gert af samræmingaraðila flutninga.</span><span class="sxs-lookup"><span data-stu-id="11166-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="11166-106">Áður en þessari handbók er notuð þarf að keyra í "Setja upp aukagjald og aukalegt sniðmát".</span><span class="sxs-lookup"><span data-stu-id="11166-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="11166-107">Setja upp aukaúthlutun</span><span class="sxs-lookup"><span data-stu-id="11166-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="11166-108">Fara í flutningsstjórnun > Uppsetning >Einkunn > Úthlutun aukaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="11166-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="11166-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="11166-109">Click New.</span></span>
3. <span data-ttu-id="11166-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="11166-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="11166-111">Víxla útvíkkun á liðnum upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="11166-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="11166-112">Í reitnum Stöð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="11166-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="11166-113">á listanum, Velja Stöðvar sem þú stofnaðir aukalegt sniðmát fyrir þegar þú keyrðir "Setja upp aukagjald og aukalegt sniðmát“-leiðbeiningum .</span><span class="sxs-lookup"><span data-stu-id="11166-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="11166-114">Í reitnum Aukalegt auðkenni stöðvar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="11166-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="11166-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="11166-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="11166-116">Víxla útvíkkun á liðnum skilyrði.</span><span class="sxs-lookup"><span data-stu-id="11166-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="11166-117">Í hlutanum Skilyrði er hægt að velja nákvæm skilyrði fyrir þegar gjöld eiga að gilda, byggt á mismunandi gildi sem er boðið hér.</span><span class="sxs-lookup"><span data-stu-id="11166-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="11166-118">Stillt á Alltaf að nota valkost á Já.</span><span class="sxs-lookup"><span data-stu-id="11166-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="11166-119">Veljið valkost í reitnum stig aukaúthlutunar.</span><span class="sxs-lookup"><span data-stu-id="11166-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="11166-120">Víxla útvíkkun á liðnum útreikningur.</span><span class="sxs-lookup"><span data-stu-id="11166-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="11166-121">Veljið í svæðinu aukagjalds ‚Flatt'.</span><span class="sxs-lookup"><span data-stu-id="11166-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="11166-122">Gerð aukagjalds ákvarðar hvernig reikna á gjaldið raunverulega.</span><span class="sxs-lookup"><span data-stu-id="11166-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="11166-123">Í þessu dæmi er það flatt gjald.</span><span class="sxs-lookup"><span data-stu-id="11166-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="11166-124">Í reitinn aukagjald skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="11166-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="11166-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="11166-125">Click Save.</span></span>


