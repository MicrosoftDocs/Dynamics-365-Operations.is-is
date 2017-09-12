--- 
title: " Stofna fjárhagsvíddir fyrir afgreiðslukassa og skilgreina víddagildi í afgreiðslukössum"
description: "Þetta ferli fer í gegnum stofnun fjárhagslegar víddir fyrir afgreiðslukassa á sölustað og sýnir hvernig skal skilgreina gildi fjárhagsvídda á afgreiðslukassa."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8a3a6abc19bae20b7899628d0463cf458955671a
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="07226-103"> Stofna fjárhagsvíddir fyrir afgreiðslukassa og skilgreina víddagildi í afgreiðslukössum</span><span class="sxs-lookup"><span data-stu-id="07226-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="07226-104">Þetta ferli fer í gegnum stofnun fjárhagslegar víddir fyrir afgreiðslukassa á sölustað og sýnir hvernig skal skilgreina gildi fjárhagsvídda á afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="07226-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="07226-105">Þetta ferli ekki taka með aðrar tengdar skref, s.s. að stofna víddarsamstæður og lykilskipulag.</span><span class="sxs-lookup"><span data-stu-id="07226-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="07226-106">Þessum verkefnum er að finna í öðrum efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="07226-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="07226-107">Þessi skráning notar sýnigögn USRT fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="07226-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="07226-108">Fara í fjárhag > Línurit yfir lykla > Víddir > Fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="07226-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="07226-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="07226-109">Click New.</span></span>
3. <span data-ttu-id="07226-110">Veljið í svæðinu Nota gildi frá,veldu valkostur'.</span><span class="sxs-lookup"><span data-stu-id="07226-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="07226-111">Í reitinn Heiti víddar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="07226-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="07226-112">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="07226-112">Click Activate.</span></span>
6. <span data-ttu-id="07226-113">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="07226-113">Click Close.</span></span>
7. <span data-ttu-id="07226-114">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="07226-114">Click Activate.</span></span>
8. <span data-ttu-id="07226-115">Smellt er á víddargildi.</span><span class="sxs-lookup"><span data-stu-id="07226-115">Click Dimension values.</span></span>
9. <span data-ttu-id="07226-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="07226-116">Close the page.</span></span>
10. <span data-ttu-id="07226-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="07226-117">Click Save.</span></span>
11. <span data-ttu-id="07226-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="07226-118">Close the page.</span></span>
12. <span data-ttu-id="07226-119">Fara í Smásala og viðskipti > Uppsetning rásar > Uppsetning smásölustaðar >Skrár.</span><span class="sxs-lookup"><span data-stu-id="07226-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="07226-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="07226-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="07226-121">Víxla útvíkkun á liðnum fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="07226-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="07226-122">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="07226-122">Click Edit.</span></span>
16. <span data-ttu-id="07226-123">Í reitnum afgreiðslustöð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="07226-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="07226-124">Á listanum, Finna og velja víddargildi fyrir afgreiðslukassi sem verið er að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="07226-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="07226-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="07226-125">Click Save.</span></span>


