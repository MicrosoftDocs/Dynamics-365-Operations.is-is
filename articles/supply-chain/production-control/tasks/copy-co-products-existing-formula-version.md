--- 
title: "Afrita aukaafurðir úr fyrirliggjandi formúluútgáfu"
description: "Þessi verklýsing sýnir hvernig á að afrita aukaafurðir úr eldri útgáfu formúlu yfir í mismunandi formúluútgáfu fyrir útgefna afurð."
author: YuyuScheller
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 80543780c423b5beac3ec57f4fa035e560aaa4ce
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="014a7-103">Afrita aukaafurðir úr fyrirliggjandi formúluútgáfu</span><span class="sxs-lookup"><span data-stu-id="014a7-103">Copy co-products from an existing formula version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="014a7-104">Þessi verklýsing sýnir hvernig á að afrita aukaafurðir úr eldri útgáfu formúlu yfir í mismunandi formúluútgáfu fyrir útgefna afurð.</span><span class="sxs-lookup"><span data-stu-id="014a7-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="014a7-105">Það er skilyrði að minnsta kosti eitt formúluútgáfan tengist aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="014a7-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="014a7-106">Gögn fyrirtækisins sýnigögn USP2 er notuð til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="014a7-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="014a7-107">Finna útgefin afurð</span><span class="sxs-lookup"><span data-stu-id="014a7-107">Find a released product</span></span>
1. <span data-ttu-id="014a7-108">Farðu í Losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="014a7-108">Go to Released products.</span></span>
2. <span data-ttu-id="014a7-109">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="014a7-109">Click Show filters.</span></span>
    * <span data-ttu-id="014a7-110">Verið er að bæta við reitnum Framleiðslugerð í svarglugga síu.</span><span class="sxs-lookup"><span data-stu-id="014a7-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="014a7-111">Smella á svæði bæta Við síu til að bæta við svæðinu framleiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="014a7-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="014a7-112">Í Næsta skref þarf að færa handvirkt inn Formúlu í svæðinu framleiðslugerð áður en þú velur Nota.</span><span class="sxs-lookup"><span data-stu-id="014a7-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="014a7-113">Þetta stillir síuna á lista yfir útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="014a7-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="014a7-114">Færa inn handvirkt Formúlu í svæðinu framleiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="014a7-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="014a7-115">Smellið á Staðfesta</span><span class="sxs-lookup"><span data-stu-id="014a7-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="014a7-116">Velja útgefin afurð</span><span class="sxs-lookup"><span data-stu-id="014a7-116">Select a released product</span></span>
1. <span data-ttu-id="014a7-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="014a7-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="014a7-118">Smellt er á formúluútgáfa.</span><span class="sxs-lookup"><span data-stu-id="014a7-118">Click Formula versions.</span></span>
    * <span data-ttu-id="014a7-119">Smellt er á formúluútgáfum á tækniaðgerðarúðu.</span><span class="sxs-lookup"><span data-stu-id="014a7-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="014a7-120">Afrita aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="014a7-120">Copy co-products</span></span>
1. <span data-ttu-id="014a7-121">Á Aðgerðasvæðinu skal smellt á formúluútgáfu.</span><span class="sxs-lookup"><span data-stu-id="014a7-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="014a7-122">Smellt er á aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="014a7-122">Click Co-products.</span></span>
3. <span data-ttu-id="014a7-123">Smellið á Afrit.</span><span class="sxs-lookup"><span data-stu-id="014a7-123">Click Copy.</span></span>
4. <span data-ttu-id="014a7-124">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="014a7-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="014a7-125">Sláið inn eða veldu gildi í reitnum formúluútgáfa.</span><span class="sxs-lookup"><span data-stu-id="014a7-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="014a7-126">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="014a7-126">Click OK.</span></span>
7. <span data-ttu-id="014a7-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="014a7-127">Close the page.</span></span>


