---
title: Rökstuðningsskjöl fjárhagsáætlunargerðar
description: Rökstuðningsskjöl veita sögu fyrir þá sem biðja fjárhagsáætlun að útskýra hvers vegna tilgreind fjárhagsáætlun er nauðsynleg.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 321da6643b421070ddd9f32bddd3e8d72f0adb86
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188557"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="80a2f-103">Rökstuðningsskjöl fjárhagsáætlunargerðar</span><span class="sxs-lookup"><span data-stu-id="80a2f-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80a2f-104">Rökstuðningsskjöl veita sögu fyrir þá sem biðja fjárhagsáætlun að útskýra hvers vegna tilgreind fjárhagsáætlun er nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="80a2f-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="80a2f-105">Sniðmát fjárhagsáætlunargerðar er stofnað af fjárhagsáætlunarstjóra í Microsoft Word og úthlutað til núverandi ferli fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="80a2f-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="80a2f-106">Eigendur fjárhagsáætlunar getur svo opnað sniðmát og haft gögn sjálfvirkt útfyllt í Word á grunni beiðnar um fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="80a2f-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="80a2f-107">Þeir geta svo bætt við viðbótartexti eða gögn áður en það er vistað og fest sérsniðið jöfnunarfylgiskjal við fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="80a2f-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="80a2f-108">Setja upp Microsoft Dynamics Office-viðbætur fyrir Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="80a2f-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="80a2f-109">Opna nýtt Microsoft Word skjal.</span><span class="sxs-lookup"><span data-stu-id="80a2f-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="80a2f-110">Smellt er á **Setja inn** á borða, og smellt er á **Verslun**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="80a2f-111">Leita að Microsoft Dynamics Office-innbót og Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="80a2f-112">Í Word í hægri rúðunni skal smella á **Bæta við upplýsingum um þjón**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="80a2f-113">Rita eða líma vefslóð þjóns og Smellt er á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="80a2f-114">Skilgreina jöfnunarsniðmát í Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="80a2f-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="80a2f-115">Smellið á **Hönnun** í Microsoft Dynamics Office-innbót eftir að þú hefur skráð þig inn.</span><span class="sxs-lookup"><span data-stu-id="80a2f-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="80a2f-116">Fyrir upplýsingar úr haus Smellið á hnappinn **Bæta við reitum**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="80a2f-117">Velurðu eining gagnaveita BudgetPlanJustification, og Smellið á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="80a2f-118">**athugasemd:** Þessi eining er áskilið fyrir jöfnunarfylgiskjal.</span><span class="sxs-lookup"><span data-stu-id="80a2f-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="80a2f-119">Hægt er að nota aðra lögaðila en upphleðslan til baka í Microsoft Dynamics 365 Finance mun ekki takast ef þessi eining er ekki höfð með.</span><span class="sxs-lookup"><span data-stu-id="80a2f-119">Other entities can be used but the upload back to Microsoft Dynamics 365 Finance will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="80a2f-120">Bæta við merkjunum og gildunum BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, og DocumentNumber og í Word-skjalið.</span><span class="sxs-lookup"><span data-stu-id="80a2f-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="80a2f-121">**athugasemd:** Hægt er að nota sín eigin sérsniðnu merki, frekar en stöðluð merki, ef þess er þörf.</span><span class="sxs-lookup"><span data-stu-id="80a2f-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="80a2f-122">Smelltu á **Lokið** til að ljúka haushlutanum.</span><span class="sxs-lookup"><span data-stu-id="80a2f-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="80a2f-123">Fyrir upplýsingar línustigs um upphæðir fjárhagsáætlunar Smelltu á **Bæta við tafla**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="80a2f-124">Aftur velurðu eining gagnaveita BudgetPlanJustification, og Smellið á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="80a2f-125">Bæta við reitum fyrir EffectiveDate, ScenarioName, AccountDisplayValue, og AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="80a2f-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="80a2f-126">**athugasemd:** Ef athugasemdir eru í boði til innan stakra fjárhagsáætlunarlína er hægt að bæta þeim við töfluna hér.</span><span class="sxs-lookup"><span data-stu-id="80a2f-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="80a2f-127">Bæta við Auka leiðbeiningar til að veita notanda og framkvæma öll nauðsynleg snið eða stíl á fylgiskjali.</span><span class="sxs-lookup"><span data-stu-id="80a2f-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="80a2f-128">Vistaðu skjalið á staðbundinni tölvu og lokaðu skránni áður en haldið er áfram.</span><span class="sxs-lookup"><span data-stu-id="80a2f-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="80a2f-129">Setja upp Ferli fjárhagsáætlunargerðar sem nota á jöfnunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="80a2f-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="80a2f-130">Farðu í **Fjárhagsáætlun** &gt; **Uppsetning** &gt; **Fjárhagsáætlunargerð** &gt; **Sniðmát jöfnunarskjala**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-130">Go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="80a2f-131">Smellt er á **Nýtt** og flett að nýstofnuðu skjali í Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="80a2f-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="80a2f-132">Færa skal inn sniðmátsheiti til birtingar og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="80a2f-132">Enter a template display name and description.</span></span> <span data-ttu-id="80a2f-133">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-133">Click **OK**.</span></span>
4.  <span data-ttu-id="80a2f-134">Farðu í **Fjárhagsáætlun** &gt; **Setja upp** &gt; **Fjárhagsáætlunar** **gerð** &gt; **Ferli fjárhagsáætlunargerðar**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="80a2f-135">Veldu ferlið þar sem nota á jöfnunarsniðmátið og smelltu á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="80a2f-136">Í reitnum **Sniðmát rökstuðningsskjals** velurðu viðeigandi sniðmát og vistar.</span><span class="sxs-lookup"><span data-stu-id="80a2f-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="80a2f-137">Breyta og vista sérsniðnum rökstuðningsskjölum</span><span class="sxs-lookup"><span data-stu-id="80a2f-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="80a2f-138">Stofnaðu nýja fjárhagsáætlun eða opnaðu fyrirliggjandi fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="80a2f-138">Create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="80a2f-139">Í fellilistavalmynd **Jöfnun** Velja **Stofna nýjan rökstuðning**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="80a2f-140">Eftir útfyllingu upplýsinga, velja að hlaða upp sérsniðnu fylgiskjali æyr fellilistavalmyndinni **Rökstuðningur**.</span><span class="sxs-lookup"><span data-stu-id="80a2f-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>



