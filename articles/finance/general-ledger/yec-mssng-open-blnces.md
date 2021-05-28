---
title: Opnar innistæður vantar í árslokalokun
description: Þetta efnisatriði útskýrir hvers vegna opna stöður kann að vanta þegar þú lokar ári og hvernig á að endurbyggja þær stöður ef þær vantar.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028569"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="e7a8f-103">Opnar innistæður vantar í árslokalokun</span><span class="sxs-lookup"><span data-stu-id="e7a8f-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7a8f-104">Þetta efnisatriði útskýrir hvers vegna opna stöður kann að vanta þegar þú lokar ári og hvernig á að endurbyggja þær stöður ef þær vantar.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="e7a8f-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="e7a8f-105">Symptom</span></span>

<span data-ttu-id="e7a8f-106">Hvers vegna eru engar upphafsstöður eftir keyrslu árslokalokun í Fjárhag?</span><span class="sxs-lookup"><span data-stu-id="e7a8f-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="e7a8f-107">Lausn</span><span class="sxs-lookup"><span data-stu-id="e7a8f-107">Resolution</span></span>

<span data-ttu-id="e7a8f-108">Hér eru nokkur atriði sem skal athuga ef þú hefur lokað ári í Fjárhag og síðan myndað prófjöfnuð sem sýnir ekki opnunarstöður fyrir næsta fjárhagsár.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="e7a8f-109">Ef reiturinn **Afturkalla fyrri lokun** er stilltur á **Já** er verið að afturkalla fyrri árslokalokun fyrir sama fjárhagsár.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="e7a8f-110">Þegar keyra á ferli til að bakfæra árslokalokun verður öllum færslum fyrir bæði lokunar- og opnunarstöður eytt rétt eins og árinu hafi aldrei verið lokað.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="e7a8f-111">Fylgiskjölunum er einnig eytt.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-111">The vouchers are also deleted.</span></span> <span data-ttu-id="e7a8f-112">Ferlið fyrir lokun í árslok verður ekki keyrt aftur sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="e7a8f-113">Hefja þarf ferlið aftur og í þetta skipti uppfæra **Afturkalla fyrri lokun** valkostinn í **Nei**.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="e7a8f-114">Fjallað er um þessar aðstæður í algengum spurningum um árslokalokun.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="e7a8f-115">Frekari upplýsingar eru í [Algengar spurningar um verkþætti árslokunar](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="e7a8f-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="e7a8f-116">Einkenni</span><span class="sxs-lookup"><span data-stu-id="e7a8f-116">Symptom</span></span>

<span data-ttu-id="e7a8f-117">Ég keyrði árslokalokun með valkostinn **Afturkalla fyrri lokun** stilltan á **Nei** en er samt sem áður ekki með opnunarstöður fyrir fjárhagsárið mitt.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="e7a8f-118">Lausn</span><span class="sxs-lookup"><span data-stu-id="e7a8f-118">Resolution</span></span>

<span data-ttu-id="e7a8f-119">Athugaðu fyrst stöðu runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-119">First check the status of the batch job.</span></span> <span data-ttu-id="e7a8f-120">Að loka ári felur í sér fjölda ótengdra verka, en mikilvægasta skrefið er runuverkið með verklýsinguna **Skref 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="e7a8f-121">Opnunarfærslur, og valfrjálsar lokunarfærslur, eru bókaðar í Fjárhag í þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="e7a8f-122">[![Sögulisti runa](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="e7a8f-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="e7a8f-123">Ef þér tókst að ljúka þessu skrefi en sérð ekki opnunarstöðurnar á síðunni **Fyrirspurn prófjöfnuðar** (**Fjárhagur > Fyrirspurnir og skýrslur > Prófjöfnuður**) skaltu fara yfir niðurstöður runuvinnslu árslokalokunar til að komast að því hvort tekist hafi að ljúka skrefinu Endurbyggja stöður.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="e7a8f-124">[![Niðurstöður runuvinnslu árslokalokunar](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="e7a8f-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="e7a8f-125">Ef þetta skref tókst ekki af einhverjum ástæðum, tókst líklega að bóka opnunarfærslurnar (og lokunarfærslurnar ef það var gert).</span><span class="sxs-lookup"><span data-stu-id="e7a8f-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="e7a8f-126">Þú getur gengið úr skugga um að tekist hafi að bóka færslurnar í Fjárhag með því að nota síðuna **Fyrirspurn um fylgiskjalsfærslur** með því að gefa upp fylgiskjalsnúmerið og dagsetninguna sem gefið er upp í svarglugga árslokalokunar fyrir árið sem þú lokaðir (**Fjárhagur > Fyrirspurnir og skýrslur > Færslur fylgiskjals**).</span><span class="sxs-lookup"><span data-stu-id="e7a8f-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="e7a8f-127">[![Fyrirspurn um afsláttarmiðafærslur](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="e7a8f-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="e7a8f-128">Ef fylgiskjöl opnunar (og valfrjálst lokunar) eru til staðar þarftu ekki að keyra árslokalokun á nýjan leik.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="e7a8f-129">Í staðinn er vísað í næsta kafla til að fá upplýsingar um hvernig haldið er áfram.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="e7a8f-130">Einkenni</span><span class="sxs-lookup"><span data-stu-id="e7a8f-130">Symptom</span></span>

<span data-ttu-id="e7a8f-131">Skrefið „Endurbyggja stöður“ í árslokalokun tókst ekki, þarft ég að keyra allt ferli árslokalokunar aftur?</span><span class="sxs-lookup"><span data-stu-id="e7a8f-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="e7a8f-132">Lausn</span><span class="sxs-lookup"><span data-stu-id="e7a8f-132">Resolution</span></span>

<span data-ttu-id="e7a8f-133">Skrefið Endurbyggja stöður uppfærir stöður í Fjárhag sem eru notaðar þegar fyrirspurn um prófjöfnuð er búin til.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="e7a8f-134">Þetta er lokaskrefið í árslokalokun.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="e7a8f-135">Ef þetta skref er eina skrefið sem mistókst hafa færslur í Fjárhag verið bókaðar.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="e7a8f-136">Þú þarft ekki að loka árinu aftur.</span><span class="sxs-lookup"><span data-stu-id="e7a8f-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="e7a8f-137">Þú getur keyrt ferlið til að endurbyggja stöðurnar á handvirkan hátt með því að nota síðuna **Fjárhagsvíddasamstæður** (**Fjárhagur > Bókhaldslykill > Víddir > Fjárhagsvíddasamstæður**).</span><span class="sxs-lookup"><span data-stu-id="e7a8f-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="e7a8f-138">[![Hnappurinn Endurbyggja stöður á síðu fjárhagsvíddasamstæða](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="e7a8f-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="e7a8f-139">Ef það tekur langan tíma að vinna úr þessu skrefi mælum við með því að farið verði yfir bestu starfsvenjur fyrir fjárhagsvíddasamstæður eins og lýst er í [Bestu starfsvenjur fyrir uppfærslu á fjárhagsvíddasamstæðum](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="e7a8f-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

