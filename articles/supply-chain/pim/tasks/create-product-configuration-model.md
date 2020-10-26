---
title: Stofna afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig á að stofna afbrigðalíkan afurðar og færa inn grunnupplýsingar eins og eigindir og undiríhlutir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c81b3af7460c636245dcc16affcb05b724fbc70
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986120"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="25dcb-103">Stofna afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="25dcb-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25dcb-104">Þessi verklýsing sýnir hvernig á að stofna afbrigðalíkan afurðar og færa inn grunnupplýsingar eins og eigindir og undiríhlutir.</span><span class="sxs-lookup"><span data-stu-id="25dcb-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="25dcb-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="25dcb-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="25dcb-106">Stofna framleiðslulíkan</span><span class="sxs-lookup"><span data-stu-id="25dcb-106">Create a product model</span></span>
1. <span data-ttu-id="25dcb-107">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="25dcb-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="25dcb-108">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="25dcb-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="25dcb-109">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="25dcb-109">Click New.</span></span>
4. <span data-ttu-id="25dcb-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25dcb-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="25dcb-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="25dcb-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="25dcb-112">Í reitnum Stefna leysis skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="25dcb-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="25dcb-113">Leysisstefnu ákvarðar hvernig skorður í afbrigðalíkani afurðar sem byggir á skorðum eru unnar.</span><span class="sxs-lookup"><span data-stu-id="25dcb-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="25dcb-114">Þetta val getur haft áhrif á afköst afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="25dcb-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="25dcb-115">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25dcb-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="25dcb-116">Rótaríhlutur stendur fyrir afbrigðalíkan afurðar, en einnig er hægt að nota það í öðrum vörulíkan.</span><span class="sxs-lookup"><span data-stu-id="25dcb-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="25dcb-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="25dcb-117">Click OK.</span></span>
9. <span data-ttu-id="25dcb-118">Veljið valkost í svæðinu skilgreiningar Endurnýtingu .</span><span class="sxs-lookup"><span data-stu-id="25dcb-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="25dcb-119">Ef færibreytan endurnýtingu skilgreiningar er stillt á Já, mun kerfið leita að eins skilgreiningar eftir hverja stillingarlotu og nota aftur ef nákvæm samsvörun finnst.</span><span class="sxs-lookup"><span data-stu-id="25dcb-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="25dcb-120">Bæta við eigindum</span><span class="sxs-lookup"><span data-stu-id="25dcb-120">Add attributes</span></span>
1. <span data-ttu-id="25dcb-121">Útvíkka hlutann eigindir.</span><span class="sxs-lookup"><span data-stu-id="25dcb-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="25dcb-122">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="25dcb-122">Click Add.</span></span>
3. <span data-ttu-id="25dcb-123">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="25dcb-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="25dcb-124">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25dcb-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="25dcb-125">Í reitinn Heiti leysis skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25dcb-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="25dcb-126">Heiti Leysara er notaður af skorðu leysara afurðaafbrigðastillis.</span><span class="sxs-lookup"><span data-stu-id="25dcb-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="25dcb-127">Hún má ekki innihalda bil eða sérstafir nema _ (undirstriki).</span><span class="sxs-lookup"><span data-stu-id="25dcb-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="25dcb-128">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="25dcb-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="25dcb-129">Texti lýsingar birtist notandanum skilgreiningu og þar af leiðandi getur þjónað sem hjálp í að velja rétt gildi eigindar.</span><span class="sxs-lookup"><span data-stu-id="25dcb-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="25dcb-130">Færa inn eða veljið gildi í svæðinu gerð eigindar.</span><span class="sxs-lookup"><span data-stu-id="25dcb-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="25dcb-131">Gerð eigindar ákvarðar hvaða gildi eru tiltæk fyrir eigindina.</span><span class="sxs-lookup"><span data-stu-id="25dcb-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="25dcb-132">Velja skal gátreit Taka í endurnýtingu .</span><span class="sxs-lookup"><span data-stu-id="25dcb-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="25dcb-133">Þessi valkostur er aðeins tiltækur þegar valkosturinn Endurnýtingu skilgreininga er valin.</span><span class="sxs-lookup"><span data-stu-id="25dcb-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="25dcb-134">Að hafa eigind með í gátreit Endurnýta þýðir að þessi eigind verður athuguð þegar kerfið leitar að nákvæm samsvörun.</span><span class="sxs-lookup"><span data-stu-id="25dcb-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="25dcb-135">Bæta við undiríhlutir</span><span class="sxs-lookup"><span data-stu-id="25dcb-135">Add subcomponents</span></span>
1. <span data-ttu-id="25dcb-136">Stækkaðu hlutann undiríhlutir.</span><span class="sxs-lookup"><span data-stu-id="25dcb-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="25dcb-137">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="25dcb-137">Click Add.</span></span>
3. <span data-ttu-id="25dcb-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="25dcb-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="25dcb-139">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25dcb-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="25dcb-140">Í reitinn Heiti leysis skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25dcb-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="25dcb-141">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="25dcb-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="25dcb-142">Færa inn eða veljið gildi í svæðinu íhlutur.</span><span class="sxs-lookup"><span data-stu-id="25dcb-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="25dcb-143">Hver undirþáttagerð verður að vísa í íhlutarskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="25dcb-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="25dcb-144">Þessi hönnun styður endurnýtanlegu íhluti og tryggir að þegar íhlutur hefur verið skilgreint er hægt að nota í mörg framleiðslulíkön.</span><span class="sxs-lookup"><span data-stu-id="25dcb-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="25dcb-145">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="25dcb-145">Click Save.</span></span>
9. <span data-ttu-id="25dcb-146">Smellt er á uppskriftarlínuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="25dcb-146">Click BOM line details.</span></span>
    * <span data-ttu-id="25dcb-147">Upplýsingar um uppskriftalínuskjámyndina gera notandanum kleift að velja viðeigandi eiginleika fyrir undiríhlutina.</span><span class="sxs-lookup"><span data-stu-id="25dcb-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="25dcb-148">Hægt er að gefa hverjum eiginleika fast gildi eða varpa honum á eigind.</span><span class="sxs-lookup"><span data-stu-id="25dcb-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="25dcb-149">Að varpa á eigind leiðir til að Uppskrift línueiginleika fær mismunandi gildi eftir því hvað var valið í skilgreiningarhlutanum.</span><span class="sxs-lookup"><span data-stu-id="25dcb-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="25dcb-150">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="25dcb-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="25dcb-151">Hver undirþáttagerð táknar skilgreinanleg afurðarsniðmát með skorðuskilgreiningartækni.</span><span class="sxs-lookup"><span data-stu-id="25dcb-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="25dcb-152">Tilvísun er gerð með vörunúmeri.</span><span class="sxs-lookup"><span data-stu-id="25dcb-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="25dcb-153">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="25dcb-153">Select the Set check box.</span></span>
12. <span data-ttu-id="25dcb-154">Velja skal Já í Útreiknings reitnum.</span><span class="sxs-lookup"><span data-stu-id="25dcb-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="25dcb-155">Stilla valkost útreiknings tryggir að afurðin verða teknar með við útreikning kostnaðar fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="25dcb-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="25dcb-156">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="25dcb-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="25dcb-157">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="25dcb-157">Select the Set check box.</span></span>
15. <span data-ttu-id="25dcb-158">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="25dcb-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="25dcb-159">Magn svæðið ákvarðar hversu mikið þessarar afurðar verður að nota í skilgreindu vörunni.</span><span class="sxs-lookup"><span data-stu-id="25dcb-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="25dcb-160">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="25dcb-160">Select the Set check box.</span></span>
17. <span data-ttu-id="25dcb-161">Í reitinn Á röð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="25dcb-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="25dcb-162">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="25dcb-162">Click OK.</span></span>

