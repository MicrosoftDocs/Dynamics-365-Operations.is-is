---
title: "Stofna fjárhagsáætlun úr færslulyklum og samtölulyklum"
description: "Þessi grein gefur yfirlit yfir ferli þess að búa til fjárhagsáætlanir á grunni heildarreikninga. Hún útskýrir einnig hvernig skuli kveikja á fjárhagsáætlunarstýringu fyrir heildarreikninga, ef fjárhagsáætlunarstýringar er krafist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e3c86bd32a05a392fcb82a86f2c461cc3abfb03
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="f05c8-104">Stofna fjárhagsáætlun úr færslulyklum og samtölulyklum</span><span class="sxs-lookup"><span data-stu-id="f05c8-104">Create a budget from transaction accounts and total accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f05c8-105">Þessi grein gefur yfirlit yfir ferli þess að búa til fjárhagsáætlanir á grunni heildarreikninga.</span><span class="sxs-lookup"><span data-stu-id="f05c8-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="f05c8-106">Hún útskýrir einnig hvernig skuli kveikja á fjárhagsáætlunarstýringu fyrir heildarreikninga, ef fjárhagsáætlunarstýringar er krafist.</span><span class="sxs-lookup"><span data-stu-id="f05c8-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="f05c8-107">Bæði fjárhagsáætlun og skjöl í fjárhagsáætlunarskrá leyfa fjárhagsáætlanagerð á aðallyklum sem hefur°tegund aðallykils°sem **Samtals**.</span><span class="sxs-lookup"><span data-stu-id="f05c8-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="f05c8-108">Aðeins er hægt að bóka rauntölur í aðallykla færslur.</span><span class="sxs-lookup"><span data-stu-id="f05c8-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="f05c8-109">Fyrir°reglubundnu vinnsluna **Mynda fjárhagsáætlun úr fjárhag** í flipanum **Uppruni** er hægt að tilgreina **Samtals** aðallykilgerð sem skilyrði.</span><span class="sxs-lookup"><span data-stu-id="f05c8-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="f05c8-110">Í þessu tilfelli verður hver samtal aðallykils tekin með í°markfjárhagsáætlunina og°upphæðin jafngildir heildarupphæð á sviði°valinna°aðallykla.</span><span class="sxs-lookup"><span data-stu-id="f05c8-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="f05c8-111">Hægt er að virkja°fjárhagsáætlunarstýringu fyrir aðallykla af gerðinni **Samtals**.</span><span class="sxs-lookup"><span data-stu-id="f05c8-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="f05c8-112">Þessi virkni er studd gegnum notkun fjárhagsáætlunarflokka.</span><span class="sxs-lookup"><span data-stu-id="f05c8-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="f05c8-113">Fyrir hvern samtals aðallykil verður fjárhagsáætlunin sem á að stýra fyrir flokk fjárhagsáætlana að vera stofnuð á **síðunni **Skilgreining fjárhagsáætlunarstýringar.</span><span class="sxs-lookup"><span data-stu-id="f05c8-113">For each total main account, the budget that should be controlled for a budget group must be created on the **Budget control configuration **page.</span></span> <span data-ttu-id="f05c8-114">Skilyrði sem er tilgreind verða að vera samtölur aðallykils og svið lykla.</span><span class="sxs-lookup"><span data-stu-id="f05c8-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="f05c8-115">Til að hraða stofnun fjárhagsáætlunarflokka er hægt nýta Stýringu fjárhagsáætlunarflokka gagnaeiningar.</span><span class="sxs-lookup"><span data-stu-id="f05c8-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="f05c8-116">Þegar fjárhagsáætlun er notuð í skýrslugerð, til dæmis í fjárhagsskýrslu, er samtala áætlunarinnar fyrir samtölulykilinn samsett úr eftirfarandi upphæðum:</span><span class="sxs-lookup"><span data-stu-id="f05c8-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="f05c8-117">Fjárhagsáætlanirnar sem eru stofnaðar úr hverjum færslufjárhagslykli innan bils samtölulykilsins.</span><span class="sxs-lookup"><span data-stu-id="f05c8-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="f05c8-118">Fjárhagsáætlunarupphæðin sem er færð beint inn á samtölulykilinn.</span><span class="sxs-lookup"><span data-stu-id="f05c8-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="f05c8-119">Þetta°gerir kleift að stofna aðskildar fjárhagsáætlanir fyrir mikilvægustu færslulyklana innan bilsins í samtölulyklinum og að bæta eftirstandandi upphæð fjárhagsáætlunar við samtölulykilinn.</span><span class="sxs-lookup"><span data-stu-id="f05c8-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




