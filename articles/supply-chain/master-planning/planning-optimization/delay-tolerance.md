---
title: Vikmörk tafar (neikvæður dagafjöldi)
description: Í þessu efnisatriði er að finna upplýsingar um útreikning á vikmörkum tafar og hvernig það hefur áhrif á áætlaða stofnun pöntunar í fínstillingu skipulagningar.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306464"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="c969d-103">Vikmörk tafar (neikvæður dagafjöldi)</span><span class="sxs-lookup"><span data-stu-id="c969d-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="c969d-104">Virkni vikmarka tafar gerir fínstillingu skipulagningar kleift að taka til greina gildið fyrir **Neikvæðan dagafjölda** sem er stillt fyrir þekjuflokka.</span><span class="sxs-lookup"><span data-stu-id="c969d-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="c969d-105">Hún er notuð til að víkka út tímabil vikmarka tafar sem er notað í aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="c969d-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="c969d-106">Þannig er hægt að komast hjá því að stofna nýjar framboðspantanir ef fyrirliggjandi framboð getur annað eftirspurn eftir stutta töf.</span><span class="sxs-lookup"><span data-stu-id="c969d-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="c969d-107">Tilgangur virkninnar er að ákveða hvort skynsamlegt sé að búa til nýja framboðspöntun fyrir tiltekna eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="c969d-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="c969d-108">Kveikja á eiginleikanum í kerfinu</span><span class="sxs-lookup"><span data-stu-id="c969d-108">Turn on the feature in your system</span></span>

<span data-ttu-id="c969d-109">Til að gera virkni fyrir vikmörk tafar aðgengilega í kerfinu skal fara í [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Neikvæður dagafjöldi fyrir fínstillingu skipulagningar*.</span><span class="sxs-lookup"><span data-stu-id="c969d-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="c969d-110">Vikmörk tafar í fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="c969d-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="c969d-111">Vikmörk tafar sýnir fjölda daga fram yfir afhendingartímann sem þú ert til í að bíða áður en þú pantar nýja áfyllingu þegar fyrirliggjandi framboð er þegar áætlað.</span><span class="sxs-lookup"><span data-stu-id="c969d-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="c969d-112">Vikmörk tafar eru skilgreind með því að nota almanaksdaga, ekki viðskiptadaga.</span><span class="sxs-lookup"><span data-stu-id="c969d-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="c969d-113">Við aðaláætlanagerð, þegar kerfið reiknar út vikmörk tafar, tekur hún til greina stillinguna **Neikvæður dagafjöldi**.</span><span class="sxs-lookup"><span data-stu-id="c969d-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="c969d-114">Hægt er að stilla gildið **Neikvæður dagafjöldi** á annaðhvort síðunni **Þekjuflokkar** eða síðunni **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="c969d-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="c969d-115">Kerfið tengir útreikning á vikmörkum tafar við *fyrstu áfyllingardagsetninguna*, sem jafngildir deginum í dag að viðbættum afhendingartímanum.</span><span class="sxs-lookup"><span data-stu-id="c969d-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="c969d-116">Vikmörk tafar eru reiknuð út með því að nota eftirfarandi formúlu þar sem *hámark()* finnur stærra gildið af gildunum tveimur:</span><span class="sxs-lookup"><span data-stu-id="c969d-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="c969d-117">*hámark(Fyrsti áfyllingardagur, lokadagur eftirspurnar)* – *Lokadagur eftirspurnar* + *Neikvæður dagafjöldi*</span><span class="sxs-lookup"><span data-stu-id="c969d-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="c969d-118">Þessi formúla tryggir að aðaláætlanagerð búi ekki til nýjar framboðspantanir þegar næg eftirspurn er til meðan afhendingartími afurðar er í gangi.</span><span class="sxs-lookup"><span data-stu-id="c969d-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="c969d-119">Útreikningur vikmarka tafar í fínstillingu skipulagningar notar alltaf útreikning kvikra neikvæðra daga úr innbyggðu aðaláætlanagerðinni.</span><span class="sxs-lookup"><span data-stu-id="c969d-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="c969d-120">Stillingin **Nota kvika neikvæða daga** á síðunni **Færibreytur aðaláætlanagerðar** hefur engin áhrif á þessa hegðun.</span><span class="sxs-lookup"><span data-stu-id="c969d-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="c969d-121">Ef fyrirliggjandi framboð felur í sér töfum á eftirspurn sem er minni en eða jafnt og reiknuð vikmörk tafar, bindur fínstilling skipulagningar fyrirliggjandi framboð við eftirspurnina.</span><span class="sxs-lookup"><span data-stu-id="c969d-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="c969d-122">Í sumum tilfellum er betra að fresta eftirspurninni en að enda með offramboð.</span><span class="sxs-lookup"><span data-stu-id="c969d-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="c969d-123">Í eftirfarandi undirhlutum eru dæmi sem sýna hvernig vikmörk tafar hafa áhrif á gerð áætlaðra pantana í fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="c969d-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="c969d-124">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="c969d-124">Example 1</span></span>

<span data-ttu-id="c969d-125">Afurð er með eftirfarandi skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="c969d-125">A product has the following configuration:</span></span>

- <span data-ttu-id="c969d-126">**Afhendingartími:** *10*</span><span class="sxs-lookup"><span data-stu-id="c969d-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="c969d-127">**Neikvæður dagafjöldi:** *2*</span><span class="sxs-lookup"><span data-stu-id="c969d-127">**Negative days:** *2*</span></span>

<span data-ttu-id="c969d-128">Eftirfarandi framboð og eftirspurn er til fyrir afurðina:</span><span class="sxs-lookup"><span data-stu-id="c969d-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="c969d-129">**Eftirspurn fyrir daginn í dag:** Sölupöntun fyrir magnið 10</span><span class="sxs-lookup"><span data-stu-id="c969d-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="c969d-130">**Birgðir eftir 12 daga:** Innkaupapöntun fyrir magnið 10</span><span class="sxs-lookup"><span data-stu-id="c969d-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="c969d-131">Núverandi framboð getur tryggt eftirspurnina innan 12 daga og það tímabil jafngildir vikmörkum tafa.</span><span class="sxs-lookup"><span data-stu-id="c969d-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="c969d-132">Þegar aðaláætlanagerð er keyrð eru því engar áætlaðar pantanir stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="c969d-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="c969d-133">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="c969d-133">Example 2</span></span>

<span data-ttu-id="c969d-134">Afurð er með eftirfarandi skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="c969d-134">A product has the following configuration:</span></span>

- <span data-ttu-id="c969d-135">**Afhendingartími:** *10*</span><span class="sxs-lookup"><span data-stu-id="c969d-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="c969d-136">**Neikvæður dagafjöldi:** *0*</span><span class="sxs-lookup"><span data-stu-id="c969d-136">**Negative days:** *0*</span></span>

<span data-ttu-id="c969d-137">Eftirfarandi framboð og eftirspurn er til fyrir afurðina:</span><span class="sxs-lookup"><span data-stu-id="c969d-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="c969d-138">**Eftirspurn fyrir daginn í dag:** Sölupöntun fyrir magnið 10</span><span class="sxs-lookup"><span data-stu-id="c969d-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="c969d-139">**Birgðir eftir 12 daga:** Innkaupapöntun fyrir magnið 10</span><span class="sxs-lookup"><span data-stu-id="c969d-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="c969d-140">Núverandi framboð getur aðeins annað eftirspurn eftir 12 daga.</span><span class="sxs-lookup"><span data-stu-id="c969d-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="c969d-141">Hins vegar eru vikmörk tafa 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="c969d-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="c969d-142">Þegar aðaláætlanagerð er keyrð er því áætluð pöntun fyrir magnið 10 stofnuð.</span><span class="sxs-lookup"><span data-stu-id="c969d-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="c969d-143">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="c969d-143">Example 3</span></span>

<span data-ttu-id="c969d-144">Afurð er með eftirfarandi skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="c969d-144">A product has the following configuration:</span></span>

- <span data-ttu-id="c969d-145">**Afhendingartími:** *10*</span><span class="sxs-lookup"><span data-stu-id="c969d-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="c969d-146">**Neikvæður dagafjöldi:** *2*</span><span class="sxs-lookup"><span data-stu-id="c969d-146">**Negative days:** *2*</span></span>

<span data-ttu-id="c969d-147">Eftirfarandi framboð og eftirspurn er til fyrir afurðina:</span><span class="sxs-lookup"><span data-stu-id="c969d-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="c969d-148">**Eftirspurn eftir 11 daga:** Sölupöntun fyrir magnið 10</span><span class="sxs-lookup"><span data-stu-id="c969d-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="c969d-149">**Birgðir eftir 14 daga:** Innkaupapöntun fyrir magnið 10</span><span class="sxs-lookup"><span data-stu-id="c969d-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="c969d-150">Núverandi framboð getur aðeins annað eftirspurn eftir þrjá daga.</span><span class="sxs-lookup"><span data-stu-id="c969d-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="c969d-151">Hinsvegar eru vikmörk tafar tveir dagar.</span><span class="sxs-lookup"><span data-stu-id="c969d-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="c969d-152">(Í þessu tilviki fela vikmörk tafa aðeins í sér neikvæðu dagana tvo.</span><span class="sxs-lookup"><span data-stu-id="c969d-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="c969d-153">Eftirspurnardagurinn er ekki hafður með vegna þess að hann kemur á eftir afhendingartíma afurðar.) Þegar aðaláætlanagerð er keyrð er því áætluð pöntun fyrir magnið 10 stofnuð.</span><span class="sxs-lookup"><span data-stu-id="c969d-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
