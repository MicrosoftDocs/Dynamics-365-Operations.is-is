---
title: Bókun í bakfærslubók
description: Þetta efni lýsir getu sem gerir þér kleift að bakfæra fylgiskjöl af færslulista fylgiskjala eða úr fjárhagsfærslubókum.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248586"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="b8782-103">Bókun í bakfærslubók</span><span class="sxs-lookup"><span data-stu-id="b8782-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8782-104">Þetta efni lýsir getu Microsoft Dynamics 365 Finance sem gerir þér kleift að bakfæra heila færslubók eða bakfæra eitt eða fleiri fylgiskjöl af færslulistum fylgiskjala án tillits til uppruna.</span><span class="sxs-lookup"><span data-stu-id="b8782-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="b8782-105">Bakfærsla færslubóka</span><span class="sxs-lookup"><span data-stu-id="b8782-105">Reversing journals</span></span>

<span data-ttu-id="b8782-106">Hægt er að bakfæra eina færslubókarlínu í einu.</span><span class="sxs-lookup"><span data-stu-id="b8782-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="b8782-107">Með bakfærslu á færslubók geturðu bakfært heila fjárhagsfærslubók.</span><span class="sxs-lookup"><span data-stu-id="b8782-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="b8782-108">Til að bakfæra færslubók:</span><span class="sxs-lookup"><span data-stu-id="b8782-108">To reverse a journal:</span></span> 
- <span data-ttu-id="b8782-109">Opnaðu fjárhagsfærslubókina og síaðu á bókaðar færslubækur</span><span class="sxs-lookup"><span data-stu-id="b8782-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="b8782-110">Smelltu á bakfærsluvalmyndina efst á síðunni</span><span class="sxs-lookup"><span data-stu-id="b8782-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="b8782-111">Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra</span><span class="sxs-lookup"><span data-stu-id="b8782-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b8782-112">Veldu Já til að nota núverandi færsludagsetningar eða Nei til að slá inn nýja.</span><span class="sxs-lookup"><span data-stu-id="b8782-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="b8782-113">Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú vilt færa inn nýja færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="b8782-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b8782-114">Ef þú valdir Nei, slærðu inn færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="b8782-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b8782-115">Sláðu inn athugasemd sem þú vilt bæta við bakfærsluna</span><span class="sxs-lookup"><span data-stu-id="b8782-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="b8782-116">Smelltu á hnappinn Bakfæra.</span><span class="sxs-lookup"><span data-stu-id="b8782-116">Click the Reverse button</span></span>

<span data-ttu-id="b8782-117">Færslunar verða bakfærðar.</span><span class="sxs-lookup"><span data-stu-id="b8782-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="b8782-118">Ef fjöldi fylgiskjala er yfir 100 línur, verður bakfærsluferlið keyrt með runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="b8782-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="b8782-119">Þú getur skoðað niðurstöður bakfærslu með því að skoða athugasemdir í runuvinnslunni sem var keyrð.</span><span class="sxs-lookup"><span data-stu-id="b8782-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="b8782-120">Allar bilanir verða tilgreindar í runuvinnslusögunni.</span><span class="sxs-lookup"><span data-stu-id="b8782-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="b8782-121">Ef fjöldi fylgiskjala er 100 línur eða minna, mun bakfærsluvinnslan keyra þegar í stað.</span><span class="sxs-lookup"><span data-stu-id="b8782-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="b8782-122">Niðurstöðurnar verða kynntar í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra og ástæðu þess að ekki var hægt að bakfæra þau.</span><span class="sxs-lookup"><span data-stu-id="b8782-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="b8782-123">Smelltu á OK til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="b8782-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="b8782-124">Bakfærsla fylgiskjala af færslulista fylgiskjala.</span><span class="sxs-lookup"><span data-stu-id="b8782-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="b8782-125">Þú getur líka bakfært fylgiskjöl úr **Fylgiskjalafærslulisti** yfir allar undirfærslubækur.</span><span class="sxs-lookup"><span data-stu-id="b8782-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="b8782-126">Að auki geturðu bakfært fleiri en eitt fylgiskjal í einu.</span><span class="sxs-lookup"><span data-stu-id="b8782-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="b8782-127">Til að bakfæra eitt eða fleiri fylgiskjöl:</span><span class="sxs-lookup"><span data-stu-id="b8782-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="b8782-128">Smelltu á bakfærsluvalmyndina efst á síðunni</span><span class="sxs-lookup"><span data-stu-id="b8782-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="b8782-129">Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra</span><span class="sxs-lookup"><span data-stu-id="b8782-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b8782-130">Veldu Já til að nota núverandi færsludagsetningar eða Nei til að slá inn nýja.</span><span class="sxs-lookup"><span data-stu-id="b8782-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="b8782-131">Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú vilt færa inn nýja færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="b8782-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b8782-132">Ef þú valdir Nei, slærðu inn færsludagsetningu fyrir bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="b8782-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b8782-133">Sláðu inn athugasemd sem þú vilt bæta við bakfærsluna</span><span class="sxs-lookup"><span data-stu-id="b8782-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="b8782-134">Smelltu á hnappinn Bakfæra.</span><span class="sxs-lookup"><span data-stu-id="b8782-134">Click the Reverse button</span></span>

<span data-ttu-id="b8782-135">Færslunar verða bakfærðar.</span><span class="sxs-lookup"><span data-stu-id="b8782-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="b8782-136">Ef fjöldi fylgiskjala er yfir 100 línur, verður bakfærsluferlið keyrt með runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="b8782-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="b8782-137">Þú getur skoðað niðurstöður bakfærslu með því að skoða athugasemdir í runuvinnslunni sem var keyrð.</span><span class="sxs-lookup"><span data-stu-id="b8782-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="b8782-138">Allar bilanir verða tilgreindar í runuvinnslusögunni.</span><span class="sxs-lookup"><span data-stu-id="b8782-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="b8782-139">Ef fjöldi fylgiskjala er 100 línur eða minna, mun bakfærsluvinnslan keyra þegar í stað.</span><span class="sxs-lookup"><span data-stu-id="b8782-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="b8782-140">Niðurstöðurnar verða kynntar í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra og ástæðu þess að ekki var hægt að bakfæra þau.</span><span class="sxs-lookup"><span data-stu-id="b8782-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="b8782-141">Smelltu á OK til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="b8782-141">Click on Ok to close the dialog.</span></span>

