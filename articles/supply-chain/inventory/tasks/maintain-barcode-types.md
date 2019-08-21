---
title: Vinna með gerðir strikamerkja
description: Þessi verklýsing sýnir hvernig á að setja upp nýja skilgreiningu strikamerkis sem er hægt að nota sem hluta af tiltektarlistaskýrslu.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0551784ff55f5dc05fbe92ee354316eb04d755cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845448"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="76200-103">Vinna með gerðir strikamerkja</span><span class="sxs-lookup"><span data-stu-id="76200-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76200-104">Þessi verklýsing sýnir hvernig á að setja upp nýja skilgreiningu strikamerkis sem er hægt að nota sem hluta af tiltektarlistaskýrslu.</span><span class="sxs-lookup"><span data-stu-id="76200-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="76200-105">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="76200-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="76200-106">Ef verið er að nota USMF má nota dæmagildin sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="76200-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="76200-107">Þessi verkefni myndu yfirleitt vera framkvæmd af yfirmanni vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="76200-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="76200-108">Fara á strikamerki.</span><span class="sxs-lookup"><span data-stu-id="76200-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="76200-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="76200-109">Click New.</span></span>
3. <span data-ttu-id="76200-110">Í reitinn uppsetning strikamerki skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="76200-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="76200-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="76200-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="76200-112">Veljið valkost í svæðinu strikamerki.</span><span class="sxs-lookup"><span data-stu-id="76200-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="76200-113">Ef verið er að nota USMF er hægt að velja ‚Kóði 39‘.</span><span class="sxs-lookup"><span data-stu-id="76200-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="76200-114">Í reitinn Stærð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="76200-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="76200-115">Í reitinn hámarkslengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="76200-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="76200-116">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="76200-116">Click Save.</span></span>
9. <span data-ttu-id="76200-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="76200-117">Close the page.</span></span>
10. <span data-ttu-id="76200-118">Fara í Færibreytur birgða- og vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="76200-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="76200-119">Sláið inn eða veldu gildi í reitnum uppsetningarreitur strikamerkis.</span><span class="sxs-lookup"><span data-stu-id="76200-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="76200-120">Velja uppsetningu strikamerkja sem er stofnað áður en hafa í huga að strikamerkissnið verður að samsvara sniði einkvæms auðkennis fyrir færslugerðina sem nota á í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="76200-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="76200-121">Til dæmis, fyrir tiltektarleiðir, ætti strikamerkissnið að samsvara sniði tilvísunar tiltektarleiðar, sem er yfirleitt númeraröð.</span><span class="sxs-lookup"><span data-stu-id="76200-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="76200-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="76200-122">Click Save.</span></span>
13. <span data-ttu-id="76200-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="76200-123">Close the page.</span></span>

