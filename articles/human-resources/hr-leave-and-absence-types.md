---
title: Grunnstilla gerðir leyfis og fjarvista
description: Settu upp tegundir orlofs sem starfsmenn geta tekið í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e4c4b9c83ca648c21ac20bd20b739af8a6b9ed
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271128"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="eb6aa-103">Grunnstilla gerðir leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="eb6aa-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eb6aa-104">Gerðir leyfa í Dynamics 365 Human Resources skilgreina hinar ýmsu gerðir fjarvista sem starfsmaður getur gefið upp.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="eb6aa-105">Þú getur sérsniðið leyfi eftir tegundum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="eb6aa-106">Dæmi um orlofsgerðir eru:</span><span class="sxs-lookup"><span data-stu-id="eb6aa-106">Examples of leave types include:</span></span>

- <span data-ttu-id="eb6aa-107">Greitt frí (PTO)</span><span class="sxs-lookup"><span data-stu-id="eb6aa-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="eb6aa-108">Ógreidd leyfi</span><span class="sxs-lookup"><span data-stu-id="eb6aa-108">Unpaid leave</span></span>
- <span data-ttu-id="eb6aa-109">Frí á launum</span><span class="sxs-lookup"><span data-stu-id="eb6aa-109">Paid vacation</span></span>
- <span data-ttu-id="eb6aa-110">Veikindaleyfi</span><span class="sxs-lookup"><span data-stu-id="eb6aa-110">Sick leave</span></span>
- <span data-ttu-id="eb6aa-111">Læknaleyfi</span><span class="sxs-lookup"><span data-stu-id="eb6aa-111">Medical leave</span></span>
- <span data-ttu-id="eb6aa-112">Fjölskylduleyfi</span><span class="sxs-lookup"><span data-stu-id="eb6aa-112">Family leave</span></span>
- <span data-ttu-id="eb6aa-113">Örorkubætur til skamms tíma</span><span class="sxs-lookup"><span data-stu-id="eb6aa-113">Short-term disability</span></span>
- <span data-ttu-id="eb6aa-114">Sorgarleyfi</span><span class="sxs-lookup"><span data-stu-id="eb6aa-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="eb6aa-115">Bættu við leyfisgerð</span><span class="sxs-lookup"><span data-stu-id="eb6aa-115">Add a leave type</span></span>

1. <span data-ttu-id="eb6aa-116">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="eb6aa-117">Undir **Skipulag**, veldu **Tegundir og leyfi**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="eb6aa-118">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-118">Select **New**.</span></span>

4. <span data-ttu-id="eb6aa-119">Sláðu inn heiti fyrir leyfisgerðina undir **Gerð**, veldu verkflæði frá **Auðkenni vinnuflæðis** og sláðu inn lýsingu undir **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="eb6aa-120">Í **Almennt**, veldu **Enginn**, **Áætlað** eða **Óáætlað** fellilistanum **Flokkur**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="eb6aa-121">Veldu launakóða úr fellilistanum **Vinnukóða**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="eb6aa-122">Undir **Ástæðukóða krafist**, veldu hvort þú vilt þurfa ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="eb6aa-123">Ef þú vilt þurfa ástæðukóða gætirðu þurft að bæta þeim við.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="eb6aa-124">Undir **Ástæða númer**, veldu **Bæta við**, veldu ástæðukóða og veldu síðan **Virkt** gátreitinn við hliðina.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="eb6aa-125">Undir **Takmarka aðgang að völdum hlutverkum**, veldu hvort þú vilt takmarka aðgang.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="eb6aa-126">Veldu síðan öryggishlutverkin undir **Öryggishlutverk fyrir þessa leyfisgerð**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="eb6aa-127">Öryggishlutverkin eru skilgreind í verkflæðinu sem þú valdir undir **Auðkenni vinnuflæðis** fyrr í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="eb6aa-128">Undir **Litur dagatals** skal velja hvaða lit á að sýna fyrir leyfis- og fjarvistadagatöl fyrir þessa leyfisgerð.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="eb6aa-129">Undir **Frestunartengsl** skal velja hvort eigi að fresta þessari leyfisgerð eða fresta annarri leyfisgerð eða láta fresta vegna annarrar leyfisgerðar.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="eb6aa-130">Þegar beiðni um fjarvist er send inn fyrir frestaða leyfisgerð verður frestun leyfis sjálfkrafa búin til fyrir frestaða leyfisgerð.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="eb6aa-131">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="eb6aa-132">Stilla reglur leyfisgerða</span><span class="sxs-lookup"><span data-stu-id="eb6aa-132">Configure leave type rules</span></span>

1. <span data-ttu-id="eb6aa-133">Setja valkosti til að námunda fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="eb6aa-134">Valkostir fela í sér **Enginn**, **Upp**, **Niður** og **Næst**.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="eb6aa-135">Þú getur einnig stillt námundun námundunar fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="eb6aa-136">Stilltu **Leiðrétting á fríi** til að námunda fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="eb6aa-137">Þegar þú velur þennan valkost notar Human Resources þann fjölda frídaga sem falla á virkum degi til að ákvarða hvernig á að safna fríi fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="eb6aa-138">Til dæmis, ef jóladagur fellur á mánudag, dregur Human Resources einn dag frá orlofstegundinni þegar unnið er með uppsafnanir.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="eb6aa-139">Frí er stillt í vinnutímadagatalinu.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="eb6aa-140">Fyrir frekari upplýsingar, sjá [Búðu til vinnutímadagatal](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="eb6aa-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="eb6aa-141">Stillið **Yfirfærð leyfisgerð** fyrir leyfisgerð.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="eb6aa-142">Þegar þessi valkostur er valinn verða allar yfirfærðar stöður fluttar í tilgreinda gerð leyfis.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="eb6aa-143">Yfirfærsluleyfisgerðin þarf einnig að vera með í áætlun um leyfi og fjarveru.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
4. <span data-ttu-id="eb6aa-144">Skilgreinið **Gildistímareglur** fyrir leyfisgerðina.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="eb6aa-145">Þegar þessi valkostur er skilgreindur er hægt að velja einingu daga eða mánaða og stilla tímalengd gildistímans.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiration.</span></span> <span data-ttu-id="eb6aa-146">Gildisdagsetning gildistímareglu er notuð til að ákvarða hvenær á að hefja keyrslu runuvinnslunnar sem vinnur úr gildistíma leyfis eða dagsetninguna þegar reglan tekur gildi.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-146">The effective date of the expiration rule is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="eb6aa-147">Gildistíminn mun alltaf sjást í upphafsdagsetningu uppsafnaðs tímabils.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-147">The expiration itself will always occur on the accrual period start date.</span></span> <span data-ttu-id="eb6aa-148">Ef til dæmis upphafsdagur uppsöfnunartímabils er 3. ágúst 2021 og gildistímareglan var sett á 6 mánuði, verður reglan unnin með hliðsjón af lokadeginum frá upphafsdegi uppsöfnunartímabilsins, þannig að hún yrði framkvæmd 3. febrúar 2022.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-148">For example, if the accrual period start date is August 3, 2021, and the expiration rule was set at 6 months, the rule will be processed based on the expiration offset from the accrual period start date, so it would be executed on February 3, 2022.</span></span> <span data-ttu-id="eb6aa-149">Allar leyfisstöður sem eru til staðar þegar gildistíminn rennur út verða dregnar frá leyfisgerðinni og teknar inn í leyfsstöðuna.</span><span class="sxs-lookup"><span data-stu-id="eb6aa-149">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span>
 
## <a name="see-also"></a><span data-ttu-id="eb6aa-150">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="eb6aa-150">See also</span></span>

- [<span data-ttu-id="eb6aa-151">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="eb6aa-151">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="eb6aa-152">Búa til leyfis- og fjarvistaáætlun</span><span class="sxs-lookup"><span data-stu-id="eb6aa-152">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="eb6aa-153">Búa til dagatal fyrir vinnutíma</span><span class="sxs-lookup"><span data-stu-id="eb6aa-153">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="eb6aa-154">Fresta leyfi</span><span class="sxs-lookup"><span data-stu-id="eb6aa-154">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)
- [<span data-ttu-id="eb6aa-155">Búa til verkflæði fyrir beiðni um kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="eb6aa-155">Create a buy and sell leave request workflow</span></span>](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
