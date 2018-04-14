---
title: Yfirlit yfir uppsafnanir
description: "Þessi grein lýsir áföllnum gjöldum og veitir upplýsingar um hvernig skuli setja þær upp og stofna færslur."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0b4d8e7eb268857ce753415a24e600b8006eb5e3
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="fffa0-103">Yfirlit yfir uppsafnanir</span><span class="sxs-lookup"><span data-stu-id="fffa0-103">Accruals overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="fffa0-104">Þessi grein lýsir áföllnum gjöldum og veitir upplýsingar um hvernig skuli setja þær upp og stofna færslur.</span><span class="sxs-lookup"><span data-stu-id="fffa0-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="fffa0-105">Uppsafnanir eru notaðar í rekstrarbókhaldi til að rekja tekjur sem eru viðurkenndar á tímabilinu sem þær eru fengnar í, ekki þegar greiðsla er móttekin, og til að rekja útgjöld (kostnað) sem eru viðurkennd þegar þau eiga sér stað, ekki þegar greiðsla er gerð.</span><span class="sxs-lookup"><span data-stu-id="fffa0-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="fffa0-106">Uppsöfnunarskemu</span><span class="sxs-lookup"><span data-stu-id="fffa0-106">Accrual schemes</span></span>
<span data-ttu-id="fffa0-107">Uppsöfnunarskemu eru notuð til að setja upp frestaðar tekjur og kostnað, og hægt er að nota sama uppsöfnunarskema fyrir tekjur og kostnað.</span><span class="sxs-lookup"><span data-stu-id="fffa0-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="fffa0-108">Fjárhagsuppsafnanir endurdreifa kostnaði eða tekjum í færslubókarlínu svo að kostnaður eða tekjur eru samþykktar á viðeigandi tímabilum.</span><span class="sxs-lookup"><span data-stu-id="fffa0-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="fffa0-109">Á síðunni **Uppsöfnunarskema** eru tilgreindir debet- og kreditlyklar sem verða notaðir þegar uppsöfnunarskema er beitt.</span><span class="sxs-lookup"><span data-stu-id="fffa0-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="fffa0-110">**Debet** – Aðallykill sem er skilgreindur mun skipta út aðallykli debets í fylgiskjali færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="fffa0-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="fffa0-111">Þessi lykill verður einnig notaður fyrir bakfærslu á frestun sem byggir á uppsöfnunarfærslum fjárhags.</span><span class="sxs-lookup"><span data-stu-id="fffa0-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="fffa0-112">**Kredit** – Aðallykill sem er skilgreindur mun skipta út aðallykli kredits í fylgiskjali færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="fffa0-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="fffa0-113">Þessi lykill verður einnig notaður fyrir bakfærslu á frestun sem byggir á uppsöfnunarfærslum fjárhags.</span><span class="sxs-lookup"><span data-stu-id="fffa0-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="fffa0-114">Þegar búið er að ákvarða hvaða lykla á að nota, er hægt að tilgreina hvernig fylgiskjalsnúmer er stofnað þegar uppsöfnunarfærslur eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="fffa0-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="fffa0-115">Einnig er hægt að tilgreina hversu oft færslur eiga sér stað, fjölda skipta sem færslur eru stofnaðar og hvenær færslur eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="fffa0-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="fffa0-116">Eftir að uppsöfnunarskema hefur verið stofnað er hægt að nota það í sumum færslubókum með aðgerðinni Fjárhagsuppsafnanir.</span><span class="sxs-lookup"><span data-stu-id="fffa0-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="fffa0-117">Fjárhagsuppsafnanir</span><span class="sxs-lookup"><span data-stu-id="fffa0-117">Ledger accruals</span></span>
<span data-ttu-id="fffa0-118">Þegar færslubók er færð inn er hægt að smella á **Fjárhagsuppsafnanir** í valmyndinni **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="fffa0-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="fffa0-119">Síðan þegar uppsöfnunarskema er valið muntu sjá grunnupphæðina úr færslubókinni sem verður dreift yfir tímabilið, eins og ákvarðast af uppsöfnunarskemanu.</span><span class="sxs-lookup"><span data-stu-id="fffa0-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="fffa0-120">Til dæmis, ef þú greiðir tryggingu starfsmanns fyrir allt árið í janúar og upphæðin er 12.000, er verður að viðurkenna þann kostnað í hverjum mánuði.</span><span class="sxs-lookup"><span data-stu-id="fffa0-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="fffa0-121">Hægt er að velja upphafsdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="fffa0-121">You can select the start date.</span></span> <span data-ttu-id="fffa0-122">Einnig er hægt að tilgreina hvort upphæðin sem er safnað upp sé byggð á lyklinum eða mótlyklinum.</span><span class="sxs-lookup"><span data-stu-id="fffa0-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="fffa0-123">Þegar valið hefur verið gert er smellt á **Færslur** til að skoða allar færslur sem hafa verið stofnaðar samkvæmt uppsöfnunarskemanu.</span><span class="sxs-lookup"><span data-stu-id="fffa0-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="fffa0-124">Til dæmis, ef þú dreifir 12.000 af tryggingakostnaði yfir árið sjást 1.000 fyrir hvern mánuð.</span><span class="sxs-lookup"><span data-stu-id="fffa0-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="fffa0-125">Þegar færslubókin er bókuð, er hægt að skoða færslurnar með því að nota fyrirspurnarsíðuna **Fylgiskjalsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="fffa0-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="fffa0-126">Ef ekki er hægt að nota uppsöfnunarskema (til dæmis, þegar reikningur sölupöntunar eða innkaupareikningur á í hlut) er hægt að kreditfæra fyrirframgreidda upphæð og debetupphæð kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="fffa0-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="fffa0-127">Síðan er hægt að velja **Mótfærsla** þegar uppsöfnunarskemanu er beitt.</span><span class="sxs-lookup"><span data-stu-id="fffa0-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="fffa0-128">Nánari upplýsingar, sjá [stofna uppsöfnunarskemu](tasks/create-accrual-schemes.md) og [Stofna uppsöfnunarfærslur fjárhags](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="fffa0-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

