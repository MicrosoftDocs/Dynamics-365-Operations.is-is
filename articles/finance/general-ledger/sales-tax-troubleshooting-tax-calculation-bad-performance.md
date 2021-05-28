---
title: Framkvæmd skattaútreiknings hefur áhrif á færslur
description: Í þessu efnisatriði eru gefnar upp upplýsingar um úrræðaleit sem tengist afköstum á skattaútreikningi og áhrif þeirra á færslur.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020140"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="3a5d6-103">Framkvæmd skattaútreiknings hefur áhrif á færslur</span><span class="sxs-lookup"><span data-stu-id="3a5d6-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a5d6-104">Stundum verður færsla fyrir áhrifum af afkastavandamálum skattaútreiknings.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="3a5d6-105">Til að leysa úr vandamálinu skal fylgja skrefunum í eftirfarandi hlutum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="3a5d6-106">Farið yfir færslulínufjöldann</span><span class="sxs-lookup"><span data-stu-id="3a5d6-106">Review the transaction line count</span></span>

<span data-ttu-id="3a5d6-107">Ákvarða hvort færslan sé með mikinn fjölda lína (til dæmis fleiri en nokkur hundruð).</span><span class="sxs-lookup"><span data-stu-id="3a5d6-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="3a5d6-108">Annars skaltu færa þig yfir í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="3a5d6-109">Ef færsla er ekki með nokkur hundruð línur, skal fresta skattútreikningi.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="3a5d6-110">Frekari upplýsingar er að finna í [Virkja frestaðan skattaútreikning í færslubókum](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="3a5d6-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="3a5d6-111">Því næst er hægt að ákvarða hvort eftirfarandi skilyrði séu fyrir hendi:</span><span class="sxs-lookup"><span data-stu-id="3a5d6-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="3a5d6-112">Það eru innflutningsfærslur úr stórum skrám.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="3a5d6-113">Margar lotur vinna úr sama skattaútreikningi á færslu samtímis.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="3a5d6-114">Færslan hefur margar línur og yfirlitin eru uppfærð í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="3a5d6-115">Til dæmis er reiturinn **Reiknuð upphæð virðisaukaskatts** á síðunni **Almenn færslubók** uppfærður í rauntíma þegar reitum línu er breytt.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="3a5d6-116">[![Reitur reiknaðrar upphæðar virðisaukaskatts á síðu fylgiskjals færslubókar](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="3a5d6-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="3a5d6-117">Séu einhverju þessara skilyrða til staðar skal fresta skattútreikningnum.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="3a5d6-118">Skoða kallastaflann</span><span class="sxs-lookup"><span data-stu-id="3a5d6-118">Review the call stack</span></span>

<span data-ttu-id="3a5d6-119">Farið yfir kallstaflann til að ákvarða hvort skattreikningur er kallaður mörgum sinnum.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="3a5d6-120">Annars skaltu færa þig yfir í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="3a5d6-121">Ef kallað er á kallstaflann mörgum sinnum skal fylgja þessum skrefum til að hjálpa til við að stytta tíma skattaútreiknings.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="3a5d6-122">Hafi færslubók tekið tillit til færslunnar skal fresta skattútreikningi.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="3a5d6-123">Frekari upplýsingar er að finna í [Virkja frestaðan skattaútreikning í færslubókum](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="3a5d6-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="3a5d6-124">Ef færslan er innkaupapöntun og forritsútgáfan er eldri en 10.0.15 er hægt að fresta skattaútreikningi þar til kemur að endanlegum útreikningi með því að virkja forútgáfu fyrir **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="3a5d6-125">Farið yfir kallastaflann</span><span class="sxs-lookup"><span data-stu-id="3a5d6-125">Review the call stack timeline</span></span>

<span data-ttu-id="3a5d6-126">Farið yfir tímalínu kallstaflans til að ákvarða hvort eftirfarandi vandamál séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="3a5d6-127">Ef svo er skaltu virkja forútgáfuna fyrir **TaxUncommittedDoIsolateScopeFlighting** til að laga vandamálið.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="3a5d6-128">Færslan veldur því að kerfið hættir að svara þar til lotunni lýkur.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="3a5d6-129">Þess vegna getur færslan ekki reiknað út niðurstöður skatts.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="3a5d6-130">Eftirfarandi skýringarmynd sýnir skilaboðagluggann „Lotu lauk“ sem þú fékkst.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="3a5d6-131">[![Skilaboð fyrir lok lotu](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="3a5d6-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="3a5d6-132">Aðferðir **TaxUncommitted** taka lengri tíma en aðrar aðferðir.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="3a5d6-133">Á eftirfarandi mynd tekur til dæmis aðferðin **TaxUncommitted::updateTaxUncommitted()** 43.347,42 sekúndur, en hinar aðferðirnar taka 0,09 sekúndur.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="3a5d6-134">[![Tímalengd aðferðar](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="3a5d6-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="3a5d6-135">Sérstilling og kallað í skattaútreikning</span><span class="sxs-lookup"><span data-stu-id="3a5d6-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="3a5d6-136">Þegar gerðar eru sérstillingar skal ekki kalla á skattaútreikning með aðferðinni **insert()** eða **update()** fyrir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="3a5d6-137">Skattaútreikning ætti að framkalla á færslustigi.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="3a5d6-138">Ákvarða hvort sérstilling sé til staðar</span><span class="sxs-lookup"><span data-stu-id="3a5d6-138">Determine whether customization exists</span></span>

<span data-ttu-id="3a5d6-139">Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="3a5d6-140">Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.</span><span class="sxs-lookup"><span data-stu-id="3a5d6-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
