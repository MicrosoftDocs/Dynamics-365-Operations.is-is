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
ms.openlocfilehash: 7834745923bf5ec05018ff5829ddaa0b75df5db7
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145577"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="25841-103">Vinna með gerðir strikamerkja</span><span class="sxs-lookup"><span data-stu-id="25841-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25841-104">Þessi verklýsing sýnir hvernig á að setja upp nýja skilgreiningu strikamerkis sem er hægt að nota sem hluta af tiltektarlistaskýrslu.</span><span class="sxs-lookup"><span data-stu-id="25841-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="25841-105">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="25841-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="25841-106">Ef verið er að nota USMF má nota dæmagildin sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="25841-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="25841-107">Þessi verkefni myndu yfirleitt vera framkvæmd af yfirmanni vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="25841-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="25841-108">Fara á strikamerki.</span><span class="sxs-lookup"><span data-stu-id="25841-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="25841-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="25841-109">Click New.</span></span>
3. <span data-ttu-id="25841-110">Í reitinn uppsetning strikamerki skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25841-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="25841-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="25841-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25841-112">Veljið valkost í svæðinu strikamerki.</span><span class="sxs-lookup"><span data-stu-id="25841-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="25841-113">Ef verið er að nota USMF er hægt að velja ‚Kóði 39‘.</span><span class="sxs-lookup"><span data-stu-id="25841-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="25841-114">Í reitinn Stærð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="25841-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="25841-115">Í reitinn hámarkslengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="25841-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="25841-116">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="25841-116">Click Save.</span></span>
9. <span data-ttu-id="25841-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25841-117">Close the page.</span></span>
10. <span data-ttu-id="25841-118">Fara í Færibreytur birgða- og vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="25841-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="25841-119">Sláið inn eða veldu gildi í reitnum uppsetningarreitur strikamerkis.</span><span class="sxs-lookup"><span data-stu-id="25841-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="25841-120">Velja uppsetningu strikamerkja sem er stofnað áður en hafa í huga að strikamerkissnið verður að samsvara sniði einkvæms auðkennis fyrir færslugerðina sem nota á í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="25841-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="25841-121">Til dæmis, fyrir tiltektarleiðir, ætti strikamerkissnið að samsvara sniði tilvísunar tiltektarleiðar, sem er yfirleitt númeraröð.</span><span class="sxs-lookup"><span data-stu-id="25841-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="25841-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="25841-122">Click Save.</span></span>
13. <span data-ttu-id="25841-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25841-123">Close the page.</span></span>

