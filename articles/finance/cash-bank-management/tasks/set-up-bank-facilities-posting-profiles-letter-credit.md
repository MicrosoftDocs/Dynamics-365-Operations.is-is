---
title: Setja upp starfsstöðvar banka og bókunarreglur fyrir bankaábyrgð
description: Þetta ferli fer í gegnum stofnun Bankaaðstöðu og bókunarreglu sem þarf til að vinna kreditbréf.
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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc94100461bc82e9e7cd243f198711ab61a79b0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225274"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="e4d3c-103">Setja upp starfsstöðvar banka og bókunarreglur fyrir bankaábyrgð</span><span class="sxs-lookup"><span data-stu-id="e4d3c-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4d3c-104">Þetta ferli fer í gegnum stofnun Bankaaðstöðu og bókunarreglu sem þarf til að vinna kreditbréf.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="e4d3c-105">Þetta verkefni notar sýnifyrirtækið ‚USMF‘.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="e4d3c-106">Fjárhagsfæribreyta</span><span class="sxs-lookup"><span data-stu-id="e4d3c-106">General ledger parameter</span></span>
1. <span data-ttu-id="e4d3c-107">Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="e4d3c-108">Útvíkka hlutann Bankaskjal.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="e4d3c-109">Veldu valkostinn Virkja innflutning kreditbréfs.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="e4d3c-110">Veldu valkostinn Virkja útflutning kreditbréfs.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="e4d3c-111">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-111">Click Save.</span></span>
6. <span data-ttu-id="e4d3c-112">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="e4d3c-113">Stofna Bankaaðstöðu</span><span class="sxs-lookup"><span data-stu-id="e4d3c-113">Create Bank facility</span></span>
1. <span data-ttu-id="e4d3c-114">Fara í Reiðufjár- og bankastjórnun > Uppsetning >Bankaaðstöður.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="e4d3c-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-115">Click New.</span></span>
3. <span data-ttu-id="e4d3c-116">Í reitnum Aðstöðuflokkur færirðu inn heiti á bankaaðstöðu.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="e4d3c-117">Í svæðinu Lýsing er færð inn lýsing bankaaðstöðuflokks.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="e4d3c-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-118">Click Save.</span></span>
6. <span data-ttu-id="e4d3c-119">Smellið á flipann Aðstöðugerð.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="e4d3c-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-120">Click New.</span></span>
8. <span data-ttu-id="e4d3c-121">Færið inn einkvæman kóða í reitnum Aðstaða.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="e4d3c-122">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="e4d3c-123">Í reitnum Aðstöðuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e4d3c-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e4d3c-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="e4d3c-126">Í svæðinu Eðli aðstöðu velurðu eðli bankaaðstöðunnar.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="e4d3c-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-127">Click Save.</span></span>
15. <span data-ttu-id="e4d3c-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="e4d3c-129">Bókunarregla banka</span><span class="sxs-lookup"><span data-stu-id="e4d3c-129">Bank posting profile</span></span>
1. <span data-ttu-id="e4d3c-130">Fara í Reiðufjár- og bankastjórnun > Uppsetning >Bókunarregla bankaskjala.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="e4d3c-131">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-131">Click New.</span></span>
3. <span data-ttu-id="e4d3c-132">Í reitnum Númer reiknings/flokks smellirðu á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e4d3c-133">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e4d3c-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e4d3c-135">Veldu aðallykil til jöfnunar.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="e4d3c-136">Þessi reikningur er notaður við útreikning á sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="e4d3c-137">Í reitnum Gjaldalykill velurðu lykil fyrir kostnaðarfærslur.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="e4d3c-138">Í reitnum Framlegðarlykill velurðu lykil fyrir framlegðarfærslur.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="e4d3c-139">Þessi lykill er tekjufærður þegar opnunarframlegð er bókuð og kreditfærð þegar greiðslan er bókuð.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="e4d3c-140">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e4d3c-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]