---
title: Skrá notkun
description: Þetta efni útskýrir hvernig á að skrá notkun í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 174c816c7a6442b07e4722c03045293b94c59153
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024661"
---
# <a name="register-consumption"></a><span data-ttu-id="4e941-103">Skrá notkun</span><span class="sxs-lookup"><span data-stu-id="4e941-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4e941-104">Þegar viðhaldsverkum hefur verið lokið í verkbeiðni er næsta skref að gera notkunarskráningar og bóka færslubækurnar.</span><span class="sxs-lookup"><span data-stu-id="4e941-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="4e941-105">Þú getur gert skráningar á eftirfarandi notkunargerðum: Tímum, vörum og kostnaði.</span><span class="sxs-lookup"><span data-stu-id="4e941-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="4e941-106">Mismunandi notkunargerðir eru skráðar og bókaðar á síðunni **Færslubækur verkbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="4e941-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="4e941-107">Uppsetning færslubókarinnar í **Eignastjórnun** er notuð til að stofna og bóka aðskildar færslubækur fyrir tíma, vörur og kostnað í einingunni **Verkefnisstjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="4e941-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="4e941-108">Þú gætir verið fær um að bæta við eða eyða spálínum í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="4e941-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="4e941-109">Uppsetning á líftímastöðu verkbeiðni, tengdri verkefnisgerð og stigareglum sem tengjast verkgerðinni ákvarðar hvort þú getur bætt við eða breytt færslubókarlínum.</span><span class="sxs-lookup"><span data-stu-id="4e941-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="4e941-110">Lestu meira um líftímastöður verkbeiðna og tengd verkefnisstig í [Sameining við verkefnastjórnun og bókhald](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="4e941-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="4e941-111">Það er mögulegt að setja upp sjálfvirka bókun færslubóka í líftímastöður verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="4e941-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="4e941-112">Sjá [Líftímastöður verkbeiðni](../setup-for-work-orders/work-order-lifecycle-states.md) fyrir meiri upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="4e941-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="4e941-113">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="4e941-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4e941-114">Veldu verkbeiðnina og smelltu á **Færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="4e941-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="4e941-115">Smelltu á **Afrita úr spá** til að flytja allar spálínur sem kunna að vera tengdar verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="4e941-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="4e941-116">Þú getur valið hvaða notkunargerðir þú vilt flytja.</span><span class="sxs-lookup"><span data-stu-id="4e941-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="4e941-117">Ef nauðsyn krefur geturðu bætt við fleiri notkunarlínum á viðkomandi flýtiflipa með því að smella á **Bæta við línu** og fylla út gögn á línunni.</span><span class="sxs-lookup"><span data-stu-id="4e941-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="4e941-118">Smelltu á **Staðfesta færslubækur** til að staðfesta færslubókarlínurnar áður en þær eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="4e941-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="4e941-119">Smelltu á **Bóka færslubækur** til að bóka færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="4e941-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="4e941-120">Eftir að þú hefur bókað notkunarfærslubækurnar geturðu uppfært líftímastöðu verkbeiðni, til dæmis í „Lokið“, til að gefa til kynna að verkbeiðninni sé lokið.</span><span class="sxs-lookup"><span data-stu-id="4e941-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="4e941-121">Í reitnum **Sýna** sem er staðsettur efst á síðunni **Verkbeiðnifærslubækur** velurðu hvaða færslubókarlínur þú vilt sjá: Allar, óbókaðar eða Bókaðar.</span><span class="sxs-lookup"><span data-stu-id="4e941-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="4e941-122">Bókaðar færslubækur eru með hak í gátreitnum **Bókað**.</span><span class="sxs-lookup"><span data-stu-id="4e941-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="4e941-123">Þegar vörulínur eru stofnaðar í verkbeiðnifærslubókinni eru vöruvíddir og rakningarvíddir sem tengjast vörunni sjálfkrafa fluttar á færslubókarlínuna.</span><span class="sxs-lookup"><span data-stu-id="4e941-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="4e941-124">Skjámyndin hér að neðan sýnir dæmi um skráningu klukkutíma og vöru í verkbeiðni í **Verkbeiðnifærslubókum**.</span><span class="sxs-lookup"><span data-stu-id="4e941-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Mynd 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="4e941-126">Skiptu tíma á verkbeiðnum með nokkrum verkbeiðniverkum</span><span class="sxs-lookup"><span data-stu-id="4e941-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="4e941-127">Ef verkbeiðni inniheldur nokkur verkbeiðniverk geturðu skráð vinnutíma með því að nota virknina **Skipta tímum**, sem þýðir að klukkustundar skráningarlínu má dreifa jafnt um hvert verkbeiðniverk.</span><span class="sxs-lookup"><span data-stu-id="4e941-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="4e941-128">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="4e941-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4e941-129">Veldu verkbeiðnina og smelltu á **Færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="4e941-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="4e941-130">Veldu klukkutímaskráningarlínuna sem þú vilt skipta og smelltu á **Skipta tímum**.</span><span class="sxs-lookup"><span data-stu-id="4e941-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="4e941-131">Í glugganum **Skipta tímum á viðhaldsverkum verkbeiðni** birtist nafn starfskrafts sem er innskráður sjálfkrafa í reitnum **Starfskraftur**.</span><span class="sxs-lookup"><span data-stu-id="4e941-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="4e941-132">Hægt er að velja annan starfskraft, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="4e941-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="4e941-133">Veldu flokk fyrir klukkutímaskráninguna í reitnum **Flokkur**.</span><span class="sxs-lookup"><span data-stu-id="4e941-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="4e941-134">Settu fjölda vinnutíma sem á að skipta í reitnum **Klukkutímar**.</span><span class="sxs-lookup"><span data-stu-id="4e941-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![Mynd 2](media/02-consumption.png)

7. <span data-ttu-id="4e941-136">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e941-136">Click **OK**.</span></span>

<span data-ttu-id="4e941-137">*Dæmi:* Í skjámyndinni hér að neðan eru dagbókarlínur fyrir verkbeiðni sem innihalda þrjú verkbeiðniverk.</span><span class="sxs-lookup"><span data-stu-id="4e941-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="4e941-138">Fyrstu línunni, sem hefur að geyma þrjá vinnutíma, hefur verið skipt og er einn vinnutími skráður í hvert verkbeiðniverk.</span><span class="sxs-lookup"><span data-stu-id="4e941-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="4e941-139">Eftir að þriggja tíma skráningarlínur eru búnar til ákveður þú hvað þú átt að gera við upphaflegu klukkutímaskráningarlínuna (fyrsta línan í dæminu).</span><span class="sxs-lookup"><span data-stu-id="4e941-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="4e941-140">Þú getur haldið því eins og það er eða eytt því.</span><span class="sxs-lookup"><span data-stu-id="4e941-140">You can keep it as is or delete it.</span></span> 

![Mynd 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="4e941-142">Fjárhagsvíddir á notkunarskráningum</span><span class="sxs-lookup"><span data-stu-id="4e941-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="4e941-143">Þegar þú skráir notkun er fjárhagsvíddum tengdum mismunandi skráningartegundum bætt við skráningarnar í tiltekinni röð.</span><span class="sxs-lookup"><span data-stu-id="4e941-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="4e941-144">*Skráning klukkustundar og kostnaðar:* Í fyrsta lagi er fjárhagsvíddum úr færslubókarhaus bætt við, ef einhver er.</span><span class="sxs-lookup"><span data-stu-id="4e941-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="4e941-145">Næst er fjárhagsvíddum úr tengdri verkbeiðniverki bætt við.</span><span class="sxs-lookup"><span data-stu-id="4e941-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="4e941-146">Að lokum er fjárhagsvíddum úr tilföngunum (starfsmanni) bætt við.</span><span class="sxs-lookup"><span data-stu-id="4e941-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="4e941-147">*Vöruskráningar:* Í fyrsta lagi er fjárhagsvíddum úr færslubókarhaus bætt við, ef einhver er.</span><span class="sxs-lookup"><span data-stu-id="4e941-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="4e941-148">Síðan er fjárhagsvíddum úr tengdri verkbeiðniverki bætt við.</span><span class="sxs-lookup"><span data-stu-id="4e941-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="4e941-149">Næst er fjárhagsvíddum af svæðinu bætt við.</span><span class="sxs-lookup"><span data-stu-id="4e941-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="4e941-150">Að lokum er fjárhagsvíddum úr vörunni bætt við.</span><span class="sxs-lookup"><span data-stu-id="4e941-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="4e941-151">Fyrir allar þrjár skráningargerðirnar er samsetning fjárhagsvíddar staðfest og ógildar samsetningar eru auðar.</span><span class="sxs-lookup"><span data-stu-id="4e941-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="4e941-152">Þetta er venjuleg skipulag í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4e941-152">This is standard setup in Finance and Operations.</span></span>

