---
title: Færa inn vinnukort verks
description: Þetta ferli leyfir þér að stofna vinnukort með því að nota skjámynd tómt vinnukort .
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 136efa1178089adb88820002a19e99ef83e1b47e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009445"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="52117-103">Færa inn vinnukort verks</span><span class="sxs-lookup"><span data-stu-id="52117-103">Enter project timesheets</span></span>



<span data-ttu-id="52117-104">Þetta ferli leyfir þér að stofna vinnukort með því að nota skjámynd tómt vinnukort .</span><span class="sxs-lookup"><span data-stu-id="52117-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="52117-105">Nýtt tímablað getur verið byggt á upplýsingum úr fyrra tímablaði eða úr verki og verkþáttarúthlutunum í **Eftirlæti notanda**.</span><span class="sxs-lookup"><span data-stu-id="52117-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="52117-106">Að sjálfgefnu sýnir listasíðan **Öll tímablöð** öll tímablöð þín fyrir núgildandi tímabil.</span><span class="sxs-lookup"><span data-stu-id="52117-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="52117-107">Hægt er að nota fellilistann fyrir reitinn **Sýna** á síðunni **Mín tímablöð** til að sía tímablaðalista eftir tímabili eða verki, eða skoða tímablöð sem voru stofnuð fyrir hönd annarra starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="52117-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="52117-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USSI.</span><span class="sxs-lookup"><span data-stu-id="52117-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="52117-109">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Tímablöð > Tímablöðin mín**.</span><span class="sxs-lookup"><span data-stu-id="52117-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="52117-110">Til að færa inn nýtt tímablað skaltu smella á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="52117-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="52117-111">Tilföng fellilistanum sýnir starfsmanns sem er úthlutað á núverandi notanda, sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="52117-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="52117-112">Ef notandinn er skráður sem fulltrúa, þetta mun birta lista yfir nöfn þannig að notandi má slá inn tímablað fyrir þeirra hönd.</span><span class="sxs-lookup"><span data-stu-id="52117-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="52117-113">í retinum **Dagsetning** ritarðu dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="52117-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="52117-114">Ef þessi valkostur er valinn er nýrri tímablaðslínur stofnuð með því að nota stillingar vinnukorts sem voru skilgreind sem eftirlæti.</span><span class="sxs-lookup"><span data-stu-id="52117-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="52117-115">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="52117-115">Click **OK**.</span></span>
5. <span data-ttu-id="52117-116">Smelltu á **Nýja línu**.</span><span class="sxs-lookup"><span data-stu-id="52117-116">Click **New line**.</span></span>
6. <span data-ttu-id="52117-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="52117-117">In the list, mark the selected row.</span></span> <span data-ttu-id="52117-118">Reiturinn **Lögaðili** birtir núgildandi lögaðila sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="52117-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="52117-119">Í reitnum **Verk** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="52117-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="52117-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="52117-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="52117-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="52117-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="52117-122">Í reitnum **Verkþáttarnúmer** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="52117-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="52117-123">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="52117-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="52117-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="52117-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="52117-125">Í reitnum **Flokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="52117-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="52117-126">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="52117-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="52117-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="52117-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="52117-128">Færið inn fjölda stunda unnar á hverjum degi.</span><span class="sxs-lookup"><span data-stu-id="52117-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="52117-129">Færið inn klukkustundir á aukastafasniði.</span><span class="sxs-lookup"><span data-stu-id="52117-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="52117-130">Ef til dæmis er unnið í tvo tíma og fimmtán mínútur, er fært inn 2.25.</span><span class="sxs-lookup"><span data-stu-id="52117-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="52117-131">Í **Upplýsingar um línu** eru eftirfarandi valkostir tiltækir:</span><span class="sxs-lookup"><span data-stu-id="52117-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="52117-132">Bættu upplýsingum um skatta og fjárhagsvíddir við á flipann **Almennt** og **Fjárhagslegar víddir**.</span><span class="sxs-lookup"><span data-stu-id="52117-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="52117-133">Bættu við athugasemdum um tímalínulínuna á flipann **Athugasemd**.</span><span class="sxs-lookup"><span data-stu-id="52117-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="52117-134">Í **aðgerðarsvæðinu** smellirðu á **Verkflæði** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="52117-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="52117-135">Smelltu á **Senda**.</span><span class="sxs-lookup"><span data-stu-id="52117-135">Click **Submit**.</span></span>
22. <span data-ttu-id="52117-136">Smelltu á **Senda**.</span><span class="sxs-lookup"><span data-stu-id="52117-136">Click **Submit**.</span></span>
