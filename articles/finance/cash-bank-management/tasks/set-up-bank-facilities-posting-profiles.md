---
title: Setja upp starfsstöðvar banka og bókunarreglur fyrir ábyrgðarbréf
description: Þetta verk stofnar bankaaðstöðu og bókunarreglu sem þarf til að vinna ábyrgðarbréf.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 427159048ffbb17749e813d67a900622900a7f21
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178300"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="5ae50-103">Setja upp starfsstöðvar banka og bókunarreglur fyrir ábyrgðarbréf</span><span class="sxs-lookup"><span data-stu-id="5ae50-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ae50-104">Þetta verk stofnar bankaaðstöðu og bókunarreglu sem þarf til að vinna ábyrgðarbréf.</span><span class="sxs-lookup"><span data-stu-id="5ae50-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="5ae50-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="5ae50-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="5ae50-106">Fjárhagsfæribreyta</span><span class="sxs-lookup"><span data-stu-id="5ae50-106">General ledger parameter</span></span>
1. <span data-ttu-id="5ae50-107">Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="5ae50-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="5ae50-108">Útvíkka hlutann Bankaskjal.</span><span class="sxs-lookup"><span data-stu-id="5ae50-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="5ae50-109">Veldu valkostinn Virkja ábyrgðarbréf.</span><span class="sxs-lookup"><span data-stu-id="5ae50-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="5ae50-110">Í reitnum Færslubók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5ae50-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5ae50-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5ae50-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="5ae50-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5ae50-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5ae50-113">Smellt er á flipann Númeraraðir.</span><span class="sxs-lookup"><span data-stu-id="5ae50-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="5ae50-114">Skilgreina númeraraðarkóða fyrir númer ábyrgðarbréfs og færslutilvísanir ábyrgðarbréfs</span><span class="sxs-lookup"><span data-stu-id="5ae50-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="5ae50-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5ae50-115">Click Save.</span></span>
9. <span data-ttu-id="5ae50-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5ae50-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="5ae50-117">Stofna Bankaaðstöðu</span><span class="sxs-lookup"><span data-stu-id="5ae50-117">Create Bank facility</span></span>
1. <span data-ttu-id="5ae50-118">Fara í Reiðufjár- og bankastjórnun > Uppsetning >Bankaaðstöður.</span><span class="sxs-lookup"><span data-stu-id="5ae50-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="5ae50-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5ae50-119">Click New.</span></span>
3. <span data-ttu-id="5ae50-120">Í svæðið Aðstöðuflokkur skal færa inn heiti bankaaðstöðuflokks fyrir ábyrgðarbréf færslu.</span><span class="sxs-lookup"><span data-stu-id="5ae50-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="5ae50-121">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="5ae50-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5ae50-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5ae50-122">Click Save.</span></span>
6. <span data-ttu-id="5ae50-123">Smellið á flipann Aðstöðugerð.</span><span class="sxs-lookup"><span data-stu-id="5ae50-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="5ae50-124">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5ae50-124">Click New.</span></span>
8. <span data-ttu-id="5ae50-125">Í svæðið Aðstöðugerð skal slá inn heiti gerðar bankaaðstöðu sem tengist bankaaðstöðusamningnum.</span><span class="sxs-lookup"><span data-stu-id="5ae50-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="5ae50-126">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5ae50-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="5ae50-127">Í reitnum Aðstöðuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5ae50-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5ae50-128">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5ae50-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5ae50-129">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5ae50-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5ae50-130">Í reitnum Eðli aðstöðu skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="5ae50-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="5ae50-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5ae50-131">Click Save.</span></span>
15. <span data-ttu-id="5ae50-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5ae50-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="5ae50-133">Bókunarregla banka</span><span class="sxs-lookup"><span data-stu-id="5ae50-133">Bank posting profile</span></span>
1. <span data-ttu-id="5ae50-134">Fara í Reiðufjár- og bankastjórnun > Uppsetning >Bókunarregla bankaskjala.</span><span class="sxs-lookup"><span data-stu-id="5ae50-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="5ae50-135">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5ae50-135">Click New.</span></span>
3. <span data-ttu-id="5ae50-136">Í reitnum Númer reiknings/flokks smellirðu á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5ae50-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5ae50-137">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5ae50-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5ae50-138">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5ae50-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5ae50-139">Í reitnum Gera upp lykil velurðu lykil fyrir uppgjör.</span><span class="sxs-lookup"><span data-stu-id="5ae50-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="5ae50-140">Í reitnum Gjaldalykill velurðu lykil fyrir kostnaðarfærslur.</span><span class="sxs-lookup"><span data-stu-id="5ae50-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="5ae50-141">Í reitnum Framlegðarlykill velurðu lykil fyrir framlegðarfærslu.</span><span class="sxs-lookup"><span data-stu-id="5ae50-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="5ae50-142">Í reitnum Slitalykill velurðu lykil fyrir slitafærslu.</span><span class="sxs-lookup"><span data-stu-id="5ae50-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="5ae50-143">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="5ae50-143">Click Save.</span></span>
11. <span data-ttu-id="5ae50-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5ae50-144">Close the page.</span></span>
