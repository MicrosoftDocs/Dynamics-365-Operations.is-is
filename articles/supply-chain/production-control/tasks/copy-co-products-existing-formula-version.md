---
title: Afrita aukaafurðir úr fyrirliggjandi formúluútgáfu
description: Þessi verklýsing sýnir hvernig á að afrita aukaafurðir úr eldri útgáfu formúlu yfir í mismunandi formúluútgáfu fyrir útgefna afurð.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 182cc79a3aaacd8a3af97310bd63a37de5338157
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212366"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="67501-103">Afrita aukaafurðir úr fyrirliggjandi formúluútgáfu</span><span class="sxs-lookup"><span data-stu-id="67501-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67501-104">Þessi verklýsing sýnir hvernig á að afrita aukaafurðir úr eldri útgáfu formúlu yfir í mismunandi formúluútgáfu fyrir útgefna afurð.</span><span class="sxs-lookup"><span data-stu-id="67501-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="67501-105">Það er skilyrði að minnsta kosti ein formúluútgáfn tengist aukaafurðum.</span><span class="sxs-lookup"><span data-stu-id="67501-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="67501-106">Sýnifyrirtækjagögn USP2 eru notuð til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="67501-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="67501-107">Finna útgefin afurð</span><span class="sxs-lookup"><span data-stu-id="67501-107">Find a released product</span></span>
1. <span data-ttu-id="67501-108">Farðu í Losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="67501-108">Go to Released products.</span></span>
2. <span data-ttu-id="67501-109">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="67501-109">Click Show filters.</span></span>
    * <span data-ttu-id="67501-110">Verið er að bæta við reitnum Framleiðslugerð í svarglugga síu.</span><span class="sxs-lookup"><span data-stu-id="67501-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="67501-111">Smella á svæði bæta Við síu til að bæta við svæðinu framleiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="67501-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="67501-112">Í Næsta skref þarf að færa handvirkt inn Formúlu í svæðinu framleiðslugerð áður en þú velur Nota.</span><span class="sxs-lookup"><span data-stu-id="67501-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="67501-113">Þetta stillir síuna á lista yfir útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="67501-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="67501-114">Færa inn handvirkt Formúlu í svæðinu framleiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="67501-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="67501-115">Smellið á Staðfesta</span><span class="sxs-lookup"><span data-stu-id="67501-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="67501-116">Velja útgefin afurð</span><span class="sxs-lookup"><span data-stu-id="67501-116">Select a released product</span></span>
1. <span data-ttu-id="67501-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="67501-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="67501-118">Smellt er á formúluútgáfa.</span><span class="sxs-lookup"><span data-stu-id="67501-118">Click Formula versions.</span></span>
    * <span data-ttu-id="67501-119">Smellt er á formúluútgáfum á tækniaðgerðarúðu.</span><span class="sxs-lookup"><span data-stu-id="67501-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="67501-120">Afrita aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="67501-120">Copy co-products</span></span>
1. <span data-ttu-id="67501-121">Á Aðgerðasvæðinu skal smellt á formúluútgáfu.</span><span class="sxs-lookup"><span data-stu-id="67501-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="67501-122">Smellt er á aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="67501-122">Click Co-products.</span></span>
3. <span data-ttu-id="67501-123">Smellið á Afrit.</span><span class="sxs-lookup"><span data-stu-id="67501-123">Click Copy.</span></span>
4. <span data-ttu-id="67501-124">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="67501-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="67501-125">Sláið inn eða veldu gildi í reitnum formúluútgáfa.</span><span class="sxs-lookup"><span data-stu-id="67501-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="67501-126">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="67501-126">Click OK.</span></span>
7. <span data-ttu-id="67501-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="67501-127">Close the page.</span></span>

