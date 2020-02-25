---
title: Bókun í bakfærslubók
description: Þetta efni lýsir getu sem gerir þér kleift að bakfæra fylgiskjöl af færslulista fylgiskjala eða úr fjárhagsfærslubókum.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08aec836ce4b7b6a59c445f138365f101a78c68e
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030923"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="5985f-103">Bókun í bakfærslubók</span><span class="sxs-lookup"><span data-stu-id="5985f-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5985f-104">Þetta efni lýsir getu Microsoft Dynamics 365 Finance sem gerir þér kleift að bakfæra heila færslubók eða bakfæra eitt eða fleiri fylgiskjöl af færslulistum fylgiskjala án tillits til uppruna.</span><span class="sxs-lookup"><span data-stu-id="5985f-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="5985f-105">Bakfærsla færslubóka</span><span class="sxs-lookup"><span data-stu-id="5985f-105">Reversing journals</span></span>

<span data-ttu-id="5985f-106">Hægt er að bakfæra eina færslubókarlínu í einu.</span><span class="sxs-lookup"><span data-stu-id="5985f-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="5985f-107">Með bakfærslu á færslubók geturðu bakfært heila fjárhagsfærslubók.</span><span class="sxs-lookup"><span data-stu-id="5985f-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="5985f-108">Til að bakfæra færslubók:</span><span class="sxs-lookup"><span data-stu-id="5985f-108">To reverse a journal:</span></span> 

- <span data-ttu-id="5985f-109">Opnaðu fjárhagsfærslubókina og síaðu á bókaðar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="5985f-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="5985f-110">Veldu valmyndina **Bakfæra** efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="5985f-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="5985f-111">Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra</span><span class="sxs-lookup"><span data-stu-id="5985f-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="5985f-112">Veldu **Já** til að nota núverandi færsludagsetningar eða **Nei** til að slá inn nýja.</span><span class="sxs-lookup"><span data-stu-id="5985f-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="5985f-113">Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú verður að færa inn nýja færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="5985f-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="5985f-114">Ef þú velur **Nei** slærðu inn færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="5985f-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="5985f-115">Sláðu inn athugasemd sem þú vilt bæta við bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="5985f-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="5985f-116">Veljið hnappinn **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="5985f-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="5985f-117">Færslunar verða bakfærðar.</span><span class="sxs-lookup"><span data-stu-id="5985f-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="5985f-118">Ef fylgiskjalið inniheldur yfir 100 línur, verður bakfærsluferlið keyrt með runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="5985f-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="5985f-119">Þú getur skoðað niðurstöðurnar með því að skoða athugasemdir í runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="5985f-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="5985f-120">Öll viðskipti sem ekki var hægt að bakfæra verða skráð í sögu runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="5985f-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="5985f-121">Ef fylgiskjalið inniheldur 100 línur eða færri mun bakfærsluvinnslan keyra þegar í stað.</span><span class="sxs-lookup"><span data-stu-id="5985f-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="5985f-122">Niðurstöðurnar verða kynntar í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra, ásamt ástæðu þess að ekki var hægt að bakfæra þau.</span><span class="sxs-lookup"><span data-stu-id="5985f-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="5985f-123">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="5985f-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="5985f-124">Bakfærsla fylgiskjala af færslulista fylgiskjala.</span><span class="sxs-lookup"><span data-stu-id="5985f-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="5985f-125">Þú getur líka bakfært fylgiskjöl úr **Fylgiskjalafærslulisti** yfir allar undirfærslubækur.</span><span class="sxs-lookup"><span data-stu-id="5985f-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="5985f-126">Að auki geturðu bakfært fleiri en eitt fylgiskjal í einu.</span><span class="sxs-lookup"><span data-stu-id="5985f-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="5985f-127">Til að bakfæra eitt eða fleiri fylgiskjöl:</span><span class="sxs-lookup"><span data-stu-id="5985f-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="5985f-128">Veldu valmyndina **Bakfæra** efst á síðunni</span><span class="sxs-lookup"><span data-stu-id="5985f-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="5985f-129">Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra.</span><span class="sxs-lookup"><span data-stu-id="5985f-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="5985f-130">Veldu **Já** til að nota núverandi færsludagsetningar eða **Nei** til að slá inn nýja.</span><span class="sxs-lookup"><span data-stu-id="5985f-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="5985f-131">Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú verður að færa inn nýja færsludagsetningu til að bakfæra hana.</span><span class="sxs-lookup"><span data-stu-id="5985f-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="5985f-132">Ef þú velur **Nei** slærðu inn færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="5985f-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="5985f-133">Sláðu inn athugasemd til að lýsa bakfærslunni.</span><span class="sxs-lookup"><span data-stu-id="5985f-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="5985f-134">Veljið hnappinn **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="5985f-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="5985f-135">Færslunar verða bakfærðar.</span><span class="sxs-lookup"><span data-stu-id="5985f-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="5985f-136">Ef það eru yfir 100 fylgiskjalalínur verður bakfærsluferlið keyrt með runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="5985f-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="5985f-137">Þú getur skoðað niðurstöðurnar með því að skoða athugasemdir í runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="5985f-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="5985f-138">Öll viðskipti sem ekki var hægt að bakfæra verða skráð í sögu runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="5985f-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="5985f-139">Ef fjöldi fylgiskjala er 100 línur eða færri mun bakfærsluvinnslan keyra þegar í stað.</span><span class="sxs-lookup"><span data-stu-id="5985f-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="5985f-140">Niðurstöðurnar munu birtast í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra, ásamt ástæðu þess.</span><span class="sxs-lookup"><span data-stu-id="5985f-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="5985f-141">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="5985f-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="5985f-142">Aðeins er hægt að bakfæra færslur ef þær uppfylla viðskiptareglur um bakfærslur.</span><span class="sxs-lookup"><span data-stu-id="5985f-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="5985f-143">Ekki er hægt að bakfæra lánardrottnagreiðslum með því að nota getu sem lýst er í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="5985f-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="5985f-144">Lánardrottnagreiðslur verður að bakfæra með því að fylgja skrefunum sem talin eru upp í [Bakfæra lánardrottnagreiðslu](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="5985f-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

