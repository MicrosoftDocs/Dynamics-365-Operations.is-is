---
title: Stofna uppsöfnunarfærslur fyrir fjárhag
description: Þessar verkleiðbeiningar fara í gegnum myndun uppsöfnunarfærslna höfuðbókar sem eru byggðar á grunni uppsöfnunarskema.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06743ca3ed13906e3f65d3783db7a7f74fb53e3f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186188"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="a57f6-103">Stofna uppsöfnunarfærslur fyrir fjárhag</span><span class="sxs-lookup"><span data-stu-id="a57f6-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a57f6-104">Verk leiðbeiningar fer í gegnum myndun uppsöfnunarfærslna höfuðbókar sem eru byggðar á grunni uppsöfnunarskema</span><span class="sxs-lookup"><span data-stu-id="a57f6-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="a57f6-105">Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="a57f6-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="a57f6-106">Á listanum skal finna og velja viðeigandi færslubók eða stofna nýja.</span><span class="sxs-lookup"><span data-stu-id="a57f6-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="a57f6-107">Smellið til að fylgja tenglinum í reitnum Rununúmer færslubókar.</span><span class="sxs-lookup"><span data-stu-id="a57f6-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="a57f6-108">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a57f6-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a57f6-109">Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a57f6-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="a57f6-110">Í þessu dæmi skilgreinum við kostnað fyrir trygginguna.</span><span class="sxs-lookup"><span data-stu-id="a57f6-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="a57f6-111">Það verður reglubundin kostnaðarupphæð.</span><span class="sxs-lookup"><span data-stu-id="a57f6-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="a57f6-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="a57f6-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="a57f6-113">Í reitnum Debet skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="a57f6-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="a57f6-114">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a57f6-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="a57f6-115">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="a57f6-115">Click Functions.</span></span>
10. <span data-ttu-id="a57f6-116">Smellt er á fjárhagsuppsafnanir.</span><span class="sxs-lookup"><span data-stu-id="a57f6-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="a57f6-117">Í reitnum Auðkenni uppsöfnunar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a57f6-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="a57f6-118">Í listanum skal finna og velja uppsöfnunarskemað sem á að beita.</span><span class="sxs-lookup"><span data-stu-id="a57f6-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="a57f6-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a57f6-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a57f6-120">Dagsetning er rituð í reitinn Upphafsdagur.</span><span class="sxs-lookup"><span data-stu-id="a57f6-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="a57f6-121">Smella á Færslur.</span><span class="sxs-lookup"><span data-stu-id="a57f6-121">Click Transactions.</span></span>
16. <span data-ttu-id="a57f6-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a57f6-122">Close the page.</span></span>
17. <span data-ttu-id="a57f6-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a57f6-123">Click OK.</span></span>
18. <span data-ttu-id="a57f6-124">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="a57f6-124">Click Post.</span></span>

