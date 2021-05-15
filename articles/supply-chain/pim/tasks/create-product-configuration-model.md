---
title: Stofna afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig á að stofna afbrigðalíkan afurðar og færa inn grunnupplýsingar eins og eigindir og undiríhlutir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921366"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="b521d-103">Stofna afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="b521d-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b521d-104">Þessi verklýsing sýnir hvernig á að stofna afbrigðalíkan afurðar og færa inn grunnupplýsingar eins og eigindir og undiríhlutir.</span><span class="sxs-lookup"><span data-stu-id="b521d-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="b521d-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="b521d-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="b521d-106">Stofna framleiðslulíkan</span><span class="sxs-lookup"><span data-stu-id="b521d-106">Create a product model</span></span>

1. <span data-ttu-id="b521d-107">Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.</span><span class="sxs-lookup"><span data-stu-id="b521d-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="b521d-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b521d-108">Select **New**.</span></span>
1. <span data-ttu-id="b521d-109">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="b521d-110">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="b521d-111">Í reitnum **Stefna leysis** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="b521d-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="b521d-112">Leysisstefnu ákvarðar hvernig skorður í afbrigðalíkani afurðar sem byggir á skorðum eru unnar.</span><span class="sxs-lookup"><span data-stu-id="b521d-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="b521d-113">Þetta val getur haft áhrif á afköst afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="b521d-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="b521d-114">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="b521d-115">Rótaríhlutur stendur fyrir afbrigðalíkan afurðar, en einnig er hægt að nota það í öðrum vörulíkan.</span><span class="sxs-lookup"><span data-stu-id="b521d-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="b521d-116">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b521d-116">Select **OK**.</span></span>
1. <span data-ttu-id="b521d-117">Veljið valkost í svæðinu **Endurnota skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="b521d-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="b521d-118">Ef færibreytan endurnýtingu skilgreiningar er stillt á Já, mun kerfið leita að eins skilgreiningar eftir hverja stillingarlotu og nota aftur ef nákvæm samsvörun finnst.</span><span class="sxs-lookup"><span data-stu-id="b521d-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="b521d-119">Bæta við eigindum</span><span class="sxs-lookup"><span data-stu-id="b521d-119">Add attributes</span></span>

1. <span data-ttu-id="b521d-120">Stækka hlutann **Eigindir**.</span><span class="sxs-lookup"><span data-stu-id="b521d-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="b521d-121">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b521d-121">Select **Add**.</span></span>
3. <span data-ttu-id="b521d-122">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b521d-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b521d-123">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b521d-124">Í reitinn **Heiti leysis** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="b521d-125">Heiti Leysara er notaður af skorðu leysara afurðaafbrigðastillis.</span><span class="sxs-lookup"><span data-stu-id="b521d-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="b521d-126">Hún má ekki innihalda bil eða sérstafir nema _ (undirstriki).</span><span class="sxs-lookup"><span data-stu-id="b521d-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="b521d-127">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="b521d-128">Texti lýsingar birtist notandanum skilgreiningu og þar af leiðandi getur þjónað sem hjálp í að velja rétt gildi eigindar.</span><span class="sxs-lookup"><span data-stu-id="b521d-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="b521d-129">Færa inn eða veljið gildi í svæðinu **Gerð eigindar**.</span><span class="sxs-lookup"><span data-stu-id="b521d-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="b521d-130">Gerð eigindar ákvarðar hvaða gildi eru tiltæk fyrir eigindina.</span><span class="sxs-lookup"><span data-stu-id="b521d-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="b521d-131">Veljið gátreitinn **Taka í endurnýtingu**.</span><span class="sxs-lookup"><span data-stu-id="b521d-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="b521d-132">Þessi valkostur er aðeins tiltækur þegar valkosturinn Endurnýtingu skilgreininga er valin.</span><span class="sxs-lookup"><span data-stu-id="b521d-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="b521d-133">Að hafa eigind með í gátreit Endurnýta þýðir að þessi eigind verður athuguð þegar kerfið leitar að nákvæm samsvörun.</span><span class="sxs-lookup"><span data-stu-id="b521d-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="b521d-134">Bæta við undiríhlutir</span><span class="sxs-lookup"><span data-stu-id="b521d-134">Add subcomponents</span></span>

1. <span data-ttu-id="b521d-135">Stækkaðu hlutann **Undiríhlutir**.</span><span class="sxs-lookup"><span data-stu-id="b521d-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="b521d-136">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b521d-136">Select **Add**.</span></span>
3. <span data-ttu-id="b521d-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b521d-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b521d-138">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b521d-139">Í reitinn **Heiti leysis** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="b521d-140">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="b521d-141">Færa inn eða veljið gildi í svæðinu **Íhlutur**.</span><span class="sxs-lookup"><span data-stu-id="b521d-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="b521d-142">Hver undirþáttagerð verður að vísa í íhlutarskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b521d-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="b521d-143">Þessi hönnun styður endurnýtanlegu íhluti og tryggir að þegar íhlutur hefur verið skilgreint er hægt að nota í mörg framleiðslulíkön.</span><span class="sxs-lookup"><span data-stu-id="b521d-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="b521d-144">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b521d-144">Select **Save**.</span></span>
9. <span data-ttu-id="b521d-145">Veljið **Upplýsingar um uppskriftarlínu**.</span><span class="sxs-lookup"><span data-stu-id="b521d-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="b521d-146">Upplýsingar um uppskriftalínuskjámyndina gera notandanum kleift að velja viðeigandi eiginleika fyrir undiríhlutina.</span><span class="sxs-lookup"><span data-stu-id="b521d-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="b521d-147">Hægt er að gefa hverjum eiginleika fast gildi eða varpa honum á eigind.</span><span class="sxs-lookup"><span data-stu-id="b521d-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="b521d-148">Að varpa á eigind leiðir til að Uppskrift línueiginleika fær mismunandi gildi eftir því hvað var valið í skilgreiningarhlutanum.</span><span class="sxs-lookup"><span data-stu-id="b521d-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="b521d-149">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="b521d-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b521d-150">Hver undirþáttagerð táknar skilgreinanleg afurðarsniðmát með skorðuskilgreiningartækni.</span><span class="sxs-lookup"><span data-stu-id="b521d-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="b521d-151">Tilvísun er gerð með vörunúmeri.</span><span class="sxs-lookup"><span data-stu-id="b521d-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="b521d-152">Veljið gátreitinn **Stilla**.</span><span class="sxs-lookup"><span data-stu-id="b521d-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="b521d-153">Velja skal **Já** í reitnum **Útreikningur**.</span><span class="sxs-lookup"><span data-stu-id="b521d-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="b521d-154">Stilla valkost útreiknings tryggir að afurðin verða teknar með við útreikning kostnaðar fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="b521d-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="b521d-155">Veljið flipann **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="b521d-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="b521d-156">Veljið gátreitinn **Stilla**.</span><span class="sxs-lookup"><span data-stu-id="b521d-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="b521d-157">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="b521d-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="b521d-158">Magn svæðið ákvarðar hversu mikið þessarar afurðar verður að nota í skilgreindu vörunni.</span><span class="sxs-lookup"><span data-stu-id="b521d-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="b521d-159">Veljið gátreitinn **Stilla**.</span><span class="sxs-lookup"><span data-stu-id="b521d-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="b521d-160">Í reitinn **Á raðir** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="b521d-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="b521d-161">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b521d-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]