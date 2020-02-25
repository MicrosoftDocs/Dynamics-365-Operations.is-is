---
title: Grunnstilla gerðir leyfis og fjarvista
description: Settu upp tegundir orlofs sem starfsmenn geta tekið í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009450"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="a012b-103">Grunnstilla gerðir leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="a012b-103">Configure leave and absence types</span></span>

<span data-ttu-id="a012b-104">Gerðir leyfa í Dynamics 365 Human Resources skilgreina hinar ýmsu gerðir fjarvista sem starfsmaður getur gefið upp.</span><span class="sxs-lookup"><span data-stu-id="a012b-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="a012b-105">Þú getur sérsniðið leyfi eftir tegundum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="a012b-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="a012b-106">Dæmi um orlofsgerðir eru:</span><span class="sxs-lookup"><span data-stu-id="a012b-106">Examples of leave types include:</span></span>

- <span data-ttu-id="a012b-107">Greitt frí (PTO)</span><span class="sxs-lookup"><span data-stu-id="a012b-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="a012b-108">Ógreidd leyfi</span><span class="sxs-lookup"><span data-stu-id="a012b-108">Unpaid leave</span></span>
- <span data-ttu-id="a012b-109">Frí á launum</span><span class="sxs-lookup"><span data-stu-id="a012b-109">Paid vacation</span></span>
- <span data-ttu-id="a012b-110">Veikindaleyfi</span><span class="sxs-lookup"><span data-stu-id="a012b-110">Sick leave</span></span>
- <span data-ttu-id="a012b-111">Læknaleyfi</span><span class="sxs-lookup"><span data-stu-id="a012b-111">Medical leave</span></span>
- <span data-ttu-id="a012b-112">Fjölskylduleyfi</span><span class="sxs-lookup"><span data-stu-id="a012b-112">Family leave</span></span>
- <span data-ttu-id="a012b-113">Örorkubætur til skamms tíma</span><span class="sxs-lookup"><span data-stu-id="a012b-113">Short-term disability</span></span>
- <span data-ttu-id="a012b-114">Sorgarleyfi</span><span class="sxs-lookup"><span data-stu-id="a012b-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="a012b-115">Bættu við leyfisgerð</span><span class="sxs-lookup"><span data-stu-id="a012b-115">Add a leave type</span></span>

1. <span data-ttu-id="a012b-116">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="a012b-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="a012b-117">Undir **Skipulag**, veldu **Tegundir og leyfi**.</span><span class="sxs-lookup"><span data-stu-id="a012b-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="a012b-118">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a012b-118">Select **New**.</span></span>

4. <span data-ttu-id="a012b-119">Sláðu inn heiti fyrir leyfisgerðina undir **Gerð**, veldu verkflæði frá **Auðkenni vinnuflæðis** og sláðu inn lýsingu undir **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="a012b-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="a012b-120">Í **Almennt**, veldu **Enginn**, **Áætlað** eða **Óáætlað** fellilistanum **Flokkur**.</span><span class="sxs-lookup"><span data-stu-id="a012b-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="a012b-121">Veldu launakóða úr fellilistanum **Vinnukóða**.</span><span class="sxs-lookup"><span data-stu-id="a012b-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="a012b-122">Undir **Ástæðukóða krafist**, veldu hvort þú vilt þurfa ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="a012b-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="a012b-123">Ef þú vilt þurfa ástæðukóða gætirðu þurft að bæta þeim við.</span><span class="sxs-lookup"><span data-stu-id="a012b-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="a012b-124">Undir **Ástæða númer**, veldu **Bæta við**, veldu ástæðukóða og veldu síðan **Virkt** gátreitinn við hliðina.</span><span class="sxs-lookup"><span data-stu-id="a012b-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="a012b-125">Undir **Takmarka aðgang að völdum hlutverkum**, veldu hvort þú vilt takmarka aðgang.</span><span class="sxs-lookup"><span data-stu-id="a012b-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="a012b-126">Veldu síðan öryggishlutverkin undir **Öryggishlutverk fyrir þessa leyfisgerð**.</span><span class="sxs-lookup"><span data-stu-id="a012b-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="a012b-127">Öryggishlutverkin eru skilgreind í verkflæðinu sem þú valdir undir **Auðkenni vinnuflæðis** fyrr í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="a012b-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="a012b-128">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a012b-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="a012b-129">Stilla forskoðunareiginleika</span><span class="sxs-lookup"><span data-stu-id="a012b-129">Configure preview features</span></span>

<span data-ttu-id="a012b-130">Ef þú hefur gert forskoðunareiginleika virka fyrir leyfi og fjarveru þarftu líka að stilla stillingar fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="a012b-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="a012b-131">Setja valkosti til að námunda fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="a012b-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="a012b-132">Valkostir fela í sér **Enginn**, **Upp**, **Niður** og **Næst**.</span><span class="sxs-lookup"><span data-stu-id="a012b-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="a012b-133">Þú getur einnig stillt námundun námundunar fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="a012b-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="a012b-134">Stilltu **Leiðrétting á fríi** til að námunda fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="a012b-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="a012b-135">Þegar þú velur þennan valkost notar Human Resources þann fjölda frídaga sem falla á virkum degi til að ákvarða hvernig á að safna fríi fyrir orlofstegundina.</span><span class="sxs-lookup"><span data-stu-id="a012b-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="a012b-136">Til dæmis, ef jóladagur fellur á mánudag, dregur Human Resources einn dag frá orlofstegundinni þegar unnið er með uppsafnanir.</span><span class="sxs-lookup"><span data-stu-id="a012b-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="a012b-137">Frí er stillt í vinnutímadagatalinu.</span><span class="sxs-lookup"><span data-stu-id="a012b-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="a012b-138">Fyrir frekari upplýsingar, sjá [Búðu til vinnutímadagatal](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="a012b-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="a012b-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a012b-139">See also</span></span>

- [<span data-ttu-id="a012b-140">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="a012b-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="a012b-141">Búa til leyfis- og fjarvistaáætlun</span><span class="sxs-lookup"><span data-stu-id="a012b-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="a012b-142">Búa til dagatal fyrir vinnutíma</span><span class="sxs-lookup"><span data-stu-id="a012b-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)