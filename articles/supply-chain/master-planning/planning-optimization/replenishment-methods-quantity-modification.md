---
title: Áfyllingaraðferðir og magnbreyting
description: Í þessu efnisatriði er að finna upplýsingar um áfyllingaraðferðir í fínstillingu skipulagningar. Þar er einnig útskýrt hvernig margs konar pöntunarmagn fyrir afurð hefur áhrif á niðurstöðuna.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261697"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="6a101-104">Áfyllingaraðferðir og magnbreyting</span><span class="sxs-lookup"><span data-stu-id="6a101-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a101-105">Í þessu efnisatriði er að finna upplýsingar um áfyllingaraðferðir í fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="6a101-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="6a101-106">Þar er einnig útskýrt hvernig margs konar pöntunarmagn fyrir afurð hefur áhrif á niðurstöðuna.</span><span class="sxs-lookup"><span data-stu-id="6a101-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="6a101-107">Áfyllingaraðferðir eru einnig þekktar sem þekjuaðferðir og lotustærðaraðferðir.</span><span class="sxs-lookup"><span data-stu-id="6a101-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="6a101-108">Þekjukóðar</span><span class="sxs-lookup"><span data-stu-id="6a101-108">Coverage codes</span></span>

<span data-ttu-id="6a101-109">Hægt er að stilla fínstillingu skipulagningar þannig að hún noti aðrar áfyllingaraðferðir.</span><span class="sxs-lookup"><span data-stu-id="6a101-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="6a101-110">Áfyllingaraðferðir eru leið sem kerfið notar til að reikna út þarfir fyrir afurð.</span><span class="sxs-lookup"><span data-stu-id="6a101-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="6a101-111">Áfyllingaraðferðir eru skilgreindar af þekjukóðum sem hægt er að setja upp í annaðhvort þekjuflokknum eða afurðinni.</span><span class="sxs-lookup"><span data-stu-id="6a101-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="6a101-112">Hægt er að nota eftirfarandi þekjukóða í fínstillingu skipulagningar:</span><span class="sxs-lookup"><span data-stu-id="6a101-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="6a101-113">**Tímabil** – Áfyllingaraðferðin sameinar alla eftirspurn fyrir tímabil í eina pöntun fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="6a101-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="6a101-114">Pöntunin verður áætluð fyrir fyrsta dag tímabilsins og magn hennar mun uppfylla nettóþarfir á settu tímabili.</span><span class="sxs-lookup"><span data-stu-id="6a101-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="6a101-115">Tímabilið hefst á fyrstu eftirspurn eftir afurðinni og nær yfir skilgreinda tímalengd.</span><span class="sxs-lookup"><span data-stu-id="6a101-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="6a101-116">Næsta tímabil hefst með næstu þörfum eftir afurðinni.</span><span class="sxs-lookup"><span data-stu-id="6a101-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="6a101-117">Þekjukóði *tímabilsins* er oft notaður fyrir ófyrirsjáanlega birgðanotkun, árstíðabundnar afurðir eða dýrar afurðir.</span><span class="sxs-lookup"><span data-stu-id="6a101-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="6a101-118">Eftirfarandi skýringarmynd sýnir dæmi.</span><span class="sxs-lookup"><span data-stu-id="6a101-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="6a101-119">![Dæmi um notkun tímabilsþekjukóða](./media/coverage-code-period.png "Dæmi um notkun tímabilsþekjukóða")</span><span class="sxs-lookup"><span data-stu-id="6a101-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="6a101-120">**Þörf** – Í áfyllingaraðferðinni stofnar kerfið áætlaða innkaupa-, flutnings- eða framleiðslupöntun eftir þörfum afurðarinnar.</span><span class="sxs-lookup"><span data-stu-id="6a101-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="6a101-121">Þessi aðferð er notuð fyrir dýrar afurðir þar sem eftirspurnin er breytileg.</span><span class="sxs-lookup"><span data-stu-id="6a101-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="6a101-122">Þekjukóði *þarfa* er oft notaður í aðstæðum stillanlegrar afurðar eða framleiðslu eftir pöntun.</span><span class="sxs-lookup"><span data-stu-id="6a101-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="6a101-123">Eftirfarandi skýringarmynd sýnir dæmi.</span><span class="sxs-lookup"><span data-stu-id="6a101-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="6a101-124">![Dæmi um notkun á þekjukóða þarfa](./media/coverage-code-requirement.png "Dæmi um notkun á þekjukóða þarfa")</span><span class="sxs-lookup"><span data-stu-id="6a101-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="6a101-125">**Lágm./Hám.**</span><span class="sxs-lookup"><span data-stu-id="6a101-125">**Min./Max.**</span></span> <span data-ttu-id="6a101-126">– Áfyllingaraðferðin byggir á birgðastöðunni.</span><span class="sxs-lookup"><span data-stu-id="6a101-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="6a101-127">Hún skilgreinir áfyllingu birgða upp að tilteknu stigi þegar fyrirséð lagerstaða er undir tilteknum þröskuldi.</span><span class="sxs-lookup"><span data-stu-id="6a101-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="6a101-128">Áfyllingarmagnið verður munurinn á milli hámarksstigs og spáðs stigs lagermagns.</span><span class="sxs-lookup"><span data-stu-id="6a101-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="6a101-129">*Lágm./hám.*</span><span class="sxs-lookup"><span data-stu-id="6a101-129">The *Min./Max.*</span></span> <span data-ttu-id="6a101-130">þekjukóðinn er oft notaður fyrir fyrirséða birgðanotkun, vinsælar afurðir eða ódýrari afurðir.</span><span class="sxs-lookup"><span data-stu-id="6a101-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="6a101-131">Eftirfarandi skýringarmynd sýnir dæmi.</span><span class="sxs-lookup"><span data-stu-id="6a101-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="6a101-132">![Dæmi um notkun á þekjukóða lágm./hám.](./media/coverage-code-min-max.png "Dæmi um notkun á þekjukóða lágm./hám.")</span><span class="sxs-lookup"><span data-stu-id="6a101-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="6a101-133">**Handvirkt** – Í áfyllingaraðferðinni stingur kerfið ekki upp á innkaupa-, flutnings- eða framleiðslupöntun fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="6a101-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="6a101-134">Í staðinn er skipuleggjandi afurðarinnar ábyrgur fyrir stofnun nauðsynlegra pantana vegna áfyllingar afurðar.</span><span class="sxs-lookup"><span data-stu-id="6a101-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="6a101-135">*Handvirkur* þekjukóði er oft notaður fyrir afurðir þar sem áætlaðar pantanir myndaðar af kerfinu eru óþarfar.</span><span class="sxs-lookup"><span data-stu-id="6a101-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="6a101-136">Áhrif á pöntunarmagn úr sjálfgefnum pöntunarstillingum</span><span class="sxs-lookup"><span data-stu-id="6a101-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="6a101-137">Á síðunni **Sjálfgefin pöntunarstilling** fyrir losaða afurð er hægt að tilgreina hverja af eftirfarandi pöntunarstillingum í flýtiflipunum **Innkaupapöntun**, **Birgðir** og **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="6a101-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="6a101-138">(Flýtiflipinn **Birgðir** er notaður fyrir bæði flutningspantanir og framleiðslupantanir.)</span><span class="sxs-lookup"><span data-stu-id="6a101-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="6a101-139">**Margfeldi** – Áætlaðar pantanir verða margfeldi af þessu magni.</span><span class="sxs-lookup"><span data-stu-id="6a101-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="6a101-140">Ef til dæmis reiturinn **Margfeldi** er stilltur á *5* getur pöntun verið fyrir magnið 5, 10, 15, 20 og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="6a101-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="6a101-141">**Lágmarksmagn pöntunar** – Áætlaðar pantanir verða ekki minna en tilgreint gildi.</span><span class="sxs-lookup"><span data-stu-id="6a101-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="6a101-142">Ef til dæmis reiturinn **Lágmarksmagn pöntunar** er stillt á *10* verður áætluð pöntun með magnið 10 stofnuð þótt aðeins magn upp á fjórir sé nauðsynlegt til að anna eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="6a101-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="6a101-143">**Hámarksmagn pöntunar** – Áætlaðar pantanir fara ekki yfir tiltekið gildi.</span><span class="sxs-lookup"><span data-stu-id="6a101-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="6a101-144">Ef eftirspurnin er meiri en gildið í **Hámarksmagn pöntunar** verða stofnaðar margar áætlaðar pantanir til að anna henni.</span><span class="sxs-lookup"><span data-stu-id="6a101-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="6a101-145">Ef til dæmis reiturinn **Hámarksmagn pöntunar** er stilltur á *100* og eftirspurnin er 450 verða stofnaðar fjórar áætlaðar pantanir fyrir magnið 100 og ein áætluð pöntun fyrir magnið 50.</span><span class="sxs-lookup"><span data-stu-id="6a101-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="6a101-146">Dæmi um áfyllingu sem notar hám./lágm.</span><span class="sxs-lookup"><span data-stu-id="6a101-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="6a101-147">þekjukóði</span><span class="sxs-lookup"><span data-stu-id="6a101-147">coverage code</span></span>

<span data-ttu-id="6a101-148">Ef ekkert gildi er tilgreint í reitnum **Margfeldi** fyrir afurð á síðunni **Sjálfgefin pöntunarstilling** og ef notuð er *Hám./lágm.*</span><span class="sxs-lookup"><span data-stu-id="6a101-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="6a101-149">áfyllingaraðferðin mun fínstilling skipulagningar fylla á birgðirnar upp að tiltekinni stöðu þegar spáð lagerstaða er undir tilteknum þröskuldi.</span><span class="sxs-lookup"><span data-stu-id="6a101-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="6a101-150">Ef skilgreint er meira en eitt magn fyrir afurð mun *Hám./lágm.*</span><span class="sxs-lookup"><span data-stu-id="6a101-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="6a101-151">áfyllingaraðferðin breyta hegðun sinni og taka til greina gildið **Margfeldi**.</span><span class="sxs-lookup"><span data-stu-id="6a101-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="6a101-152">Með öðrum orðum mun fínstilling skipulagningar ennþá fylla á birgðirnar upp að skilgreindri hámarksstöðu þegar spáð lagerstaða er minni en skilgreind lágmarksstaða.</span><span class="sxs-lookup"><span data-stu-id="6a101-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="6a101-153">Hinsvegar verður áfyllingarmagnið að vera margfeldi af gildinu **Margfeldi**.</span><span class="sxs-lookup"><span data-stu-id="6a101-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="6a101-154">Ef áfyllingarmagnið (munurinn á hámarksstöðu og spáðri lagerstöðu) er ekki margfeldi af skilgreindu margfeldismagni, notar fínstilling skipulagningar fyrsta mögulega gildið sem, ásamt spáðri lagerstöðu, verður undir hámarksstöðunni.</span><span class="sxs-lookup"><span data-stu-id="6a101-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="6a101-155">Ef samtalan er minni en lágmarksstaðan notar fínstilling skipulagningar fyrsta gildið sem, ásamt spáðri lagerstöðu, verðu fyrir ofan hámarksstöðuna.</span><span class="sxs-lookup"><span data-stu-id="6a101-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="6a101-156">Eftirfarandi undirhlutar sýna dæmi um hvernig margfeldi af pöntunarmagni fyrir afurð hefur áhrif á niðurstöðuna fyrir *Lágm./hám.*</span><span class="sxs-lookup"><span data-stu-id="6a101-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="6a101-157">áfyllingaraðferð.</span><span class="sxs-lookup"><span data-stu-id="6a101-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="6a101-158">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="6a101-158">Example 1</span></span>

<span data-ttu-id="6a101-159">Afurð er með eftirfarandi skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="6a101-159">A product has the following configuration:</span></span>

- <span data-ttu-id="6a101-160">**Þekjukóði:** *Lágm./hám.*</span><span class="sxs-lookup"><span data-stu-id="6a101-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="6a101-161">**Lágmark:** *15*</span><span class="sxs-lookup"><span data-stu-id="6a101-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="6a101-162">**Hámark:** *22*</span><span class="sxs-lookup"><span data-stu-id="6a101-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="6a101-163">**Margfalt:** *0*</span><span class="sxs-lookup"><span data-stu-id="6a101-163">**Multiple:** *0*</span></span>

<span data-ttu-id="6a101-164">Það eru 10 stykki á lager af afurðinni og það er engin önnur eftirspurn eða framboð.</span><span class="sxs-lookup"><span data-stu-id="6a101-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="6a101-165">Þegar aðaláætlanagerð er keyrð verður áætluð pöntun fyrir 12 stykkjum stofnuð til að fylla á birgðirnar upp í hámarksmagnið.</span><span class="sxs-lookup"><span data-stu-id="6a101-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="6a101-166">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="6a101-166">Example 2</span></span>

<span data-ttu-id="6a101-167">Afurð er með eftirfarandi skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="6a101-167">A product has the following configuration:</span></span>

- <span data-ttu-id="6a101-168">**Þekjukóði:** *Lágm./hám.*</span><span class="sxs-lookup"><span data-stu-id="6a101-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="6a101-169">**Lágmark:** *15*</span><span class="sxs-lookup"><span data-stu-id="6a101-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="6a101-170">**Hámark:** *22*</span><span class="sxs-lookup"><span data-stu-id="6a101-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="6a101-171">**Margfalt:** *5*</span><span class="sxs-lookup"><span data-stu-id="6a101-171">**Multiple:** *5*</span></span>

<span data-ttu-id="6a101-172">Það eru 10 stykki á lager af afurðinni og það er engin önnur eftirspurn eða framboð.</span><span class="sxs-lookup"><span data-stu-id="6a101-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="6a101-173">Þegar aðaláætlanagerð er keyrð verður áætluð pöntun upp á 10 stykki stofnuð (vegna þess að 15 stykki af áfyllingu ásamt 10 stykkjum af lagerbirgðum fara yfir hámarksmagnið).</span><span class="sxs-lookup"><span data-stu-id="6a101-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="6a101-174">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="6a101-174">Example 3</span></span>

<span data-ttu-id="6a101-175">Afurð er með eftirfarandi skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="6a101-175">A product has the following configuration:</span></span>

- <span data-ttu-id="6a101-176">**Þekjukóði:** *Lágm./hám.*</span><span class="sxs-lookup"><span data-stu-id="6a101-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="6a101-177">**Lágmark:** *21*</span><span class="sxs-lookup"><span data-stu-id="6a101-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="6a101-178">**Hámark:** *24*</span><span class="sxs-lookup"><span data-stu-id="6a101-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="6a101-179">**Margfalt:** *5*</span><span class="sxs-lookup"><span data-stu-id="6a101-179">**Multiple:** *5*</span></span>

<span data-ttu-id="6a101-180">Það eru 10 stykki á lager af afurðinni og það er engin önnur eftirspurn eða framboð.</span><span class="sxs-lookup"><span data-stu-id="6a101-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="6a101-181">Þegar aðaláætlanagerð er keyrð verður áætluð pöntun upp á 15 stykki stofnuð (vegna þess að 10 stykki af áfyllingu ásamt 10 stykkjum af lagerbirgðum fara undir lágmarksmagnið).</span><span class="sxs-lookup"><span data-stu-id="6a101-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
