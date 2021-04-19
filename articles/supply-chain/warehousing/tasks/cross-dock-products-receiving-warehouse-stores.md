---
title: Hjáskipa afurðir úr viðtökuvöruhúsi í verslanir
description: Þetta ferli fer í gegnum skrefin til að stofna og vinna hjáskipun til að dreifa afurðir úr staðsetning móttökustaðar innkaupapöntunar til ein eða margar verslanir.
author: ShylaThompson
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7caec5329774baaa03c72f9236f8e3192399089
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810391"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="34140-103">Hjáskipa afurðir úr viðtökuvöruhúsi í verslanir</span><span class="sxs-lookup"><span data-stu-id="34140-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34140-104">Þetta ferli fer í gegnum skrefin til að stofna og vinna hjáskipun til að dreifa afurðir úr staðsetning móttökustaðar innkaupapöntunar til ein eða margar verslanir.</span><span class="sxs-lookup"><span data-stu-id="34140-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="34140-105">Notandinn getur stillt margar skilgreiningar og láta kerfið leggja til hvernig á að dreifa afurðir eða færa inn handvirkt þangað sem afurðir eru dreift og hversu miklu er dreift á hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="34140-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="34140-106">Aðferðin felur ekki í sér uppsetningu gagna sem nota má á hjáskipun, eins og áfyllingarreglur, stigveldi fyrirtækis og geyma þyngd.</span><span class="sxs-lookup"><span data-stu-id="34140-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="34140-107">Ferlið notar sýnigögn fyrir USRT fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="34140-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="34140-108">Fara í Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="34140-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="34140-109">Veljið innkaupapöntun af listanum og smelltu á tengil til að opna pöntunina.</span><span class="sxs-lookup"><span data-stu-id="34140-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="34140-110">Í aðgerðasvæðinu er smellt á Retail og Commerce.</span><span class="sxs-lookup"><span data-stu-id="34140-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="34140-111">Smellt er á frá Dreifingarstöð.</span><span class="sxs-lookup"><span data-stu-id="34140-111">Click Cross docking.</span></span>
5. <span data-ttu-id="34140-112">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="34140-112">Click Edit.</span></span>
    * <span data-ttu-id="34140-113">Hægt er að nota tegundina til að sía vörur í kaflanum línur.</span><span class="sxs-lookup"><span data-stu-id="34140-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="34140-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="34140-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="34140-115">í reitnum magn fyrir Dreifing frá dreifingarstöð, Færa inn gildi til að tilgreina hversu mikið magn er keypt fyrir valda afurð að vera dreifð </span><span class="sxs-lookup"><span data-stu-id="34140-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="34140-116">Í aukalega magnreitnum fyrir Dreifing frá dreifingarstöð, skal færa inn gildi til að tilgreina magn til dreifingar fyrir tiltækar afurðir til að kaupa </span><span class="sxs-lookup"><span data-stu-id="34140-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="34140-117">Færið inn 'Staðsetningarvægi' í svæðinu Dreifingu.</span><span class="sxs-lookup"><span data-stu-id="34140-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="34140-118">Hægt er að velja aðrar gerðir til að nota mismunandi reglur fyrir dreifingu.</span><span class="sxs-lookup"><span data-stu-id="34140-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="34140-119">Veljið gildi fyrir áfyllingarstigveldi í svæðinu .</span><span class="sxs-lookup"><span data-stu-id="34140-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="34140-120">Velja skal Já í svæðinu virða úrval.</span><span class="sxs-lookup"><span data-stu-id="34140-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="34140-121">Smellt er á Reikna út magn.</span><span class="sxs-lookup"><span data-stu-id="34140-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="34140-122">Smellt er á Stofna pöntun.</span><span class="sxs-lookup"><span data-stu-id="34140-122">Click Create order.</span></span>
14. <span data-ttu-id="34140-123">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="34140-123">Click Yes.</span></span>
15. <span data-ttu-id="34140-124">Á listanum skal finna og velja vöruhús sem tók á móti vörur</span><span class="sxs-lookup"><span data-stu-id="34140-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="34140-125">Smellið á pantanir til Að skoða pantanir sem var stofnað fyrir valið vöruhús</span><span class="sxs-lookup"><span data-stu-id="34140-125">Click Order to view the orders that got created for the selected warehouse</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]