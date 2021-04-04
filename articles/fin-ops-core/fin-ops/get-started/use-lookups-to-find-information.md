---
title: Leita að upplýsingum með uppflettingum
description: Mörg svæði hafa uppflettingar sem getur hjálpað við að finna auðveldlega rétt eða viðeigandi gildi. Nokkrum viðbótum hefur verið bætt við uppflettingar sem gera þessar stýringar nothæfari og auka framleiðni notenda. Í þessu efnisatriði muntu læra um þessar nýju uppflettingaraðgerðir og færð nokkur góð ráð til að ná ákjósanlegri notkun úr uppflettingum í kerfinu.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ae5f31c2cc46bf395acfbd053168e88aa69ebdc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566295"
---
# <a name="find-information-by-using-lookups"></a><span data-ttu-id="e1cd7-105">Leita að upplýsingum með uppflettingum</span><span class="sxs-lookup"><span data-stu-id="e1cd7-105">Find information by using lookups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1cd7-106">Mörg svæði hafa uppflettingar sem getur hjálpað við að finna auðveldlega rétt eða viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-106">Many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="e1cd7-107">Nokkrum viðbótum hefur verið bætt við uppflettingar sem gera þessar stýringar nothæfari og auka framleiðni notenda.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-107">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="e1cd7-108">Í þessu efnisatriði muntu læra um þessar nýju uppflettingaraðgerðir og færð nokkur góð ráð til að ná ákjósanlegri notkun úr uppflettingum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-108">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>

## <a name="responsive-lookups"></a><span data-ttu-id="e1cd7-109">Gagnvirkar uppflettingar</span><span class="sxs-lookup"><span data-stu-id="e1cd7-109">Responsive lookups</span></span>

<span data-ttu-id="e1cd7-110">Í fyrri útgáfum, þegar samskipti eru höfð við uppflettistýringu myndi notandi verða að nota skýra aðgerð til að opna í fellilista.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-110">In previous versions, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="e1cd7-111">Þetta gæti hafa verið með því að færa inn stjörnu (\*) í stýringu til að sía uppflettingu samkvæmt núverandi gildi stýringarinnar, því að smella á hnappinn fellilistanum eða með því að nota **Alt**+**Niður ör** flýtilykli.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-111">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="e1cd7-112">Uppflettistýringum hefur verið breytt á eftirfarandi hátt til að samræmast betur gildandi vefvenjum:</span><span class="sxs-lookup"><span data-stu-id="e1cd7-112">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

- <span data-ttu-id="e1cd7-113">Fellilistavalmyndir uppflettingar munu nú opnast sjálfkrafa eftir stutt hlé í vélritun, með efni fellilistans fyrir valmyndinni síað eftir gildi uppflettingar fjárhagsáætlunarstýringar.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-113">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>

    <span data-ttu-id="e1cd7-114">Athugið að gömlu hegðun sjálfvirkrar opnunar fellilista eftir ritun stjörnu (\*) hefur verið hætt.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-114">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>

- <span data-ttu-id="e1cd7-115">Eftir að uppfletting fellilista hefur opnað á eftirfarandi sér stað:</span><span class="sxs-lookup"><span data-stu-id="e1cd7-115">After the lookup drop-down menu has opened, the following will occur:</span></span>

    - <span data-ttu-id="e1cd7-116">Bendillinn verður áfram í uppflettistýringu (en ekki fluttur inn í fellilista áherslu) svo að hægt er að halda áfram að gera breytingar á gildi stýringarinnar.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-116">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="e1cd7-117">Hins vegar getur notandinn enn notað **Upp ör** og **Niður ör** til að breyta línum í fellilista og færa inn til að velja núgildandi línu fyrir fellilista.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-117">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    - <span data-ttu-id="e1cd7-118">Innihald í fellilista verður leiðrétta eftir hvaða breytingar eru gerðar í stýringu uppflettingargilda.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-118">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="e1cd7-119">Til dæmis, íhugið uppflettisvæðinu sem kallast **Borg**.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-119">For example, consider a lookup field called **City**.</span></span>

<span data-ttu-id="e1cd7-120">Þegar áhersla er á **Borg** er hægt að hefja leit að borg sem óskað er með því að slá nokkrar stafi, eins og "col."</span><span class="sxs-lookup"><span data-stu-id="e1cd7-120">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span> <span data-ttu-id="e1cd7-121">Eftir að hætt er að slá inn opnast uppflettingin sjálfkrafa, afmörkuð við þær borgir sem byrja á "col".</span><span class="sxs-lookup"><span data-stu-id="e1cd7-121">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span>

<span data-ttu-id="e1cd7-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="e1cd7-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span>

<span data-ttu-id="e1cd7-123">Á þessum tímapunkti, er bendillinn enn í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-123">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="e1cd7-124">Ef haldið er áfram því að slá svo gildið "colum" er efni uppflettingar leiðrétt sjálfkrafa til að endurspegla síðasta gildi stýringarinnar.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-124">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span>

![updateFilterLookupExample](./media/updatefilterlookupexample.png)

<span data-ttu-id="e1cd7-126">Jafnvel þótt áhersla sé enn í uppflettistýringu er einnig hægt að nota lyklana **Upp ör** eða **Niður ör** til að merkja línuna sem á að velja.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-126">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="e1cd7-127">Ef smellt er á **Færið** verður auðkennd lína valin úr leitinni og gildi stýringarinnar verður uppfært.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-127">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span>

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="e1cd7-129">Slegið inn meira en kenni</span><span class="sxs-lookup"><span data-stu-id="e1cd7-129">Typing in more than IDs</span></span>

<span data-ttu-id="e1cd7-130">Við gagnainnfærslu er eðlilegt fyrir notendur að reyna að auðkenna aðila, eins og viðskiptavin eða lánardrottinn með heiti en ekki kenni fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-130">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="e1cd7-131">Margar (en ekki allar) leitir leyfa nú samhengisgögn.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-131">Many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="e1cd7-132">Þessi öflugi eiginleiki leyfir notandanum að færa Kenni eða samsvarandi nafn í stýringu uppflettingu.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-132">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span>

<span data-ttu-id="e1cd7-133">Til dæmis, íhugið svæðið **viðskiptavinalykil** þegar sölupöntun er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-133">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="e1cd7-134">Þetta svæði sýnir á **Kenni reiknings** fyrir viðskiptavin, en notandi myndi yfirleitt vilja færa inn **lykilheiti** í stað **Kennis reiknings** fyrir þetta svæði þegar sölupöntun er stofnuð, eins og "Forest Wholesales" en "US-003."</span><span class="sxs-lookup"><span data-stu-id="e1cd7-134">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="e1cd7-135">Ef notandinn byrjaði að færa inn **Kenni reiknings** í uppflettistýringu myndi fellilistinn opnast eins og lýst er í fyrri hluta og notandinn myndi sjá uppflettinguna eins og sýnt er hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-135">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="e1cd7-136">[![Samhengisháð uppfletting þegar kenni viðskiptavinalykils er fært](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="e1cd7-136">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="e1cd7-137">Hins vegar getur notand nú einnig fært inn upphaf í **lykilheiti**.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-137">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="e1cd7-138">Ef þetta uppgötvast mun notandinn sjá eftirfarandi uppflettingu.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-138">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="e1cd7-139">Athugaðu hvernig dálkurinn **Heiti** er fluttur til að vera fyrsti dálkur í uppflettingu og hvernig uppfletting raðast og er síuð samkvæmt dálknum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-139">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="e1cd7-140">[![Samhengisháð uppfletting þegar Heiti viðskiptavinar er fært inn](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="e1cd7-140">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="e1cd7-141">Notkun dálkahausa hnitanets fyrir ítarlegri afmörkun og röðun</span><span class="sxs-lookup"><span data-stu-id="e1cd7-141">Using grid column headers for more advanced filtering and sorting</span></span>

<span data-ttu-id="e1cd7-142">Endurbætur á uppflettingu sem fjallað er um í fyrri tveimur köflum auka getu notanda mjög til að fara í línur í "byrja" leit á grundvelli uppflettingar í **Kenni** eða **Heiti** í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-142">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="e1cd7-143">Hins vegar eru aðstæður þar sem ítarlegri afmörkun (eða röðun) þarf til að finna í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-143">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="e1cd7-144">Í þessum aðstæðum þarf notandinn að nota valkosti afmörkunar og röðunar í dálkahausum hnitanets í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-144">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="e1cd7-145">Til dæmis, íhugið starfsmanns við sölupöntunarlínu sem þarf að finna rétta „kapalinn“ sem afurðar.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-145">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="e1cd7-146">Ekki er hjálplegt að slá inn „kapla“ í stýringuna **Vörunúmer**, þar sem engin afurðarheiti hefjast á „köplum.“</span><span class="sxs-lookup"><span data-stu-id="e1cd7-146">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span>

![emptyitemlookup](./media/emptyitemlookup.png)

<span data-ttu-id="e1cd7-148">Þess í stað þarf notandinn að hreinsa gildi uppflettistýringar, opna fellilista uppfletting og sía fellilista með dálkfyrirsögn hnitanets, eins og sýnt er hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-148">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="e1cd7-149">Notandi músar (eða snertiskjás) getur einfaldlega smellt (eða snert) hvaða dálkhaus sem er til að komast í valkosti síunar og röðunar fyrir þann dálk.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-149">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="e1cd7-150">Fyrir notanda lyklaborðs þarf notandinn einfaldlega að ýta á **Alt**+**Niður** **ör** aftur til að færa áhersluna inn í fellilista, en eftir það getur notandinn farið í réttan dálk rétt og stutt síðan á **Ctrl**+**G** til að opna fellilista dálkfyrirsagar í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-150">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span>

<span data-ttu-id="e1cd7-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="e1cd7-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span>

<span data-ttu-id="e1cd7-152">Eftir að afmörkun hefur verið beitt (sjá myndina hér fyrir neðan), getur notandinn fundið og valið línuna eins og venjulega.</span><span class="sxs-lookup"><span data-stu-id="e1cd7-152">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span>

![gridfilteritemlookup](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]