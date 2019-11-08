---
title: Uppfæra fjárhagsáætlanir viðhalds
description: Þetta efni útskýrir hvernig á að uppfæra fjárhagsáætlun viðhalds í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f3b771319eeb602a371500fdc69c68f88afe341
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571738"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="1f5ac-103">Uppfæra fjárhagsáætlanir viðhalds</span><span class="sxs-lookup"><span data-stu-id="1f5ac-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1f5ac-104">Síðan **Fjárhagsáætlunarlínur viðhalds** sýnir allar fjárhagsáætlunarlínur sem eru stofnaðar fyrir fjárhagsáætlunina sem er valin á síðunni **Fjárhagsáætlanir viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="1f5ac-105">(Sjá frekari upplýsingar [Stofna fjárhagsáætlanir viðhalds](create-maintenance-budget.md).) Þú getur endurútreiknað og aðlagað fjárhagsáætlunarlínur viðhalds þar til fjárhagsáætlun viðhalds er samþykkt.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="1f5ac-106">Eftir að fjárhagsáætlunartímabilið er liðið og kostnaður hefur verið bókaður í eignastjórnun geturðu einnig uppfært fjárhagsáætlunarlínurnar með raunkostnaði.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="1f5ac-107">Endurreikna fjárhagsáætlun viðhalds</span><span class="sxs-lookup"><span data-stu-id="1f5ac-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="1f5ac-108">Hægt er að endurútreikna fjárhagsáætlun viðhalds á síðunni **Fjárhagsáætlunarlínur viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="1f5ac-109">Þegar þú endurútreiknar fjárhagsáætlun viðhalds er núverandi fjárhagsliðum eytt og nýr útreikningur gerður.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="1f5ac-110">Á síðunni **Fjárhagsáætlunarlínur viðhalds** velurðu **Endurreikna**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="1f5ac-111">Í glugganum **Endurreikna fjárhagsáætlun** gerirðu nauðsynlegar breytingar fyrir nýja útreikninginn og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="1f5ac-112">Nýjar fjárhagsáætlunarlínur eru búnar til samkvæmt gildunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="1f5ac-113">Leiðrétta fjárhagsáætlunarlínur</span><span class="sxs-lookup"><span data-stu-id="1f5ac-113">Adjust budget lines</span></span>

<span data-ttu-id="1f5ac-114">Í staðinn fyrir að endurreikna alla fjárhagsáætlun viðhalds geturðu breytt völdum línum sem tengjast kostnað fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="1f5ac-115">Á síðunni **Fjárhagsáætlunarlínur viðhalds** skaltu velja línurnar til að uppfæra kostnaðar fjárhagsáætlunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="1f5ac-116">Veldu **Leiðrétta**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="1f5ac-117">Til að bæta við upphæð við valdar línur skaltu velja gátreitinn **Bæta við kostnaði** og slá síðan inn gildi í reitinn **Bæta við gildi**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="1f5ac-118">Til að margfalda fjárhagsáætlunarkostnað á völdum fjárhagsáætlunarlínum með stuðli skaltu velja gátreitinn **Margfalda kostnað** og slá inn þáttinn í **Margfalda gildi**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="1f5ac-119">Til dæmis ef þú slærð inn **1,2** í reitinn **Margfalda gildi** hækkarðu kostnað fjárhagsáætlunar á völdum línum um 20 prósent.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="1f5ac-120">Ef þú slærð inn **0,7** lækkar þú kostnað fjárhagsáætlunar á völdum línum um 30 prósent.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="1f5ac-121">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-121">Select **OK**.</span></span>

<span data-ttu-id="1f5ac-122">Valdar fjárhagsáætlunarlínur eru uppfærðar í samræmi við gildin sem þú stillir í 3. eða 4. þrepi.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="1f5ac-123">Uppfæra raunkostnað</span><span class="sxs-lookup"><span data-stu-id="1f5ac-123">Update actual costs</span></span>

<span data-ttu-id="1f5ac-124">Eftir að dagsetningarnar í fjárhagsáætlunarlínunum eru liðnar og raunkostnaður hefur verið bókaður í eignastjórnun geturðu einnig uppfært raunkostnað á fjárhagsáætlun viðhalds.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="1f5ac-125">Á síðunni **Fjárhagsáætlunarlínur viðhalds** velurðu **Uppfæra kostnað**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="1f5ac-126">Í glugganum **Reikna raunkostnað** velurðu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="1f5ac-127">Reitirnir **Raunkostnaður** á fjárhagsáætlunarlínunum eru uppfærðir ef raunkostnaður hefur verið bókaður.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="1f5ac-128">Nýjar fjárhagsáætlunarlínur gætu verið búnar til ef nýjar eignategundir hafa verið búnar til síðan þú stofnaðir fjárhagsáætlunina og ef þessar eignategundir hafa verið notaðar á eignir sem búið er að búa til vierkbeiðnir fyrir og tengdur kostnaður hefur verið bókaður fyrir.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="1f5ac-129">Nýjar fjárlagalínur sýna aðeins raunkostnað vegna þess að enginn fjárhagsáætlunarkostnaður var reiknaður fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="1f5ac-130">Til að sjá yfirlit yfir raunkostnað skipt í forvarnar-, úrbóta- og fjárfestingarkostnað er hægt að gera útreikning fyrir sama tímabil á síðunni **Stýring eignakostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="1f5ac-131">Bæta fjárhagsáætlunarlínum handvirkt við</span><span class="sxs-lookup"><span data-stu-id="1f5ac-131">Manually add budget lines</span></span>

<span data-ttu-id="1f5ac-132">Á síðunni **Fjárhagsáætlunarlínur viðhalds** er hægt að bæta við nýrri fjárhagsáætlunarlínu handvirkt með því að velja **Nýtt** og síðan val á línunni.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="1f5ac-133">Hér eru nokkur dæmi um aðstæður þar sem þessi aðferð gæti verið gagnleg:</span><span class="sxs-lookup"><span data-stu-id="1f5ac-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="1f5ac-134">Þú veist að endurnýjun sumra eigna er sem stendur á áætlunarstig, en tengdar vinnslur hafa ekki enn verið stofnaðar í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="1f5ac-135">Samt sem áður viltu að fjárhagsáætlunarkostnaðar fyrir þessar vinnslur verði tekin með í fjárhagsáætlun viðhalds.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="1f5ac-136">Nýjar eignir eða eignategundir hafa verið búnar til síðan þú gerðir fjárhagsáætlun viðhalds en viðhaldsáætlanir hafa ekki enn verið settar upp fyrir þessar eignir eða eignategundir.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="1f5ac-137">Samt sem áður viltu að fjárhagsáætlunarkostnaður fyrir þessar eignagerðir verði tekinn með í fjárhagsáætlun viðhalds.</span><span class="sxs-lookup"><span data-stu-id="1f5ac-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
