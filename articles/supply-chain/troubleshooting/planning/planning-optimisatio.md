---
title: Áætluð innkaupapöntun er stofnuð þegar innkaup eru til innan neikvæðra daga
description: Ef tryggingarkóðinn er lágmark/hámark býr Planning Optimization til innkaupatillögu þegar innkaup eru til innan neikvæðra daga.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026615"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="402e5-103">Áætluð innkaupapöntun er stofnuð þegar innkaup eru til innan neikvæðra daga</span><span class="sxs-lookup"><span data-stu-id="402e5-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="402e5-104">KB númer: 4614298</span><span class="sxs-lookup"><span data-stu-id="402e5-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="402e5-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="402e5-105">Symptoms</span></span>

<span data-ttu-id="402e5-106">Ef tryggingarkóðinn er *Lágmark/hámark* býr Planning Optimization til áætlaða innkaupatillögu þegar innkaup eru til innan neikvæðra daga.</span><span class="sxs-lookup"><span data-stu-id="402e5-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="402e5-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="402e5-107">Resolution</span></span>

<span data-ttu-id="402e5-108">Fínstilling áætlanagerðar styður ekki neikvæða daga.</span><span class="sxs-lookup"><span data-stu-id="402e5-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="402e5-109">Hins vegar er ávallt tryggt að fyrirhugaðar pantanir séu ekki áætlaðar innan afhendingartíma miðað við núgildandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="402e5-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="402e5-110">Til dæmis er afhendingartími innkaupa 10 dagar og innkaupapöntun er væntanleg átta dögum frá deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="402e5-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="402e5-111">Í þessu tilfelli verður innkaupapöntunin notuð sem framboð fyrir eftirspurn sem er fimm dagar frá deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="402e5-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="402e5-112">Þess vegna er mælt með því að afhendingartímum sé breytt þannig að þeir nái yfir allar (eða nánast allar) sviðsmyndirnar.</span><span class="sxs-lookup"><span data-stu-id="402e5-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
