---
title: Vinna úr viðburðum
description: Í líftíma starfsmannsins í Microsoft Dynamics 365 Human Resources, getur hver starfsmaður lent í ýmsum breytingum á atburði í lífinu.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 504408505168947ac725b5ee9764ecd994a64631
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429221"
---
# <a name="process-life-events"></a><span data-ttu-id="5746b-103">Vinna úr viðburðum</span><span class="sxs-lookup"><span data-stu-id="5746b-103">Process life events</span></span>

<span data-ttu-id="5746b-104">Í líftíma starfsmannsins í Microsoft Dynamics 365 Human Resources, getur hver starfsmaður lent í ýmsum breytingum á atburði í lífinu.</span><span class="sxs-lookup"><span data-stu-id="5746b-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="5746b-105">Til dæmis hjónaband, breyting á atvinnu eða breyting á skjólstæðingi/rétthafi.</span><span class="sxs-lookup"><span data-stu-id="5746b-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="5746b-106">Til að nota atburði í lífinu verður þú að virkja lífatburði á formi hagur breytur, setja upp gerðir atburða fyrir líf og setja upp val á atburði fyrir áætlunartegundir.</span><span class="sxs-lookup"><span data-stu-id="5746b-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="5746b-107">Áður en þú getur afgreitt atburði í lífinu verður þú að hafa þegar rekið opna skráningu amk einu sinni á ráðningartíma.</span><span class="sxs-lookup"><span data-stu-id="5746b-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="5746b-108">Í Bandaríkjunum er opin innritun venjulega einu sinni á ári.</span><span class="sxs-lookup"><span data-stu-id="5746b-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="5746b-109">Utan Bandaríkjanna kann að vera opin innritun við ráðningu.</span><span class="sxs-lookup"><span data-stu-id="5746b-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="5746b-110">Starfsmaður þarf ekki að velja bótaáætlun til að lífatburðir verði afgreiddir, en þeir þurfa að hafa verið með í opinni skráningarvinnslu.</span><span class="sxs-lookup"><span data-stu-id="5746b-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="5746b-111">Notaðu vinnslu lífsviðburða þegar þú ert með starfsmenn sem eru með atburði í lífinu sem eiga sér stað á framtíðardegi.</span><span class="sxs-lookup"><span data-stu-id="5746b-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="5746b-112">Þessi atburður vinnur alla atburði í lífinu sem ekki hafa verið afgreiddir (eins og atburðir í framtíðinni, eða lífatburðir sem hafa verið bættir við sem eru ekki sérstakir fyrir einn starfsmann - eitt dæmi er nýr ávinningur).</span><span class="sxs-lookup"><span data-stu-id="5746b-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="5746b-113">Atburðir í rauntíma eru faldir.</span><span class="sxs-lookup"><span data-stu-id="5746b-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="5746b-114">Til dæmis, ef í dag er 1. febrúar, og þann 14. febrúar, áætlar starfsmaður Joe Smith að breyta lögaðilum, ef þú rekur vinnslu atburða fyrir 15. febrúar, vinnur kerfið alla atburði til 15. febrúar.</span><span class="sxs-lookup"><span data-stu-id="5746b-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="5746b-115">Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla viðburða**.</span><span class="sxs-lookup"><span data-stu-id="5746b-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="5746b-116">Í valmyndinni **Keyra viðburðaferli**, tilgreindu gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="5746b-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="5746b-117">Svæði</span><span class="sxs-lookup"><span data-stu-id="5746b-117">Field</span></span> | <span data-ttu-id="5746b-118">Lýsing</span><span class="sxs-lookup"><span data-stu-id="5746b-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5746b-119">**Skráningartímabil**</span><span class="sxs-lookup"><span data-stu-id="5746b-119">**Enrollment period**</span></span> | <span data-ttu-id="5746b-120">Innritunartímabilið til að vinna úr viðburðum fyrir.</span><span class="sxs-lookup"><span data-stu-id="5746b-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="5746b-121">**Lögaðili**</span><span class="sxs-lookup"><span data-stu-id="5746b-121">**Legal entity**</span></span> | <span data-ttu-id="5746b-122">Lögaðilinn til að vinna úr viðburðum fyrir.</span><span class="sxs-lookup"><span data-stu-id="5746b-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="5746b-123">**Dagsetning viðburðar**</span><span class="sxs-lookup"><span data-stu-id="5746b-123">**Life event date**</span></span> | <span data-ttu-id="5746b-124">Kerfið vinnur alla atburði á innritunartímabilinu sem eiga sér stað fram til þessa dags.</span><span class="sxs-lookup"><span data-stu-id="5746b-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="5746b-125">**Starfskraftur**</span><span class="sxs-lookup"><span data-stu-id="5746b-125">**Worker**</span></span> | <span data-ttu-id="5746b-126">Starfskrafturinn til að vinna úr viðburðum fyrir.</span><span class="sxs-lookup"><span data-stu-id="5746b-126">The worker to process life events for.</span></span> <span data-ttu-id="5746b-127">Ef þú skilur þennan reit eftir auðan verða viðburðir allra starfsmanna afgreiddir.</span><span class="sxs-lookup"><span data-stu-id="5746b-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="5746b-128">Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="5746b-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="5746b-129">Færið inn upplýsingar fyrir ferlið.</span><span class="sxs-lookup"><span data-stu-id="5746b-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="5746b-130">Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5746b-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="5746b-131">Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5746b-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="5746b-132">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5746b-132">Select **OK**.</span></span> <span data-ttu-id="5746b-133">Ferlið keyrir með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="5746b-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="5746b-134">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5746b-134">Select **OK**.</span></span>
