---
title: Öryggismörk
description: Þetta efnisatriði lýsir því hvernig hægt er að nota öryggismörk með innbót fínstillingar á skipulagningu fyrir Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8ab5f1c3cdfa990a73951ddc5a7469644954d5c2
ms.sourcegitcommit: 646a0e7c8b8a7f2d00a50eddfa65500d0f8afbaf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/15/2020
ms.locfileid: "3814901"
---
# <a name="safety-margins"></a><span data-ttu-id="7bb95-103">Öryggismörk</span><span class="sxs-lookup"><span data-stu-id="7bb95-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7bb95-104">Þetta efnisatriði lýsir því hvernig hægt er að nota öryggismörk með innbót fínstillingar á skipulagningu fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7bb95-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="7bb95-105">Yfirlit yfir öryggismörk</span><span class="sxs-lookup"><span data-stu-id="7bb95-105">Safety margins overview</span></span>

<span data-ttu-id="7bb95-106">Tilgangurinn með öryggismörkum er að virkja uppsetningu sem býður upp á einhvern skipulagstíma utan venjulegs afhendingartíma.</span><span class="sxs-lookup"><span data-stu-id="7bb95-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="7bb95-107">Þegar þarf til dæmis að taka hráefni úr pakkningu eða skoða það þegar það kemur frá lánardrottni, er ekki einfaldlega hægt að bæta aukatímanum við afhendingartíma innkaupanna, því að aukalegi skipulagstíminn fer þá til birgja.</span><span class="sxs-lookup"><span data-stu-id="7bb95-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="7bb95-108">Í þessu dæmi er hægt að nota innhreyfingarmörkin til að tryggja að birginn afhendi á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="7bb95-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="7bb95-109">Þessi nálgun býður upp á skipulagstíma þannig að hægt sé að afgreiða varninginn innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="7bb95-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="7bb95-110">Það eru þrjár gerðir öryggismarka:</span><span class="sxs-lookup"><span data-stu-id="7bb95-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="7bb95-111">**Endurpöntunarmörk** – Skipulagstíminn til að leggja fram birgðapöntun</span><span class="sxs-lookup"><span data-stu-id="7bb95-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="7bb95-112">**Innhreyfingarmörk** – Skipulagstíminn til að afgreiða birgðir á innleið</span><span class="sxs-lookup"><span data-stu-id="7bb95-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="7bb95-113">**Úthreyfingarmörk** – Skipulagstíminn til að afgreiða sendingar</span><span class="sxs-lookup"><span data-stu-id="7bb95-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="7bb95-114">Eftirfarandi mynd sýnir hvernig þessi öryggismörk eiga við yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="7bb95-114">The following illustration shows how these safety margins apply over time.</span></span>

![Öryggismörk](media/safety-margins-1.png)

<span data-ttu-id="7bb95-116">Öll mörk eru skilgreind í dögum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-116">All margins are defined in days.</span></span> <span data-ttu-id="7bb95-117">Sjálfgefið gildi, *0* (núll), gefur til kynna að engin mörk eru notuð.</span><span class="sxs-lookup"><span data-stu-id="7bb95-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="7bb95-118">Ef mörg mörk eru sett upp, bætast þau öll við heildartímann frá *pöntunardagsetningu* birgða til *þarfadagsetningar* eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="7bb95-119">Til dæmis er uppsetning ekki með neinn afhendingartíma og allar þrjár gerðirnar af mörkum eru stilltar á einn dag.</span><span class="sxs-lookup"><span data-stu-id="7bb95-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="7bb95-120">Í slíku tilfelli verða þrír dagar á milli dagsetningar birgðapöntunar og þarfadagsetningar eftirspurnar, þannig að ef pöntunardagsetningin er 1. júlí verður dagsetning þarfa 4. júlí.</span><span class="sxs-lookup"><span data-stu-id="7bb95-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="7bb95-121">Mörk innhreyfinga</span><span class="sxs-lookup"><span data-stu-id="7bb95-121">Receipt margin</span></span>

<span data-ttu-id="7bb95-122">Mörk innhreyfinga er líklega mest notuð af öllum þremur öryggismörkunum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="7bb95-123">Þau eru notuð fyrir *afhendingardaginn* og aftur á bak frá *dagsetningu þarfa*.</span><span class="sxs-lookup"><span data-stu-id="7bb95-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="7bb95-124">Með öðrum orðum ættu afurðirnar að fá tiltekinn dagafjölda fyrir innhreyfingarmörk áður en þess gerist þörf.</span><span class="sxs-lookup"><span data-stu-id="7bb95-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="7bb95-125">Eftirfarandi mynd sýnir mörk innhreyfinga.</span><span class="sxs-lookup"><span data-stu-id="7bb95-125">The following illustration highlights the receipt margin.</span></span>

![Mörk innhreyfinga](media/safety-margins-2.png)

<span data-ttu-id="7bb95-127">Mörk innhreyfinga er yfirleitt notuð sem biðtími til að tryggja að tími gefist til vöruhúsaskráningar eða annarra tímafrekra ferla sem eru ekki hluti af almennum afhendingartíma í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="7bb95-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="7bb95-128">Fyrir innkaup er einn ávinningur sá að *afhendingardagur* innkaupapöntunarinnar er færður fram eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="7bb95-129">Ef afhendingartími er aukinn í stað þess að nota öryggismörk verður lánardrottinn samt beðinn um að afhenda á síðustu stundu.</span><span class="sxs-lookup"><span data-stu-id="7bb95-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="7bb95-130">Takið eftir að mörk innhreyfinga breyta ekki *dagsetningu þarfa* fyrir birgðirnar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="7bb95-131">Þess vegna eru mörk innhreyfinga ekki sýnileg með beinum hætti þegar dagsetningar þarfa fyrir eftirspurn og framboð eru borin saman (til dæmis á síðunni **Nettó þarfir**).</span><span class="sxs-lookup"><span data-stu-id="7bb95-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="7bb95-132">Ef mörk innhreyfinga eru t.d. stillt á fjóra daga og innkaupapöntunarlína er áætluð til innhreyfingar þann fimmtánda þess mánaðar, mun aðaláætlanagerðin reikna út að leiðrétt dagsetning innhreyfingar verði þann nítjánda þess mánaðar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="7bb95-133">Athugið að mörk innhreyfinga eru ekki notuð þegar lagerbirgðir eru notaðir sem birgðir.</span><span class="sxs-lookup"><span data-stu-id="7bb95-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="7bb95-134">Gert er ráð fyrir að allar lagerbirgðir séu lausar strax, óháð því hvenær þær voru mótteknar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="7bb95-135">Endurpöntunarmörk</span><span class="sxs-lookup"><span data-stu-id="7bb95-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="7bb95-136">**Kemur fljótlega:** Þessi eiginleiki er ekki enn studdur fyrir fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="7bb95-137">Þar til hann er studdur eru öll gildi sem eru færð inn fyrir **Endurpöntunarmagni bætt við afhendingartíma vöru** meðhöndluð sem *0* (núll).</span><span class="sxs-lookup"><span data-stu-id="7bb95-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="7bb95-138">Eftirfarandi mynd sýnir endurpöntunarmörkin.</span><span class="sxs-lookup"><span data-stu-id="7bb95-138">The following illustration highlights the reorder margin.</span></span>

![Endurpöntunarmörk](media/safety-margins-3.png)

<span data-ttu-id="7bb95-140">Endurpöntunarmörkum er bætt við á undan afhendingartíma vörunnar fyrir allar áætlaðar pantanir á meðan aðaláætlanagerð stendur.</span><span class="sxs-lookup"><span data-stu-id="7bb95-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="7bb95-141">Þess vegna tryggir það frekari tíma til að leggja fram birgðapöntun.</span><span class="sxs-lookup"><span data-stu-id="7bb95-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="7bb95-142">Þessi mörk eru yfirleitt notuð sem biðtími til að tryggja tíma fyrir samþykktarferli eða aðra innri ferla sem eru nauðsynlegir við stofnun birgðapantana.</span><span class="sxs-lookup"><span data-stu-id="7bb95-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="7bb95-143">Endurpöntunarmörkin eru sett á milli *pöntunardagsetningar* birgða og *upphafsdagsetningar*.</span><span class="sxs-lookup"><span data-stu-id="7bb95-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="7bb95-144">Mörk úthreyfinga</span><span class="sxs-lookup"><span data-stu-id="7bb95-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="7bb95-145">**Kemur fljótlega:** Þessi eiginleiki er ekki enn studdur fyrir fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="7bb95-146">Þar til hann er studdur eru öll gildi sem eru færð inn fyrir **Mörk úthreyfinga dregin af dagsetningu þarfa** meðhöndluð sem *0* (núll).</span><span class="sxs-lookup"><span data-stu-id="7bb95-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="7bb95-147">Eftirfarandi mynd sýnir mörk úthreyfinga.</span><span class="sxs-lookup"><span data-stu-id="7bb95-147">The following illustration highlights the issue margin.</span></span>

![Mörk úthreyfinga](media/safety-margins-4.png)

<span data-ttu-id="7bb95-149">Mörk úthreyfinga eru dregin frá eftirspurnardagsetningu þarfa í aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="7bb95-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="7bb95-150">Það tryggir að þú hafir tíma til að bregðast við og senda eftirspurnarpantanir á innleið.</span><span class="sxs-lookup"><span data-stu-id="7bb95-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="7bb95-151">Þessi mörk eru yfirleitt notuð sem biðtími til að tryggja tíma fyrir sendingu og tengda vöruhúsaferli á útleið.</span><span class="sxs-lookup"><span data-stu-id="7bb95-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="7bb95-152">Taktu eftir því að þegar mörk úthreyfinga eru notuð, passa tengdar þarfadagsetningar framboðs og eftirspurnar ekki saman.</span><span class="sxs-lookup"><span data-stu-id="7bb95-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="7bb95-153">Í staðinn er munurinn á milli þeirra það sem nemur úthreyfingarmörkum vegna þess að úthreyfingarmörkunum er bætt við milli *þarfadagsetningar* framboðs og *þarfadagsetningar* eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="7bb95-154">Setja upp öryggismörk</span><span class="sxs-lookup"><span data-stu-id="7bb95-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="7bb95-155">Kveikja á öryggismörkum í eiginleikastjórnun</span><span class="sxs-lookup"><span data-stu-id="7bb95-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="7bb95-156">Áður en hægt er að nota þennan eiginleiki með fínstillingu skipulagningar þarf að vera kveikt á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="7bb95-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="7bb95-157">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="7bb95-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7bb95-158">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="7bb95-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7bb95-159">**Eining:** _Aðaláætlanagerð_</span><span class="sxs-lookup"><span data-stu-id="7bb95-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="7bb95-160">**Heiti eiginleika:** _Mörk fyrir fínstillingu skipulagningar_</span><span class="sxs-lookup"><span data-stu-id="7bb95-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="7bb95-161">Skilgreina öryggismörk</span><span class="sxs-lookup"><span data-stu-id="7bb95-161">Define safety margins</span></span>

<span data-ttu-id="7bb95-162">Öryggismörk eru með sveigjanlega uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="7bb95-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="7bb95-163">Hægt er að stilla þau í bæði *þekjuflokki* og *aðaláætlun*.</span><span class="sxs-lookup"><span data-stu-id="7bb95-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="7bb95-164">Mikilvægt er að skilja að mörkin eru lögð ofan á hvert annað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="7bb95-165">Til dæmis ef innhreyfingarmörk eru tveir dagar í þekjuflokknum og þrír dagar í aðaláætlanagerðinni verða til virk innhreyfingarmörk upp á fimm daga.</span><span class="sxs-lookup"><span data-stu-id="7bb95-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="7bb95-166">Möguleikinn á því að stilla mörkin í aðaláætlanagerðinni getur verið gagnlegt þegar þú vilt líkja eftir lengri afhendingartímum eða óvissu fyrir tiltekinni áætlun, en án þess að hafa áhrif á daglega áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="7bb95-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="7bb95-167">Öryggismörk þekjuflokks</span><span class="sxs-lookup"><span data-stu-id="7bb95-167">Coverage group safety margins</span></span>

<span data-ttu-id="7bb95-168">Til að nota öryggismörk í þekjuflokki skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="7bb95-169">Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekjuflokkar**.</span><span class="sxs-lookup"><span data-stu-id="7bb95-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="7bb95-170">Í listasvæðinu skal velja þekjuflokk sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7bb95-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="7bb95-171">Í flýtiflipanum **Annað**, í hlutanum **Öryggismörk í dögum**, skal nota eftirfarandi reiti til að stilla nauðsynleg öryggismörk (í dögum):</span><span class="sxs-lookup"><span data-stu-id="7bb95-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="7bb95-172">Mörk innhreyfinga bætt við dagsetningu þarfa</span><span class="sxs-lookup"><span data-stu-id="7bb95-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="7bb95-173">Mörk úthreyfinga dregin af dagsetningu þarfa</span><span class="sxs-lookup"><span data-stu-id="7bb95-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="7bb95-174">Endurpöntunarmagni bætt við afhendingartíma vöru</span><span class="sxs-lookup"><span data-stu-id="7bb95-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="7bb95-175">Öryggismörk aðaláætlunar</span><span class="sxs-lookup"><span data-stu-id="7bb95-175">Master plan safety margins</span></span>

<span data-ttu-id="7bb95-176">Til að nota öryggismörk við aðaláætlun skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="7bb95-177">Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.</span><span class="sxs-lookup"><span data-stu-id="7bb95-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="7bb95-178">Í listasvæðinu skal velja aðaláætlun sem óskar er eftir.</span><span class="sxs-lookup"><span data-stu-id="7bb95-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="7bb95-179">Í flýtiflipanum **Öryggismörk í dögum** skal nota eftirfarandi reiti til að stilla nauðsynleg öryggismörk (í dögum):</span><span class="sxs-lookup"><span data-stu-id="7bb95-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="7bb95-180">Mörk innhreyfinga bætt við dagsetningu þarfa</span><span class="sxs-lookup"><span data-stu-id="7bb95-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="7bb95-181">Mörk úthreyfinga dregin af dagsetningu þarfa</span><span class="sxs-lookup"><span data-stu-id="7bb95-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="7bb95-182">Endurpöntunarmagni bætt við afhendingartíma vöru</span><span class="sxs-lookup"><span data-stu-id="7bb95-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="7bb95-183">Skilgreina hvort útreikningar eru byggðir á almanaksdögum eða vinnudögum</span><span class="sxs-lookup"><span data-stu-id="7bb95-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="7bb95-184">Hægt er að stilla öll öryggismörk þannig að þau séu reiknuð út frá annaðhvort almanaksdögum eða vinnudögum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="7bb95-185">Farið í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**.</span><span class="sxs-lookup"><span data-stu-id="7bb95-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="7bb95-186">Í flipanum **Almennt**, í hlutanum **Öryggismörk í dögum**, skal stilla valkostinn **Vinnudagar** á *Já* til að reikna mörk sem byggja á vinnudögum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="7bb95-187">Stillið valkostinn á *Nei* til að reikna út mörk samkvæmt almanaksdögum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="7bb95-188">Til dæmis er dagatal opið frá mánudegi til föstudags og lokað frá laugardegi til sunnudags.</span><span class="sxs-lookup"><span data-stu-id="7bb95-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="7bb95-189">Ef um er að ræða innhreyfingarmörk upp á einn dag, mun þarfadagsetning á mánudegi búa til afhendingardag á föstudeginum á undan, því að laugardagur og sunnudagur eru ekki vinnudagar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="7bb95-190">Dagatalið sem er notað til að ákvarða vinnudagana veltur á uppsetningu og gerð framboðs..</span><span class="sxs-lookup"><span data-stu-id="7bb95-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="7bb95-191">Hægt er að stýra því með dagatölum þekjuflokksins, vöruhússins og lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="7bb95-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="7bb95-192">Ef *vöruhús* er ekki hluti af þekjuvíddinni (með öðrum orðum, áætlun byggir aðeins á *svæði*), er dagatal vöruhússins ekki notað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="7bb95-193">Kerfið ræður við uppsetningu þar sem eitt eða fleiri dagatöl eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="7bb95-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="7bb95-194">Eftirfarandi undirhlutar lýsa mögulegum samsetningum sem hægt er að nota til að hafa stjórnun á niðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="7bb95-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="7bb95-195">Dagatal sem er notað við lengd</span><span class="sxs-lookup"><span data-stu-id="7bb95-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="7bb95-196">Skilgreindu dagatölin stýra raunverulegum heildartíma afhendingar í almanaksdögum, frá dagsetningu birgðapöntunar til þarfadagsetningar eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="7bb95-197">Eftirfarandi forgangsröðun dagatals er notuð:</span><span class="sxs-lookup"><span data-stu-id="7bb95-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="7bb95-198">**Afhendingartími innkaupa** – Aðeins er stuðst við dagatal þekjuflokks.</span><span class="sxs-lookup"><span data-stu-id="7bb95-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="7bb95-199">**Mörk innhreyfinga** – Dagatal þekjuflokksins er notað, ef það er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="7bb95-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="7bb95-200">Annars er dagatal vöruhúss notað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="7bb95-201">**Mörk úthreyfinga** – Dagatal þekjuflokksins er notað, ef það er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="7bb95-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="7bb95-202">Annars er dagatal vöruhúss notað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="7bb95-203">**Pöntunarmörk** – Aðeins er stuðst við dagatal þekjuflokks.</span><span class="sxs-lookup"><span data-stu-id="7bb95-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="7bb95-204">Dagatal sem er notað fyrir lokadagsetninguna</span><span class="sxs-lookup"><span data-stu-id="7bb95-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="7bb95-205">Eftirfarandi reglur eru notaðar til að ákvarða hvort áætlunarvélin geti notað tiltekna dagsetningu fyrir tiltekna dagsetningargerð:</span><span class="sxs-lookup"><span data-stu-id="7bb95-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="7bb95-206">**Dagsetning á innhreyfingu innkaupa** – Dagatal lánardrottins er notað, ef það er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="7bb95-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="7bb95-207">Annars er dagatal þekjuflokksins notað, ef það er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="7bb95-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="7bb95-208">Ef hvorugt dagatanna er skilgreint er dagatal vöruhúss notað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="7bb95-209">**Innhreyfingardagsetning flutnings** – Dagatal þekjuflokksins er notað, ef það er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="7bb95-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="7bb95-210">Annars er dagatal vöruhúss notað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="7bb95-211">**Innhreyfingardagsetning framleiðslu** – Dagatal þekjuflokksins er notað, ef það er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="7bb95-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="7bb95-212">Annars er dagatal vöruhúss notað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="7bb95-213">**Opinn dagur á úthreyfingu eftirspurnar** – Dagatal vöruhúss er notað, ef það er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="7bb95-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="7bb95-214">Annars er dagatal þekjuflokksins notað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="7bb95-215">**Opinn dagur pöntunar** – Samsetning (sniðmengi) dagatals þekjuflokksins og dagatals lánardrottins er notuð.</span><span class="sxs-lookup"><span data-stu-id="7bb95-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="7bb95-216">Bæði dagatöl verða að vera opin til að nota dagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="7bb95-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="7bb95-217">Ef aðeins eitt af dagatölum er skilgreint er dagatalið notað eitt og sér.</span><span class="sxs-lookup"><span data-stu-id="7bb95-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="7bb95-218">Yfirlit uppsetningar dagatals - fylki</span><span class="sxs-lookup"><span data-stu-id="7bb95-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="7bb95-219">Eftirfarandi mynd sýnir fylki sem tekur saman hvaða dagatöl eiga við þegar öryggismörk eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="7bb95-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="7bb95-220">(Veldu myndina til að opna hana í hágæðum.) Eftirfarandi skammstafanir og litir eru notaðir til að gefa til kynna hvar hver gerð dagatals er tilgreind:</span><span class="sxs-lookup"><span data-stu-id="7bb95-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="7bb95-221">**Þekjuflokkur (ÞF):** Grænn</span><span class="sxs-lookup"><span data-stu-id="7bb95-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="7bb95-222">**Vöruhús (VH):** Gulur</span><span class="sxs-lookup"><span data-stu-id="7bb95-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="7bb95-223">**Lánardrottinn (L):** Blár</span><span class="sxs-lookup"><span data-stu-id="7bb95-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="7bb95-224">[![Yfirlit uppsetningar dagatals - fylki](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="7bb95-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="7bb95-225">Reiknar seinkun</span><span class="sxs-lookup"><span data-stu-id="7bb95-225">Calculating delays</span></span>

<span data-ttu-id="7bb95-226">Allar þrjár gerðir öryggismarka eru höfð með þegar kerfið ákveður hvort pöntun sé seinkað.</span><span class="sxs-lookup"><span data-stu-id="7bb95-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="7bb95-227">Til dæmis er vara með afhendingartíma upp á einn dag og innhreyfingarmörk upp á þrjá daga.</span><span class="sxs-lookup"><span data-stu-id="7bb95-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="7bb95-228">Sölupöntun fyrir þessa vöru er stillt eins og krafist í dag.</span><span class="sxs-lookup"><span data-stu-id="7bb95-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="7bb95-229">Í slíku tilfelli er töfin reiknuð sem *afhendingartími* + *mörk innhreyfinga* = fjórir dagar.</span><span class="sxs-lookup"><span data-stu-id="7bb95-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="7bb95-230">Þess vegna, ef í dag er 14. ágúst, leiðir fjögurra daga töf til afhendingar þann 18. ágúst.</span><span class="sxs-lookup"><span data-stu-id="7bb95-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="7bb95-231">Eftirfarandi mynd sýnir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="7bb95-231">The following illustration shows this example.</span></span>

![Dæmi um útreikning á töfum](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="7bb95-233">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7bb95-233">Additional resources</span></span>

[<span data-ttu-id="7bb95-234">Hafist handa með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="7bb95-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="7bb95-235">Samræmisgreining á fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="7bb95-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
