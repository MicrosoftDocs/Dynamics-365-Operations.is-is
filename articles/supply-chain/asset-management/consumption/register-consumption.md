---
title: Skrá notkun
description: Þetta efni útskýrir hvernig á að skrá notkun í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c59664346c07f5e74825de41870f6635ced24ebd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216317"
---
# <a name="register-consumption"></a><span data-ttu-id="f9f93-103">Skrá notkun</span><span class="sxs-lookup"><span data-stu-id="f9f93-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f9f93-104">Þegar viðhaldsverkum hefur verið lokið í verkbeiðni er næsta skref að gera notkunarskráningar og bóka færslubækurnar.</span><span class="sxs-lookup"><span data-stu-id="f9f93-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="f9f93-105">Þú getur gert skráningar á eftirfarandi notkunargerðum: Tímum, vörum og kostnaði.</span><span class="sxs-lookup"><span data-stu-id="f9f93-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="f9f93-106">Mismunandi notkunargerðir eru skráðar og bókaðar á síðunni **Færslubækur verkbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="f9f93-107">Uppsetning færslubókarinnar í **Eignastjórnun** er notuð til að stofna og bóka aðskildar færslubækur fyrir tíma, vörur og kostnað í einingunni **Verkefnisstjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="f9f93-108">Í sumum tilfellum kann að vera hægt að bæta við eða eyða spálínum í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="f9f93-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f9f93-109">Uppsetning á líftímastöðu verkbeiðni, tengdri verkefnisgerð og stigareglum sem tengjast verkgerðinni ákvarðar hvort þú getur bætt við eða breytt færslubókarlínum.</span><span class="sxs-lookup"><span data-stu-id="f9f93-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="f9f93-110">Lestu nánar um líftímastöður verkbeiðna og tengd verkefnastig í [Spár, verkbeiðnir og verk](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="f9f93-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="f9f93-111">Það er mögulegt að setja upp sjálfvirka bókun færslubóka í líftímastöður verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="f9f93-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="f9f93-112">Sjá [Líftímastöður verkbeiðni](../setup-for-work-orders/work-order-lifecycle-states.md) fyrir meiri upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f9f93-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="f9f93-113">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f9f93-114">Veldu verkbeiðnina og smelltu á **Færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="f9f93-115">Smelltu á **Afrita úr spá** til að flytja allar spálínur sem kunna að vera tengdar verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="f9f93-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="f9f93-116">Þú getur valið hvaða notkunargerðir þú vilt flytja.</span><span class="sxs-lookup"><span data-stu-id="f9f93-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="f9f93-117">Ef nauðsyn krefur geturðu bætt við fleiri notkunarlínum á viðkomandi flýtiflipa með því að smella á **Bæta við línu** og fylla út gögn á línunni.</span><span class="sxs-lookup"><span data-stu-id="f9f93-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="f9f93-118">Smelltu á **Staðfesta færslubækur** til að staðfesta færslubókarlínurnar áður en þær eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="f9f93-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="f9f93-119">Smelltu á **Bóka færslubækur** til að bóka færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="f9f93-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="f9f93-120">Eftir að þú hefur sent neysludagbókina geturðu uppfært stöðu líftíma verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="f9f93-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="f9f93-121">Til dæmis, til að gefa til kynna að verkbeiðninni hafi verið lokið, geturðu uppfært líftímastöðunni í „Lokið“.</span><span class="sxs-lookup"><span data-stu-id="f9f93-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="f9f93-122">Í reitnum **Sýna** sem er staðsettur efst á síðunni **Verkbeiðnifærslubækur** velurðu hvaða færslubókarlínur þú vilt sjá: **Allar**, **Óbókaðar** eða **Bókaðar**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="f9f93-123">Bókaðar færslubækur eru með hak í gátreitnum **Bókað**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="f9f93-124">Þegar vörulínur eru stofnaðar í verkbeiðnifærslubókinni eru vöruvíddir og rakningarvíddir sem tengjast vörunni sjálfkrafa fluttar á færslubókarlínuna.</span><span class="sxs-lookup"><span data-stu-id="f9f93-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="f9f93-125">Skjámyndin hér að neðan sýnir dæmi um skráningu klukkutíma og vöru í verkbeiðni í **Verkbeiðnifærslubókum**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Mynd 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="f9f93-127">Skiptu tíma á verkbeiðnum með nokkrum verkbeiðniverkum</span><span class="sxs-lookup"><span data-stu-id="f9f93-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="f9f93-128">Ef verkbeiðni inniheldur nokkur verkbeiðniverk geturðu skráð vinnutíma með því að nota virknina **Skipta tímum**, sem þýðir að klukkustundar skráningarlínu má dreifa jafnt um hvert verkbeiðniverk.</span><span class="sxs-lookup"><span data-stu-id="f9f93-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="f9f93-129">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f9f93-130">Veldu verkbeiðnina og smelltu á **Færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f9f93-131">Veldu klukkutímaskráningarlínuna sem þú vilt skipta og smelltu á **Skipta tímum**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="f9f93-132">Í glugganum **Skipta tímum á viðhaldsverkum verkbeiðni** birtist nafn starfskrafts sem er innskráður sjálfkrafa í reitnum **Starfskraftur**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="f9f93-133">Hægt er að velja annan starfskraft, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="f9f93-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="f9f93-134">Veldu flokk fyrir klukkutímaskráninguna í reitnum **Flokkur**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="f9f93-135">Settu fjölda vinnutíma sem á að skipta í reitnum **Klukkutímar**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Mynd 2](media/02-consumption.png)

7. <span data-ttu-id="f9f93-137">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9f93-137">Click **OK**.</span></span>

<span data-ttu-id="f9f93-138">*Dæmi:* Í skjámyndinni hér að neðan eru dagbókarlínur fyrir verkbeiðni sem innihalda þrjú verkbeiðniverk.</span><span class="sxs-lookup"><span data-stu-id="f9f93-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="f9f93-139">Fyrstu línunni, sem hefur að geyma þrjá vinnutíma, hefur verið skipt og er einn vinnutími skráður í hvert verkbeiðniverk.</span><span class="sxs-lookup"><span data-stu-id="f9f93-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="f9f93-140">Eftir að þriggja tíma skráningarlínur eru búnar til ákveður þú hvað þú átt að gera við upphaflegu klukkutímaskráningarlínuna (fyrsta línan í dæminu).</span><span class="sxs-lookup"><span data-stu-id="f9f93-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="f9f93-141">Þú getur haldið því eins og það er eða eytt því.</span><span class="sxs-lookup"><span data-stu-id="f9f93-141">You can keep it as is or delete it.</span></span> 

![Mynd 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="f9f93-143">Fjárhagsvíddir á notkunarskráningum</span><span class="sxs-lookup"><span data-stu-id="f9f93-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="f9f93-144">Þegar þú skráir notkun er fjárhagsvíddum tengdum mismunandi skráningartegundum bætt við skráningarnar í tiltekinni röð.</span><span class="sxs-lookup"><span data-stu-id="f9f93-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="f9f93-145">*Skráning klukkustundar og kostnaðar:* Í fyrsta lagi er fjárhagsvíddum úr færslubókarhaus bætt við, ef einhver er.</span><span class="sxs-lookup"><span data-stu-id="f9f93-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f9f93-146">Næst er fjárhagsvíddum úr tengdri verkbeiðniverki bætt við.</span><span class="sxs-lookup"><span data-stu-id="f9f93-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f9f93-147">Að lokum er fjárhagsvíddum úr tilföngunum (starfsmanni) bætt við.</span><span class="sxs-lookup"><span data-stu-id="f9f93-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="f9f93-148">*Vöruskráningar:* Í fyrsta lagi er fjárhagsvíddum úr færslubókarhaus bætt við, ef einhver er.</span><span class="sxs-lookup"><span data-stu-id="f9f93-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f9f93-149">Síðan er fjárhagsvíddum úr tengdri verkbeiðniverki bætt við.</span><span class="sxs-lookup"><span data-stu-id="f9f93-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f9f93-150">Næst er fjárhagsvíddum af svæðinu bætt við.</span><span class="sxs-lookup"><span data-stu-id="f9f93-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="f9f93-151">Að lokum er fjárhagsvíddum úr vörunni bætt við.</span><span class="sxs-lookup"><span data-stu-id="f9f93-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="f9f93-152">Fyrir allar þrjár skráningargerðirnar er samsetning fjárhagsvíddar staðfest og ógildar samsetningar eru auðar.</span><span class="sxs-lookup"><span data-stu-id="f9f93-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="f9f93-153">Þetta er venjuleg uppsetning með öðrum forritum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f9f93-153">This is standard setup with other Finance and Operations apps.</span></span>

