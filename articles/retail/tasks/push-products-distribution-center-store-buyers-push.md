--- 
title: " Ýta afurðum úr dreifingarmiðstöð í verslun með dreifingu frá lager"
description: "Þetta ferli fer í gegnum skrefin til að stofna og vinna með dreifing á lager til að dreifa vörum úr einni staðsetningu á eina eða margar verslanir."
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 20c2734a8339279e3f13ca9f0a0d5398c87f846f
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="b3ba4-103"> Ýta afurðum úr dreifingarmiðstöð í verslun með dreifingu frá lager</span><span class="sxs-lookup"><span data-stu-id="b3ba4-103">Push products from distribution center to store using buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b3ba4-104">Þetta ferli fer í gegnum skrefin til að stofna og vinna með dreifing á lager til að dreifa vörum úr einni staðsetningu á eina eða margar verslanir.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="b3ba4-105">Notandinn getur stillt margar skilgreiningar og láta kerfið leggja til hvernig á að dreifa afurðir eða færa inn handvirkt þangað sem afurðir eru dreift og hversu miklu er dreift á hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="b3ba4-106">Þetta ferli ekki taka með uppsetningargögn sem hægt er að nota í dreifing á lager, eins og áfyllingarreglur, stigveldi fyrirtækis og geyma þyngd.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="b3ba4-107">Þessi aðferð notar sýnigögn USRT fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="b3ba4-108">Fara í Dreifing frá lager.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="b3ba4-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-109">Click New.</span></span>
3. <span data-ttu-id="b3ba4-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="b3ba4-111">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="b3ba4-112">Í svæðinu vöruhús, Færa inn eða velja vöruhús sem er með afurðir með lagermagn í svæðinu.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="b3ba4-113">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-113">Click Add.</span></span>
7. <span data-ttu-id="b3ba4-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b3ba4-115">Í reitnum númer afurðar, Færa inn eða veldu afurð.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="b3ba4-116">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-116">Click Add.</span></span>
10. <span data-ttu-id="b3ba4-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b3ba4-118">Í reitnum númer afurðar, Færa inn eða velja vöruvíddasamsetningar afurðar.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="b3ba4-119">Þegar afbrigði vöru er færð inn verður lína stofnuð fyrir hverja vöruvíddasamsetningu.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="b3ba4-120">Merkja línu af listanum.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="b3ba4-121">Í svæðinu Flutt magn, færðu inn hversu mörg eintök af valda afurð á að dreifa.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="b3ba4-122">Í viðbótarmagn til dreifingar frá lager svæðinu, færið inn magn afurðir sem hafa tiltækt magn til dreifingar.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="b3ba4-123">Færið inn 'Staðsetningarvægi' í svæðinu Dreifingu.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="b3ba4-124">Hægt er að velja aðrar gerðir til að nota aðra reglur fyrir dreifingu.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="b3ba4-125">Veljið gildi fyrir áfyllingarstigveldi í svæðinu .</span><span class="sxs-lookup"><span data-stu-id="b3ba4-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="b3ba4-126">Velja skal Já í svæðinu virða úrval.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="b3ba4-127">Smelltu á reikna Magn og fara yfir magnið sem er bætt við línur í hlutanum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="b3ba4-128">Smellt er á Stofna pöntun.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-128">Click Create order.</span></span>
20. <span data-ttu-id="b3ba4-129">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="b3ba4-129">Click Yes.</span></span>


