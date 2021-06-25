---
title: Slá inn hæfni
description: Starfsfólk og stjórnendur geta skráð hæfni í Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193978"
---
# <a name="enter-skills"></a><span data-ttu-id="28350-103">Slá inn hæfni</span><span class="sxs-lookup"><span data-stu-id="28350-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="28350-104">Hægt er að færa hæfni eða raunverulega hæfni fyrir starfsmenn, umsækjendur eða tengiliði í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28350-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="28350-105">Markhæfni er hæfni sem einstaklingur ætlar að ná.</span><span class="sxs-lookup"><span data-stu-id="28350-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="28350-106">Raunveruleg kunnátta er kunnátta sem einstaklingur býr þegar yfir.</span><span class="sxs-lookup"><span data-stu-id="28350-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="28350-107">Verkflæði stofnað til að samþykkja hæfni sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="28350-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="28350-108">Til að slá inn færni án þess að þurfa samþykki þarf að stofna verkflæði til að samþykkja færni sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="28350-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="28350-109">Hæfni sem starfsmenn færa inn þurfa alltaf samþykki stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="28350-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="28350-110">Þetta verkflæði samþykkir aðeins hæfni sjálfkrafa sem stjórnendur færa inn fyrir hönd annarra starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="28350-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="28350-111">Á vinnusvæðinu **Starfsmannastjórnun** velur þú **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="28350-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="28350-112">Undir **Skipulag**, veldu **Vinnuflæði mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="28350-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="28350-113">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="28350-113">Select **New**.</span></span>

4. <span data-ttu-id="28350-114">Á svæðinu **Stofna verkflæði** skal velja **Hæfni starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="28350-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="28350-115">[![Velja verkflæði starfsmannahæfni](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="28350-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="28350-116">Í glugganum **Opna þessa skrá?** skal velja **Opna**.</span><span class="sxs-lookup"><span data-stu-id="28350-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="28350-117">Þegar beðið um skal færa inn innskráningarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="28350-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="28350-118">Í verkflæðisritlinum skal velja verkflæðiseininguna **Samþykkja hæfni** og færa hana yfir á vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="28350-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="28350-119">[![Velja verkflæðiseiningu fyrir samþykkt hæfni](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="28350-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="28350-120">Tengið eininguna **Hefja** við eininguna **Samþykkja hæfni 1** og tengið síðan eininguna **Samþykkja hæfni 1** við eininguna **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="28350-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="28350-121">Hugsanlega þarf að fletta niður til að sjá eininguna **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="28350-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="28350-122">Hægt er að draga hana nær öðrum einingum.</span><span class="sxs-lookup"><span data-stu-id="28350-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="28350-123">[![Tengja verkflæðiseiningar](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="28350-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="28350-124">Tvísmellið á verkflæðiseininguna **Samþykkja hæfni 1** og hægrismellið síðan á eininguna **Skref 1**.</span><span class="sxs-lookup"><span data-stu-id="28350-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="28350-125">Hægrismellið á eininguna **Skref 1** og veljið síðan **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="28350-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="28350-126">Í glugganum **Eiginleikar** skal velja **Skilyrði** á yfirlitsstikunni vinstra megin.</span><span class="sxs-lookup"><span data-stu-id="28350-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="28350-127">Veljið **Keyra á þessu þrepi aðeins þegar eftirfarandi skilyrði eru í gildi**.</span><span class="sxs-lookup"><span data-stu-id="28350-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="28350-128">Veljið **Bæta við skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="28350-128">Select **Add condition**.</span></span> <span data-ttu-id="28350-129">Eftir **Hvar** skal velja **Hæfni í sjálfsafgreiðslu starfsmanns** og síðan velja **Hæfni í sjálfsafgreiðslu starfsmanns.Einstaklingur**.</span><span class="sxs-lookup"><span data-stu-id="28350-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="28350-130">Eftir **er** skal velja **reit** og síðan velja **Tengsl notanda við einstakling.Einstaklingur**.</span><span class="sxs-lookup"><span data-stu-id="28350-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="28350-131">[![Tilgreina skilyrði](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="28350-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="28350-132">Veljið **Úthlutun** á yfirlitsstikunni vinstra megin.</span><span class="sxs-lookup"><span data-stu-id="28350-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="28350-133">Í flipanum **Úthlutunargerð** skal velja **Stigveldi**.</span><span class="sxs-lookup"><span data-stu-id="28350-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="28350-134">Í flipanum **Stigveldisval**, í reitnum **Gerð stigveldis:** skal velja **Stjórnendastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="28350-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="28350-135">[![Tilgreina stjórnendastigveldi](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="28350-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="28350-136">Veljið **Loka**, veljið **Verkflæði** í brauðmylsnuvinnusvæðinu og veljið því næst **Vista og loka**.</span><span class="sxs-lookup"><span data-stu-id="28350-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="28350-137">Frekari upplýsingar um stofnun verkflæðis er að finna í [Yfirlit yfir verkflæðiskerfi](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="28350-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="28350-138">Slá inn hæfni starfsmanns</span><span class="sxs-lookup"><span data-stu-id="28350-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="28350-139">Veljið starfsmann.</span><span class="sxs-lookup"><span data-stu-id="28350-139">Select a worker.</span></span>

2. <span data-ttu-id="28350-140">Á aðgerðarstikunni á síðu **Starfsmanns** skal velja **Einstaklingur** og velja síðan **Hæfni**.</span><span class="sxs-lookup"><span data-stu-id="28350-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="28350-141">Á síðunni **Hæfni** skal ljúka eftirfarandi reitum fyrir hverja hæfni:</span><span class="sxs-lookup"><span data-stu-id="28350-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="28350-142">**Hæfni**: Veljið hæfni.</span><span class="sxs-lookup"><span data-stu-id="28350-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="28350-143">**Stigsgerð**: Veljið **Raunverulegt** fyrir hæfni sem starfsmaður býr þegar yfir eða veljið **Markmið** fyrir hæfni sem starfsmaður stefnir að.</span><span class="sxs-lookup"><span data-stu-id="28350-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="28350-144">**Stig**: Veljið stig fyrir hæfni starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="28350-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="28350-145">**Dagsetning stigs**: Veljið dagsetningu í dagbókarforritinu.</span><span class="sxs-lookup"><span data-stu-id="28350-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="28350-146">**Prófdómari**: Veljið prófdómara af listanum ef við á.</span><span class="sxs-lookup"><span data-stu-id="28350-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="28350-147">Hægt er að sía leitina.</span><span class="sxs-lookup"><span data-stu-id="28350-147">You can filter your search.</span></span>
   - <span data-ttu-id="28350-148">**Reynsla í árum**: Færið inn reynslu í árum.</span><span class="sxs-lookup"><span data-stu-id="28350-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="28350-149">**Staðfest**: Ef hæfnin er staðfest skal haka við kassann.</span><span class="sxs-lookup"><span data-stu-id="28350-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="28350-150">**Staðfest af**: Færið inn heiti staðfestingaraðila.</span><span class="sxs-lookup"><span data-stu-id="28350-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="28350-151">Þegar búið er að færa inn hæfni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="28350-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="28350-152">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="28350-152">See also</span></span>

[<span data-ttu-id="28350-153">Skilgreina hæfni</span><span class="sxs-lookup"><span data-stu-id="28350-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="28350-154">Kortleggja hæfni</span><span class="sxs-lookup"><span data-stu-id="28350-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]