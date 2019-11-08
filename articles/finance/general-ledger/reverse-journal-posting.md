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
ms.openlocfilehash: bc2ff30ef5d08759af700d683c207b0f5ed65d5b
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658976"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="59a02-103">Bókun í bakfærslubók</span><span class="sxs-lookup"><span data-stu-id="59a02-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="59a02-104">Þetta efni lýsir getu Microsoft Dynamics 365 Finance sem gerir þér kleift að bakfæra heila færslubók eða bakfæra eitt eða fleiri fylgiskjöl af færslulistum fylgiskjala án tillits til uppruna.</span><span class="sxs-lookup"><span data-stu-id="59a02-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="59a02-105">Bakfærsla færslubóka</span><span class="sxs-lookup"><span data-stu-id="59a02-105">Reversing journals</span></span>

<span data-ttu-id="59a02-106">Hægt er að bakfæra eina færslubókarlínu í einu.</span><span class="sxs-lookup"><span data-stu-id="59a02-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="59a02-107">Með bakfærslu á færslubók geturðu bakfært heila fjárhagsfærslubók.</span><span class="sxs-lookup"><span data-stu-id="59a02-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="59a02-108">Til að bakfæra færslubók:</span><span class="sxs-lookup"><span data-stu-id="59a02-108">To reverse a journal:</span></span> 

- <span data-ttu-id="59a02-109">Opnaðu fjárhagsfærslubókina og síaðu á bókaðar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="59a02-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="59a02-110">Veldu valmyndina **Bakfæra** efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="59a02-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="59a02-111">Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra</span><span class="sxs-lookup"><span data-stu-id="59a02-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="59a02-112">Veldu **Já** til að nota núverandi færsludagsetningar eða **Nei** til að slá inn nýja.</span><span class="sxs-lookup"><span data-stu-id="59a02-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="59a02-113">Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú verður að færa inn nýja færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="59a02-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="59a02-114">Ef þú velur **Nei** slærðu inn færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="59a02-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="59a02-115">Sláðu inn athugasemd sem þú vilt bæta við bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="59a02-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="59a02-116">Veljið hnappinn **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="59a02-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="59a02-117">Færslunar verða bakfærðar.</span><span class="sxs-lookup"><span data-stu-id="59a02-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="59a02-118">Ef fylgiskjalið inniheldur yfir 100 línur, verður bakfærsluferlið keyrt með runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="59a02-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="59a02-119">Þú getur skoðað niðurstöðurnar með því að skoða athugasemdir í runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="59a02-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="59a02-120">Öll viðskipti sem ekki var hægt að bakfæra verða skráð í sögu runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="59a02-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="59a02-121">Ef fylgiskjalið inniheldur 100 línur eða færri mun bakfærsluvinnslan keyra þegar í stað.</span><span class="sxs-lookup"><span data-stu-id="59a02-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="59a02-122">Niðurstöðurnar verða kynntar í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra, ásamt ástæðu þess að ekki var hægt að bakfæra þau.</span><span class="sxs-lookup"><span data-stu-id="59a02-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="59a02-123">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="59a02-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="59a02-124">Bakfærsla fylgiskjala af færslulista fylgiskjala.</span><span class="sxs-lookup"><span data-stu-id="59a02-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="59a02-125">Þú getur líka bakfært fylgiskjöl úr **Fylgiskjalafærslulisti** yfir allar undirfærslubækur.</span><span class="sxs-lookup"><span data-stu-id="59a02-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="59a02-126">Að auki geturðu bakfært fleiri en eitt fylgiskjal í einu.</span><span class="sxs-lookup"><span data-stu-id="59a02-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="59a02-127">Til að bakfæra eitt eða fleiri fylgiskjöl:</span><span class="sxs-lookup"><span data-stu-id="59a02-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="59a02-128">Veldu valmyndina **Bakfæra** efst á síðunni</span><span class="sxs-lookup"><span data-stu-id="59a02-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="59a02-129">Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra.</span><span class="sxs-lookup"><span data-stu-id="59a02-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="59a02-130">Veldu **Já** til að nota núverandi færsludagsetningar eða **Nei** til að slá inn nýja.</span><span class="sxs-lookup"><span data-stu-id="59a02-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="59a02-131">Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú verður að færa inn nýja færsludagsetningu til að bakfæra hana.</span><span class="sxs-lookup"><span data-stu-id="59a02-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="59a02-132">Ef þú velur **Nei** slærðu inn færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="59a02-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="59a02-133">Sláðu inn athugasemd til að lýsa bakfærslunni.</span><span class="sxs-lookup"><span data-stu-id="59a02-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="59a02-134">Veljið hnappinn **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="59a02-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="59a02-135">Færslunar verða bakfærðar.</span><span class="sxs-lookup"><span data-stu-id="59a02-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="59a02-136">Ef það eru yfir 100 fylgiskjalalínur verður bakfærsluferlið keyrt með runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="59a02-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="59a02-137">Þú getur skoðað niðurstöðurnar með því að skoða athugasemdir í runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="59a02-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="59a02-138">Öll viðskipti sem ekki var hægt að bakfæra verða skráð í sögu runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="59a02-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="59a02-139">Ef fjöldi fylgiskjala er 100 línur eða færri mun bakfærsluvinnslan keyra þegar í stað.</span><span class="sxs-lookup"><span data-stu-id="59a02-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="59a02-140">Niðurstöðurnar munu birtast í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra, ásamt ástæðu þess.</span><span class="sxs-lookup"><span data-stu-id="59a02-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="59a02-141">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="59a02-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="59a02-142">Aðeins er hægt að bakfæra færslur ef þær uppfylla viðskiptareglur um bakfærslur.</span><span class="sxs-lookup"><span data-stu-id="59a02-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="59a02-143">Ekki er hægt að bakfæra lánardrottnagreiðslum með því að nota getu sem lýst er í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="59a02-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="59a02-144">Lánardrottnagreiðslur verður að bakfæra með því að fylgja skrefunum sem talin eru upp í [Bakfæra lánardrottnagreiðslu](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="59a02-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

