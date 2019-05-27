---
title: Setja upp staðgreiðsluskatt
description: Staðgreiðsluskattur er skattur á lánardrottna sem ekki stofnar VSK-færslur.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 382b6332665af2491563960a75d498a4f007aba8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562789"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="f3201-103">Setja upp staðgreiðsluskatt</span><span class="sxs-lookup"><span data-stu-id="f3201-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3201-104">Staðgreiðsluskattur er skattur á lánardrottna sem ekki stofnar VSK-færslur.</span><span class="sxs-lookup"><span data-stu-id="f3201-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="f3201-105">Staðgreiðsluskattur sem er reiknaður á greiðslur lánardrottins er skuld.</span><span class="sxs-lookup"><span data-stu-id="f3201-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="f3201-106">Þess vegna eru bara efnahagslyklar eða afsláttarlyklar gildir við bókun á staðgreiðsluskatti.</span><span class="sxs-lookup"><span data-stu-id="f3201-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="f3201-107">Þessi leiðarvísi fyrir verk sýnir hvernig á að setja upp staðgreiðsluskatt.</span><span class="sxs-lookup"><span data-stu-id="f3201-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="f3201-108">Fara á Skattur > Óbeinir skattar > Staðgreiðsluskattur > Staðgreiðsluskattskóðar.</span><span class="sxs-lookup"><span data-stu-id="f3201-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="f3201-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f3201-109">Click New.</span></span>
3. <span data-ttu-id="f3201-110">Færa inn gildi í svæðinu fyrir staðgreiðsluskattskóði.</span><span class="sxs-lookup"><span data-stu-id="f3201-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="f3201-111">Í svæðið heiti staðgreiðsluskatts, færið inn heiti staðgreiðsluskattskóðann.</span><span class="sxs-lookup"><span data-stu-id="f3201-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="f3201-112">Í Aðaltöflu svæðinu, veljið aðallykil fyrir bókun staðgreiðsluskattskuldarinnar.</span><span class="sxs-lookup"><span data-stu-id="f3201-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="f3201-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f3201-113">Click Save.</span></span>
7. <span data-ttu-id="f3201-114">Smella á Gildi.</span><span class="sxs-lookup"><span data-stu-id="f3201-114">Click Values.</span></span>
8. <span data-ttu-id="f3201-115">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f3201-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f3201-116">Í svæðinu Gildi færa inn prósentu sem er notuð til útreiknings á staðgreiðsluskattinum.</span><span class="sxs-lookup"><span data-stu-id="f3201-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="f3201-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f3201-117">Click Save.</span></span>
11. <span data-ttu-id="f3201-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f3201-118">Close the page.</span></span>
12. <span data-ttu-id="f3201-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f3201-119">Click Save.</span></span>
13. <span data-ttu-id="f3201-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f3201-120">Close the page.</span></span>
14. <span data-ttu-id="f3201-121">Fara á Skattur > Óbeinir skattar > Staðgreiðsluskattur > Staðgreiðsluskattshópar.</span><span class="sxs-lookup"><span data-stu-id="f3201-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="f3201-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f3201-122">Click New.</span></span>
16. <span data-ttu-id="f3201-123">Færa inn kennimerki staðgreiðsluskattflokkur í flokkssvæði staðgreiðsluskatts.</span><span class="sxs-lookup"><span data-stu-id="f3201-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="f3201-124">Færið inn heiti staðgreiðsluskattflokkur í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="f3201-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="f3201-125">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f3201-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="f3201-126">Veljið staðgreiðsluskattskóði í svæðinu fyrir staðgreiðsluskattskóði.</span><span class="sxs-lookup"><span data-stu-id="f3201-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="f3201-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f3201-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="f3201-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f3201-128">Click Save.</span></span>

