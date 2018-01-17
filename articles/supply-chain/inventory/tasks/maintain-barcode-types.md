---
title: "Vinna með strikamerkjagerðir"
description: "Þessi verklýsing sýnir hvernig á að setja upp nýja skilgreiningu strikamerkis sem er hægt að nota sem hluta af tiltektarlistaskýrslu."
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: bc863ce86c4dc3cbdd3a1df881eb7a6efeea1656
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---
# <a name="maintain-bar-code-types"></a><span data-ttu-id="55f83-103">Vinna með strikamerkjagerðir</span><span class="sxs-lookup"><span data-stu-id="55f83-103">Maintain bar code types</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55f83-104">Þessi verklýsing sýnir hvernig á að setja upp nýja skilgreiningu strikamerkis sem er hægt að nota sem hluta af tiltektarlistaskýrslu.</span><span class="sxs-lookup"><span data-stu-id="55f83-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="55f83-105">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="55f83-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="55f83-106">Ef verið er að nota USMF má nota dæmagildin sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="55f83-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="55f83-107">Þessi verkefni myndu yfirleitt vera framkvæmd af yfirmanni vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="55f83-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="55f83-108">Fara á strikamerki.</span><span class="sxs-lookup"><span data-stu-id="55f83-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="55f83-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="55f83-109">Click New.</span></span>
3. <span data-ttu-id="55f83-110">Í reitinn uppsetning strikamerki skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="55f83-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="55f83-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="55f83-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="55f83-112">Veljið valkost í svæðinu strikamerki.</span><span class="sxs-lookup"><span data-stu-id="55f83-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="55f83-113">Ef verið er að nota USMF er hægt að velja ‚Kóði 39‘.</span><span class="sxs-lookup"><span data-stu-id="55f83-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="55f83-114">Í reitinn Stærð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="55f83-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="55f83-115">Í reitinn hámarkslengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="55f83-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="55f83-116">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="55f83-116">Click Save.</span></span>
9. <span data-ttu-id="55f83-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="55f83-117">Close the page.</span></span>
10. <span data-ttu-id="55f83-118">Fara í Færibreytur birgða- og vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="55f83-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="55f83-119">Sláið inn eða veldu gildi í reitnum uppsetningarreitur strikamerkis.</span><span class="sxs-lookup"><span data-stu-id="55f83-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="55f83-120">Velja uppsetningu strikamerkja sem er stofnað áður en hafa í huga að strikamerkissnið verður að samsvara sniði einkvæms auðkennis fyrir færslugerðina sem nota á í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="55f83-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="55f83-121">Til dæmis, fyrir tiltektarleiðir, ætti strikamerkissnið að samsvara sniði tilvísunar tiltektarleiðar, sem er yfirleitt númeraröð.</span><span class="sxs-lookup"><span data-stu-id="55f83-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="55f83-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="55f83-122">Click Save.</span></span>
13. <span data-ttu-id="55f83-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="55f83-123">Close the page.</span></span>

