--- 
title: "Hjáskipa afurðir úr viðtökuvöruhúsi í verslanir"
description: "Þetta ferli fer í gegnum skrefin til að stofna og vinna hjáskipun til að dreifa afurðir úr staðsetning móttökustaðar innkaupapöntunar til ein eða margar verslanir."
author: BibiSp
manager: AnnBe
ms.date: 02/17/2016
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
ms.openlocfilehash: 1182474504f7d1c051fe995c516367420ccc9701
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="9f92a-103">Hjáskipa afurðir úr viðtökuvöruhúsi í verslanir</span><span class="sxs-lookup"><span data-stu-id="9f92a-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f92a-104">Þetta ferli fer í gegnum skrefin til að stofna og vinna hjáskipun til að dreifa afurðir úr staðsetning móttökustaðar innkaupapöntunar til ein eða margar verslanir.</span><span class="sxs-lookup"><span data-stu-id="9f92a-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="9f92a-105">Notandinn getur stillt margar skilgreiningar og láta kerfið leggja til hvernig á að dreifa afurðir eða færa inn handvirkt þangað sem afurðir eru dreift og hversu miklu er dreift á hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="9f92a-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="9f92a-106">Aðferðin felur ekki í sér uppsetningu gagna sem nota má á hjáskipun, eins og áfyllingarreglur, stigveldi fyrirtækis og geyma þyngd.</span><span class="sxs-lookup"><span data-stu-id="9f92a-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="9f92a-107">Ferlið notar sýnigögn fyrir USRT fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="9f92a-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="9f92a-108">Fara í Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="9f92a-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="9f92a-109">Veljið innkaupapöntun af listanum og smelltu á tengil til að opna pöntunina.</span><span class="sxs-lookup"><span data-stu-id="9f92a-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="9f92a-110">Í aðgerðasvæðinu er smellt á Smásala.</span><span class="sxs-lookup"><span data-stu-id="9f92a-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="9f92a-111">Smellt er á frá Dreifingarstöð.</span><span class="sxs-lookup"><span data-stu-id="9f92a-111">Click Cross docking.</span></span>
5. <span data-ttu-id="9f92a-112">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="9f92a-112">Click Edit.</span></span>
    * <span data-ttu-id="9f92a-113">Hægt er að nota tegundina til að sía vörur í kaflanum línur.</span><span class="sxs-lookup"><span data-stu-id="9f92a-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="9f92a-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9f92a-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9f92a-115">í reitnum magn fyrir Dreifing frá dreifingarstöð, Færa inn gildi til að tilgreina hversu mikið magn er keypt fyrir valda afurð að vera dreifð </span><span class="sxs-lookup"><span data-stu-id="9f92a-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="9f92a-116">Í aukalega magnreitnum fyrir Dreifing frá dreifingarstöð, skal færa inn gildi til að tilgreina magn til dreifingar fyrir tiltækar afurðir til að kaupa </span><span class="sxs-lookup"><span data-stu-id="9f92a-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="9f92a-117">Færið inn 'Staðsetningarvægi' í svæðinu Dreifingu.</span><span class="sxs-lookup"><span data-stu-id="9f92a-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="9f92a-118">Hægt er að velja aðrar gerðir til að nota mismunandi reglur fyrir dreifingu.</span><span class="sxs-lookup"><span data-stu-id="9f92a-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="9f92a-119">Veljið gildi fyrir áfyllingarstigveldi í svæðinu .</span><span class="sxs-lookup"><span data-stu-id="9f92a-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="9f92a-120">Velja skal Já í svæðinu virða úrval.</span><span class="sxs-lookup"><span data-stu-id="9f92a-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="9f92a-121">Smellt er á Reikna út magn.</span><span class="sxs-lookup"><span data-stu-id="9f92a-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="9f92a-122">Smellt er á Stofna pöntun.</span><span class="sxs-lookup"><span data-stu-id="9f92a-122">Click Create order.</span></span>
14. <span data-ttu-id="9f92a-123">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="9f92a-123">Click Yes.</span></span>
15. <span data-ttu-id="9f92a-124">Á listanum skal finna og velja vöruhús sem tók á móti vörur</span><span class="sxs-lookup"><span data-stu-id="9f92a-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="9f92a-125">Smellið á pantanir til Að skoða pantanir sem var stofnað fyrir valið vöruhús</span><span class="sxs-lookup"><span data-stu-id="9f92a-125">Click Order to view the orders that got created for the selected warehouse</span></span>


