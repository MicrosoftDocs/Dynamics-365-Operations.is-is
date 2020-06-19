---
title: Grunnstilla gerðir leyfis og fjarvista
description: Settu upp tegundir orlofs sem starfsmenn geta tekið í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1802938f54a1d78e6ea60572a76177a037192ae0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428594"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="4dec3-103">Grunnstilla gerðir leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="4dec3-103">Configure leave and absence types</span></span>

<span data-ttu-id="4dec3-104">Gerðir leyfa í Dynamics 365 Human Resources skilgreina hinar ýmsu gerðir fjarvista sem starfsmaður getur gefið upp.</span><span class="sxs-lookup"><span data-stu-id="4dec3-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="4dec3-105">Þú getur sérsniðið leyfi eftir tegundum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4dec3-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="4dec3-106">Dæmi um orlofsgerðir eru:</span><span class="sxs-lookup"><span data-stu-id="4dec3-106">Examples of leave types include:</span></span>

- <span data-ttu-id="4dec3-107">Greitt frí (PTO)</span><span class="sxs-lookup"><span data-stu-id="4dec3-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="4dec3-108">Ógreidd leyfi</span><span class="sxs-lookup"><span data-stu-id="4dec3-108">Unpaid leave</span></span>
- <span data-ttu-id="4dec3-109">Frí á launum</span><span class="sxs-lookup"><span data-stu-id="4dec3-109">Paid vacation</span></span>
- <span data-ttu-id="4dec3-110">Veikindaleyfi</span><span class="sxs-lookup"><span data-stu-id="4dec3-110">Sick leave</span></span>
- <span data-ttu-id="4dec3-111">Læknaleyfi</span><span class="sxs-lookup"><span data-stu-id="4dec3-111">Medical leave</span></span>
- <span data-ttu-id="4dec3-112">Fjölskylduleyfi</span><span class="sxs-lookup"><span data-stu-id="4dec3-112">Family leave</span></span>
- <span data-ttu-id="4dec3-113">Örorkubætur til skamms tíma</span><span class="sxs-lookup"><span data-stu-id="4dec3-113">Short-term disability</span></span>
- <span data-ttu-id="4dec3-114">Sorgarleyfi</span><span class="sxs-lookup"><span data-stu-id="4dec3-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="4dec3-115">Bættu við leyfisgerð</span><span class="sxs-lookup"><span data-stu-id="4dec3-115">Add a leave type</span></span>

1. <span data-ttu-id="4dec3-116">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="4dec3-117">Undir **Skipulag**, veldu **Tegundir og leyfi**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="4dec3-118">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-118">Select **New**.</span></span>

4. <span data-ttu-id="4dec3-119">Sláðu inn heiti fyrir leyfisgerðina undir **Gerð**, veldu verkflæði frá **Auðkenni vinnuflæðis** og sláðu inn lýsingu undir **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="4dec3-120">Í **Almennt**, veldu **Enginn**, **Áætlað** eða **Óáætlað** fellilistanum **Flokkur**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="4dec3-121">Veldu launakóða úr fellilistanum **Vinnukóða**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="4dec3-122">Undir **Ástæðukóða krafist**, veldu hvort þú vilt þurfa ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="4dec3-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="4dec3-123">Ef þú vilt þurfa ástæðukóða gætirðu þurft að bæta þeim við.</span><span class="sxs-lookup"><span data-stu-id="4dec3-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="4dec3-124">Undir **Ástæða númer**, veldu **Bæta við**, veldu ástæðukóða og veldu síðan **Virkt** gátreitinn við hliðina.</span><span class="sxs-lookup"><span data-stu-id="4dec3-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="4dec3-125">Undir **Takmarka aðgang að völdum hlutverkum**, veldu hvort þú vilt takmarka aðgang.</span><span class="sxs-lookup"><span data-stu-id="4dec3-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="4dec3-126">Veldu síðan öryggishlutverkin undir **Öryggishlutverk fyrir þessa leyfisgerð**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="4dec3-127">Öryggishlutverkin eru skilgreind í verkflæðinu sem þú valdir undir **Auðkenni vinnuflæðis** fyrr í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="4dec3-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="4dec3-128">Undir **Frestunartengsl** skal velja hvort eigi að fresta þessari leyfisgerð eða fresta annarri leyfisgerð eða láta fresta vegna annarrar leyfisgerðar.</span><span class="sxs-lookup"><span data-stu-id="4dec3-128">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="4dec3-129">Þegar beiðni um fjarvist er send inn fyrir frestaða leyfisgerð verður frestun leyfis sjálfkrafa búin til fyrir frestaða leyfisgerð.</span><span class="sxs-lookup"><span data-stu-id="4dec3-129">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="4dec3-130">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-130">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="4dec3-131">Stilla reglur leyfisgerða</span><span class="sxs-lookup"><span data-stu-id="4dec3-131">Configure leave type rules</span></span>

1. <span data-ttu-id="4dec3-132">Setja valkosti til að námunda fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="4dec3-132">Set rounding options for the leave type.</span></span> <span data-ttu-id="4dec3-133">Valkostir fela í sér **Enginn**, **Upp**, **Niður** og **Næst**.</span><span class="sxs-lookup"><span data-stu-id="4dec3-133">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="4dec3-134">Þú getur einnig stillt námundun námundunar fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="4dec3-134">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="4dec3-135">Stilltu **Leiðrétting á fríi** til að námunda fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="4dec3-135">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="4dec3-136">Þegar þú velur þennan valkost notar Human Resources þann fjölda frídaga sem falla á virkum degi til að ákvarða hvernig á að safna fríi fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="4dec3-136">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="4dec3-137">Til dæmis, ef jóladagur fellur á mánudag, dregur Human Resources einn dag frá orlofstegundinni þegar unnið er með uppsafnanir.</span><span class="sxs-lookup"><span data-stu-id="4dec3-137">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="4dec3-138">Frí er stillt í vinnutímadagatalinu.</span><span class="sxs-lookup"><span data-stu-id="4dec3-138">You set holidays in the working time calendar.</span></span> <span data-ttu-id="4dec3-139">Fyrir frekari upplýsingar, sjá [Búðu til vinnutímadagatal](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="4dec3-139">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="4dec3-140">Stillið **Yfirfærð leyfisgerð** fyrir leyfisgerð.</span><span class="sxs-lookup"><span data-stu-id="4dec3-140">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="4dec3-141">Þegar þessi valkostur er valinn verða allar yfirfærðar stöður fluttar í tilgreinda gerð leyfis.</span><span class="sxs-lookup"><span data-stu-id="4dec3-141">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="4dec3-142">Yfirfærsluleyfisgerðin þarf einnig að vera með í áætlun um leyfi og fjarveru.</span><span class="sxs-lookup"><span data-stu-id="4dec3-142">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="4dec3-143">Skilgreinið **Gildistímareglur** fyrir leyfisgerðina.</span><span class="sxs-lookup"><span data-stu-id="4dec3-143">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="4dec3-144">Þegar þessi valkostur er skilgreindur er hægt að velja einingu daga eða mánaða og stilla tímalengd gildistímans.</span><span class="sxs-lookup"><span data-stu-id="4dec3-144">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="4dec3-145">Einnig er hægt að stilla gildisdagsetningu gildistímareglunnar.</span><span class="sxs-lookup"><span data-stu-id="4dec3-145">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="4dec3-146">Allar leyfisstöður sem eru til staðar þegar gildistíminn rennur út verða dregnar frá leyfisgerðinni og teknar inn í leyfsstöðuna.</span><span class="sxs-lookup"><span data-stu-id="4dec3-146">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="4dec3-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4dec3-147">See also</span></span>

- [<span data-ttu-id="4dec3-148">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="4dec3-148">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="4dec3-149">Búa til leyfis- og fjarvistaáætlun</span><span class="sxs-lookup"><span data-stu-id="4dec3-149">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="4dec3-150">Búa til dagatal fyrir vinnutíma</span><span class="sxs-lookup"><span data-stu-id="4dec3-150">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="4dec3-151">Fresta leyfi</span><span class="sxs-lookup"><span data-stu-id="4dec3-151">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

