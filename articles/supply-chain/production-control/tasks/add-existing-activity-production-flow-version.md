---
title: Bæta fyrirliggjandi verkþætti við útgáfu framleiðsluflæðis
description: Þegar nýjar útgáfur framleiðsluflæða eru stofnaðar, er hægt að velja að bæta við aðgerðum sem voru stofnaðar fyrir eldri útgáfur, við nýju útgáfuna.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f95958e57b1b1a93e43eb2cf02d2651ccb9587b6
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979757"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="e23c7-103">Bæta fyrirliggjandi verkþætti við útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="e23c7-103">Add an existing activity to a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e23c7-104">Þegar nýjar útgáfur framleiðsluflæða eru stofnaðar, er hægt að velja að bæta við aðgerðum sem voru stofnaðar fyrir eldri útgáfur, við nýju útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="e23c7-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="e23c7-105">Þessi verklýsing sýnir hvernig er ný útgáfa stofnuð fyrir fyrirliggjandi framleiðsluflæði, án þess að afrita verkþætti.</span><span class="sxs-lookup"><span data-stu-id="e23c7-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="e23c7-106">Í næsta skref er fyrirliggjandi verkþáttar bætt við í nýju útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="e23c7-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="e23c7-107">Þetta verki krefst framleiðsluflæði með útgáfu og verkþætti sem þegar hafa verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="e23c7-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="e23c7-108">Stofna nýja útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="e23c7-108">Create a new production flow version</span></span>
1. <span data-ttu-id="e23c7-109">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="e23c7-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="e23c7-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e23c7-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e23c7-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e23c7-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e23c7-112">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="e23c7-112">Click Edit.</span></span>
5. <span data-ttu-id="e23c7-113">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e23c7-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="e23c7-114">Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="e23c7-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="e23c7-115">Athugið að áður en stofnuð er nýja útgáfu framleiðsluflæðis, skal athuga lokadagsetningu- og tíma hinnar virku útgáfu.</span><span class="sxs-lookup"><span data-stu-id="e23c7-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="e23c7-116">Ný útgáfa verður stofnuð með virka upphafsdagsetningu, sem tengist lokadagsetningu valinnar útgáfu.</span><span class="sxs-lookup"><span data-stu-id="e23c7-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="e23c7-117">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e23c7-117">Click Add.</span></span>
8. <span data-ttu-id="e23c7-118">Velja Nei fyrir í reitnum Afrita úr útgáfu.</span><span class="sxs-lookup"><span data-stu-id="e23c7-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="e23c7-119">Veljið Nei til að byrja auða útgáfu ef flestum verkþætti afrituðu útgáfu er skipt út fyrir nýjum verkþætti.</span><span class="sxs-lookup"><span data-stu-id="e23c7-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="e23c7-120">Bæta við óbreyttum verkþætti til að bæta við núverandi aðgerðum í skjámyndinni Verkþættir handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e23c7-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="e23c7-121">Velja Nei í svæðinu gera eftirrit af kanban-reglum.</span><span class="sxs-lookup"><span data-stu-id="e23c7-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="e23c7-122">Þegar verkþættir eru ekki afritaðar í nýju útgáfuna, er ekki hægt að afrita kanban-reglur þegar verið er að stofna nýju útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="e23c7-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="e23c7-123">Í staðinn muntu nota kanban-aðgerðina stofna útskiptingu síðar í skjámynd kanban-reglu, til að skipta út kanban-reglum hinnar gömlu útgáfu framleiðsluflæðis með kanban-reglum með því að nota aðgerðir hinnar nýju útgáfu.</span><span class="sxs-lookup"><span data-stu-id="e23c7-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="e23c7-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e23c7-124">Click OK.</span></span>
11. <span data-ttu-id="e23c7-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e23c7-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="e23c7-126">Bæta við fyrirliggjandi verkþætti.</span><span class="sxs-lookup"><span data-stu-id="e23c7-126">Add an existing activity</span></span>
1. <span data-ttu-id="e23c7-127">Smellt er á Verkþætti.</span><span class="sxs-lookup"><span data-stu-id="e23c7-127">Click Activities.</span></span>
2. <span data-ttu-id="e23c7-128">Smelltu á Bæta við núverandi til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e23c7-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="e23c7-129">Finndu og veldu fyrirliggjandi verkþátt til að bæta við nýju útgáfu framleiðsluflæðis.</span><span class="sxs-lookup"><span data-stu-id="e23c7-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="e23c7-130">Athugið að listinn sýnir alla verkþætti sem hafa verið stofnaðar fyrir þessa framleiðsluflæði fyrir allar eldri útgáfur flæðis.</span><span class="sxs-lookup"><span data-stu-id="e23c7-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="e23c7-131">Í reitinn verkþáttur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e23c7-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="e23c7-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e23c7-132">Click OK.</span></span>

