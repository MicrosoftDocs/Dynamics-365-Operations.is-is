---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (11. janúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a89ba455acbed9724da6826ac4d41c6a481490
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518244"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a><span data-ttu-id="66c55-103">Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (11. janúar 2019)</span><span class="sxs-lookup"><span data-stu-id="66c55-103">What's new or changed in Dynamics 365 for Talent Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="66c55-104">**Smíði 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="66c55-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="66c55-105">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.</span><span class="sxs-lookup"><span data-stu-id="66c55-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="66c55-106">Breytingar</span><span class="sxs-lookup"><span data-stu-id="66c55-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="66c55-107">Sannprófa leyfisbeiðnir með því að spá fyrir um tiltæka stöðu</span><span class="sxs-lookup"><span data-stu-id="66c55-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="66c55-108">Breytingar sem gerðar eru í þessari útgáfu leyfa starfsmönnum að biðja um leyfi fram í tímann án þess að draga frá núverandi stöðu.</span><span class="sxs-lookup"><span data-stu-id="66c55-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="66c55-109">Stöðluð verkflæði verða notuð fyrir allar beiðnir fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="66c55-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="66c55-110">Nánari upplýsingar er að finna í [Uppsöfnun frís sem byggist á vinnustundum](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="66c55-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="66c55-111">Skoðaðu áætlaða stöðu leyfis í ESS og Fólk</span><span class="sxs-lookup"><span data-stu-id="66c55-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="66c55-112">Þessi eiginleiki gerir mannauðsstjóra, stjórnendum og starfsmönnum kleift að skoða stöður fyrir leyfistímabil fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="66c55-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="66c55-113">Starfsmenn geta skoðað framtíðarstöður á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna** og mannauðsstjóri hefur aðgang að sömu upplýsingum með vinnusvæðinu **Fólk**.</span><span class="sxs-lookup"><span data-stu-id="66c55-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="66c55-114">Tilkynningar um breytingar á stöðum leyfa</span><span class="sxs-lookup"><span data-stu-id="66c55-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="66c55-115">Leyfisstöður munu sýna núverandi stöðu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="66c55-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="66c55-116">Framtíðarstöður er að finna á vinnusvæðunum **Sjálfsafgreiðsla starfsmanna** og **Fólk** með því að slá inn „frá og með dagsetningu“ til að reikna út áætlaða stöðu.</span><span class="sxs-lookup"><span data-stu-id="66c55-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="66c55-117">Leiðsögn hefur verið bætt við til að skoða áætlaðar stöður á eftirfarandi svæðum:</span><span class="sxs-lookup"><span data-stu-id="66c55-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="66c55-118">Spjaldið **Frítími** á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="66c55-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="66c55-119">Spjaldið **Leyfi og fjarvistir** á vinnusvæðinu **Sjálfsafgreiðsla stjórnanda**.</span><span class="sxs-lookup"><span data-stu-id="66c55-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="66c55-120">Síðan **Leyfi og fjarvistir** á vinnusvæðinu **Fólk**.</span><span class="sxs-lookup"><span data-stu-id="66c55-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="66c55-121">Leyfa aukastafi fyrir breytilegt launafyrirkomulag (reiðufjáráætlanir)</span><span class="sxs-lookup"><span data-stu-id="66c55-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="66c55-122">Breytileg umbun og áætlanir reiðufjár er nú með aukalegan sveigjanleika fyrir upphæðir og hnekkingar fyrir gildi þar sem upphæðir eru með aukastöfum.</span><span class="sxs-lookup"><span data-stu-id="66c55-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="66c55-123">Ekki er hægt að breyta dagsetningum fyrir skráningar á breytilegum launum eftir að áætlunin er vistuð</span><span class="sxs-lookup"><span data-stu-id="66c55-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="66c55-124">Þessi breyting gerir kleift að uppfæra lokadag áætlunar (lengd eða útrunnin) eftir að áætlunin hefur verið vistuð.</span><span class="sxs-lookup"><span data-stu-id="66c55-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="66c55-125">Enn er hægt að kveikja og slökkva á áætlunum óháð upphafs- og lokadögum.</span><span class="sxs-lookup"><span data-stu-id="66c55-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="66c55-126">Launaupplýsingar eru tiltækar þegar öryggishlutverki launastjóra hefur verið úthlutað</span><span class="sxs-lookup"><span data-stu-id="66c55-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="66c55-127">Hlutverk launastjóra hefur verið uppfært til að hafa aðgang að launaupplýsingum á meðan beiðnin er í ferli.</span><span class="sxs-lookup"><span data-stu-id="66c55-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="66c55-128">Sjálfsafgreiðsla starfsmanns | Köfun niður í stöðustigveldi úr reit mistekst að sækja yfirhnút</span><span class="sxs-lookup"><span data-stu-id="66c55-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="66c55-129">Breytingar hafa verið gerðar til að koma í veg fyrir villu sem átti sér stað þegar stöðustigveldinu var bætt við ný vinnusvæði og við flettingu í skipulagseiningum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="66c55-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="66c55-130">Ný villuleitarboð þegar númer starfsmanns er notað</span><span class="sxs-lookup"><span data-stu-id="66c55-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="66c55-131">Breyting hefur verið gerð til að skýra hvað vandamálið er þegar starfsmaður er ráðinn og næsta starfsmannanúmer er í notkun.</span><span class="sxs-lookup"><span data-stu-id="66c55-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="66c55-132">Vinnusvæði fyrir sjálfsafgreiðslu starfsmanns valið sem upphafssíða</span><span class="sxs-lookup"><span data-stu-id="66c55-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="66c55-133">Þegar vinnusvæðið **Sjálfsafgreiðsla starfsmanna** er valið sem upphafssíða fyrir notanda og þessum notanda er ekki úthlutað hlutverki starfsmanns mun kerfið beina honum að sjálfgefna yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="66c55-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="66c55-134">Ástæðukóði uppsagnar uppfærir skrá stöðuverkefnis</span><span class="sxs-lookup"><span data-stu-id="66c55-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="66c55-135">Ástæðukóði uppsagnar uppfærir nú stöðuverkefnið þegar starfsmanni er sagt upp störfum og stöðunni er lokað.</span><span class="sxs-lookup"><span data-stu-id="66c55-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
